---
title: 基本的なサンプル
ms.date: 03/30/2017
ms.assetid: c1910bc1-3d0a-4fa6-b12a-4ed6fe759620
ms.openlocfilehash: 8c99b4955dcc00015d54391dcb509b312190ddab
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43392251"
---
# <a name="basic-sample"></a><span data-ttu-id="b7297-102">基本的なサンプル</span><span class="sxs-lookup"><span data-stu-id="b7297-102">Basic Sample</span></span>
<span data-ttu-id="b7297-103">このサンプルでは、サービスを探索可能にする方法と、探索可能なサービスの検索方法および呼び出し方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b7297-103">This sample shows how to make a service discoverable and how to search for and call a discoverable service.</span></span> <span data-ttu-id="b7297-104">このサンプルは、2 つのプロジェクト (サービスとクライアント) で構成されます。</span><span class="sxs-lookup"><span data-stu-id="b7297-104">This sample is composed of two projects: service and client.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b7297-105">このサンプルでは、探索をコードで実装しています。</span><span class="sxs-lookup"><span data-stu-id="b7297-105">This sample implements discovery in code.</span></span>  <span data-ttu-id="b7297-106">構成で探索を実装するサンプルについては、次を参照してください。[構成](../../../../docs/framework/wcf/samples/configuration-sample.md)します。</span><span class="sxs-lookup"><span data-stu-id="b7297-106">For a sample that implements discovery in configuration, see [Configuration](../../../../docs/framework/wcf/samples/configuration-sample.md).</span></span>  
  
## <a name="service"></a><span data-ttu-id="b7297-107">サービス</span><span class="sxs-lookup"><span data-stu-id="b7297-107">Service</span></span>  
 <span data-ttu-id="b7297-108">これは簡単な電卓サービスの実装です。</span><span class="sxs-lookup"><span data-stu-id="b7297-108">This is a simple calculator service implementation.</span></span> <span data-ttu-id="b7297-109">探索関連のコードは `Main` にあります。ここでは、次のコードに示すように、 <xref:System.ServiceModel.Discovery.ServiceDiscoveryBehavior> がサービス ホストに追加され、<xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> が追加されます。</span><span class="sxs-lookup"><span data-stu-id="b7297-109">The discovery related code can be found in `Main` where a <xref:System.ServiceModel.Discovery.ServiceDiscoveryBehavior> is added to the service host and a <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> is added as shown in the following code.</span></span>  
  
```  
using (ServiceHost serviceHost = new ServiceHost(typeof(CalculatorService), baseAddress))  
{  
    serviceHost.AddServiceEndpoint(typeof(ICalculatorService), new   
      WSHttpBinding(), String.Empty);  
  
    // Make the service discoverable over UDP multicast  
    serviceHost.Description.Behaviors.Add(new ServiceDiscoveryBehavior());                  
    serviceHost.AddServiceEndpoint(new UdpDiscoveryEndpoint());  
  
    serviceHost.Open();  
    // ...  
}  
```  
  
## <a name="client"></a><span data-ttu-id="b7297-110">Client</span><span class="sxs-lookup"><span data-stu-id="b7297-110">Client</span></span>  
 <span data-ttu-id="b7297-111">クライアントは、<xref:System.ServiceModel.Discovery.DynamicEndpoint> を使用してサービスを検索します。</span><span class="sxs-lookup"><span data-stu-id="b7297-111">The client uses a <xref:System.ServiceModel.Discovery.DynamicEndpoint> to locate the service.</span></span> <span data-ttu-id="b7297-112"><xref:System.ServiceModel.Discovery.DynamicEndpoint> は標準エンドポイントで、クライアントが開いたときにサービスのエンドポイントを解決します。</span><span class="sxs-lookup"><span data-stu-id="b7297-112">The <xref:System.ServiceModel.Discovery.DynamicEndpoint>, a standard endpoint, resolves the endpoint of the service when the client is opened.</span></span> <span data-ttu-id="b7297-113">この場合、<xref:System.ServiceModel.Discovery.DynamicEndpoint> は、サービス コントラクトに基づいてサービスを検索します。</span><span class="sxs-lookup"><span data-stu-id="b7297-113">In this case, the <xref:System.ServiceModel.Discovery.DynamicEndpoint> looks for the service based on the service contract.</span></span> <span data-ttu-id="b7297-114"><xref:System.ServiceModel.Discovery.DynamicEndpoint> は、既定で <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> を検索します。</span><span class="sxs-lookup"><span data-stu-id="b7297-114">The <xref:System.ServiceModel.Discovery.DynamicEndpoint> conducts the search over a <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> by default.</span></span> <span data-ttu-id="b7297-115">サービス エンドポイントが見つかると、クライアントは指定されたバインディングを介してそのサービスに接続します。</span><span class="sxs-lookup"><span data-stu-id="b7297-115">Once it locates a service endpoint, the client connects to that service over the specified binding.</span></span>  
  
