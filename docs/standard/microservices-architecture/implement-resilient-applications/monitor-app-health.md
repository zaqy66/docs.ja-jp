---
title: 正常性の監視
description: 正常性の監視を実施する 1 つの方法を探ります。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/16/2018
ms.openlocfilehash: 666b55608ca4e5d18448e1a0b4a1735f3e856474
ms.sourcegitcommit: 542aa405b295955eb055765f33723cb8b588d0d0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "54362484"
---
# <a name="health-monitoring"></a><span data-ttu-id="2812b-103">正常性の監視</span><span class="sxs-lookup"><span data-stu-id="2812b-103">Health monitoring</span></span>

<span data-ttu-id="2812b-104">正常性を監視することで、コンテナーとマイクロサービスの状態に関する情報をほぼリアルタイムに得ることができます。</span><span class="sxs-lookup"><span data-stu-id="2812b-104">Health monitoring can allow near-real-time information about the state of your containers and microservices.</span></span> <span data-ttu-id="2812b-105">正常性の監視はマイクロサービス運用の複数の側面において不可欠であり、オーケストレーターで段階的に部分的なアプリケーションのアップグレードを行う際に特に重要です。</span><span class="sxs-lookup"><span data-stu-id="2812b-105">Health monitoring is critical to multiple aspects of operating microservices and is especially important when orchestrators perform partial application upgrades in phases, as explained later.</span></span>

<span data-ttu-id="2812b-106">マイクロサービス ベースのアプリケーションでは、多くの場合、ハートビートまたは正常性チェックを使用して、パフォーマンス モニター、スケジューラー、およびオーケストレーターで多数のサービスを追跡できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2812b-106">Microservices-based applications often use heartbeats or health checks to enable their performance monitors, schedulers, and orchestrators to keep track of the multitude of services.</span></span> <span data-ttu-id="2812b-107">サービスが必要に応じて、またはスケジュールに従って、ある種の "アライブ" シグナルを送信できない場合、更新プログラムの展開時にアプリケーションがリスクに直面する可能性があります。あるいは、単に障害の検出が遅すぎたために障害の連鎖を防ぐことができず、最終的に大規模な停止が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2812b-107">If services cannot send some sort of “I’m alive” signal, either on demand or on a schedule, your application might face risks when you deploy updates, or it might just detect failures too late and not be able to stop cascading failures that can end up in major outages.</span></span>

<span data-ttu-id="2812b-108">標準的なモデルでは、サービスは状態に関するレポートを送信し、その情報が集約され、アプリケーションの正常性状態の概要が提供されます。</span><span class="sxs-lookup"><span data-stu-id="2812b-108">In the typical model, services send reports about their status, and that information is aggregated to provide an overall view of the state of health of your application.</span></span> <span data-ttu-id="2812b-109">オーケストレーターを使用する場合は、オーケストレーターのクラスターに正常性情報を提供することができるため、クラスターは適切に機能できます。</span><span class="sxs-lookup"><span data-stu-id="2812b-109">If you're using an orchestrator, you can provide health information to your orchestrator’s cluster, so that the cluster can act accordingly.</span></span> <span data-ttu-id="2812b-110">アプリケーション用にカスタマイズされている高品質の正常性レポートに投資する場合、実行中のアプリケーションの問題をはるかに簡単に検出して修正することができます。</span><span class="sxs-lookup"><span data-stu-id="2812b-110">If you invest in high-quality health reporting that's customized for your application, you can detect and fix issues for your running application much more easily.</span></span>

## <a name="implement-health-checks-in-aspnet-core-services"></a><span data-ttu-id="2812b-111">ASP.NET Core サービスでの正常性チェックを実装する</span><span class="sxs-lookup"><span data-stu-id="2812b-111">Implement health checks in ASP.NET Core services</span></span>

