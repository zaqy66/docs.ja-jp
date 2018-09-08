---
title: Windows Workflow Foundation の機能仕様
ms.date: 03/30/2017
ms.assetid: e84d12da-a055-45f6-b4d1-878d127b46b6
ms.openlocfilehash: b18c6dd76762f4495ac475cd3dfa4e1995733b59
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44205076"
---
# <a name="windows-workflow-foundation-feature-specifics"></a><span data-ttu-id="91e03-102">Windows Workflow Foundation の機能仕様</span><span class="sxs-lookup"><span data-stu-id="91e03-102">Windows Workflow Foundation Feature Specifics</span></span>
[!INCLUDE[netfx40_long](../../../includes/netfx40-long-md.md)]<span data-ttu-id="91e03-103"> は、Windows Workflow Foundation にいくつかの機能を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e03-103"> adds a number of features to Windows Workflow Foundation.</span></span> <span data-ttu-id="91e03-104">このドキュメントでは、いくつかの新機能について説明し、役に立つ可能性のあるシナリオの詳細を示します。</span><span class="sxs-lookup"><span data-stu-id="91e03-104">This document describes a number of the new features, and gives details about scenarios in which they may be useful.</span></span>  
  
## <a name="messaging-activities"></a><span data-ttu-id="91e03-105">メッセージング アクティビティ</span><span class="sxs-lookup"><span data-stu-id="91e03-105">Messaging Activities</span></span>  
 <span data-ttu-id="91e03-106">メッセージング アクティビティ (<xref:System.ServiceModel.Activities.Receive>、 <xref:System.ServiceModel.Activities.SendReply>、 <xref:System.ServiceModel.Activities.Send>、 <xref:System.ServiceModel.Activities.ReceiveReply>)、ワークフローから WCF メッセージを送受信するために使用します。</span><span class="sxs-lookup"><span data-stu-id="91e03-106">The messaging activities (<xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.SendReply>, <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.ReceiveReply>) are used to send and receive WCF messages from your workflow.</span></span>  <span data-ttu-id="91e03-107"><xref:System.ServiceModel.Activities.Receive> <xref:System.ServiceModel.Activities.SendReply>アクティビティが標準の WCF web サービスと同様に、WSDL 経由で公開される Windows Communication Foundation (WCF) サービスの操作を形成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="91e03-107"><xref:System.ServiceModel.Activities.Receive> and <xref:System.ServiceModel.Activities.SendReply> activities are used to form a Windows Communication Foundation (WCF) service operation that is exposed via WSDL just like standard WCF web services.</span></span>  <span data-ttu-id="91e03-108"><xref:System.ServiceModel.Activities.Send> <xref:System.ServiceModel.Activities.ReceiveReply> WCF のような web サービスを使用するために使用<xref:System.ServiceModel.ChannelFactory>は**サービス参照の追加**エクスペリエンスは、事前構成済みのアクティビティを生成する Workflow Foundation にも存在します。</span><span class="sxs-lookup"><span data-stu-id="91e03-108"><xref:System.ServiceModel.Activities.Send> and <xref:System.ServiceModel.Activities.ReceiveReply> are used to consume a web service similar to a WCF <xref:System.ServiceModel.ChannelFactory>; an **Add Service Reference** experience also exists for Workflow Foundation that generates pre-configured activities.</span></span>  
  
### <a name="getting-started-with-messaging-activities"></a><span data-ttu-id="91e03-109">メッセージング アクティビティの概要</span><span class="sxs-lookup"><span data-stu-id="91e03-109">Getting Started with Messaging Activities</span></span>  
  
-   <span data-ttu-id="91e03-110">[!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)] で、WCF ワークフロー サービス アプリケーション プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="91e03-110">In [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)], create a WCF Workflow Service Application project.</span></span> <span data-ttu-id="91e03-111"><xref:System.ServiceModel.Activities.Receive> と <xref:System.ServiceModel.Activities.SendReply> のペアがキャンバスに配置されます。</span><span class="sxs-lookup"><span data-stu-id="91e03-111">A <xref:System.ServiceModel.Activities.Receive> and <xref:System.ServiceModel.Activities.SendReply> pair will be placed on your canvas.</span></span>  
  
-   <span data-ttu-id="91e03-112">クリックし、プロジェクトを右クリックして**サービス参照の追加**します。</span><span class="sxs-lookup"><span data-stu-id="91e03-112">Right-click on the project and select **Add Service Reference**.</span></span>  <span data-ttu-id="91e03-113">既存の web サービス WSDL をポイントしてクリックして**OK**します。</span><span class="sxs-lookup"><span data-stu-id="91e03-113">Point to an existing web service WSDL and click **OK**.</span></span>  <span data-ttu-id="91e03-114">生成されたアクティビティを表示するプロジェクトをビルド (を使用して実装<xref:System.ServiceModel.Activities.Send>と<xref:System.ServiceModel.Activities.ReceiveReply>)、ツールボックスにします。</span><span class="sxs-lookup"><span data-stu-id="91e03-114">Build your project to show the generated activities (implemented using <xref:System.ServiceModel.Activities.Send> and <xref:System.ServiceModel.Activities.ReceiveReply>) in your toolbox.</span></span>  
  
-   <span data-ttu-id="91e03-115">これらのアクティビティのサンプルは次のセクションにあります。</span><span class="sxs-lookup"><span data-stu-id="91e03-115">Samples for these activities can be found in the following sections:</span></span>  
  
    -   <span data-ttu-id="91e03-116">Basic:[サービス](../../../docs/framework/windows-workflow-foundation/samples/services.md)</span><span class="sxs-lookup"><span data-stu-id="91e03-116">Basic: [Services](../../../docs/framework/windows-workflow-foundation/samples/services.md)</span></span>  
  
    -   <span data-ttu-id="91e03-117">シナリオ:[サービス](../../../docs/framework/windows-workflow-foundation/samples/services.md)</span><span class="sxs-lookup"><span data-stu-id="91e03-117">Scenarios: [Services](../../../docs/framework/windows-workflow-foundation/samples/services.md)</span></span>  
  
