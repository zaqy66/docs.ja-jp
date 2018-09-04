---
title: ルーティング サービスを使用した Hello World
ms.date: 03/30/2017
ms.assetid: 0f4b0d5b-6522-4ad5-9f3a-baa78316d7d1
ms.openlocfilehash: 490d91da22b11c269c4d3c11d376087919a608e0
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43519200"
---
# <a name="hello-world-with-the-routing-service"></a><span data-ttu-id="e94b1-102">ルーティング サービスを使用した Hello World</span><span class="sxs-lookup"><span data-stu-id="e94b1-102">Hello World with the Routing Service</span></span>
<span data-ttu-id="e94b1-103">このサンプルでは、Windows Communication Foundation (WCF) ルーティング サービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="e94b1-103">This sample demonstrates the Windows Communication Foundation (WCF) Routing Service.</span></span> <span data-ttu-id="e94b1-104">ルーティング サービスは、WCF コンポーネント、アプリケーションでコンテンツ ベースのルーターを含めるが簡単です。</span><span class="sxs-lookup"><span data-stu-id="e94b1-104">The Routing Service is a WCF component that makes it easy to include a content-based router in your application.</span></span> <span data-ttu-id="e94b1-105">このサンプルでは、ルーティング サービスを使用して通信する標準の WCF 電卓のサンプルを適応します。</span><span class="sxs-lookup"><span data-stu-id="e94b1-105">This sample adapts the standard WCF Calculator Sample to communicate using the Routing Service.</span></span> <span data-ttu-id="e94b1-106">このサンプルの電卓クライアントは、ルーターによって公開されるエンドポイントにメッセージを送信するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="e94b1-106">In this sample, the Calculator client is configured to send messages to an endpoint exposed by the router.</span></span> <span data-ttu-id="e94b1-107">ルーティング サービスは、送信されてきたすべてのメッセージを受け入れ、電卓サービスに対応するエンドポイントに転送するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="e94b1-107">The Routing Service is configured to accept all messages sent to it and to forward them to an endpoint that corresponds to the Calculator service.</span></span> <span data-ttu-id="e94b1-108">したがって、クライアントから送信されたメッセージはルーターで受信され、実際の電卓サービスに再ルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="e94b1-108">Thus messages sent from the client are received by the router and re-routed to the actual Calculator service.</span></span> <span data-ttu-id="e94b1-109">電卓サービスからのメッセージはルーターに送り返され、ルーターから電卓クライアントに渡されます。</span><span class="sxs-lookup"><span data-stu-id="e94b1-109">Messages from the Calculator service are sent back to the router, which in turn passes them back to the Calculator client.</span></span>  
  
### <a name="to-use-this-sample"></a><span data-ttu-id="e94b1-110">このサンプルを使用するには</span><span class="sxs-lookup"><span data-stu-id="e94b1-110">To use this sample</span></span>  
  
1.  <span data-ttu-id="e94b1-111">[!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] を使用して、HelloRoutingService.sln を開きます。</span><span class="sxs-lookup"><span data-stu-id="e94b1-111">Using [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], open HelloRoutingService.sln.</span></span>  
  
