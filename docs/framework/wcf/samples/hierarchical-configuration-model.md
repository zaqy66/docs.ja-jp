---
title: 階層的な構成モデル
ms.date: 03/30/2017
ms.assetid: 28dcc698-226c-4b77-9e51-8bf45a36216c
ms.openlocfilehash: ce0bc69424495594e0ee9c6b950a5fa9c4d5f993
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/27/2018
ms.locfileid: "43000102"
---
# <a name="hierarchical-configuration-model"></a><span data-ttu-id="8ed67-102">階層的な構成モデル</span><span class="sxs-lookup"><span data-stu-id="8ed67-102">Hierarchical Configuration Model</span></span>
<span data-ttu-id="8ed67-103">このサンプルでは、サービスの構成ファイルの階層を実装する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-103">This sample demonstrates how to implement a hierarchy of configuration files for services.</span></span> <span data-ttu-id="8ed67-104">また、バインド、サービス動作、およびエンドポイント動作を階層の上位レベルから継承する方法も示します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-104">It also shows how bindings, service behaviors, and endpoint behaviors are inherited from higher levels in the hierarchy.</span></span>  
  
## <a name="sample-details"></a><span data-ttu-id="8ed67-105">サンプルの詳細</span><span class="sxs-lookup"><span data-stu-id="8ed67-105">Sample details</span></span>  
 <span data-ttu-id="8ed67-106">WCF での開発、機能の 1 つ[!INCLUDE[netfx40_long](../../../../includes/netfx40-long-md.md)]階層的な構成モデルの拡張機能です。</span><span class="sxs-lookup"><span data-stu-id="8ed67-106">One of the features developed for WCF in [!INCLUDE[netfx40_long](../../../../includes/netfx40-long-md.md)] is the improvement in the hierarchical configuration model.</span></span> <span data-ttu-id="8ed67-107">階層的な構成モデルは、たとえば、Machine.config -> Rootweb.config -> Web.config のように定義されます。[!INCLUDE[netfx40_short](../../../../includes/netfx40-short-md.md)] では、構成階層の上位レベルで定義されるこれらのバインドおよび動作が、明示的な構成なしにサービスに追加されます。</span><span class="sxs-lookup"><span data-stu-id="8ed67-107">An example of a hierarchical configuration model would be the one defined by Machine.config -> Rootweb.config -> Web.config. In [!INCLUDE[netfx40_short](../../../../includes/netfx40-short-md.md)], those bindings and behaviors that are defined in upper levels in the configuration hierarchy are added to your services with no explicit configuration.</span></span> <span data-ttu-id="8ed67-108">このサンプルでは、コンピューター レベルまたはアプリケーション レベルで定義された構成要素に依存することによって簡単なサービス構成を実現する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-108">This sample shows how it is possible to simplify your service configuration by relying on configuration elements defined at the computer or the application level.</span></span>  
  
 <span data-ttu-id="8ed67-109">このサンプルは、階層の 3 つのレベルで定義された 9 個のサービスから構成されます。</span><span class="sxs-lookup"><span data-stu-id="8ed67-109">This sample consists of nine services, defined in three levels of hierarchy.</span></span> <span data-ttu-id="8ed67-110">`Service1` はルートになります。</span><span class="sxs-lookup"><span data-stu-id="8ed67-110">`Service1` is at the root.</span></span> <span data-ttu-id="8ed67-111">`Service2` と `Service3` は `Service1` から既定の要素を継承します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-111">`Service2` and `Service3` inherit the default elements from `Service1`.</span></span> <span data-ttu-id="8ed67-112">`Service4`、`Service5`、`Service6`、および `Service7` は、階層の第 3 レベルで定義され、`Service3` から既定の要素を継承します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-112">`Service4`, `Service5`, `Service6` and `Service7` are defined at a third level of the hierarchy, inheriting the default elements from `Service3`.</span></span> <span data-ttu-id="8ed67-113">最後に、`Service10` および `Service11` は階層の第 4 レベルに置かれます。</span><span class="sxs-lookup"><span data-stu-id="8ed67-113">Finally `Service10` and `Service11` are at a fourth level of the hierarchy.</span></span>  
  
 <span data-ttu-id="8ed67-114">すべてのサービスは `IDesc` コントラクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-114">All the services implement the `IDesc` contract.</span></span> <span data-ttu-id="8ed67-115">`IDesc` インターフェイスの定義を次に示します。この定義は、このインターフェイスで公開されるメソッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="8ed67-115">The following is the definition of the `IDesc` interface that shows the methods exposed in this interface.</span></span> <span data-ttu-id="8ed67-116">`IDesc` インターフェイスは Service1.cs で定義されます。</span><span class="sxs-lookup"><span data-stu-id="8ed67-116">The `IDesc` interface is defined in Service1.cs.</span></span>  
  