-   [<span data-ttu-id="91e03-118">概念説明のドキュメント</span><span class="sxs-lookup"><span data-stu-id="91e03-118">Conceptual documentation</span></span>](https://go.microsoft.com/fwlink/?LinkId=204801)  
  
-   [<span data-ttu-id="91e03-119">メッセージング アクティビティ デザイナーのドキュメント</span><span class="sxs-lookup"><span data-stu-id="91e03-119">Messaging activities designer documentation</span></span>](https://go.microsoft.com/fwlink/?LinkId=204802)  
  
### <a name="messaging-activities-example-scenario"></a><span data-ttu-id="91e03-120">メッセージング アクティビティのシナリオ例</span><span class="sxs-lookup"><span data-stu-id="91e03-120">Messaging Activities Example Scenario</span></span>  
 <span data-ttu-id="91e03-121">A`BestPriceFinder`サービスは、複数の航空会社サービスを特定のルートの最良チケット価格を検索します。</span><span class="sxs-lookup"><span data-stu-id="91e03-121">A `BestPriceFinder` service calls out to multiple airline services to find the best ticket price for a particular route.</span></span>  <span data-ttu-id="91e03-122">このシナリオを実装するには、メッセージ アクティビティを使用して、価格要求を受信、バックエンド サービスから価格を取得し、価格要求に最良価格で応答することが必要ですが。</span><span class="sxs-lookup"><span data-stu-id="91e03-122">Implementing this scenario would require you to use the message activities to receive the price request, retrieve the prices from the back-end services, and reply to the price request with the best price.</span></span>  <span data-ttu-id="91e03-123">最適な価格を計算するためのビジネス ロジックを作成する他の既定のアクティビティを使用する必要も出ています。</span><span class="sxs-lookup"><span data-stu-id="91e03-123">It would also require you to use other out-of-box activities to create the business logic for calculating the best price.</span></span>  
  
## <a name="workflowservicehost"></a><span data-ttu-id="91e03-124">WorkflowServiceHost</span><span class="sxs-lookup"><span data-stu-id="91e03-124">WorkflowServiceHost</span></span>  
 <span data-ttu-id="91e03-125"><xref:System.ServiceModel.WorkflowServiceHost> (ただし、ワークフローがホストされるためにメッセージングを使用する必要はありません)、複数のインスタンス、構成、および WCF メッセージングをサポートする既定のワークフロー ホストです。</span><span class="sxs-lookup"><span data-stu-id="91e03-125">The <xref:System.ServiceModel.WorkflowServiceHost> is the out-of-box workflow host that supports multiple instances, configuration, and WCF messaging (although the workflows aren’t required to use messaging in order to be hosted).</span></span>  <span data-ttu-id="91e03-126">また、一連のサービス動作を介して永続性、追跡、およびインスタンス コントロールを統合します。</span><span class="sxs-lookup"><span data-stu-id="91e03-126">It also integrates with persistence, tracking, and instance control through a set of service behaviors.</span></span>  <span data-ttu-id="91e03-127">WCF のと同様に<xref:System.ServiceModel.ServiceHost>、<xref:System.ServiceModel.WorkflowServiceHost>コンソール/WinForms と WPF アプリケーションまたは Windows サービスで自己ホストしたり、web ホスト (.xamlx ファイル) として IIS または WAS でします。</span><span class="sxs-lookup"><span data-stu-id="91e03-127">Just like WCF’s <xref:System.ServiceModel.ServiceHost>, the <xref:System.ServiceModel.WorkflowServiceHost> can be self-hosted in a console/WinForms/WPF application or Windows service, or web-hosted (as a .xamlx file) in IIS or WAS.</span></span>  
  
### <a name="getting-started-with-workflow-service-host"></a><span data-ttu-id="91e03-128">ワークフロー サービス ホストの概要</span><span class="sxs-lookup"><span data-stu-id="91e03-128">Getting Started with Workflow Service Host</span></span>  
  
-   <span data-ttu-id="91e03-129">Visual Studio 2010 で WCF ワークフロー サービス アプリケーション プロジェクトを作成します。 を使用するようこのプロジェクトに設定されます<xref:System.ServiceModel.WorkflowServiceHost>web ホスト環境でします。</span><span class="sxs-lookup"><span data-stu-id="91e03-129">In Visual Studio 2010, create a WCF Workflow Service Application project: this project will be set up to use <xref:System.ServiceModel.WorkflowServiceHost> in a web-host environment.</span></span>  
  
-   <span data-ttu-id="91e03-130">非メッセージング ワークフローをホストするには、メッセージに基づいてインスタンスを作成するカスタム <xref:System.ServiceModel.Activities.WorkflowHostingEndpoint> を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e03-130">In order to host a non-messaging workflow, add a custom <xref:System.ServiceModel.Activities.WorkflowHostingEndpoint> that will create the instance based on a message.</span></span>  
  
-   <span data-ttu-id="91e03-131">ワークフロー インスタンスは、<xref:System.ServiceModel.Activities.WorkflowControlEndpoint> を <xref:System.ServiceModel.WorkflowServiceHost> に追加し、<xref:System.ServiceModel.Activities.WorkflowControlClient> を使用することで制御 (中断や終了など) できます。</span><span class="sxs-lookup"><span data-stu-id="91e03-131">Workflow instances can be controlled (e.g. suspended or terminated) by adding a <xref:System.ServiceModel.Activities.WorkflowControlEndpoint> to the <xref:System.ServiceModel.WorkflowServiceHost> and then using a <xref:System.ServiceModel.Activities.WorkflowControlClient>.</span></span>  
  
-   <span data-ttu-id="91e03-132"><xref:System.ServiceModel.WorkflowServiceHost> のサンプルは次のセクションにあります。</span><span class="sxs-lookup"><span data-stu-id="91e03-132">Samples for the <xref:System.ServiceModel.WorkflowServiceHost> can be found in the following sections:</span></span>  
  
    -   [<span data-ttu-id="91e03-133">実行</span><span class="sxs-lookup"><span data-stu-id="91e03-133">Execution</span></span>](../../../docs/framework/windows-workflow-foundation/samples/execution.md)  
  
    -   <span data-ttu-id="91e03-134">Basic:[サービス](../../../docs/framework/windows-workflow-foundation/samples/services.md)</span><span class="sxs-lookup"><span data-stu-id="91e03-134">Basic: [Services](../../../docs/framework/windows-workflow-foundation/samples/services.md)</span></span>  
  
    -   <span data-ttu-id="91e03-135">シナリオ:[サービス](../../../docs/framework/windows-workflow-foundation/samples/services.md)</span><span class="sxs-lookup"><span data-stu-id="91e03-135">Scenarios: [Services](../../../docs/framework/windows-workflow-foundation/samples/services.md)</span></span>  
  
    -   <span data-ttu-id="91e03-136">アプリケーション:[中断インスタンスの管理](../../../docs/framework/windows-workflow-foundation/samples/suspended-instance-management.md)</span><span class="sxs-lookup"><span data-stu-id="91e03-136">Application: [Suspended Instance Management](../../../docs/framework/windows-workflow-foundation/samples/suspended-instance-management.md)</span></span>  
  
-   [<span data-ttu-id="91e03-137">WorkflowServiceHost の概念に関するドキュメント</span><span class="sxs-lookup"><span data-stu-id="91e03-137">WorkflowServiceHost Conceptual Documentation</span></span>](https://go.microsoft.com/fwlink/?LinkId=204807)  
  
### <a name="workflowservicehost-scenario"></a><span data-ttu-id="91e03-138">WorkflowServiceHost のシナリオ</span><span class="sxs-lookup"><span data-stu-id="91e03-138">WorkflowServiceHost Scenario</span></span>  
 <span data-ttu-id="91e03-139">BestPriceFinder サービスは、複数の航空会社サービスを特定のルートの最良チケット価格を検索します。</span><span class="sxs-lookup"><span data-stu-id="91e03-139">A BestPriceFinder service calls out to multiple airline services to find the best ticket price for a particular route.</span></span>  <span data-ttu-id="91e03-140">このシナリオを実装する必要にワークフローをホスト<xref:System.ServiceModel.WorkflowServiceHost>します。</span><span class="sxs-lookup"><span data-stu-id="91e03-140">Implementing this scenario would require you to host the workflow in <xref:System.ServiceModel.WorkflowServiceHost>.</span></span>  <span data-ttu-id="91e03-141">メッセージ アクティビティを使用しても、価格要求を受信、バックエンド サービスから価格を取得および価格要求に最良価格で応答するには。</span><span class="sxs-lookup"><span data-stu-id="91e03-141">It would also use the message activities to receive the price request, retrieve the prices from the back-end services, and reply to the price request with the best price.</span></span>  
  
## <a name="correlation"></a><span data-ttu-id="91e03-142">相関関係</span><span class="sxs-lookup"><span data-stu-id="91e03-142">Correlation</span></span>  
 <span data-ttu-id="91e03-143">相関関係は次の 2 つのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="91e03-143">A correlation is one of two things:</span></span>  
  
-   <span data-ttu-id="91e03-144">メッセージをグループ化する方法。つまり、要求メッセージとその応答の関係。</span><span class="sxs-lookup"><span data-stu-id="91e03-144">A way of grouping messages together; that is, the relationship between a request message and its reply.</span></span>  
  
-   <span data-ttu-id="91e03-145">サービス インスタンスにデータの一部をマッピングする方法。</span><span class="sxs-lookup"><span data-stu-id="91e03-145">A way of mapping a piece of data to a service instance</span></span>  
  
### <a name="getting-started"></a><span data-ttu-id="91e03-146">作業の開始</span><span class="sxs-lookup"><span data-stu-id="91e03-146">Getting Started</span></span>  
  
-   <span data-ttu-id="91e03-147">相関を開始するには、Visual Studio で新規プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="91e03-147">To get started with correlation, create a new project in Visual Studio.</span></span> <span data-ttu-id="91e03-148"><xref:System.ServiceModel.Activities.CorrelationHandle> 型の変数を作成します。</span><span class="sxs-lookup"><span data-stu-id="91e03-148">Create a variable of type <xref:System.ServiceModel.Activities.CorrelationHandle>.</span></span>  
  
-   <span data-ttu-id="91e03-149">メッセージのグループ化に使用する相関関係の例は、メッセージをグループ化する要求/応答の相関関係です。</span><span class="sxs-lookup"><span data-stu-id="91e03-149">An example of correlation used to group messages together is a Request-Reply correlation that groups messages together.</span></span>  
  
    -   <span data-ttu-id="91e03-150"><xref:System.ServiceModel.Activities.Receive>アクティビティをクリックして、<xref:System.ServiceModel.Activities.Receive.CorrelationInitializers%2A>プロパティを追加し、<xref:System.ServiceModel.Activities.RequestReplyCorrelationInitializer>上記の最初の手順で作成された、CorrelationHandle を使用して。</span><span class="sxs-lookup"><span data-stu-id="91e03-150">On a <xref:System.ServiceModel.Activities.Receive> activity, click on the <xref:System.ServiceModel.Activities.Receive.CorrelationInitializers%2A> property and add a <xref:System.ServiceModel.Activities.RequestReplyCorrelationInitializer> using the CorrelationHandle created in the first step above.</span></span>  
  
    -   <span data-ttu-id="91e03-151">作成、<xref:System.ServiceModel.Activities.SendReply>アクティビティを右クリックし、 <xref:System.ServiceModel.Activities.Receive> "SendReply の作成" をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91e03-151">Create a <xref:System.ServiceModel.Activities.SendReply> activity by right-clicking on the <xref:System.ServiceModel.Activities.Receive> and clicking "Create SendReply".</span></span> <span data-ttu-id="91e03-152">これをワークフローの <xref:System.ServiceModel.Activities.Receive> アクティビティの後に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="91e03-152">Paste it into your workflow after the <xref:System.ServiceModel.Activities.Receive> activity.</span></span>  
  
-   <span data-ttu-id="91e03-153">データの一部をサービス インスタンスにマッピングする例は、データの一部 (オーダー ID など) を特定のワークフロー インスタンスにマップするコンテンツ ベースの相関関係です。</span><span class="sxs-lookup"><span data-stu-id="91e03-153">An example of mapping a piece of data to a service instance is content-based correlation which maps a piece of data (for example, an order ID) to a particular workflow instance.</span></span>  
  
    -   <span data-ttu-id="91e03-154">任意のメッセージング アクティビティで、`CorrelationInitializers` プロパティをクリックし、上記で作成した <xref:System.ServiceModel.Activities.QueryCorrelationInitializer> 変数を使用して <xref:System.ServiceModel.Activities.CorrelationHandle> を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e03-154">On any messaging activity, click on the `CorrelationInitializers` property and add a <xref:System.ServiceModel.Activities.QueryCorrelationInitializer> using the <xref:System.ServiceModel.Activities.CorrelationHandle> variable created above.</span></span> <span data-ttu-id="91e03-155">ドロップダウン メニューで、メッセージ上の目的のプロパティ (OrderID など) をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="91e03-155">Double-click on the desired property on the message (e.g. OrderID) from the drop-down menu.</span></span> <span data-ttu-id="91e03-156">`CorrelatesWith` プロパティを上記で使用した <xref:System.ServiceModel.Activities.CorrelationHandle> 変数に設定します。</span><span class="sxs-lookup"><span data-stu-id="91e03-156">Set the `CorrelatesWith` property to the <xref:System.ServiceModel.Activities.CorrelationHandle> variable used above.</span></span>  
  
-   <span data-ttu-id="91e03-157">サンプル:</span><span class="sxs-lookup"><span data-stu-id="91e03-157">Samples:</span></span>  
  
    -   <span data-ttu-id="91e03-158">Basic:[サービス](../../../docs/framework/windows-workflow-foundation/samples/services.md)</span><span class="sxs-lookup"><span data-stu-id="91e03-158">Basic: [Services](../../../docs/framework/windows-workflow-foundation/samples/services.md)</span></span>  
  
    -   <span data-ttu-id="91e03-159">シナリオ:[サービス](../../../docs/framework/windows-workflow-foundation/samples/services.md)</span><span class="sxs-lookup"><span data-stu-id="91e03-159">Scenarios: [Services](../../../docs/framework/windows-workflow-foundation/samples/services.md)</span></span>  
  
    -   [<span data-ttu-id="91e03-160">相関関係の概念に関するドキュメント</span><span class="sxs-lookup"><span data-stu-id="91e03-160">Correlation Conceptual Documentation</span></span>](https://go.microsoft.com/fwlink/?LinkId=204939)  
  
### <a name="correlation-scenario"></a><span data-ttu-id="91e03-161">相関関係のシナリオ</span><span class="sxs-lookup"><span data-stu-id="91e03-161">Correlation Scenario</span></span>  
 <span data-ttu-id="91e03-162">注文処理ワークフローを使用して、新規注文の作成とプロセス内にある既存の注文の更新を処理します。</span><span class="sxs-lookup"><span data-stu-id="91e03-162">An order-processing workflow is used to handle new order creation and updating existing orders that are in process.</span></span>  <span data-ttu-id="91e03-163">このシナリオを実装する必要にワークフローをホスト<xref:System.ServiceModel.WorkflowServiceHost>とメッセージング アクティビティを使用します。</span><span class="sxs-lookup"><span data-stu-id="91e03-163">Implementing this scenario would require you to host the workflow in <xref:System.ServiceModel.WorkflowServiceHost> and use the messaging activities.</span></span>  <span data-ttu-id="91e03-164">基づく相関関係が必要になることも、`orderId`に適切なワークフローに更新が行われることを確認します。</span><span class="sxs-lookup"><span data-stu-id="91e03-164">It would also require correlation based on the `orderId` to ensure that updates are made to the correct workflow.</span></span>  
  
## <a name="simplified-configuration"></a><span data-ttu-id="91e03-165">簡略化された構成</span><span class="sxs-lookup"><span data-stu-id="91e03-165">Simplified Configuration</span></span>  
 <span data-ttu-id="91e03-166">WCF 構成スキーマは複雑であり、機能を検索するハードの多くのユーザーを提供します。</span><span class="sxs-lookup"><span data-stu-id="91e03-166">The WCF configuration schema is complex and provides users with many hard to find features.</span></span> <span data-ttu-id="91e03-167">[!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)]、WCF ユーザーが次の機能が、サービスを構成する際に役立つを中心に説明しました。</span><span class="sxs-lookup"><span data-stu-id="91e03-167">In [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)], we have focused on helping WCF users configure their services with the following features:</span></span>  
  
-   <span data-ttu-id="91e03-168">サービスごとの明示的な構成の必要性をなくします。</span><span class="sxs-lookup"><span data-stu-id="91e03-168">Removing the need for explicit per-service configuration.</span></span> <span data-ttu-id="91e03-169">いずれかを構成しなかった場合\<service > 要素に、サービスと、サービスに任意のエンドポイントをプログラムで定義されていませんし、サービス コントラクトおよびサービスのベース アドレスごとに 1 つに、一連のエンドポイントが自動的に追加します。サービスによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="91e03-169">If you do not configure any \<service> elements for your service, and your service does not define programmatically any endpoint, then a set of endpoints will be automatically added to your service, one per service base address and per contract implemented by your service.</span></span>  
  
-   <span data-ttu-id="91e03-170">明示的な構成のないサービスに適用される WCF バインディングおよび動作の既定値をユーザーが定義できるようにします。</span><span class="sxs-lookup"><span data-stu-id="91e03-170">Enables the user to define default values for WCF bindings and behaviors, which will be applied to services with no explicit configuration.</span></span>  
  
-   <span data-ttu-id="91e03-171">標準のエンドポイントは、事前に構成された再利用可能なエンドポイントを定義します。このエンドポイントは、1 つ以上のエンドポイント プロパティ (アドレス、バインド、およびコントラクト) に対して固定値を持ち、カスタム プロパティを定義できるようにします。</span><span class="sxs-lookup"><span data-stu-id="91e03-171">Standard endpoints define reusable preconfigured endpoints, which have fixed values for one or more of the endpoint properties (address, binding and contract), and allow defining custom properties.</span></span>  
  
-   <span data-ttu-id="91e03-172">最後に、 <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601> WCF クライアントの構成、構成が選択されているまたはアプリケーション ドメインの読み込み時間後に変更のシナリオで役に立ちますの集中管理することができます。</span><span class="sxs-lookup"><span data-stu-id="91e03-172">Finally, the <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601> allows you to do central management of WCF client configuration, useful in scenarios in which configuration is selected or changed after the application domain load time.</span></span>  
  
### <a name="getting-started"></a><span data-ttu-id="91e03-173">作業の開始</span><span class="sxs-lookup"><span data-stu-id="91e03-173">Getting Started</span></span>  
  
-   [<span data-ttu-id="91e03-174">Wcf 4.0 開発者ガイド</span><span class="sxs-lookup"><span data-stu-id="91e03-174">A Developer's Guide to WCF 4.0</span></span>](https://go.microsoft.com/fwlink/?LinkId=204940)  
  
-   [<span data-ttu-id="91e03-175">構成チャネル ファクトリ</span><span class="sxs-lookup"><span data-stu-id="91e03-175">Configuration Channel Factory</span></span>](https://go.microsoft.com/fwlink/?LinkId=204941)  
  
-   [<span data-ttu-id="91e03-176">標準エンドポイント要素</span><span class="sxs-lookup"><span data-stu-id="91e03-176">Standard Endpoint Element</span></span>](https://go.microsoft.com/fwlink/?LinkId=204942)  
  
-   [<span data-ttu-id="91e03-177">サービス構成の向上では、.Net Framework 4</span><span class="sxs-lookup"><span data-stu-id="91e03-177">Service configuration improvements in .Net Framework 4</span></span>](https://go.microsoft.com/fwlink/?LinkId=204943)  
  
-   [<span data-ttu-id="91e03-178">.NET 4 で一般的なユーザーの誤り: WF/WCF サービス構成名の入力ミス</span><span class="sxs-lookup"><span data-stu-id="91e03-178">Common User Mistake in .NET 4: Mistyping the WF/WCF Service Configuration Name</span></span>](https://go.microsoft.com/fwlink/?LinkId=204944)  
  
### <a name="simplified-configuration-scenarios"></a><span data-ttu-id="91e03-179">簡略化された構成のシナリオ</span><span class="sxs-lookup"><span data-stu-id="91e03-179">Simplified Configuration Scenarios</span></span>  
  
-   <span data-ttu-id="91e03-180">経験豊富な ASMX 開発者が WCF の使用を開始しようとするとします。</span><span class="sxs-lookup"><span data-stu-id="91e03-180">An experienced ASMX developer wants to start using WCF.</span></span> <span data-ttu-id="91e03-181">ただし、WCF は複雑すぎるようです。</span><span class="sxs-lookup"><span data-stu-id="91e03-181">However, WCF seems way too complicated!</span></span> <span data-ttu-id="91e03-182">構成ファイルに書き込む必要のある情報は何ですか。</span><span class="sxs-lookup"><span data-stu-id="91e03-182">What is all that information that I need to write in a configuration file?</span></span> <span data-ttu-id="91e03-183">.NET 4 では、構成ファイルをまったく使用しないこともできます。</span><span class="sxs-lookup"><span data-stu-id="91e03-183">In .NET 4, you can even decide to not have a configuration file at all.</span></span>  
  
-   <span data-ttu-id="91e03-184">既存の WCF サービスのセットは構成とメンテナンスが非常に困難です。</span><span class="sxs-lookup"><span data-stu-id="91e03-184">An existing set of WCF services are very difficult to configure and maintain.</span></span> <span data-ttu-id="91e03-185">構成ファイルには、変更するのが非常に危険な XML コードが何千行もあります。</span><span class="sxs-lookup"><span data-stu-id="91e03-185">The configuration file has thousands of lines of XML code that are extremely dangerous to touch.</span></span> <span data-ttu-id="91e03-186">コード量を管理しやすい量に減らすための支援が必要です。</span><span class="sxs-lookup"><span data-stu-id="91e03-186">Help is needed to reduce that amount of code to something more manageable.</span></span>  
  
## <a name="data-contract-resolver"></a><span data-ttu-id="91e03-187">データ コントラクト リゾルバー</span><span class="sxs-lookup"><span data-stu-id="91e03-187">Data Contract Resolver</span></span>  
 <span data-ttu-id="91e03-188">.NET 3.5 では、既知の型の設計にはいくつかの制限がありました。</span><span class="sxs-lookup"><span data-stu-id="91e03-188">In .NET 3.5, there were a few limitations in the design of known types:</span></span>  
  
-   <span data-ttu-id="91e03-189">シリアル化または逆シリアル化中に既知の型を動的に追加することはできませんでした。</span><span class="sxs-lookup"><span data-stu-id="91e03-189">Adding known types dynamically, during serialization or deserialization, was not possible.</span></span>  
  
-   <span data-ttu-id="91e03-190">シリアライザーは不明な xsi:type の情報を処理できませんでした。</span><span class="sxs-lookup"><span data-stu-id="91e03-190">Serializers could not deal with unknown xsi:type information.</span></span>  
  
-   <span data-ttu-id="91e03-191">ユーザーは、ネットワーク上のシリアル化インスタンスのサイズを小さくするなど、ネットワーク上に出現する xsi:type を指定できませんでした。</span><span class="sxs-lookup"><span data-stu-id="91e03-191">It was not possible for users to specify what xsi:type they would like to have appear on the wire to, for instance, make the size of a serialization instance on the wire smaller.</span></span>  
  
 <span data-ttu-id="91e03-192">[DataContractResolver](../../../docs/framework/wcf/samples/datacontractresolver.md) .NET 4.5 でこれらの問題を解決します。</span><span class="sxs-lookup"><span data-stu-id="91e03-192">The [DataContractResolver](../../../docs/framework/wcf/samples/datacontractresolver.md) solves these issues in .NET 4.5.</span></span>  
  
### <a name="getting-started"></a><span data-ttu-id="91e03-193">作業の開始</span><span class="sxs-lookup"><span data-stu-id="91e03-193">Getting Started</span></span>  
  
-   [<span data-ttu-id="91e03-194">データ コントラクト リゾルバー API のドキュメント</span><span class="sxs-lookup"><span data-stu-id="91e03-194">Data Contract Resolver API documentation</span></span>](https://go.microsoft.com/fwlink/?LinkId=204946)  
  
-   [<span data-ttu-id="91e03-195">データ コントラクト リゾルバーの概要</span><span class="sxs-lookup"><span data-stu-id="91e03-195">Introducing the Data Contract Resolver</span></span>](https://go.microsoft.com/fwlink/?LinkId=204947)  
  
-   <span data-ttu-id="91e03-196">サンプル:</span><span class="sxs-lookup"><span data-stu-id="91e03-196">Samples:</span></span>  
  
    -   [<span data-ttu-id="91e03-197">DataContractResolver</span><span class="sxs-lookup"><span data-stu-id="91e03-197">DataContractResolver</span></span>](../../../docs/framework/wcf/samples/datacontractresolver.md)  
  
    -   [<span data-ttu-id="91e03-198">KnownAssemblyAttribute</span><span class="sxs-lookup"><span data-stu-id="91e03-198">KnownAssemblyAttribute</span></span>](../../../docs/framework/wcf/samples/knownassemblyattribute.md)  
  
### <a name="data-contract-resolver-scenarios"></a><span data-ttu-id="91e03-199">データ コントラクト リゾルバーのシナリオ</span><span class="sxs-lookup"><span data-stu-id="91e03-199">Data Contract Resolver Scenarios</span></span>  
  
-   <span data-ttu-id="91e03-200">数十の <xref:System.Runtime.Serialization.KnownTypeAttribute> オブジェクトをサービスで宣言する必要性の回避。</span><span class="sxs-lookup"><span data-stu-id="91e03-200">Avoiding having to declare tens of <xref:System.Runtime.Serialization.KnownTypeAttribute> objects in a service.</span></span>  
  
-   <span data-ttu-id="91e03-201">XML BLOB のサイズの削減。</span><span class="sxs-lookup"><span data-stu-id="91e03-201">Reducing the size of the XML blob.</span></span>  
  
## <a name="flowchart"></a><span data-ttu-id="91e03-202">フローチャート</span><span class="sxs-lookup"><span data-stu-id="91e03-202">Flowchart</span></span>  
 <span data-ttu-id="91e03-203">フローチャートは、ドメインの問題を視覚的に表すための既知のパラダイムです。</span><span class="sxs-lookup"><span data-stu-id="91e03-203">Flowchart is a well-known paradigm to visually represent domain problems.</span></span> <span data-ttu-id="91e03-204">これは .NET の 4 で導入される新しい制御フロー スタイルです。</span><span class="sxs-lookup"><span data-stu-id="91e03-204">It is a new control flow style we’re introducing in .NET 4.</span></span> <span data-ttu-id="91e03-205">フローチャートの主な特性は、一度に 1 つのアクティビティのみ実行されることです。</span><span class="sxs-lookup"><span data-stu-id="91e03-205">A core characteristic of Flowchart is that only one activity is executed at any given time.</span></span> <span data-ttu-id="91e03-206">フローチャートはループと代替結果を表すことができますが、その性質上、複数ノードの同時実行を表すことはできません。</span><span class="sxs-lookup"><span data-stu-id="91e03-206">Flowcharts can express loops and alternative outcomes, but cannot natively express concurrent execution of multiple nodes.</span></span>  
  
### <a name="getting-started"></a><span data-ttu-id="91e03-207">作業の開始</span><span class="sxs-lookup"><span data-stu-id="91e03-207">Getting Started</span></span>  
  
-   <span data-ttu-id="91e03-208">[!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)] で、ワークフロー コンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="91e03-208">In [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)], create a workflow console application.</span></span> <span data-ttu-id="91e03-209">ワークフロー デザイナーにフローチャートを追加します。</span><span class="sxs-lookup"><span data-stu-id="91e03-209">Add a Flowchart in the workflow designer.</span></span>  
  
-   <span data-ttu-id="91e03-210">フローチャート機能では、次のクラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="91e03-210">The flowchart feature uses the following classes:</span></span>  
  
    -   <xref:System.Activities.Statements.Flowchart>  
  
    -   <xref:System.Activities.Statements.FlowNode>  
  
    -   <xref:System.Activities.Statements.FlowDecision>  
  
    -   <xref:System.Activities.Statements.FlowStep>  
  
    -   <xref:System.Activities.Statements.FlowSwitch%601>  
  
-   <span data-ttu-id="91e03-211">サンプル:</span><span class="sxs-lookup"><span data-stu-id="91e03-211">Samples:</span></span>  
  
    -   [<span data-ttu-id="91e03-212">TryCatch を使用した Flowchart アクティビティでのエラー処理</span><span class="sxs-lookup"><span data-stu-id="91e03-212">Fault Handling in a Flowchart Activity Using TryCatch</span></span>](../../../docs/framework/windows-workflow-foundation/samples/fault-handling-in-a-flowchart-activity-using-trycatch.md)  
  
    -   [<span data-ttu-id="91e03-213">FlowChart と Pick の組み合わせを使用する StateMachine シナリオ</span><span class="sxs-lookup"><span data-stu-id="91e03-213">StateMachine Scenario Using a Combination of FlowChart and Pick</span></span>](../../../docs/framework/windows-workflow-foundation/samples/statemachine-scenario-using-a-combination-of-flowchart-and-pick.md)  
  
    -   [<span data-ttu-id="91e03-214">雇用プロセス</span><span class="sxs-lookup"><span data-stu-id="91e03-214">Hiring Process</span></span>](../../../docs/framework/windows-workflow-foundation/samples/hiring-process.md)  
  
-   <span data-ttu-id="91e03-215">デザイナー ドキュメント:</span><span class="sxs-lookup"><span data-stu-id="91e03-215">Designer Documentation:</span></span>  
  
    -   [<span data-ttu-id="91e03-216">フローチャート アクティビティ デザイナー</span><span class="sxs-lookup"><span data-stu-id="91e03-216">Flowchart Activity Designers</span></span>](/visualstudio/workflow-designer/flowchart-activity-designers)  
  
### <a name="flowchart-scenarios"></a><span data-ttu-id="91e03-217">フローチャートのシナリオ</span><span class="sxs-lookup"><span data-stu-id="91e03-217">Flowchart Scenarios</span></span>  
 <span data-ttu-id="91e03-218">フローチャート アクティビティを使用して推測ゲームを実装できます。</span><span class="sxs-lookup"><span data-stu-id="91e03-218">A flowchart activity can be used to implement a guessing game.</span></span> <span data-ttu-id="91e03-219">推測ゲームは非常に単純です。コンピューターによってランダムな数値が選択され、プレーヤーはその数値を推測する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91e03-219">The guessing game is very simple: the computer selects a random number and the player has to guess that number.</span></span> <span data-ttu-id="91e03-220">プレーヤーが推測を送信するとき、コンピューターが表示されます (つまり"試行数が小さい) ヒント。</span><span class="sxs-lookup"><span data-stu-id="91e03-220">When the player submits each guess, the computer shows him a hint (i.e. "try a lower number").</span></span> <span data-ttu-id="91e03-221">プレーヤーが 6 回以下で数値を見つけた場合は、特別な祝福のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="91e03-221">If the player finds the number in less than 7 attempts, he receives a special congratulation from the computer.</span></span> <span data-ttu-id="91e03-222">このゲームは、次の手続き型アクティビティの組み合わせで実装できます。</span><span class="sxs-lookup"><span data-stu-id="91e03-222">This game can be implemented with a combination of the following procedural activities:</span></span>  
  
-   <xref:System.Activities.Statements.Sequence>  
  
-   <xref:System.Activities.Statements.While>  
  
-   <xref:System.Activities.Statements.Switch%601>  
  
-   <xref:System.Activities.Statements.TryCatch>  
  
-   <xref:System.Activities.Statements.Assign%601>  
  
-   <xref:System.Activities.Statements.If>  
  
## <a name="procedural-activities-sequence-if-foreach-switch-assign-dowhile-while"></a><span data-ttu-id="91e03-223">手続き型アクティビティ (Sequence、If、ForEach、Switch、Assign、DoWhile、While)</span><span class="sxs-lookup"><span data-stu-id="91e03-223">Procedural activities (Sequence, If, ForEach, Switch, Assign, DoWhile, While)</span></span>  
 <span data-ttu-id="91e03-224">手続き型アクティビティは、プログラマになじみのある概念を使用してシーケンシャル制御フローをモデル化するメカニズムを提供します。</span><span class="sxs-lookup"><span data-stu-id="91e03-224">Procedural activities provide a mechanism to model sequential control flow using concepts that are familiar to programmers.</span></span> <span data-ttu-id="91e03-225">これらのアクティビティにより、従来の構造型プログラミング言語構成要素が有効になり、該当する場合には C#/VB などの一般的な手続き型言語と同等の言語が提供されます。</span><span class="sxs-lookup"><span data-stu-id="91e03-225">These activities enable traditionally structured programming language constructs and, when appropriate, provide language parity with common procedural languages such as C#/VB.</span></span>  
  
### <a name="getting-started"></a><span data-ttu-id="91e03-226">作業の開始</span><span class="sxs-lookup"><span data-stu-id="91e03-226">Getting Started</span></span>  
  
-   <span data-ttu-id="91e03-227">[!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)] で、ワークフロー コンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="91e03-227">In [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)], create a workflow console application.</span></span> <span data-ttu-id="91e03-228">ワークフロー デザイナーで、手続き型アクティビティを追加します。</span><span class="sxs-lookup"><span data-stu-id="91e03-228">Add procedural activities in the workflow designer.</span></span>  
  
-   <span data-ttu-id="91e03-229">サンプル:</span><span class="sxs-lookup"><span data-stu-id="91e03-229">Samples:</span></span>  
  
    -   [<span data-ttu-id="91e03-230">雇用プロセス</span><span class="sxs-lookup"><span data-stu-id="91e03-230">Hiring Process</span></span>](../../../docs/framework/windows-workflow-foundation/samples/hiring-process.md)  
  
    -   [<span data-ttu-id="91e03-231">企業の購買プロセス</span><span class="sxs-lookup"><span data-stu-id="91e03-231">Corporate Purchase Process</span></span>](../../../docs/framework/windows-workflow-foundation/samples/corporate-purchase-process.md)  
  
-   <span data-ttu-id="91e03-232">デザイナー ドキュメント:</span><span class="sxs-lookup"><span data-stu-id="91e03-232">Designer Documentation:</span></span>  
  
    -   [<span data-ttu-id="91e03-233">Parallel アクティビティ デザイナー</span><span class="sxs-lookup"><span data-stu-id="91e03-233">Parallel Activity Designer</span></span>](/visualstudio/workflow-designer/parallel-activity-designer)  
  
    -   [<span data-ttu-id="91e03-234">ParallelForEach\<T > アクティビティ デザイナー</span><span class="sxs-lookup"><span data-stu-id="91e03-234">ParallelForEach\<T> Activity Designer</span></span>](/visualstudio/workflow-designer/parallelforeach-t-activity-designer)  
  
### <a name="procedural-activity-scenarios"></a><span data-ttu-id="91e03-235">手続き型アクティビティのシナリオ</span><span class="sxs-lookup"><span data-stu-id="91e03-235">Procedural Activity Scenarios</span></span>  
  
-   <span data-ttu-id="91e03-236"><xref:System.Activities.Statements.Parallel>イントラネット ドキュメント管理システムでは、ドキュメント承認ワークフローが。</span><span class="sxs-lookup"><span data-stu-id="91e03-236"><xref:System.Activities.Statements.Parallel>: An intranet document management system has a document approval workflow.</span></span> <span data-ttu-id="91e03-237">ドキュメントは、イントラネットに公開する前に、複数の部門の担当者によって承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91e03-237">Documents need to be approved by people in several departments before they can be published to the intranet.</span></span> <span data-ttu-id="91e03-238">承認; の確立された注文がないです。「承認保留」フェーズで、ドキュメントには、いつでもが発生することができます。</span><span class="sxs-lookup"><span data-stu-id="91e03-238">There isn’t an established order for the approvals; they can occur at any time while the document is in the "approval pending" phase.</span></span> <span data-ttu-id="91e03-239">ユーザーがレビューのためにドキュメントを送信した場合は、直属のマネージャー、イントラネット管理者、および内部コミュニケーション マネージャーがそのドキュメントを承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91e03-239">When a user submits a document for review it must be approved by her direct manager, the intranet administrator, and the internal communications manager.</span></span>  
  
-   <span data-ttu-id="91e03-240"><xref:System.Activities.Statements.ParallelForEach%601>: WF アプリケーションは、大規模企業内での企業購買を管理します。</span><span class="sxs-lookup"><span data-stu-id="91e03-240"><xref:System.Activities.Statements.ParallelForEach%601>: A WF application manages corporate buys within a large company.</span></span> <span data-ttu-id="91e03-241">企業の規則では、購買作業を計画する前に 3 社の異なるベンダーを評価する必要があると規定されています。</span><span class="sxs-lookup"><span data-stu-id="91e03-241">The corporate rules dictate that before planning any purchase operation, the valuations of three different vendors is required.</span></span> <span data-ttu-id="91e03-242">購買部門の従業員は、企業のベンダー リストから 3 社のベンダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="91e03-242">An employee from the buying department selects three vendors from the company’s vendor list.</span></span> <span data-ttu-id="91e03-243">これらのベンダーを選択し、通知した後で、企業は経済提案書を待ちます。</span><span class="sxs-lookup"><span data-stu-id="91e03-243">After these vendors have been selected and notified, the company will wait for their economic proposals.</span></span> <span data-ttu-id="91e03-244">提案書は任意の順序で到着します。</span><span class="sxs-lookup"><span data-stu-id="91e03-244">The proposals can come in any order.</span></span> <span data-ttu-id="91e03-245">WF でこのシナリオを実装するには、ベンダーのコレクションを反復処理して経済提案書を求める <xref:System.Activities.Statements.ParallelForEach%601> を使用します。</span><span class="sxs-lookup"><span data-stu-id="91e03-245">To implement this scenario in WF, we use a <xref:System.Activities.Statements.ParallelForEach%601> that will iterate through our collection of vendors and ask for their economic proposals.</span></span> <span data-ttu-id="91e03-246">すべての提案が収集された後で、最良の提案が選択されて表示されます。</span><span class="sxs-lookup"><span data-stu-id="91e03-246">After all offers are gathered, the best one is selected and displayed.</span></span>  
  
## <a name="invokemethod"></a><span data-ttu-id="91e03-247">InvokeMethod</span><span class="sxs-lookup"><span data-stu-id="91e03-247">InvokeMethod</span></span>  
 <span data-ttu-id="91e03-248"><xref:System.Activities.Statements.InvokeMethod> アクティビティでは、オブジェクト内のパブリック メソッドまたはスコープ内の型を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="91e03-248">The <xref:System.Activities.Statements.InvokeMethod> activity allows invoking public methods in objects or types in scope.</span></span> <span data-ttu-id="91e03-249">パラメーター付きまたはパラメーターなし (パラメーター配列を含む) でのインスタンス メソッドおよび静的メソッドの呼び出し、および汎用メソッドの呼び出しがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="91e03-249">It supports invoking instance and static methods with or without parameters (including parameter arrays), and generic methods.</span></span> <span data-ttu-id="91e03-250">メソッドを同期および非同期で実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="91e03-250">It also allows executing method synchronously and asynchronously.</span></span>  
  
### <a name="getting-started"></a><span data-ttu-id="91e03-251">作業の開始</span><span class="sxs-lookup"><span data-stu-id="91e03-251">Getting Started</span></span>  
  
-   <span data-ttu-id="91e03-252">[!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)] で、ワークフロー コンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="91e03-252">In [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)], create a workflow console application.</span></span> <span data-ttu-id="91e03-253">ワークフロー デザイナーに <xref:System.Activities.Statements.InvokeMethod> アクティビティを追加し、そこに静的メソッドとインスタンス メソッドを構成します。</span><span class="sxs-lookup"><span data-stu-id="91e03-253">Add an <xref:System.Activities.Statements.InvokeMethod> activity in the workflow designer, and configure static and instance methods on it.</span></span>  
  
-   <span data-ttu-id="91e03-254">サンプル:</span><span class="sxs-lookup"><span data-stu-id="91e03-254">Samples:</span></span>  
  
    -   [<span data-ttu-id="91e03-255">InvokeMethod</span><span class="sxs-lookup"><span data-stu-id="91e03-255">InvokeMethod</span></span>](../../../docs/framework/windows-workflow-foundation/samples/invokemethod.md)  
  
-   <span data-ttu-id="91e03-256">デザイナー ドキュメント: [InvokeMethod アクティビティ デザイナー](/visualstudio/workflow-designer/invokemethod-activity-designer)</span><span class="sxs-lookup"><span data-stu-id="91e03-256">Designer Documentation: [InvokeMethod Activity Designer](/visualstudio/workflow-designer/invokemethod-activity-designer)</span></span>  
  
### <a name="invokemethod-scenarios"></a><span data-ttu-id="91e03-257">InvokeMethod のシナリオ</span><span class="sxs-lookup"><span data-stu-id="91e03-257">InvokeMethod Scenarios</span></span>  
  
-   <span data-ttu-id="91e03-258">スコープ内のオブジェクトのメソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="91e03-258">A method in an object in scope needs to be invoked.</span></span> <span data-ttu-id="91e03-259">たとえば、辞書に値を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91e03-259">For example, a value needs to be added to a dictionary.</span></span> <span data-ttu-id="91e03-260">辞書のインスタンスの Add メソッドが呼び出され、キーと値が指定されます。</span><span class="sxs-lookup"><span data-stu-id="91e03-260">The Add method of the instance of the dictionary is invoked, and the key and value are provided.</span></span>  
  
-   <span data-ttu-id="91e03-261">レガシー CLR オブジェクトに対してメソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="91e03-261">A method needs to be invoked on a legacy CLR object.</span></span> <span data-ttu-id="91e03-262">カスタム アクティビティを作成してそのレガシー クラスの呼び出しをラップする代わりに、ワークフロー実行中にそのクラスがスコープ内にある場合には <xref:System.Activities.Statements.InvokeMethod> を使用できます。</span><span class="sxs-lookup"><span data-stu-id="91e03-262">Instead of creating a custom activity to wrap the call to that legacy class, if it is in scope during the workflow execution, <xref:System.Activities.Statements.InvokeMethod> can be used.</span></span>  
  
## <a name="error-handling-activities"></a><span data-ttu-id="91e03-263">エラー処理アクティビティ</span><span class="sxs-lookup"><span data-stu-id="91e03-263">Error handling activities</span></span>  
 <span data-ttu-id="91e03-264"><xref:System.Activities.Statements.TryCatch> アクティビティには、含まれるアクティビティのセットの実行中に発生する例外をキャッチするメカニズムが用意されています (C#/VB の Try/Catch コンストラクトに類似)。</span><span class="sxs-lookup"><span data-stu-id="91e03-264">The <xref:System.Activities.Statements.TryCatch> activity provides a mechanism for catching exceptions that occur during the execution of a set of contained activities (similar to the Try/Catch construct in C#/VB).</span></span> <span data-ttu-id="91e03-265"><xref:System.Activities.Statements.TryCatch> はワークフロー レベルの例外処理を提供します。</span><span class="sxs-lookup"><span data-stu-id="91e03-265"><xref:System.Activities.Statements.TryCatch> provides exception handling at the workflow level.</span></span> <span data-ttu-id="91e03-266">ハンドルされていない例外がスローされると、ワークフローが中止され、Finally ブロックは実行されません。</span><span class="sxs-lookup"><span data-stu-id="91e03-266">When an unhandled exception is thrown, the workflow is aborted and the Finally block won’t be executed.</span></span> <span data-ttu-id="91e03-267">この動作は C# と一貫性があります。</span><span class="sxs-lookup"><span data-stu-id="91e03-267">This behavior is consistent with C#.</span></span>  
  
### <a name="getting-started"></a><span data-ttu-id="91e03-268">作業の開始</span><span class="sxs-lookup"><span data-stu-id="91e03-268">Getting Started</span></span>  
  
-   <span data-ttu-id="91e03-269">[!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)] で、ワークフロー コンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="91e03-269">In [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)], create a workflow console application.</span></span> <span data-ttu-id="91e03-270">ワークフロー デザイナーで <xref:System.Activities.Statements.TryCatch> アクティビティを追加します。</span><span class="sxs-lookup"><span data-stu-id="91e03-270">Add a <xref:System.Activities.Statements.TryCatch> activity in the workflow designer.</span></span>  
  
-   <span data-ttu-id="91e03-271">サンプル:</span><span class="sxs-lookup"><span data-stu-id="91e03-271">Samples:</span></span>  
  
    1.  [<span data-ttu-id="91e03-272">TryCatch を使用した Flowchart アクティビティでのエラー処理</span><span class="sxs-lookup"><span data-stu-id="91e03-272">Fault Handling in a Flowchart Activity Using TryCatch</span></span>](../../../docs/framework/windows-workflow-foundation/samples/fault-handling-in-a-flowchart-activity-using-trycatch.md)  
  
    2.  [<span data-ttu-id="91e03-273">手続き型アクティビティの使用</span><span class="sxs-lookup"><span data-stu-id="91e03-273">Using Procedural Activities</span></span>](../../../docs/framework/windows-workflow-foundation/samples/using-procedural-activities.md)  
  
-   <span data-ttu-id="91e03-274">デザイナー ドキュメント:[エラー処理アクティビティ デザイナー](/visualstudio/workflow-designer/error-handling-activity-designers)</span><span class="sxs-lookup"><span data-stu-id="91e03-274">Designer Documentation: [Error Handling Activity Designers](/visualstudio/workflow-designer/error-handling-activity-designers)</span></span>  
  
### <a name="error-handling-scenarios"></a><span data-ttu-id="91e03-275">エラー処理のシナリオ</span><span class="sxs-lookup"><span data-stu-id="91e03-275">Error handling scenarios</span></span>  
 <span data-ttu-id="91e03-276">アクティビティのセットを実行する必要があり、エラーの発生時に特定のロジックを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91e03-276">A set of activities needs to be executed, and specific logic needs to be executed when an error occurs.</span></span> <span data-ttu-id="91e03-277">そのエラー処理ロジック中にエラーが回復不能であることがわかった場合は、例外が再スローされ、親アクティビティ (またはホスト) によって問題が処理されます。</span><span class="sxs-lookup"><span data-stu-id="91e03-277">If during that error handling logic it is found that the error is not recoverable, the exception will be rethrown, and the parent activity (or the host) will deal with the problem.</span></span>  
  
## <a name="pick-activity"></a><span data-ttu-id="91e03-278">Pick アクティビティ</span><span class="sxs-lookup"><span data-stu-id="91e03-278">Pick activity</span></span>  
 <span data-ttu-id="91e03-279"><xref:System.Activities.Statements.Pick> アクティビティは、WF でイベント ベースの制御フロー モデリングを提供します。</span><span class="sxs-lookup"><span data-stu-id="91e03-279">The <xref:System.Activities.Statements.Pick> Activity provides event-based control flow modeling in WF.</span></span> <span data-ttu-id="91e03-280"><xref:System.Activities.Statements.Pick> には、多数の分岐が含まれています。各分岐は、特定のイベントが発生すると実行されます。</span><span class="sxs-lookup"><span data-stu-id="91e03-280"><xref:System.Activities.Statements.Pick> contains many branches where each branch waits for a particular event to occur before running.</span></span> <span data-ttu-id="91e03-281">この設定では、<xref:System.Activities.Statements.Pick> は、アクティビティがリッスンしているイベント セットの 1 つのみを実行する <xref:System.Activities.Statements.Switch%601> と同様に動作します。</span><span class="sxs-lookup"><span data-stu-id="91e03-281">In this setup, a <xref:System.Activities.Statements.Pick> behaves similar to a <xref:System.Activities.Statements.Switch%601> to which the Activity will execute only one of the set of events it is listening.</span></span> <span data-ttu-id="91e03-282">各分岐はイベント ドリブンなので、発生したイベントが対応する分岐を実行します。</span><span class="sxs-lookup"><span data-stu-id="91e03-282">Each branch is event driven and the event that occurs runs the corresponding branch first.</span></span> <span data-ttu-id="91e03-283">他のすべての分岐は、イベントのリッスンをキャンセルし、停止します。</span><span class="sxs-lookup"><span data-stu-id="91e03-283">All other branches cancel and stop listening for events.</span></span>  
  
### <a name="getting-started"></a><span data-ttu-id="91e03-284">作業の開始</span><span class="sxs-lookup"><span data-stu-id="91e03-284">Getting Started</span></span>  
  
-   <span data-ttu-id="91e03-285">[!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)] で、ワークフロー コンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="91e03-285">In [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)], create a workflow console application.</span></span> <span data-ttu-id="91e03-286">ワークフロー デザイナーで <xref:System.Activities.Statements.Pick> アクティビティを追加します。</span><span class="sxs-lookup"><span data-stu-id="91e03-286">Add a <xref:System.Activities.Statements.Pick> activity in the workflow designer.</span></span>  
  