```csharp  
public static void Main()  
{  
   DynamicEndpoint dynamicEndpoint = new DynamicEndpoint( ContractDescription.GetContract(typeof(ICalculatorService)), new WSHttpBinding());  
   // ...  
}              
```  
  
 <span data-ttu-id="b7297-116">クライアントは、`InvokeCalculatorService` クラスを使用してサービスを検索する <xref:System.ServiceModel.Discovery.DiscoveryClient> という名前のメソッドを定義します。</span><span class="sxs-lookup"><span data-stu-id="b7297-116">The client defines a method called `InvokeCalculatorService` that uses the <xref:System.ServiceModel.Discovery.DiscoveryClient> class to search for services.</span></span> <span data-ttu-id="b7297-117"><xref:System.ServiceModel.Discovery.DynamicEndpoint> は <xref:System.ServiceModel.Description.ServiceEndpoint> を継承しているため、`InvokeCalculatorService` メソッドに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="b7297-117">The <xref:System.ServiceModel.Discovery.DynamicEndpoint> inherits from <xref:System.ServiceModel.Description.ServiceEndpoint>, so it can be passed to the `InvokeCalculatorService` method.</span></span> <span data-ttu-id="b7297-118">この例では、次に <xref:System.ServiceModel.Discovery.DynamicEndpoint> を使用して `CalculatorServiceClient` インスタンスを作成し、電卓サービスのさまざまな操作を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b7297-118">The example then uses the <xref:System.ServiceModel.Discovery.DynamicEndpoint> to create an instance of `CalculatorServiceClient` and calls the various operations of the calculator service.</span></span>  
  
```csharp  
static void InvokeCalculatorService(ServiceEndpoint serviceEndpoint)  
{  
   // Create a client  
   CalculatorServiceClient client = new CalculatorServiceClient(serviceEndpoint);  
  
   Console.WriteLine("Invoking CalculatorService");  
   Console.WriteLine();  
  
   double value1 = 100.00D;  
   double value2 = 15.99D;  
  
   // Call the Add service operation.  
   double result = client.Add(value1, value2);  
   Console.WriteLine("Add({0},{1}) = {2}", value1, value2, result);  
  
   // Call the Subtract service operation.  
   result = client.Subtract(value1, value2);  
   Console.WriteLine("Subtract({0},{1}) = {2}", value1, value2, result);  
  
   // Call the Multiply service operation.  
   result = client.Multiply(value1, value2);  
   Console.WriteLine("Multiply({0},{1}) = {2}", value1, value2, result);  
  
   // Call the Divide service operation.  
   result = client.Divide(value1, value2);  
   Console.WriteLine("Divide({0},{1}) = {2}", value1, value2, result);  
   Console.WriteLine();  
  
   //Closing the client gracefully closes the connection and cleans up resources  
   client.Close();  
}  
```  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="b7297-119">このサンプルを使用するには</span><span class="sxs-lookup"><span data-stu-id="b7297-119">To use this sample</span></span>  
  
1.  <span data-ttu-id="b7297-120">このサンプルでは HTTP エンドポイントを使用します。このサンプルを実行するには、適切な URL ACL を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7297-120">This sample uses HTTP endpoints and to run this sample, proper URL ACLs must be added.</span></span> <span data-ttu-id="b7297-121">詳細については、次を参照してください。[構成の HTTP および HTTPS](https://go.microsoft.com/fwlink/?LinkId=70353)します。</span><span class="sxs-lookup"><span data-stu-id="b7297-121">For more information, see [Configuring HTTP and HTTPS](https://go.microsoft.com/fwlink/?LinkId=70353).</span></span> <span data-ttu-id="b7297-122">管理特権で次のコマンドを実行すると、適切な ACL が追加されます。</span><span class="sxs-lookup"><span data-stu-id="b7297-122">Executing the following command at an elevated privilege should add the appropriate ACLs.</span></span> <span data-ttu-id="b7297-123">そのままではコマンドが動作しない場合は、代わりに、ドメインとユーザー名を引数に指定して実行してみてください。</span><span class="sxs-lookup"><span data-stu-id="b7297-123">You may want to substitute your Domain and Username for the following arguments if the command does not work as is.</span></span> `netsh http add urlacl url=http://+:8000/ user=%DOMAIN%\%UserName%`  
  
2.  <span data-ttu-id="b7297-124">[!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] を使用して Basic.sln を開き、サンプルをビルドします。</span><span class="sxs-lookup"><span data-stu-id="b7297-124">Using [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], open the Basic.sln and build the sample.</span></span>  
  
3.  <span data-ttu-id="b7297-125">service.exe アプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="b7297-125">Run the service.exe application.</span></span>  
  
4.  <span data-ttu-id="b7297-126">サービスが開始したら、client.exe を実行します。</span><span class="sxs-lookup"><span data-stu-id="b7297-126">After the service has started, run the client.exe.</span></span>  
  
5.  <span data-ttu-id="b7297-127">クライアントがサービスのアドレスを知ることなくサービスを検索できたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b7297-127">Observe that the client was able to find the service without knowing its address.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="b7297-128">サンプルは、既にコンピューターにインストールされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="b7297-128">The samples may already be installed on your machine.</span></span> <span data-ttu-id="b7297-129">続行する前に、次の (既定の) ディレクトリを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b7297-129">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="b7297-130">このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。</span><span class="sxs-lookup"><span data-stu-id="b7297-130">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="b7297-131">このサンプルは、次のディレクトリに格納されます。</span><span class="sxs-lookup"><span data-stu-id="b7297-131">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Discovery\Basic`  
  
## <a name="see-also"></a><span data-ttu-id="b7297-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7297-132">See Also</span></span>
