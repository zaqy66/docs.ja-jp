---
title: サーキット ブレーカー パターンの実装
description: '.NET マイクロサービス: コンテナー化された .NET アプリケーションのアーキテクチャ | HTTP 再試行の補足システムとしてサーキット ブレーカー パターンを実装する'
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 07/03/2018
ms.openlocfilehash: d5902c5a0744d74ae5086a4df3aee606b24b6030
ms.sourcegitcommit: 59b51cd7c95c75be85bd6ef715e9ef8c85720bac
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2018
ms.locfileid: "37875168"
---
# <a name="implement-the-circuit-breaker-pattern"></a><span data-ttu-id="83b3f-103">サーキット ブレーカー パターンを実装する</span><span class="sxs-lookup"><span data-stu-id="83b3f-103">Implement the Circuit Breaker pattern</span></span>

<span data-ttu-id="83b3f-104">前述のように、リモート サービスやリソースに接続を試行する際に発生し得る、復旧にどのくらい時間がかかるかわからない障害を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-104">As noted earlier, you should handle faults that might take a variable amount of time to recover from, as it might happen when you try to connect to a remote service or resource.</span></span> <span data-ttu-id="83b3f-105">この種類の障害を処理することにより、アプリケーションの安定性と回復性が向上します。</span><span class="sxs-lookup"><span data-stu-id="83b3f-105">Handling this type of fault can improve the stability and resiliency of an application.</span></span>

<span data-ttu-id="83b3f-106">分散環境において、リモート リソースとサービスの呼び出しは、低速なネットワーク接続やタイムアウト、あるいはリソースが低速であったり、一時的に利用不可能であったりなどの、一時的な障害が原因で失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-106">In a distributed environment, calls to remote resources and services can fail due to transient faults, such as slow network connections and timeouts, or if resources are being slow or are temporarily unavailable.</span></span> <span data-ttu-id="83b3f-107">このような障害は通常しばらくすると自動的に修正されます。堅牢なクラウド アプリケーションなら "再試行パターン" などの方法でそうした障害を処理する備えができているはずです。</span><span class="sxs-lookup"><span data-stu-id="83b3f-107">These faults typically correct themselves after a short time, and a robust cloud application should be prepared to handle them by using a strategy like the "Retry pattern".</span></span> 

<span data-ttu-id="83b3f-108">ただし、予期しないイベントが原因で、障害の修正に非常に長い時間がかかる状況もあり得ます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-108">However, there can also be situations where faults are due to unanticipated events that might take much longer to fix.</span></span> <span data-ttu-id="83b3f-109">このような障害の重大度は、部分的な接続の損失からサービスの完全な不具合まで多岐にわたります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-109">These faults can range in severity from a partial loss of connectivity to the complete failure of a service.</span></span> <span data-ttu-id="83b3f-110">このような状況では、アプリケーションが成功の見込みの薄い操作を再試行し続けることは無駄かもしれません。</span><span class="sxs-lookup"><span data-stu-id="83b3f-110">In these situations, it might be pointless for an application to continually retry an operation that is unlikely to succeed.</span></span> 

<span data-ttu-id="83b3f-111">代わりに、アプリケーションが操作の失敗を受け入れ、失敗を処理するようにコードを書く必要があります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-111">Instead, the application should be coded to accept that the operation has failed and handle the failure accordingly.</span></span>