-   <span data-ttu-id="91e03-287">サンプル: [Pick アクティビティの使用](../../../docs/framework/windows-workflow-foundation/samples/using-the-pick-activity.md)</span><span class="sxs-lookup"><span data-stu-id="91e03-287">Sample: [Using the Pick Activity](../../../docs/framework/windows-workflow-foundation/samples/using-the-pick-activity.md)</span></span>  
  
-   <span data-ttu-id="91e03-288">デザイナー ドキュメント: [Pick アクティビティ デザイナー](/visualstudio/workflow-designer/pick-activity-designer)</span><span class="sxs-lookup"><span data-stu-id="91e03-288">Designer documentation: [Pick Activity Designer](/visualstudio/workflow-designer/pick-activity-designer)</span></span>  
  
### <a name="pick-scenario"></a><span data-ttu-id="91e03-289">Pick のシナリオ</span><span class="sxs-lookup"><span data-stu-id="91e03-289">Pick Scenario</span></span>  
 <span data-ttu-id="91e03-290">ユーザーに入力を求めるプロンプトを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91e03-290">A user needs to be prompted for input.</span></span> <span data-ttu-id="91e03-291">通常の状況下では、開発者は <xref:System.Console.ReadLine%2A> のようなメソッド呼び出しを使用してユーザーの入力を求めます。</span><span class="sxs-lookup"><span data-stu-id="91e03-291">Under normal circumstances, the developer would use a method call like <xref:System.Console.ReadLine%2A> to prompt for a user’s input.</span></span> <span data-ttu-id="91e03-292">この設定の問題は、ユーザーが何か入力するまでプログラムが待機することです。</span><span class="sxs-lookup"><span data-stu-id="91e03-292">The problem with this setup is that the program waits until the user enters something.</span></span> <span data-ttu-id="91e03-293">このシナリオでは、ブロッキング アクティビティのブロックを解除するためにタイムアウトが必要です。</span><span class="sxs-lookup"><span data-stu-id="91e03-293">In this scenario, a time-out is needed to unblock a blocking activity.</span></span> <span data-ttu-id="91e03-294">一般的なシナリオでは、特定の期間内にタスクが完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91e03-294">A common scenario is one that requires a task to be completed within a given time duration.</span></span> <span data-ttu-id="91e03-295">ブロッキング アクティビティのタイムアウトは、Pick が大量の値を追加するシナリオです。</span><span class="sxs-lookup"><span data-stu-id="91e03-295">Timing out a blocking activity is a scenario where Pick adds a lot of value.</span></span>  
  