<span data-ttu-id="2812b-112">ASP.NET Core マイクロサービスまたは Web アプリケーションを開発する場合、ASP.NET チームの *Health Checks* という名前の実験的な帯域外ライブラリ (ASP.NETCore に正式には含まれておらず、現在は非推奨です) を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="2812b-112">When developing an ASP.NET Core microservice or web application, you can use an experimental out-of-band library (not official as part of ASP.NETCore and now deprecated) named *Health Checks* from the ASP.NET team.</span></span> <span data-ttu-id="2812b-113">これは、こちらの [dotnet-architecture GitHub リポジトリ](https://github.com/dotnet-architecture/HealthChecks)で入手できます。</span><span class="sxs-lookup"><span data-stu-id="2812b-113">It's available at this [dotnet-architecture GitHub repository](https://github.com/dotnet-architecture/HealthChecks).</span></span> <span data-ttu-id="2812b-114">ただし、公式バージョンの *Health Checks* は [ASP.NET Core 2.2 でリリースされる予定](https://github.com/aspnet/Announcements/issues/307)です (2018 年末までに正式にリリースされる見込みです)。</span><span class="sxs-lookup"><span data-stu-id="2812b-114">However, the official version of *Health Checks* [will be released in ASP.NET Core 2.2](https://github.com/aspnet/Announcements/issues/307) (Should be officially released by the end of 2018).</span></span>

<span data-ttu-id="2812b-115">このライブラリは使いやすく、アプリケーションに必要な特定の外部リソース (SQL Server データベースやリモート API など) が正しく動作していることを検証できる機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="2812b-115">This library is easy to use and provides features that let you validate that any specific external resource needed for your application (like a SQL Server database or remote API) is working properly.</span></span> <span data-ttu-id="2812b-116">このライブラリを使用すれば、リソースが正常であるかどうかを判断することもできます。これについては後で説明します。</span><span class="sxs-lookup"><span data-stu-id="2812b-116">When you use this library, you can also decide what it means that the resource is healthy, as we explain later.</span></span>

<span data-ttu-id="2812b-117">このライブラリを使用するには、まず、マイクロサービスでライブラリを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2812b-117">In order to use this library, you need to first use the library in your microservices.</span></span> <span data-ttu-id="2812b-118">次に、正常性レポートのクエリを実行するフロント エンド アプリケーションが必要になります。</span><span class="sxs-lookup"><span data-stu-id="2812b-118">Second, you need a front-end application that queries for the health reports.</span></span> <span data-ttu-id="2812b-119">このフロント エンド アプリケーションはカスタム レポート アプリケーションである場合があります。また、正常性状態に応じて対応できるオーケストレーター自体である場合もあります。</span><span class="sxs-lookup"><span data-stu-id="2812b-119">That front-end application could be a custom reporting application, or it could be an orchestrator itself that can react accordingly to the health states.</span></span>

### <a name="use-the-healthchecks-library-in-your-back-end-aspnet-microservices"></a><span data-ttu-id="2812b-120">バック エンド ASP.NET マイクロサービス内で HealthChecks ライブラリを使用する</span><span class="sxs-lookup"><span data-stu-id="2812b-120">Use the HealthChecks library in your back-end ASP.NET microservices</span></span>

<span data-ttu-id="2812b-121">EShopOnContainers サンプル アプリケーションでの HealthChecks ライブラリの使用方法を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="2812b-121">You can see how the HealthChecks library is used in the eShopOnContainers sample application.</span></span> <span data-ttu-id="2812b-122">開始するには、各マイクロサービスの正常性状態の構成要素を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2812b-122">To begin, you need to define what constitutes a healthy status for each microservice.</span></span> <span data-ttu-id="2812b-123">サンプル アプリケーションでは、マイクロサービス API が HTTP 経由でアクセス可能である場合と、それに関連する SQL Server データベースも使用可能である場合、マイクロサービスは正常な状態です。</span><span class="sxs-lookup"><span data-stu-id="2812b-123">In the sample application, the microservices are healthy if the microservice API is accessible via HTTP and if its related SQL Server database is also available.</span></span>

<span data-ttu-id="2812b-124">将来的には、HealthChecks ライブラリを NuGet パッケージとしてインストールできるようになります。</span><span class="sxs-lookup"><span data-stu-id="2812b-124">In the future, you'll be able to install the HealthChecks library as a NuGet package.</span></span> <span data-ttu-id="2812b-125">ただし、このドキュメントの作成時点では、ソリューションの一部として、コードをダウンロードしてコンパイルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2812b-125">But as of this writing, you need to download and compile the code as part of your solution.</span></span> <span data-ttu-id="2812b-126">[https://github.com/dotnet-architecture/HealthChecks](<https://github.com/dotnet-architecture/HealthChecks>) にあるコードを複製し、次のフォルダーをソリューションにコピーします。</span><span class="sxs-lookup"><span data-stu-id="2812b-126">Clone the code available at <https://github.com/dotnet-architecture/HealthChecks> and copy the following folders to your solution:</span></span>

- <span data-ttu-id="2812b-127">src/common</span><span class="sxs-lookup"><span data-stu-id="2812b-127">src/common</span></span>
- <span data-ttu-id="2812b-128">src/Microsoft.AspNetCore.HealthChecks</span><span class="sxs-lookup"><span data-stu-id="2812b-128">src/Microsoft.AspNetCore.HealthChecks</span></span>
- <span data-ttu-id="2812b-129">src/Microsoft.Extensions.HealthChecks</span><span class="sxs-lookup"><span data-stu-id="2812b-129">src/Microsoft.Extensions.HealthChecks</span></span>
- <span data-ttu-id="2812b-130">src/Microsoft.Extensions.HealthChecks.SqlServer</span><span class="sxs-lookup"><span data-stu-id="2812b-130">src/Microsoft.Extensions.HealthChecks.SqlServer</span></span>

<span data-ttu-id="2812b-131">Azure の場合 (Microsoft.Extensions.HealthChecks.AzureStorage) のように追加チェックを使用することもできますが、このバージョンの eShopOnContainers には Azure に対する依存関係がないため、必要ありません。</span><span class="sxs-lookup"><span data-stu-id="2812b-131">You could also use additional checks like the ones for Azure (Microsoft.Extensions.HealthChecks.AzureStorage), but since this version of eShopOnContainers does not have any dependency on Azure, you do not need it.</span></span> <span data-ttu-id="2812b-132">EShopOnContainers は ASP.NET Core に基づいているため、ASP.NET の正常性チェックは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="2812b-132">You do not need the ASP.NET health checks, because eShopOnContainers is based on ASP.NET Core.</span></span>

<span data-ttu-id="2812b-133">図 8-7 には、マイクロサービスで構成要素として使用する準備ができている、Visual Studio の HealthChecks ライブラリが示されています。</span><span class="sxs-lookup"><span data-stu-id="2812b-133">Figure 8-7 shows the HealthChecks library in Visual Studio, ready to be used as a building block by any microservices.</span></span>

![3 つのプロジェクトが表示された HealthChecks フォルダーのソリューション エクスプローラー ビュー。](./media/image6.png)

<span data-ttu-id="2812b-135">**図 8-7**</span><span class="sxs-lookup"><span data-stu-id="2812b-135">**Figure 8-7**.</span></span> <span data-ttu-id="2812b-136">Visual Studio ソリューションの ASP.NET Core HealthChecks ライブラリ ソース コード</span><span class="sxs-lookup"><span data-stu-id="2812b-136">ASP.NET Core HealthChecks library source code in a Visual Studio solution</span></span>

<span data-ttu-id="2812b-137">前述のとおり、各マイクロサービス プロジェクトでまず行うことは、3 つの HealthChecks ライブラリへの参照を追加することです。</span><span class="sxs-lookup"><span data-stu-id="2812b-137">As introduced earlier, the first thing to do in each microservice project is to add a reference to the three HealthChecks libraries.</span></span> <span data-ttu-id="2812b-138">その後、そのマイクロサービスで実行する正常性チェックのアクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="2812b-138">After that, you add the health check actions that you want to perform in that microservice.</span></span> <span data-ttu-id="2812b-139">これらのアクションは基本的に他のマイクロサービス (HttpUrlCheck) またはデータベース (現時点では SQL Server データベースの SqlCheck\*) に依存します。</span><span class="sxs-lookup"><span data-stu-id="2812b-139">These actions are basically dependencies on other microservices (HttpUrlCheck) or databases (currently SqlCheck\* for SQL Server databases).</span></span> <span data-ttu-id="2812b-140">各 ASP.NET マイクロサービスまたは ASP.NET Web アプリケーションのスタートアップ クラス内でアクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="2812b-140">You add the action within the Startup class of each ASP.NET microservice or ASP.NET web application.</span></span>

<span data-ttu-id="2812b-141">各サービスまたは Web アプリケーションは、すべての HTTP またはデータベースの依存関係を 1 つの AddHealthCheck メソッドとして追加することで構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2812b-141">Each service or web application should be configured by adding all its HTTP or database dependencies as one AddHealthCheck method.</span></span> <span data-ttu-id="2812b-142">たとえば、eShopOnContainers の MVC Web アプリケーションは多くのサービスに依存するため、正常性チェックにはいくつかの AddCheck メソッドが追加されています。</span><span class="sxs-lookup"><span data-stu-id="2812b-142">For example, the MVC web application from eShopOnContainers depends on many services, therefore has several AddCheck methods added to the health checks.</span></span>

<span data-ttu-id="2812b-143">たとえば、次の (単純化された) コードでは、カタログ マイクロサービスが SQL Server データベースに対する依存関係をどのように追加するかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="2812b-143">For instance, in the following (simplified) code you can see how the catalog microservice adds a dependency on its SQL Server database.</span></span>

```csharp
// Startup.cs from Catalog.api microservice
//
public class Startup
{
    public void ConfigureServices(IServiceCollection services)
    {
        // Add framework services
        services.AddHealthChecks(checks =>
        {
            checks.AddSqlCheck("CatalogDb", Configuration["ConnectionString"]);
        });
        // Other services
    }
}
```

<span data-ttu-id="2812b-144">ただし、eShopOnContainers の MVC Web アプリケーションには、残りのマイクロサービスに対する複数の依存関係があります。</span><span class="sxs-lookup"><span data-stu-id="2812b-144">However, the MVC web application of eShopOnContainers has multiple dependencies on the rest of the microservices.</span></span> <span data-ttu-id="2812b-145">そのため、次の (単純化された) 例に示すように、マイクロサービスごとに 1 つの AddUrlCheck メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2812b-145">Therefore, it calls one AddUrlCheck method for each microservice, as shown in the following (simplified) example:</span></span>

```csharp
// Startup.cs from the MVC web app
public class Startup
{
    public void ConfigureServices(IServiceCollection services)
    {
        services.AddMvc();
        services.Configure<AppSettings>(Configuration);
        services.AddHealthChecks(checks =>
        {
            checks.AddUrlCheck(Configuration["CatalogUrl"]);
            checks.AddUrlCheck(Configuration["OrderingUrl"]);
            checks.AddUrlCheck(Configuration["BasketUrl"]);
            checks.AddUrlCheck(Configuration["IdentityUrl"]);
        });
    }
}
```

<span data-ttu-id="2812b-146">したがって、そのすべてのチェックでも正常であると判断されるまで、マイクロサービスでは "正常" 状態と示されません。</span><span class="sxs-lookup"><span data-stu-id="2812b-146">Thus, a microservice will not provide a “healthy” status until all its checks are healthy as well.</span></span>

<span data-ttu-id="2812b-147">マイクロサービスにサービスまたは SQL Server に対する依存関係がない場合は、Healthy("Ok") チェックを追加するだけ済みます。</span><span class="sxs-lookup"><span data-stu-id="2812b-147">If the microservice does not have a dependency on a service or on SQL Server, you should just add a Healthy("Ok") check.</span></span> <span data-ttu-id="2812b-148">次のコードは eShopOnContainers `basket.api` マイクロサービスのものです</span><span class="sxs-lookup"><span data-stu-id="2812b-148">The following code is from the eShopOnContainers `basket.api` microservice.</span></span> <span data-ttu-id="2812b-149">(バスケット マイクロサービスでは Redis Cache を使用しますが、ライブラリにはまだ Redis 正常性チェック プロバイダーは含まれていません)。</span><span class="sxs-lookup"><span data-stu-id="2812b-149">(The basket microservice uses the Redis cache, but the library does not yet include a Redis health check provider.)</span></span>

```csharp
services.AddHealthChecks(checks =>
{
    checks.AddValueTaskCheck("HTTP Endpoint", () => new
        ValueTask<IHealthCheckResult>(HealthCheckResult.Healthy("Ok")));
});
```

<span data-ttu-id="2812b-150">サービスまたは Web アプリケーションで正常性チェック エンドポイントを公開するには、`UseHealthChecks([*url_for_health_checks*])` 拡張メソッドを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2812b-150">For a service or web application to expose the health check endpoint, it has to enable the `UseHealthChecks([*url_for_health_checks*])` extension method.</span></span> <span data-ttu-id="2812b-151">このメソッドは、次の簡略化されたコードに示すように、ASP.NET Core サービスまたは Web アプリケーションの `Program` クラスのメイン メソッドの `WebHostBuilder` レベルで <xref:Microsoft.AspNetCore.WebHost.CreateDefaultBuilder> の直後に配置されます。</span><span class="sxs-lookup"><span data-stu-id="2812b-151">This method goes at the `WebHostBuilder` level in the main method of the `Program` class of your ASP.NET Core service or web application, right after <xref:Microsoft.AspNetCore.WebHost.CreateDefaultBuilder> as shown in the following simplified code:</span></span>

```csharp
namespace Microsoft.eShopOnContainers.WebMVC
{
    public class Program
    {
        public static void Main(string[] args)
        {
            var host = WebHost.CreateDefaultBuilder(args)
                .UseHealthChecks("/hc")
                .UseContentRoot(Directory.GetCurrentDirectory())
                .UseStartup<Startup>()
                .Build();

            host.Run();
        }
    }
}
```

<span data-ttu-id="2812b-152">プロセスのしくみは次のとおりです。まず、各マイクロサービスがエンドポイント /hc を公開します。</span><span class="sxs-lookup"><span data-stu-id="2812b-152">The process works this way: each microservice exposes the endpoint /hc.</span></span> <span data-ttu-id="2812b-153">そのエンドポイントは、HealthChecks ライブラリの ASP.NET Core ミドルウェアによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="2812b-153">That endpoint is created by the HealthChecks library ASP.NET Core middleware.</span></span> <span data-ttu-id="2812b-154">そのエンドポイントが呼び出されたときに、スタートアップ クラスの AddHealthChecks メソッドで構成されているすべての正常性チェックが実行されます。</span><span class="sxs-lookup"><span data-stu-id="2812b-154">When that endpoint is invoked, it runs all the health checks that are configured in the AddHealthChecks method in the Startup class.</span></span>

<span data-ttu-id="2812b-155">UseHealthChecks メソッドにはポートまたはパスが必要です。</span><span class="sxs-lookup"><span data-stu-id="2812b-155">The UseHealthChecks method expects a port or a path.</span></span> <span data-ttu-id="2812b-156">そのポートまたはパスはエンドポイントであり、サービスの正常性状態を確認するために使用します。</span><span class="sxs-lookup"><span data-stu-id="2812b-156">That port or path is the endpoint to use to check the health state of the service.</span></span> <span data-ttu-id="2812b-157">たとえば、カタログ マイクロサービスではパス /hc を使用します。</span><span class="sxs-lookup"><span data-stu-id="2812b-157">For instance, the catalog microservice uses the path /hc.</span></span>

### <a name="cache-health-check-responses"></a><span data-ttu-id="2812b-158">正常性チェック応答をキャッシュする</span><span class="sxs-lookup"><span data-stu-id="2812b-158">Cache health check responses</span></span>

<span data-ttu-id="2812b-159">サービスでサービス拒否攻撃 (DoS) が発生しないようにする場合や、リソースを頻繁に確認しすぎてサービスのパフォーマンスが影響を受けることのないようにするだけの場合は、戻り値をキャッシュし、各正常性チェックのキャッシュ期間を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="2812b-159">Since you do not want to cause a Denial of Service (DoS) in your services, or you simply do not want to impact service performance by checking resources too frequently, you can cache the returns and configure a cache duration for each health check.</span></span>

<span data-ttu-id="2812b-160">既定では、キャッシュ期間は内部的に 5 分に設定されますが、次のコードのように、各正常性チェックでそのキャッシュ期間を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="2812b-160">By default, the cache duration is internally set to 5 minutes, but you can change that cache duration on each health check, as in the following code:</span></span>

```csharp
checks.AddUrlCheck(Configuration["CatalogUrl"],1); // 1 min as cache duration
```

### <a name="query-your-microservices-to-report-about-their-health-status"></a><span data-ttu-id="2812b-161">マイクロサービスでクエリを実行してその正常性状態についてレポートする</span><span class="sxs-lookup"><span data-stu-id="2812b-161">Query your microservices to report about their health status</span></span>

<span data-ttu-id="2812b-162">この記事の説明に従って正常性チェックを構成し、マイクロサービスを Docker で実行した後、正常かどうかをブラウザーから直接確認することができます。</span><span class="sxs-lookup"><span data-stu-id="2812b-162">When you've configured health checks as described in this article and you have the microservice running in Docker, you can directly check from a browser if it's healthy.</span></span>

<span data-ttu-id="2812b-163">図 8-8 に示すように、Docker ホスト内でコンテナー ポートを公開し、外部の Docker ホスト IP または `localhost` を介してコンテナーにアクセスできるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2812b-163">You have to publish the container port in the Docker host, so you can access the container through the external Docker host IP or through `localhost`, as shown in figure 8-8.</span></span>

![正常性チェックから返された JSON 応答のブラウザー ビュー](./media/image7.png)

<span data-ttu-id="2812b-165">**図 8-8**</span><span class="sxs-lookup"><span data-stu-id="2812b-165">**Figure 8-8**.</span></span> <span data-ttu-id="2812b-166">ブラウザーからの単一サービスの正常性状態の確認</span><span class="sxs-lookup"><span data-stu-id="2812b-166">Checking health status of a single service from a browser</span></span>

<span data-ttu-id="2812b-167">このテストでは、catalog.api マイクロサービス (ポート 5101 で実行されている) が正常であり、JSON で HTTP ステータス 200 とステータス情報が返されていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="2812b-167">In that test, you can see that the catalog.api microservice (running on port 5101) is healthy, returning HTTP status 200 and status information in JSON.</span></span> <span data-ttu-id="2812b-168">これは、内部的にサービスが SQL Server データベースの依存関係の正常性も確認し、その正常性チェック自体が正常とレポートされたことも意味します。</span><span class="sxs-lookup"><span data-stu-id="2812b-168">It also means that internally the service also checked the health of its SQL Server database dependency and that health check was reported itself as healthy.</span></span>

## <a name="use-watchdogs"></a><span data-ttu-id="2812b-169">ウォッチドッグを使用する</span><span class="sxs-lookup"><span data-stu-id="2812b-169">Use watchdogs</span></span>

<span data-ttu-id="2812b-170">ウォッチドッグは、サービス間の正常性と負荷を監視し、前述の `HealthChecks` ライブラリを使用してクエリを実行することでマイクロサービスに関する正常性をレポートできる別個のサービスです。</span><span class="sxs-lookup"><span data-stu-id="2812b-170">A watchdog is a separate service that can watch health and load across services, and report health about the microservices by querying with the `HealthChecks` library introduced earlier.</span></span> <span data-ttu-id="2812b-171">これは、単一サービスのビューに基づいて検出されないエラーを防ぐのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2812b-171">This can help prevent errors that would not be detected based on the view of a single service.</span></span> <span data-ttu-id="2812b-172">また、ウォッチドッグは、ユーザーの介入なしで既知の状態に応じて修復アクションを実行できるコードをホストする場合に適しています。</span><span class="sxs-lookup"><span data-stu-id="2812b-172">Watchdogs also are a good place to host code that can perform remediation actions for known conditions without user interaction.</span></span>

<span data-ttu-id="2812b-173">eShopOnContainers サンプルには、図 8-9 に示すように、サンプルの正常性チェック レポートを表示する Web ページが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2812b-173">The eShopOnContainers sample contains a web page that displays sample health check reports, as shown in Figure 8-9.</span></span> <span data-ttu-id="2812b-174">これは、eShopOnContainers でマイクロサービスと Web アプリケーションの状態を表示するだけなので、使用可能な最も単純なウォッチドッグです。</span><span class="sxs-lookup"><span data-stu-id="2812b-174">This is the simplest watchdog you could have since it only shows the state of the microservices and web applications in eShopOnContainers.</span></span> <span data-ttu-id="2812b-175">通常、ウォッチドッグは異常状態の検出時にもアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="2812b-175">Usually a watchdog also takes actions when it detects unhealthy states.</span></span>

![eShopOnContainers の 5 つのマイクロサービスの正常性状態が表示された WebStatus アプリのブラウザー ビュー。](./media/image8.png)

<span data-ttu-id="2812b-177">**図 8-9**</span><span class="sxs-lookup"><span data-stu-id="2812b-177">**Figure 8-9**.</span></span> <span data-ttu-id="2812b-178">eShopOnContainers のサンプルの正常性チェック レポート</span><span class="sxs-lookup"><span data-stu-id="2812b-178">Sample health check report in eShopOnContainers</span></span>

<span data-ttu-id="2812b-179">つまり、ASP.NET Core HealthChecks ライブラリの ASP.NET ミドルウェアでは、マイクロサービスごとに 1 つの正常性チェック エンドポイントを提供します。</span><span class="sxs-lookup"><span data-stu-id="2812b-179">In summary, the ASP.NET middleware of the ASP.NET Core HealthChecks library provides a single health check endpoint for each microservice.</span></span> <span data-ttu-id="2812b-180">これにより、定義されているすべての正常性チェックが実行され、これらすべてのチェックに応じて、全体的な正常性状態が返されます。</span><span class="sxs-lookup"><span data-stu-id="2812b-180">This will execute all the health checks defined within it and return an overall health state depending on all those checks.</span></span>

<span data-ttu-id="2812b-181">HealthChecks ライブラリは、今後の外部リソースの新しい正常性チェックにより拡張可能です。</span><span class="sxs-lookup"><span data-stu-id="2812b-181">The HealthChecks library is extensible through new health checks of future external resources.</span></span> <span data-ttu-id="2812b-182">たとえば、今後、ライブラリに Redis Cache や他のデータベースの正常性チェックが含まれることが予想されます。</span><span class="sxs-lookup"><span data-stu-id="2812b-182">For example, we expect that in the future the library will have health checks for Redis cache and for other databases.</span></span> <span data-ttu-id="2812b-183">ライブラリでは複数のサービスまたはアプリケーションの依存関係での正常性レポートが可能であるため、これらの正常性チェックに基づいてアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="2812b-183">The library allows health reporting by multiple service or application dependencies, and you can then take actions based on those health checks.</span></span>

## <a name="health-checks-when-using-orchestrators"></a><span data-ttu-id="2812b-184">オーケストレーターを使用する場合の正常性チェック</span><span class="sxs-lookup"><span data-stu-id="2812b-184">Health checks when using orchestrators</span></span>

<span data-ttu-id="2812b-185">マイクロサービスの可用性を監視するために、Kubernetes、Service Fabric などのオーケストレーターではマイクロサービスのテスト要求を送信して、定期的に正常性チェックを実行します。</span><span class="sxs-lookup"><span data-stu-id="2812b-185">To monitor the availability of your microservices, orchestrators like Kubernetes and Service Fabric periodically perform health checks by sending requests to test the microservices.</span></span> <span data-ttu-id="2812b-186">オーケストレーターでサービス/コンテナーが異常であると判断された場合、そのインスタンスへの要求のルーティングが停止します。</span><span class="sxs-lookup"><span data-stu-id="2812b-186">When an orchestrator determines that a service/container is unhealthy, it stops routing requests to that instance.</span></span> <span data-ttu-id="2812b-187">通常は、そのコンテナーの新しいインスタンスも作成されます。</span><span class="sxs-lookup"><span data-stu-id="2812b-187">It also usually creates a new instance of that container.</span></span>

<span data-ttu-id="2812b-188">たとえば、ほとんどのオーケストレーターでは、ダウンタイムなしの展開を管理するために正常性チェックを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2812b-188">For instance, most orchestrators can use health checks to manage zero-downtime deployments.</span></span> <span data-ttu-id="2812b-189">サービス/コンテナーの状態が正常に変わった場合にのみ、オーケストレーターはサービス/コンテナー インスタンスへのトラフィックのルーティングを開始します。</span><span class="sxs-lookup"><span data-stu-id="2812b-189">Only when the status of a service/container changes to healthy will the orchestrator start routing traffic to service/container instances.</span></span>

<span data-ttu-id="2812b-190">正常性の監視は、オーケストレーターがアプリケーションのアップグレードを実行する場合に特に重要です。</span><span class="sxs-lookup"><span data-stu-id="2812b-190">Health monitoring is especially important when an orchestrator performs an application upgrade.</span></span> <span data-ttu-id="2812b-191">いくつかのオーケストレーター (Azure Service Fabric など) ではサービスを段階的に更新します。たとえば、アプリケーションのアップグレードごとに 5 分の 1 のクラスター サーフェスを更新する場合があります。</span><span class="sxs-lookup"><span data-stu-id="2812b-191">Some orchestrators (like Azure Service Fabric) update services in phases—for example, they might update one-fifth of the cluster surface for each application upgrade.</span></span> <span data-ttu-id="2812b-192">同時にアップグレードされるノード セットは*アップグレード ドメイン* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="2812b-192">The set of nodes that's upgraded at the same time is referred to as an *upgrade domain*.</span></span> <span data-ttu-id="2812b-193">各アップグレード ドメインがアップグレードされ、ユーザーが使用できるようになったら、そのアップグレード ドメインは、展開が次のアップグレード ドメインに移る前に正常性チェックを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2812b-193">After each upgrade domain has been upgraded and is available to users, that upgrade domain must pass health checks before the deployment moves to the next upgrade domain.</span></span>

<span data-ttu-id="2812b-194">サービスの正常性のもう 1 つの側面は、サービスからのメトリックのレポートです。</span><span class="sxs-lookup"><span data-stu-id="2812b-194">Another aspect of service health is reporting metrics from the service.</span></span> <span data-ttu-id="2812b-195">これは、Service Fabric などの一部のオーケストレーターの正常性モデルの高度な機能です。</span><span class="sxs-lookup"><span data-stu-id="2812b-195">This is an advanced capability of the health model of some orchestrators, like Service Fabric.</span></span> <span data-ttu-id="2812b-196">メトリックは、リソース使用量のバランスをとるために使用されるため、オーケストレーターの使用時に重要になります。</span><span class="sxs-lookup"><span data-stu-id="2812b-196">Metrics are important when using an orchestrator because they are used to balance resource usage.</span></span> <span data-ttu-id="2812b-197">メトリックをシステム正常性のインジケーターにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="2812b-197">Metrics also can be an indicator of system health.</span></span> <span data-ttu-id="2812b-198">たとえば、アプリケーションに多くのマイクロサービスがあり、各インスタンスで要求/秒 (RPS) メトリックをレポートするとします。</span><span class="sxs-lookup"><span data-stu-id="2812b-198">For example, you might have an application that has many microservices, and each instance reports a requests-per-second (RPS) metric.</span></span> <span data-ttu-id="2812b-199">1 つのサービスが別のサービスより多くのリソース (メモリやプロセッサなど) を使用している場合、オーケストレーターはクラスター内でサービス インスタンスを移動して、リソース使用率を均一に保つことができます。</span><span class="sxs-lookup"><span data-stu-id="2812b-199">If one service is using more resources (memory, processor, etc.) than another service, the orchestrator could move service instances around in the cluster to try to maintain even resource utilization.</span></span>

<span data-ttu-id="2812b-200">Azure Service Fabric には、単純な正常性チェックよりも高度な独自の[正常性の監視モデル](/azure/service-fabric/service-fabric-health-introduction)が提供されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2812b-200">Note that Azure Service Fabric provides its own [Health Monitoring model](/azure/service-fabric/service-fabric-health-introduction), which is more advanced than simple health checks.</span></span>

## <a name="advanced-monitoring-visualization-analysis-and-alerts"></a><span data-ttu-id="2812b-201">高度な監視: 視覚化、分析、およびアラート</span><span class="sxs-lookup"><span data-stu-id="2812b-201">Advanced monitoring: visualization, analysis, and alerts</span></span>

<span data-ttu-id="2812b-202">監視の最後の部分は、イベント ストリームの視覚化、サービス パフォーマンスのレポート、および問題の検出時のアラートです。</span><span class="sxs-lookup"><span data-stu-id="2812b-202">The final part of monitoring is visualizing the event stream, reporting on service performance, and alerting when an issue is detected.</span></span> <span data-ttu-id="2812b-203">監視のこの部分ではさまざまなソリューションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2812b-203">You can use different solutions for this aspect of monitoring.</span></span>

<span data-ttu-id="2812b-204">[ASP.NET Core HealthChecks](https://github.com/dotnet-architecture/HealthChecks) の説明の際に示したカスタム ページのように、サービスの状態を示す単純なカスタム アプリケーションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2812b-204">You can use simple custom applications showing the state of your services, like the custom page shown when explaining the [ASP.NET Core HealthChecks](https://github.com/dotnet-architecture/HealthChecks).</span></span> <span data-ttu-id="2812b-205">また、Azure Application Insights などのより高度なツールを使用して、イベントのストリームに基づき、アラートを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="2812b-205">Or you could use more advanced tools like Azure Application Insights to raise alerts based on the stream of events.</span></span>

<span data-ttu-id="2812b-206">最後に、すべてのイベント ストリームを格納していた場合、Microsoft Power BI、または Kibana や Splunk などの他のソリューションを使用して、データを視覚化することができます。</span><span class="sxs-lookup"><span data-stu-id="2812b-206">Finally, if you're storing all the event streams, you can use Microsoft Power BI or other solutions like Kibana or Splunk to visualize the data.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2812b-207">その他の技術情報</span><span class="sxs-lookup"><span data-stu-id="2812b-207">Additional resources</span></span>

- <span data-ttu-id="2812b-208">**ASP.NET Core HealthChecks** (早期リリース)\\</span><span class="sxs-lookup"><span data-stu-id="2812b-208">**ASP.NET Core HealthChecks** (experimental release)\\</span></span>
  [*https://github.com/dotnet-architecture/HealthChecks/*](https://github.com/dotnet-architecture/HealthChecks/)

- <span data-ttu-id="2812b-209">**Service Fabric 正常性監視の概要**\\</span><span class="sxs-lookup"><span data-stu-id="2812b-209">**Introduction to Service Fabric health monitoring**\\</span></span>
  [*https://docs.microsoft.com/azure/service-fabric/service-fabric-health-introduction*](/azure/service-fabric/service-fabric-health-introduction)

- <span data-ttu-id="2812b-210">**Azure Application Insights**\\</span><span class="sxs-lookup"><span data-stu-id="2812b-210">**Azure Application Insights**\\</span></span>
  [*https://azure.microsoft.com/services/application-insights/*](https://azure.microsoft.com/services/application-insights/)

- <span data-ttu-id="2812b-211">**Microsoft Operations Management Suite**\\</span><span class="sxs-lookup"><span data-stu-id="2812b-211">**Microsoft Operations Management Suite**\\</span></span>
  [*https://www.microsoft.com/cloud-platform/operations-management-suite*](https://www.microsoft.com/cloud-platform/operations-management-suite)

>[!div class="step-by-step"]
><span data-ttu-id="2812b-212">[前へ](implement-circuit-breaker-pattern.md)
>[次へ](../secure-net-microservices-web-applications/index.md)</span><span class="sxs-lookup"><span data-stu-id="2812b-212">[Previous](implement-circuit-breaker-pattern.md)
[Next](../secure-net-microservices-web-applications/index.md)</span></span>