<span data-ttu-id="83b3f-112">HTTP 再試行を不注意に使用すると、自分のソフトウェアにサービス拒否 ([DoS](https://en.wikipedia.org/wiki/Denial-of-service_attack)) 攻撃が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-112">Using Http retries carelessly could result in creating a Denial of Service ([DoS](https://en.wikipedia.org/wiki/Denial-of-service_attack)) attack within your own software.</span></span> <span data-ttu-id="83b3f-113">マイクロサービスが失敗したか、動作が遅いとき、複数のクライアントで失敗した要求の再試行が繰り返されることがあります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-113">As a microservice fails or performs slowly, multiple clients might repeatedly retry failed requests.</span></span> <span data-ttu-id="83b3f-114">その結果、失敗を繰り返すサービスに宛てられるトラフィックが急激に増えるという危険なリスクが発生します。</span><span class="sxs-lookup"><span data-stu-id="83b3f-114">That creates a dangerous risk of exponentially increasing traffic targeted at the failing service.</span></span>

<span data-ttu-id="83b3f-115">そのため、試行を続けるに値しないとき、再試行が要求を停止するように、何らかの防壁が必要になります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-115">Therefore, you need some kind of defense barrier so the retries stop requests when it is not worth to keep trying.</span></span> <span data-ttu-id="83b3f-116">その防壁こそがサーキット ブレーカーです。</span><span class="sxs-lookup"><span data-stu-id="83b3f-116">That defense barrier is precisely the circuit breaker.</span></span>

<span data-ttu-id="83b3f-117">サーキット ブレーカー パターンの目的は、"再試行パターン" とは異なります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-117">The Circuit Breaker pattern has a different purpose than the "Retry pattern".</span></span> <span data-ttu-id="83b3f-118">"再試行パターン" では、操作が最終的には成功するとの見込みをもってアプリケーションに操作を再試行させます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-118">The "Retry pattern" enables an application to retry an operation in the expectation that the operation will eventually succeed.</span></span> <span data-ttu-id="83b3f-119">サーキット ブレーカー パターンは、失敗する可能性の高い操作をアプリケーションが実行しないようにします。</span><span class="sxs-lookup"><span data-stu-id="83b3f-119">The Circuit Breaker pattern prevents an application from performing an operation that is likely to fail.</span></span> <span data-ttu-id="83b3f-120">アプリケーションでは、これら 2 つのパターンを組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-120">An application can combine these two patterns.</span></span> <span data-ttu-id="83b3f-121">しかしながら、再試行のロジックはサーキット ブレーカーが返す例外に対応できる必要があり、障害が一時的ではないことをサーキット ブレーカーが示す場合、再試行を中止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-121">However, the retry logic should be sensitive to any exception returned by the circuit breaker, and it should abandon retry attempts if the circuit breaker indicates that a fault is not transient.</span></span>

## <a name="implement-circuit-breaker-pattern-with-httpclientfactory-and-polly"></a><span data-ttu-id="83b3f-122">HttpClientFactory と Polly でサーキット ブレーカー パターンを実装する</span><span class="sxs-lookup"><span data-stu-id="83b3f-122">Implement Circuit Breaker pattern with HttpClientFactory and Polly</span></span>

<span data-ttu-id="83b3f-123">再試行の実装と同じように、サーキット ブレーカーの推奨されるアプローチは、Polly など実績のある .NET ライブラリを活用し、HttpClientFactory とネイティブ統合することです。</span><span class="sxs-lookup"><span data-stu-id="83b3f-123">As when implementing retries, the recommended approach for circuit breakers is to take advantage of proven .NET libraries like Polly and its native integration with HttpClientFactory.</span></span>

<span data-ttu-id="83b3f-124">サーキット ブレーカー ポリシーを HttpClientFactory の外向きミドルウェア パイプラインに追加することは、HttpClientFactory の使用時、既にあるものにコードの増分を 1 つ分追加することと同じくらい簡単です。</span><span class="sxs-lookup"><span data-stu-id="83b3f-124">Adding a circuit breaker policy into your HttpClientFactory outgoing middleware pipeline is as simple as adding a single incremental piece of code to what you already have when using HttpClientFactory.</span></span>

<span data-ttu-id="83b3f-125">HTTP 呼び出しの再試行に使用されるコードに追加する必要があるのは、ConfigureServices() メソッドから抜粋された次の増分コードで示されているように、使用するポリシーのリストにサーキット ブレーカー ポリシーを追加するコードだけです。</span><span class="sxs-lookup"><span data-stu-id="83b3f-125">The only addition here to the code used for HTTP call retries is the code where you add the Circuit Breaker policy to the list of policies to use, as shown in the following incremental code, part of the ConfigureServices() method.</span></span>

```csharp
//ConfigureServices()  - Startup.cs
services.AddHttpClient<IBasketService, BasketService>()
        .SetHandlerLifetime(TimeSpan.FromMinutes(5))  //Set lifetime to 5 minutes
        .AddPolicyHandler(GetRetryPolicy())
        .AddPolicyHandler(GetCircuitBreakerPolicy());
```

<span data-ttu-id="83b3f-126">`AddPolicyHandler()` メソッドは、使用する HttpClient オブジェクトにポリシーを追加します。</span><span class="sxs-lookup"><span data-stu-id="83b3f-126">The `AddPolicyHandler()`method is what adds policies to the HttpClient objects you will use.</span></span> <span data-ttu-id="83b3f-127">この場合、サーキット ブレーカーの Polly のポリシーを追加しています。</span><span class="sxs-lookup"><span data-stu-id="83b3f-127">In this case, it is adding a Polly’s policy for a circuit breaker.</span></span>

<span data-ttu-id="83b3f-128">手法のモジュール性を高める目的で、次のコードのように、GetCircuitBreakerPolicy() という名前の別個のメソッドにサーキット ブレーカー ポリシーが定義されます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-128">In order to have a more modular approach, the Circuit Breaker Policy is defined in a separate method named GetCircuitBreakerPolicy(), as the following code.</span></span>

```csharp
static IAsyncPolicy<HttpResponseMessage> GetCircuitBreakerPolicy()
{
    return HttpPolicyExtensions
        .HandleTransientHttpError()
        .CircuitBreakerAsync(5, TimeSpan.FromSeconds(30));
}
```

<span data-ttu-id="83b3f-129">上記のコード例では、HTTP 要求の再試行時、例外が 5 つ発生したとき、サーキットを中断する (またはオープン状態にする) ようにサーキット ブレーカー ポリシーが構成されています。</span><span class="sxs-lookup"><span data-stu-id="83b3f-129">In the code example above, the circuit breaker policy is configured so it breaks or opens the circuit when there have been five exceptions when retrying the Http requests.</span></span> <span data-ttu-id="83b3f-130">30 秒がその期間 (中断) になります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-130">Then, 30 seconds will be the duration or the break.</span></span>

<span data-ttu-id="83b3f-131">サーキット ブレーカーは、HTTP 呼び出しを実行しているクライアント アプリケーションまたはサービスとは別の環境に展開されている特定のリソースに問題がある場合に、要求をフォールバック インフラストラクチャにリダイレクトするために使用する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-131">Circuit breakers should also be used to redirect requests to a fallback infrastructure if you had issues in a particular resource that is deployed in a different environment than the client application or service that is performing the HTTP call.</span></span> <span data-ttu-id="83b3f-132">こうすれば、バックエンドのマイクロサービスのみに影響を与え、クライアント アプリケーションには影響を与えないデータセンターの停止が生じた場合に、クライアント アプリケーションはフォールバック サービスにリダイレクトできます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-132">That way, if there is an outage in the datacenter that impacts only your backend microservices but not your client applications, the client applications can redirect to the fallback services.</span></span> <span data-ttu-id="83b3f-133">Polly では、この[フェールオーバー ポリシー](https://github.com/App-vNext/Polly/wiki/Polly-Roadmap#failover-policy) シナリオを自動化するための新しいポリシーが計画されています。</span><span class="sxs-lookup"><span data-stu-id="83b3f-133">Polly is planning a new policy to automate this [failover policy](https://github.com/App-vNext/Polly/wiki/Polly-Roadmap#failover-policy) scenario.</span></span> 

<span data-ttu-id="83b3f-134">これらすべての機能は、位置を意識することなく Azure に自動的にフェールオーバーを管理させるのとは対照的に、フェールオーバーを .NET コード内から管理する場合のためのものです。</span><span class="sxs-lookup"><span data-stu-id="83b3f-134">All those features are for cases where you're managing the failover from within the .NET code, as opposed to having it managed automatically for you by Azure, with location transparency.</span></span> 

<span data-ttu-id="83b3f-135">使用という観点からは、HttpClient を使用するとき、ここで新しいものは何も追加する必要がありません。前のセクションで示したように、HttpClient と HttpClientFactory の使用時とコードが同じであるからです。</span><span class="sxs-lookup"><span data-stu-id="83b3f-135">From a usage point of view, when using HttpClient, there’s no need to add anything new here because the code is the same than when using HttpClient with HttpClientFactory, as shown in previous sections.</span></span> 

## <a name="testing-http-retries-and-circuit-breakers-in-eshoponcontainers"></a><span data-ttu-id="83b3f-136">eShopOnContainers で HTTP の再試行とサーキット ブレーカーをテストする</span><span class="sxs-lookup"><span data-stu-id="83b3f-136">Testing Http retries and circuit breakers in eShopOnContainers</span></span>


<span data-ttu-id="83b3f-137">Docker ホスト内で eShopOnContainers ソリューションを起動する場合、このソリューションは複数のコンテナーを起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-137">Whenever you start the eShopOnContainers solution in a Docker host, it needs to start multiple containers.</span></span> <span data-ttu-id="83b3f-138">SQL Server コンテナーなど、一部のコンテナーは起動と初期化が低速です。</span><span class="sxs-lookup"><span data-stu-id="83b3f-138">Some of the containers are slower to start and initialize, like the SQL Server container.</span></span> <span data-ttu-id="83b3f-139">eShopOnContainers アプリケーションを Docker に初めて展開する場合は、イメージとデータベースを設定する必要があるため、特にそうです。</span><span class="sxs-lookup"><span data-stu-id="83b3f-139">This is especially true the first time you deploy the eShopOnContainers application into Docker, because it needs to set up the images and the database.</span></span> <span data-ttu-id="83b3f-140">一部のコンテナーは他のコンテナーより起動が低速だという事実により、以前のセクションで説明したように docker-compose レベルでコンテナー間の依存関係を設定している場合であっても、残りのサービスによる初期化時の HTTP 例外のスローが引き起こされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-140">The fact that some containers start slower than others can cause the rest of the services to initially throw HTTP exceptions, even if you set dependencies between containers at the docker-compose level, as explained in previous sections.</span></span> <span data-ttu-id="83b3f-141">コンテナー間の docker-compose 依存関係は、プロセス レベルだけのものです。</span><span class="sxs-lookup"><span data-stu-id="83b3f-141">Those docker-compose dependencies between containers are just at the process level.</span></span> <span data-ttu-id="83b3f-142">コンテナーのエントリ ポイント プロセスは起動されても、SQL Server はクエリに対して準備ができていないことがあります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-142">The container’s entry point process might be started, but SQL Server might not be ready for queries.</span></span> <span data-ttu-id="83b3f-143">結果としてエラーの連鎖が生じ、アプリケーションがその特定のコンテナーを利用しようとするときに例外が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-143">The result can be a cascade of errors, and the application can get an exception when trying to consume that particular container.</span></span> 

<span data-ttu-id="83b3f-144">また、起動時のこのタイプのエラーは、アプリケーションをクラウドに展開する際に生じることもあります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-144">You might also see this type of error on startup when the application is deploying to the cloud.</span></span> <span data-ttu-id="83b3f-145">その場合、オーケストレーターは、クラスターのノード全体でコンテナーの数を分散させる際に、コンテナーを 1 つのノードまたは VM から別の場所に移動することがあります (つまり、新しいインスタンスを起動する)。</span><span class="sxs-lookup"><span data-stu-id="83b3f-145">In that case, orchestrators might be moving containers from one node or VM to another (that is, starting new instances) when balancing the number of containers across the cluster’s nodes.</span></span>

<span data-ttu-id="83b3f-146">すべてのコンテナーを起動するとき、'eShopOnContainers' では、上記の再試行パターンを利用してこれらの問題を解決します。</span><span class="sxs-lookup"><span data-stu-id="83b3f-146">The way 'eShopOnContainers' solves those issues when starting all the containers is by using the Retry pattern illustrated earlier.</span></span> 

### <a name="testing-the-circuit-breaker-in-eshoponcontainers"></a><span data-ttu-id="83b3f-147">eShopOnContainers でサーキット ブレーカーをテストする</span><span class="sxs-lookup"><span data-stu-id="83b3f-147">Testing the circuit breaker in eShopOnContainers</span></span>

<span data-ttu-id="83b3f-148">いくつかの方法でサーキットを中断し/オープン状態にし、eShopOnContainers でテストできます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-148">There are a few ways you can break/open the circuit and test it with eShopOnContainers.</span></span>

<span data-ttu-id="83b3f-149">1 つの方法は、サーキット ブレーカー ポリシーで許可する再試行の数を 1 まで減らし、ソリューション全体を Docker に再展開することです。</span><span class="sxs-lookup"><span data-stu-id="83b3f-149">One option is to lower the allowed number of retries to 1 in the circuit breaker policy and redeploy the whole solution into Docker.</span></span> <span data-ttu-id="83b3f-150">再試行を 1 回にすることで、展開中に HTTP 要求が失敗し、サーキット ブレーカーがオープン状態になって、エラーが発生する可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-150">With a single retry, there is a good chance that an HTTP request will fail during deployment, the circuit breaker will open, and you get an error.</span></span>

<span data-ttu-id="83b3f-151">もう 1 つの方法は、Basket マイクロサービスで実装されているカスタムのミドルウェアを使用することです。</span><span class="sxs-lookup"><span data-stu-id="83b3f-151">Another option is to use custom middleware that is implemented in the Basket microservice.</span></span> <span data-ttu-id="83b3f-152">このミドルウェアが有効な場合、すべての HTTP 要求を捕捉し、状態コード 500 を返します。</span><span class="sxs-lookup"><span data-stu-id="83b3f-152">When this middleware is enabled, it catches all HTTP requests and returns status code 500.</span></span> <span data-ttu-id="83b3f-153">次のように、"failing" URI に GET 要求を実行してミドルウェアを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-153">You can enable the middleware by making a GET request to the failing URI, like the following:</span></span>

- `GET http://localhost:5103/failing`

<span data-ttu-id="83b3f-154">この要求は、ミドルウェアの現在の状態を返します。</span><span class="sxs-lookup"><span data-stu-id="83b3f-154">This request returns the current state of the middleware.</span></span> <span data-ttu-id="83b3f-155">ミドルウェアが有効な場合、要求は状態コード 500 を返します。</span><span class="sxs-lookup"><span data-stu-id="83b3f-155">If the middleware is enabled, the request return status code 500.</span></span> <span data-ttu-id="83b3f-156">ミドルウェアが無効の場合、応答はありません。</span><span class="sxs-lookup"><span data-stu-id="83b3f-156">If the middleware is disabled, there is no response.</span></span> 

- `GET http://localhost:5103/failing?enable`

<span data-ttu-id="83b3f-157">この要求はミドルウェアを有効にします。</span><span class="sxs-lookup"><span data-stu-id="83b3f-157">This request enables the middleware.</span></span> 

- `GET http://localhost:5103/failing?disable`

<span data-ttu-id="83b3f-158">この要求はミドルウェアを無効にします。</span><span class="sxs-lookup"><span data-stu-id="83b3f-158">This request disables the middleware.</span></span> 

<span data-ttu-id="83b3f-159">たとえば、アプリケーションが実行されたら、任意のブラウザーで次の URI を使用して要求を実行することにより、ミドルウェアを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-159">For instance, once the application is running, you can enable the middleware by making a request using the following URI in any browser.</span></span> <span data-ttu-id="83b3f-160">注文マイクロサービスにはポート 5103 を使用することにご注意ください。</span><span class="sxs-lookup"><span data-stu-id="83b3f-160">Note that the ordering microservice uses port 5103.</span></span>

`http://localhost:5103/failing?enable` 

<span data-ttu-id="83b3f-161">その後、図 10-4 に示されているように、URI http://localhost:5103/failing を使用して状態を確認できます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-161">You can then check the status using the URI http://localhost:5103/failing, as shown in Figure 10-4.</span></span>

![](./media/image4.png)

<span data-ttu-id="83b3f-162">**図 10-4**.</span><span class="sxs-lookup"><span data-stu-id="83b3f-162">**Figure 10-4**.</span></span> <span data-ttu-id="83b3f-163">"failing" ASP.NET ミドルウェアの状態を確認している。この場合は無効。</span><span class="sxs-lookup"><span data-stu-id="83b3f-163">Checking the state of the “Failing” ASP.NET middleware – In this case, disabled.</span></span> 

<span data-ttu-id="83b3f-164">この時点で Basket マイクロサービスは、呼び出すたびに状態コード 500 を返します。</span><span class="sxs-lookup"><span data-stu-id="83b3f-164">At this point, the Basket microservice responds with status code 500 whenever you call invoke it.</span></span>

<span data-ttu-id="83b3f-165">ミドルウェアを実行したら、MVC Web アプリから注文してみることができます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-165">Once the middleware is running, you can try making an order from the MVC web application.</span></span> <span data-ttu-id="83b3f-166">要求は失敗するため、サーキットがオープン状態になります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-166">Because the requests fail, the circuit will open.</span></span> 

<span data-ttu-id="83b3f-167">次の例では、MVC Web アプリが、注文のためのロジック内に catch ブロックを含んでいることがわかります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-167">In the following example, you can see that the MVC web application has a catch block in the logic for placing an order.</span></span>  <span data-ttu-id="83b3f-168">コードがサーキット オープンの例外を捕捉すると、ユーザーに待機を促すメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="83b3f-168">If the code catches an open-circuit exception, it shows the user a friendly message telling them to wait.</span></span>

```csharp
public class CartController : Controller
{
    //…
    public async Task<IActionResult> Index()
    {
        try
        {          
            var user = _appUserParser.Parse(HttpContext.User);
            //Http requests using the Typed Client (Service Agent)
            var vm = await _basketSvc.GetBasket(user);
            return View(vm);
        }
        catch (BrokenCircuitException)
        {
            // Catches error when Basket.api is in circuit-opened mode                 
            HandleBrokenCircuitException();
        }
        return View();
    }       

    private void HandleBrokenCircuitException()
    {
        TempData["BasketInoperativeMsg"] = "Basket Service is inoperative, please try later on. (Business message due to Circuit-Breaker)";
    }
}
```

<span data-ttu-id="83b3f-169">まとめます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-169">Here’s a summary.</span></span> <span data-ttu-id="83b3f-170">再試行ポリシーは、HTTP 要求の実行を数回試行し、HTTP エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="83b3f-170">The Retry policy tries several times to make the HTTP request and gets HTTP errors.</span></span> <span data-ttu-id="83b3f-171">再試行回数がサーキット ブレーカー ポリシーに設定された最大回数に達すると (この場合は 5 回)、アプリケーションは BrokenCircuitException をスローします。</span><span class="sxs-lookup"><span data-stu-id="83b3f-171">When the number of retries reaches the maximum number set for the Circuit Breaker policy (in this case, 5), the application throws a BrokenCircuitException.</span></span> <span data-ttu-id="83b3f-172">結果として、図 10-5 に示されているようなメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-172">The result is a friendly message, as shown in Figure 10-5.</span></span>

![](./media/image5.png)

<span data-ttu-id="83b3f-173">**図 10-5**.</span><span class="sxs-lookup"><span data-stu-id="83b3f-173">**Figure 10-5**.</span></span> <span data-ttu-id="83b3f-174">サーキット ブレーカーが UI にエラーを返している</span><span class="sxs-lookup"><span data-stu-id="83b3f-174">Circuit breaker returning an error to the UI</span></span>

<span data-ttu-id="83b3f-175">サーキットをいつオープン状態にするか/中断するかに関して、別のロジックを実装できます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-175">You can implement different logic for when to open/break the circuit.</span></span> <span data-ttu-id="83b3f-176">または、フォールバック データセンターか冗長バックエンド システムがある場合、他のバックエンド マイクロサービスに対して HTTP 要求を試行することができます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-176">Or you can try an HTTP request against a different back-end microservice if there is a fallback datacenter or redundant back-end system.</span></span> 

<span data-ttu-id="83b3f-177">最後に、`CircuitBreakerPolicy` の別の可能性として、`Isolate` (サーキットを強制的にオープン状態にし、オープン状態を維持する) と `Reset` (もう一度クローズド状態にする) を使用する方法があります。</span><span class="sxs-lookup"><span data-stu-id="83b3f-177">Finally, another possibility for the `CircuitBreakerPolicy` is to use `Isolate` (which forces open and holds open the circuit) and `Reset` (which closes it again).</span></span> <span data-ttu-id="83b3f-178">これらは、ポリシーに対して Isolate と Reset を直接呼び出すユーティリティ HTTP エンドポイントを構築するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-178">These could be used to build a utility HTTP endpoint that invokes Isolate and Reset directly on the policy.</span></span>  <span data-ttu-id="83b3f-179">このような HTTP エンドポイントは、アップグレードしたい場合など、ダウンストリーム システムを一時的に分離するために運用環境で適切な安全性を保つために使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-179">Such an HTTP endpoint could also be used, suitably secured, in production for temporarily isolating a downstream system, such as when you want to upgrade it.</span></span> <span data-ttu-id="83b3f-180">または、障害が発生する恐れがあるダウンストリーム システムを保護するために手動でサーキットを切断することもできます。</span><span class="sxs-lookup"><span data-stu-id="83b3f-180">Or it could trip the circuit manually to protect a downstream system you suspect to be faulting.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="83b3f-181">その他の技術情報</span><span class="sxs-lookup"><span data-stu-id="83b3f-181">Additional resources</span></span>


-   <span data-ttu-id="83b3f-182">**サーキット ブレーカー パターン**
    [*https://docs.microsoft.com/azure/architecture/patterns/circuit-breaker*](https://docs.microsoft.com/azure/architecture/patterns/circuit-breaker)</span><span class="sxs-lookup"><span data-stu-id="83b3f-182">**Circuit Breaker pattern**
[*https://docs.microsoft.com/azure/architecture/patterns/circuit-breaker*](https://docs.microsoft.com/azure/architecture/patterns/circuit-breaker)</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="83b3f-183">[前へ](implement-http-call-retries-exponential-backoff-polly.md)
[次へ](monitor-app-health.md)</span><span class="sxs-lookup"><span data-stu-id="83b3f-183">[Previous](implement-http-call-retries-exponential-backoff-polly.md)
[Next](monitor-app-health.md)</span></span>