## <a name="wcf-routing-service"></a><span data-ttu-id="91e03-296">WCF ルーティング サービス</span><span class="sxs-lookup"><span data-stu-id="91e03-296">WCF Routing Service</span></span>  
 <span data-ttu-id="91e03-297">一般的なソフトウェア ルーターをクライアントとサービス間の WCFmessages のフローを制御できるようにするには、ルーティング サービスは設計されています。</span><span class="sxs-lookup"><span data-stu-id="91e03-297">The Routing Service is designed to be a generic software Router that allows you to control how WCFmessages flow in between your clients and services.</span></span>  <span data-ttu-id="91e03-298">ルーティング サービスできます、サービスからクライアントを分離するために、構成の観点からさらに多くの自由を提供するサービスをホストする方法を検討する場合がある場合、柔軟性をサポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="91e03-298">The Routing Service allows you to decouple your clients from your services, which gives you much more freedom in terms of the configurations that you can support and the flexibility you have when considering how to host your services.</span></span>  <span data-ttu-id="91e03-299">.NET 3.5 では、クライアントとサービスが密接に結び付いています。クライアントは、すべてのサービスとの対話に必要し、していた場所について知っておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="91e03-299">In .NET 3.5, clients and services were tightly coupled; a client had to know about all of the services it needed to talk to and where they were located.</span></span> <span data-ttu-id="91e03-300">また、.Net Framework 3.5 の WCF には次の制限がありました。</span><span class="sxs-lookup"><span data-stu-id="91e03-300">In addition, WCF in .Net Framework 3.5 had the following limitations:</span></span>  
  