2.  <span data-ttu-id="e94b1-112">F5 キーを押すか、Ctrl キーと Shift キーを押しながら B キーを押します。</span><span class="sxs-lookup"><span data-stu-id="e94b1-112">Press F5 or CTRL+SHIFT+B.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="e94b1-113">F5 キーを押した場合は、電卓クライアントが自動的に起動します。</span><span class="sxs-lookup"><span data-stu-id="e94b1-113">If you press F5, the Calculator Client automatically starts.</span></span> <span data-ttu-id="e94b1-114">Ctrl キーと Shift キーを押しながら B キーを押した (ビルドする) 場合は、次のアプリケーションを手動で開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e94b1-114">If you press CTRL+SHIFT+B (build), you must start following applications yourself.</span></span>  
    >  
    > 1.  <span data-ttu-id="e94b1-115">電卓クライアント (./CalculatorClient/bin/client.exe)</span><span class="sxs-lookup"><span data-stu-id="e94b1-115">Calculator client (./CalculatorClient/bin/client.exe</span></span>  
    > 2.  <span data-ttu-id="e94b1-116">電卓サービス (./CalculatorService/bin/service.exe)</span><span class="sxs-lookup"><span data-stu-id="e94b1-116">Calculator service (./CalculatorService/bin/service.exe)</span></span>  
    > 3.  <span data-ttu-id="e94b1-117">ルーティング サービス (./RoutingService/bin/RoutingService.exe)</span><span class="sxs-lookup"><span data-stu-id="e94b1-117">Routing service (./RoutingService/bin/RoutingService.exe)</span></span>  
  
3.  <span data-ttu-id="e94b1-118">Enter キーを押してクライアントを起動します。</span><span class="sxs-lookup"><span data-stu-id="e94b1-118">Press ENTER to start the client.</span></span>  
  
     <span data-ttu-id="e94b1-119">次の出力が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e94b1-119">You should see the following output:</span></span>  
  
     <span data-ttu-id="e94b1-120">Add(100,15.99) = 115.99</span><span class="sxs-lookup"><span data-stu-id="e94b1-120">Add(100,15.99) = 115.99</span></span>  
  
     <span data-ttu-id="e94b1-121">Subtract(145,76.54) = 68.46</span><span class="sxs-lookup"><span data-stu-id="e94b1-121">Subtract(145,76.54) = 68.46</span></span>  
  
     <span data-ttu-id="e94b1-122">Multiply(9,81.25) = 731.25</span><span class="sxs-lookup"><span data-stu-id="e94b1-122">Multiply(9,81.25) = 731.25</span></span>  
  
     <span data-ttu-id="e94b1-123">Divide(22,7) = 3.14285714285714</span><span class="sxs-lookup"><span data-stu-id="e94b1-123">Divide(22,7) = 3.14285714285714</span></span>  
  
## <a name="configurable-via-code-or-appconfig"></a><span data-ttu-id="e94b1-124">コードまたは App.Config で構成可能</span><span class="sxs-lookup"><span data-stu-id="e94b1-124">Configurable via Code or App.Config</span></span>  
 <span data-ttu-id="e94b1-125">サンプルは、提供された時点では、App.config ファイルを使用してルーターの動作を定義するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="e94b1-125">The sample ships configured to use an App.config file to define the router’s behavior.</span></span> <span data-ttu-id="e94b1-126">App.config ファイルの名前を別の名前に変更して認識されないようにし、ConfigureRouterViaCode() に対するメソッド呼び出しのコメントを解除することもできます。</span><span class="sxs-lookup"><span data-stu-id="e94b1-126">You can also change the name of the App.config file to something else so that it is not recognized and uncomment the method call to ConfigureRouterViaCode().</span></span> <span data-ttu-id="e94b1-127">どちらの方法でも、ルーターの動作は同じになります。</span><span class="sxs-lookup"><span data-stu-id="e94b1-127">Either method results in the same behavior from the router.</span></span>  
  
### <a name="scenario"></a><span data-ttu-id="e94b1-128">シナリオ</span><span class="sxs-lookup"><span data-stu-id="e94b1-128">Scenario</span></span>  
 <span data-ttu-id="e94b1-129">このサンプルでは、基本的なメッセージ ポンプとして機能するルーターを示します。</span><span class="sxs-lookup"><span data-stu-id="e94b1-129">This sample demonstrates the router acting as a basic message pump.</span></span> <span data-ttu-id="e94b1-130">ルーティング サービスは、構成済みの一連の送信先エンドポイントに直接メッセージを渡すように構成された透過的なプロキシ ノードとして機能します。</span><span class="sxs-lookup"><span data-stu-id="e94b1-130">The routing service acts as a transparent proxy node configured to pass messages directly to a preconfigured set of destination endpoints.</span></span>  
  
### <a name="real-world-scenario"></a><span data-ttu-id="e94b1-131">実際のシナリオ</span><span class="sxs-lookup"><span data-stu-id="e94b1-131">Real World Scenario</span></span>  
 <span data-ttu-id="e94b1-132">Contoso では、サービスの名前指定、アドレス指定、構成、およびセキュリティに関する柔軟性を高めるために、</span><span class="sxs-lookup"><span data-stu-id="e94b1-132">Contoso wants to increase the flexibility it has in the naming, addressing, configuration, and security of its services.</span></span> <span data-ttu-id="e94b1-133">基本的なメッセージ ポンプをサービスの前に配置して、それをエンドポイントとして公開しています。</span><span class="sxs-lookup"><span data-stu-id="e94b1-133">To do this, they place a basic message pump in front of their services to act as a public facing endpoint.</span></span> <span data-ttu-id="e94b1-134">これにより、実際のサービスの前にセキュリティが追加され、スケールアウトされたソリューションやサービスのバージョン管理を後で簡単に実装できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e94b1-134">This allows them to place additional security in front of their actual services and make it easier to implement scaled out solutions or service versioning at a later date.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="e94b1-135">サンプルは、既にコンピューターにインストールされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="e94b1-135">The samples may already be installed on your computer.</span></span> <span data-ttu-id="e94b1-136">続行する前に、次の (既定の) ディレクトリを確認してください。</span><span class="sxs-lookup"><span data-stu-id="e94b1-136">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="e94b1-137">このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。</span><span class="sxs-lookup"><span data-stu-id="e94b1-137">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="e94b1-138">このサンプルは、次のディレクトリに格納されます。</span><span class="sxs-lookup"><span data-stu-id="e94b1-138">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\RoutingServices\HelloRoutingService`  
  
## <a name="see-also"></a><span data-ttu-id="e94b1-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="e94b1-139">See Also</span></span>  
 [<span data-ttu-id="e94b1-140">AppFabric のホストおよび永続化のサンプル</span><span class="sxs-lookup"><span data-stu-id="e94b1-140">AppFabric Hosting and Persistence Samples</span></span>](https://go.microsoft.com/fwlink/?LinkId=193961)