```csharp  
// Define a service contract  
[ServiceContract(Namespace="http://Microsoft.Samples.ConfigHierarchicalModel")]  
public interface IDesc  
{  
    [OperationContract]  
    List<string> ListEndpoints();  
    [OperationContract]  
    List<string> ListServiceBehaviors();  
    [OperationContract]  
    List<string> ListEndpointBehaviors();  
}  
```  
  
 <span data-ttu-id="8ed67-117">サービスによるこれらのメソッドの実装は単純です。</span><span class="sxs-lookup"><span data-stu-id="8ed67-117">The implementation of these methods by the services is straightforward.</span></span> <span data-ttu-id="8ed67-118">`ListEndpoints` は、すべてのサービス エンドポイントを反復処理し、サービスにあるすべてのエンドポイントのリストを返します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-118">`ListEndpoints` iterates through all the service endpoints and returns a list of all the endpoints that the service has.</span></span> <span data-ttu-id="8ed67-119">`ListServiceBehaviors` は、サービスに追加されたすべての動作を反復処理し、サービスに関連付けられているすべてのサービス動作のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-119">`ListServiceBehaviors` iterates through all the behaviors added to the service and returns the list of all the service behaviors associated with the service.</span></span> <span data-ttu-id="8ed67-120">`ListEndpointBehaviors` は、`ListServiceBehaviors` と同様に動作しますが、サービス動作ではなくエンドポイント動作のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-120">`ListEndpointBehaviors` behaves in a similar way to `ListServiceBehaviors`, but it returns the list of endpoint behaviors instead.</span></span>  
  
 <span data-ttu-id="8ed67-121">この実装により、クライアントは、サービスで公開されているエンドポイントの数、およびサービスに追加されたサービス動作とエンドポイント動作を認識できます。</span><span class="sxs-lookup"><span data-stu-id="8ed67-121">This implementation allows the client to know how many endpoints the service is exposing and which service behaviors and endpoint behaviors have been added to the service.</span></span> <span data-ttu-id="8ed67-122">サンプルの一部として実装されているクライアントは、ソリューションのすべてのサービスにサービス参照を追加し、サービスごとにこれらの要素を示します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-122">The client that has been implemented as part of the sample adds a service reference to all the services in the solution and shows these elements for each one of the services.</span></span>  
  
## <a name="to-use-this-sample"></a><span data-ttu-id="8ed67-123">このサンプルを使用するには</span><span class="sxs-lookup"><span data-stu-id="8ed67-123">To use this sample</span></span>  
  
#### <a name="to-run-the-client"></a><span data-ttu-id="8ed67-124">クライアントを実行するには</span><span class="sxs-lookup"><span data-stu-id="8ed67-124">To run the client</span></span>  
  
1.  <span data-ttu-id="8ed67-125">[!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] を使用して、ConfigHierarchicalModel.sln ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="8ed67-125">Using [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], open the ConfigHierarchicalModel.sln file.</span></span>  
  
2.  <span data-ttu-id="8ed67-126">クライアント プロジェクトはまだスタートアップ プロジェクトに設定されていないので、次の手順で設定します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-126">The client project is not already set up as the start-up project, follow these steps.</span></span>  
  
    1.  <span data-ttu-id="8ed67-127">**ソリューション エクスプ ローラー**ソリューションを右クリックし、**プロパティ**します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-127">In **Solution Explorer**, right-click the solution and then select **Properties**.</span></span>  
  
    2.  <span data-ttu-id="8ed67-128">**共通プロパティ**を選択します**スタートアップ プロジェクト**、 をクリックし、**シングル スタートアップ プロジェクト**します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-128">In **Common Properties**, select **Startup Project**, and then click **Single startup project**.</span></span>  
  
    3.  <span data-ttu-id="8ed67-129">**シングル スタートアップ プロジェクト**ドロップダウン リストで選択**クライアント**します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-129">From the **Single startup project** drop-down, select **Client**.</span></span>  
  
    4.  <span data-ttu-id="8ed67-130">クリックして**OK**ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8ed67-130">Click **OK** to close the dialog.</span></span>  
  
3.  <span data-ttu-id="8ed67-131">サンプルをビルドするには、Ctrl キーと Shift キーを押しながら B キーを押します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-131">To build the sample, press CTRL+SHIFT+B.</span></span>  
  
4.  <span data-ttu-id="8ed67-132">クライアントを実行するには、Ctrl キーを押しながら F5 キーを押します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-132">To run the client, press Ctrl+F5.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8ed67-133">次の手順が機能しない場合、環境が設定されている正しく、次の手順を使用することを確認します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-133">If these steps do not work, make sure that your environment has been properly set up, using the following steps:</span></span>  
>   
> 1.  <span data-ttu-id="8ed67-134">実行したことを確認、 [Windows Communication Foundation サンプルの 1 回限りのセットアップ手順](one-time-setup-procedure-for-the-wcf-samples.md)します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-134">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
> 2.  <span data-ttu-id="8ed67-135">ソリューションをビルドする手順については、 [Windows Communication Foundation サンプルのビルド](building-the-samples.md)します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-135">To build the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
> 3.  <span data-ttu-id="8ed67-136">1 つまたは複数のコンピューター構成でサンプルを実行する手順については、 [Windows Communication Foundation サンプルの実行](running-the-samples.md)します。</span><span class="sxs-lookup"><span data-stu-id="8ed67-136">To run the sample in a single or multiple computer configurations, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="8ed67-137">サンプルは、既にコンピューターにインストールされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="8ed67-137">The samples may already be installed on your computer.</span></span> <span data-ttu-id="8ed67-138">続行する前に、次の (既定の) ディレクトリを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8ed67-138">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="8ed67-139">このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](http://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。</span><span class="sxs-lookup"><span data-stu-id="8ed67-139">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="8ed67-140">このサンプルは、次のディレクトリに格納されます。</span><span class="sxs-lookup"><span data-stu-id="8ed67-140">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Services\ConfigHierarchicalModel`  
  
## <a name="see-also"></a><span data-ttu-id="8ed67-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="8ed67-141">See Also</span></span>  
 [<span data-ttu-id="8ed67-142">AppFabric 管理のサンプル</span><span class="sxs-lookup"><span data-stu-id="8ed67-142">AppFabric Management Samples</span></span>](http://go.microsoft.com/fwlink/?LinkId=193960)