-   <span data-ttu-id="91e03-301">ロジックをクライアントにハードコーディングする必要があったため、エラー処理が複雑でした。</span><span class="sxs-lookup"><span data-stu-id="91e03-301">Error handling was complex, as this logic had to be hard-coded into the client.</span></span>  
  
-   <span data-ttu-id="91e03-302">クライアントとサービスは常に同じバインディングを使用する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="91e03-302">Clients and services had to always use the same bindings.</span></span>  
  
-   <span data-ttu-id="91e03-303">サービスが適切に分類されていることはほとんどありませんでした。複数のサービス間で選択するよりも、クライアントがすべてを実装する 1 つのサービスと対話する方が簡単です。</span><span class="sxs-lookup"><span data-stu-id="91e03-303">Services were rarely well factored: it is easier to have the client talk to one service which implements everything, rather than needing to choose between multiple services.</span></span>  
  
 <span data-ttu-id="91e03-304">.Net 4 のルーティング サービスは、これらの問題を簡単に解決できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="91e03-304">The routing service in .Net 4 is designed to make these problems easier to solve.</span></span> <span data-ttu-id="91e03-305">新しいルーティング サービスには次の機能があります。</span><span class="sxs-lookup"><span data-stu-id="91e03-305">The new routing service has the following features:</span></span>  
  
1.  <span data-ttu-id="91e03-306">コンテント ベースのルーティング (<xref:System.ServiceModel.Dispatcher.MessageFilter> オブジェクトがメッセージを調べて送信先を判断します。)</span><span class="sxs-lookup"><span data-stu-id="91e03-306">Content based routing (<xref:System.ServiceModel.Dispatcher.MessageFilter> objects examine a message to determine where it should be sent.)</span></span>  
  
2.  <span data-ttu-id="91e03-307">プロトコル ブリッジ (トランスポートとメッセージ)</span><span class="sxs-lookup"><span data-stu-id="91e03-307">Protocol bridging (transport & message)</span></span>  
  
3.  <span data-ttu-id="91e03-308">エラー処理 (ルーターは、通信例外をキャッチし、バックアップ エンドポイントにフェールオーバーします)</span><span class="sxs-lookup"><span data-stu-id="91e03-308">Error handling (the router catches communication exceptions and fails over to backup endpoints)</span></span>  
  
4.  <span data-ttu-id="91e03-309"><xref:System.ServiceModel.Dispatcher.MessageFilterTable%601> およびルーティング構成の動的 (メモリ内) 更新。</span><span class="sxs-lookup"><span data-stu-id="91e03-309">Dynamic (in memory) update of <xref:System.ServiceModel.Dispatcher.MessageFilterTable%601> and Routing Configuration.</span></span>  
  
### <a name="getting-started"></a><span data-ttu-id="91e03-310">作業の開始</span><span class="sxs-lookup"><span data-stu-id="91e03-310">Getting Started</span></span>  
  
1.  <span data-ttu-id="91e03-311">ドキュメント:[ルーティング](../../../docs/framework/wcf/feature-details/routing.md)</span><span class="sxs-lookup"><span data-stu-id="91e03-311">Documentation: [Routing](../../../docs/framework/wcf/feature-details/routing.md)</span></span>  
  
2.  <span data-ttu-id="91e03-312">サンプル:[ルーティング サービス&#91;WCF サンプル&#93;](../../../docs/framework/wcf/samples/routing-services.md)</span><span class="sxs-lookup"><span data-stu-id="91e03-312">Samples: [Routing Services &#91;WCF Samples&#93;](../../../docs/framework/wcf/samples/routing-services.md)</span></span>  
  
3.  <span data-ttu-id="91e03-313">ブログ:[ルーティング規則。](https://go.microsoft.com/fwlink/?LinkId=204956)</span><span class="sxs-lookup"><span data-stu-id="91e03-313">Blog: [Routing Rules!](https://go.microsoft.com/fwlink/?LinkId=204956)</span></span>  
  
### <a name="routing-scenarios"></a><span data-ttu-id="91e03-314">ルーティング シナリオ</span><span class="sxs-lookup"><span data-stu-id="91e03-314">Routing Scenarios</span></span>  
 <span data-ttu-id="91e03-315">ルーティング サービスは、次のシナリオに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="91e03-315">The routing service is useful in the following scenarios:</span></span>  
  
-   <span data-ttu-id="91e03-316">クライアントは、複数のサービスを直接アドレス指定することなく、これらのサービスと対話できます。</span><span class="sxs-lookup"><span data-stu-id="91e03-316">Clients can talk to multiple services without having to address them all directly.</span></span>  
  
-   <span data-ttu-id="91e03-317">クライアントは、ルーティング先を判断するためにクライアント要求で追加のロジックを実行できます。</span><span class="sxs-lookup"><span data-stu-id="91e03-317">Clients can perform additional logic on a client request to determine where to route it</span></span>  
  
-   <span data-ttu-id="91e03-318">クライアントをリファクタリングすることなく、クライアントが実行する操作を複数のサービス実装に分解します。</span><span class="sxs-lookup"><span data-stu-id="91e03-318">Decompose the operations a client performs into multiple service implementations without refactoring the client.</span></span>  
  
-   <span data-ttu-id="91e03-319">クライアントとサービスは、異なるセキュリティ設定の異なるバインディングで会話できます。</span><span class="sxs-lookup"><span data-stu-id="91e03-319">Clients and services can speak different bindings with different security settings.</span></span>  
  
-   <span data-ttu-id="91e03-320">クライアントは、障害またはサービスの使用不能に対してより堅牢になることができます。</span><span class="sxs-lookup"><span data-stu-id="91e03-320">Clients can be enabled to be more robust against failure or the unavailability of services.</span></span>  
  
## <a name="wcf-discovery"></a><span data-ttu-id="91e03-321">WCF Discovery</span><span class="sxs-lookup"><span data-stu-id="91e03-321">WCF Discovery</span></span>  
 <span data-ttu-id="91e03-322">WCF Discovery に、アプリケーションのインフラストラクチャに探索メカニズムを組み込むことができるフレームワーク テクノロジです。</span><span class="sxs-lookup"><span data-stu-id="91e03-322">WCF Discovery is a framework technology that allows you to incorporate a discovery mechanism to your application infrastructure.</span></span> <span data-ttu-id="91e03-323">これを使用して、サービスを探索可能にし、サービスを検索するようにクライアントを構成できます。</span><span class="sxs-lookup"><span data-stu-id="91e03-323">You can use this to make your service discoverable, and configure your clients to search for services.</span></span> <span data-ttu-id="91e03-324">クライアントはエンドポイントでハードコーディングする必要がなくなるため、アプリケーションはより堅牢になりフォールト トレランスが向上します。</span><span class="sxs-lookup"><span data-stu-id="91e03-324">Clients no longer need to be hard coded with endpoint, making your application more robust and fault tolerant.</span></span> <span data-ttu-id="91e03-325">探索は、アプリケーションに自動構成機能をビルドするための最適なプラットフォームです。</span><span class="sxs-lookup"><span data-stu-id="91e03-325">Discovery is the perfect platform to build auto-configuration capabilities into your application.</span></span>  
  
 <span data-ttu-id="91e03-326">製品は、WS-Discovery 標準の上に構築されます。</span><span class="sxs-lookup"><span data-stu-id="91e03-326">The product is built on top of the WS-Discovery standard.</span></span> <span data-ttu-id="91e03-327">相互運用可能、拡張可能、および汎用的になるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="91e03-327">It’s designed to be interoperable, extensible, and generic.</span></span> <span data-ttu-id="91e03-328">製品では 2 つの操作モードがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="91e03-328">The product supports two modes of operation:</span></span>  
  
1.  <span data-ttu-id="91e03-329">マネージド: 既存のサービスに関する知識を持つエンティティがネットワーク上にあり、クライアントは情報を直接クエリします。</span><span class="sxs-lookup"><span data-stu-id="91e03-329">Managed: where there is an entity on the network knowledgeable about existing services, clients query it directly for information.</span></span> <span data-ttu-id="91e03-330">これは Active Directory に類似しています。</span><span class="sxs-lookup"><span data-stu-id="91e03-330">This is analogous to Active Directory.</span></span>  
  
2.  <span data-ttu-id="91e03-331">アドホック: クライアントはマルチキャスト メッセージを使用してサービスを特定します。</span><span class="sxs-lookup"><span data-stu-id="91e03-331">Ad-hoc: where clients use multicast messages to locate services.</span></span>  
  
 <span data-ttu-id="91e03-332">さらに、探索メッセージはネットワーク プロトコルに依存しません。モード要件をサポートする任意のプロトコル上でこれらを使用できます。</span><span class="sxs-lookup"><span data-stu-id="91e03-332">Furthermore, discovery messages are network protocol agnostic; you can use them on top any protocol that supports the mode requirements.</span></span> <span data-ttu-id="91e03-333">たとえば、探索マルチキャスト メッセージを UDP チャネルまたはマルチキャスト メッセージングをサポートするその他のネットワークを介して送信されることができます。</span><span class="sxs-lookup"><span data-stu-id="91e03-333">For example, discovery multicast messages can be sent over the UDP channel or any other network that supports multicast messaging.</span></span>  <span data-ttu-id="91e03-334">これらの設計ポイント機能の柔軟性と組み合わせて、ソリューションに探索を適応させることができます。</span><span class="sxs-lookup"><span data-stu-id="91e03-334">These design points, combined with feature flexibility, allow you to adapt the discovery specifically to your solution.</span></span>  
  
### <a name="getting-started"></a><span data-ttu-id="91e03-335">作業の開始</span><span class="sxs-lookup"><span data-stu-id="91e03-335">Getting Started</span></span>  
  
-   <span data-ttu-id="91e03-336">ドキュメント: [WCF Discovery](../../../docs/framework/wcf/feature-details/wcf-discovery.md)</span><span class="sxs-lookup"><span data-stu-id="91e03-336">Documentation: [WCF Discovery](../../../docs/framework/wcf/feature-details/wcf-discovery.md)</span></span>  
  
-   <span data-ttu-id="91e03-337">サンプル:[探索 (サンプル)](../../../docs/framework/wcf/samples/discovery-samples.md)</span><span class="sxs-lookup"><span data-stu-id="91e03-337">Samples: [Discovery (Samples)](../../../docs/framework/wcf/samples/discovery-samples.md)</span></span>  
  
### <a name="discovery-scenarios"></a><span data-ttu-id="91e03-338">探索のシナリオ</span><span class="sxs-lookup"><span data-stu-id="91e03-338">Discovery Scenarios</span></span>  
 <span data-ttu-id="91e03-339">サービスがいつ使用可能になるかが不明なため、開発者はエンドポイントのハードコーディングを望みません。</span><span class="sxs-lookup"><span data-stu-id="91e03-339">A developer doesn't want to hard code endpoints, since it is unknown when my service will be available.</span></span> <span data-ttu-id="91e03-340">代わりに、開発者は実行時にサービスを選択することを望んでいます。</span><span class="sxs-lookup"><span data-stu-id="91e03-340">Instead, the developer wants to choose a service at runtime.</span></span> <span data-ttu-id="91e03-341">アプリケーションのコンポーネント間に、切り離し、堅牢性、および自動構成がさらに必要です。</span><span class="sxs-lookup"><span data-stu-id="91e03-341">More decoupling, robustness, and auto-configuration is needed between the components in the application.</span></span>  
  
## <a name="tracking"></a><span data-ttu-id="91e03-342">追跡</span><span class="sxs-lookup"><span data-stu-id="91e03-342">Tracking</span></span>  
 <span data-ttu-id="91e03-343">ワークフロー追跡では、ワークフロー インスタンスの実行に関する洞察を提供します。</span><span class="sxs-lookup"><span data-stu-id="91e03-343">Workflow tracking provides insight into the execution of a workflow instance.</span></span>  <span data-ttu-id="91e03-344">追跡イベントは、ワークフロー インスタンス レベルで、ワークフロー内のアクティビティの実行時にワークフローから出力されます。</span><span class="sxs-lookup"><span data-stu-id="91e03-344">The tracking events are emitted from a workflow at the workflow instance level and when activities within the workflow execute.</span></span> <span data-ttu-id="91e03-345">追跡レコードを定期受信するにはワークフロー追跡参加要素をワークフロー ホストに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91e03-345">A workflow tracking participant needs to be added to the workflow host to subscribe to tracking records.</span></span> <span data-ttu-id="91e03-346">追跡レコードは、追跡プロファイルを使用してフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="91e03-346">The tracking records are filtered using a tracking profile.</span></span> <span data-ttu-id="91e03-347">.Net Framework には ETW (Event Tracing for Windows) 追跡参加要素が用意されており、基本プロファイルが machine.config ファイルにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="91e03-347">The .Net Framework provides an ETW (Event Tracing for Windows) tracking participant, and a basic profile is installed in the machine.config file.</span></span>  
  
### <a name="getting-started"></a><span data-ttu-id="91e03-348">作業の開始</span><span class="sxs-lookup"><span data-stu-id="91e03-348">Getting Started</span></span>  
  
1.  <span data-ttu-id="91e03-349">[!INCLUDE[vs2010](../../../includes/vs2010-md.md)] で、WCF ワークフロー サービス アプリケーション プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="91e03-349">In [!INCLUDE[vs2010](../../../includes/vs2010-md.md)], create a WCF Workflow Service Application project.</span></span> <span data-ttu-id="91e03-350">開始するキャンバスに <xref:System.ServiceModel.Activities.Receive> と <xref:System.ServiceModel.Activities.SendReply> のペアが配置されます。</span><span class="sxs-lookup"><span data-stu-id="91e03-350">A <xref:System.ServiceModel.Activities.Receive> and <xref:System.ServiceModel.Activities.SendReply> pair will be placed on your canvas to start.</span></span>  
  
2.  <span data-ttu-id="91e03-351">web.config を開き、プロファイルなしで ETW 追跡動作を追加します。</span><span class="sxs-lookup"><span data-stu-id="91e03-351">Open the web.config and add an ETW tracking behavior with no profile.</span></span>  
  
    1.  <span data-ttu-id="91e03-352">既定のプロファイルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="91e03-352">The default profile is used.</span></span>  
  
    2.  <span data-ttu-id="91e03-353">イベント ビューアーを開き、次のノードで分析チャネルを有効にする:**イベント ビューアー**、 **Applications and Services Logs**、 **Microsoft**、 **Windows**、**アプリケーション サーバー-アプリケーション**します。</span><span class="sxs-lookup"><span data-stu-id="91e03-353">Open event viewer and enable the analytic channel in the following node: **Event Viewer**, **Applications and Services Logs**, **Microsoft**, **Windows**, **Application Server-Applications**.</span></span> <span data-ttu-id="91e03-354">右クリック**分析**選択**ログの有効化**します。</span><span class="sxs-lookup"><span data-stu-id="91e03-354">Right-click **Analytic** and select **Enable Log**.</span></span>  
  
    3.  <span data-ttu-id="91e03-355">ワークフロー サービスを実行します。</span><span class="sxs-lookup"><span data-stu-id="91e03-355">Run the workflow service.</span></span>  
  
    4.  <span data-ttu-id="91e03-356">イベント ビューアーでワークフロー追跡イベントを確認します。</span><span class="sxs-lookup"><span data-stu-id="91e03-356">Observe the workflow tracking events in event viewer.</span></span>  
  
3.  <span data-ttu-id="91e03-357">サンプル:[追跡](../../../docs/framework/windows-workflow-foundation/samples/tracking.md)</span><span class="sxs-lookup"><span data-stu-id="91e03-357">Samples: [Tracking](../../../docs/framework/windows-workflow-foundation/samples/tracking.md)</span></span>  
  
4.  <span data-ttu-id="91e03-358">概念説明のドキュメント:[ワークフロー追跡とトレース](../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)</span><span class="sxs-lookup"><span data-stu-id="91e03-358">Conceptual documentation: [Workflow Tracking and Tracing](../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)</span></span>  
  
## <a name="sql-workflow-instance-store"></a><span data-ttu-id="91e03-359">SQL Workflow Instance Store</span><span class="sxs-lookup"><span data-stu-id="91e03-359">SQL Workflow Instance Store</span></span>  
 <span data-ttu-id="91e03-360"><xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore> は、SQL Server ベースのインスタンス ストアの実装です。</span><span class="sxs-lookup"><span data-stu-id="91e03-360">The <xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore> is a SQL Server-based implementation of an instance store.</span></span> <span data-ttu-id="91e03-361">インスタンス ストアは、実行中のインスタンスの状態を、そのインスタンスの読み込みと再開に必要なすべてのデータと共に格納します。</span><span class="sxs-lookup"><span data-stu-id="91e03-361">An instance store stores the state of a running instance together with all data necessary to load and resume that instance.</span></span> <span data-ttu-id="91e03-362">サービス ホストは、ワークフローが永続的な場合にインスタンス状態を保存するようインスタンス ストアに指示し、そのインスタンスのメッセージが到着するか遅延アクティビティが期限切れになったときにインスタンス状態を読み込むようインスタンス ストアに指示します。</span><span class="sxs-lookup"><span data-stu-id="91e03-362">The service host instructs the instance store to save the instance state if the workflow persists, and it instructs the instance store to load the instance state when a message arrives for that instance or a delay activity expires.</span></span>  
  
### <a name="getting-started"></a><span data-ttu-id="91e03-363">作業の開始</span><span class="sxs-lookup"><span data-stu-id="91e03-363">Getting Started</span></span>  
  
1.  <span data-ttu-id="91e03-364">[!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)] で、暗黙的または明示的な <xref:System.Activities.Statements.Persist> アクティビティを含むワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="91e03-364">In [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)], create a Workflow that contains an implicit or explicit <xref:System.Activities.Statements.Persist> activity.</span></span> <span data-ttu-id="91e03-365"><xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore> 動作をワークフロー サービス ホストに追加します。</span><span class="sxs-lookup"><span data-stu-id="91e03-365">Add the <xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore> behavior to your workflow service host.</span></span> <span data-ttu-id="91e03-366">これはコードまたはアプリケーション構成ファイルで行うことができます。</span><span class="sxs-lookup"><span data-stu-id="91e03-366">This can be done in code or in the application configuration file.</span></span>  
  
2.  <span data-ttu-id="91e03-367">サンプル:[永続化](../../../docs/framework/windows-workflow-foundation/samples/persistence.md)</span><span class="sxs-lookup"><span data-stu-id="91e03-367">Samples: [Persistence](../../../docs/framework/windows-workflow-foundation/samples/persistence.md)</span></span>  
  
3.  <span data-ttu-id="91e03-368">概念説明のドキュメント: [SQL Workflow Instance Store](../../../docs/framework/windows-workflow-foundation/sql-workflow-instance-store.md)します。</span><span class="sxs-lookup"><span data-stu-id="91e03-368">Conceptual documentation: [SQL Workflow Instance Store](../../../docs/framework/windows-workflow-foundation/sql-workflow-instance-store.md).</span></span>
