---
title: '方法 : 基本的な Windows Communication Foundation クライアントを構成する'
ms.date: 09/14/2018
helpviewer_keywords:
- WCF clients [WCF], configuring
ms.assetid: d067b86d-afb0-47bf-94f6-45180a3d8d78
ms.openlocfilehash: 3f267edf87711de8a5969e3e0b577648008c5a75
ms.sourcegitcommit: dfb2a100cfb4d3902c042f17b3204f49bc7635e7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/21/2018
ms.locfileid: "46524864"
---
# <a name="how-to-configure-a-basic-windows-communication-foundation-client"></a><span data-ttu-id="7b83b-102">方法 : 基本的な Windows Communication Foundation クライアントを構成する</span><span class="sxs-lookup"><span data-stu-id="7b83b-102">How to: Configure a Basic Windows Communication Foundation Client</span></span>

<span data-ttu-id="7b83b-103">これは、5 番目の基本的な Windows Communication Foundation (WCF) アプリケーションを作成するために必要な 6 つのタスクです。</span><span class="sxs-lookup"><span data-stu-id="7b83b-103">This is the fifth of six tasks required to create a basic Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="7b83b-104">6 つのすべてのタスクの概要については、「[チュートリアル入門](../../../docs/framework/wcf/getting-started-tutorial.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b83b-104">For an overview of all six of the tasks, see the [Getting Started Tutorial](../../../docs/framework/wcf/getting-started-tutorial.md) topic.</span></span>

<span data-ttu-id="7b83b-105">このトピックで説明を使用して生成されたクライアント構成ファイル、**サービス参照の追加**Visual Studio の機能または[ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)します。</span><span class="sxs-lookup"><span data-stu-id="7b83b-105">This topic discusses the client configuration file that was generated using the **Add Service Reference** functionality of Visual Studio or the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md).</span></span> <span data-ttu-id="7b83b-106">クライアントを構成するには、クライアントがサービスにアクセスするために使用するエンドポイントを指定します。</span><span class="sxs-lookup"><span data-stu-id="7b83b-106">Configuring the client consists of specifying the endpoint that the client uses to access the service.</span></span> <span data-ttu-id="7b83b-107">エンドポイントが、アドレス、バインディング、およびコントラクト、およびこれらの各クライアントを構成する過程で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b83b-107">An endpoint has an address, a binding, and a contract, and each of these must be specified in the process of configuring the client.</span></span>

## <a name="configure-a-windows-communication-foundation-client"></a><span data-ttu-id="7b83b-108">Windows Communication Foundation クライアントを構成します。</span><span class="sxs-lookup"><span data-stu-id="7b83b-108">Configure a Windows Communication Foundation client</span></span>

<span data-ttu-id="7b83b-109">GettingStartedClient プロジェクトから生成された構成ファイル (App.config) を開きます。</span><span class="sxs-lookup"><span data-stu-id="7b83b-109">Open the generated configuration file (App.config) from the GettingStartedClient project.</span></span> <span data-ttu-id="7b83b-110">生成された構成ファイルを次の例に示します。</span><span class="sxs-lookup"><span data-stu-id="7b83b-110">The following example is a view of the generated configuration file.</span></span> <span data-ttu-id="7b83b-111">[\<system.serviceModel >](../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)セクションの下にある [\<endpoint >](https://msdn.microsoft.com/library/13aa23b7-2f08-4add-8dbf-a99f8127c017)要素を見つけてください。</span><span class="sxs-lookup"><span data-stu-id="7b83b-111">Under the [\<system.serviceModel>](../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md) section, find the [\<endpoint>](https://msdn.microsoft.com/library/13aa23b7-2f08-4add-8dbf-a99f8127c017) element.</span></span>

```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
        <startup>
          <!-- specifies the version of WCF to use-->
            <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5,Profile=Client" />
        </startup>
        <system.serviceModel>
            <bindings>
                <!-- Uses wsHttpBinding-->
                <wsHttpBinding>
                    <binding name="WSHttpBinding_ICalculator" />
                </wsHttpBinding>
            </bindings>
            <client>
                <!-- specifies the endpoint to use when calling the service -->
                <endpoint address="http://localhost:8000/ServiceModelSamples/Service/CalculatorService"
                    binding="wsHttpBinding" bindingConfiguration="WSHttpBinding_ICalculator"
                    contract="ServiceReference1.ICalculator" name="WSHttpBinding_ICalculator">
                    <identity>
                        <userPrincipalName value="migree@redmond.corp.microsoft.com" />
                    </identity>
                </endpoint>
            </client>
        </system.serviceModel>
    </configuration>
```

<span data-ttu-id="7b83b-112">この例では、次のアドレスにあるサービスにアクセスするクライアントが使用するエンドポイント:`http://localhost:8000/ServiceModelSamples/Service/CalculatorService`します。</span><span class="sxs-lookup"><span data-stu-id="7b83b-112">This example configures the endpoint that the client uses to access the service that is located at the following address: `http://localhost:8000/ServiceModelSamples/Service/CalculatorService`.</span></span>

<span data-ttu-id="7b83b-113">endpoint 要素は、`ServiceReference1.ICalculator` サービス コントラクトが、WCF クライアントと WCF サービス間の通信に使用されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="7b83b-113">The endpoint element specifies that the `ServiceReference1.ICalculator` service contract is used for communication between the WCF client and service.</span></span> <span data-ttu-id="7b83b-114">WCF チャネルはシステム標準の <xref:System.ServiceModel.WSHttpBinding> で構成されます。</span><span class="sxs-lookup"><span data-stu-id="7b83b-114">The WCF channel is configured with the system-provided <xref:System.ServiceModel.WSHttpBinding>.</span></span> <span data-ttu-id="7b83b-115">このコントラクトを使用して生成された**サービス参照の追加**Visual Studio でします。</span><span class="sxs-lookup"><span data-stu-id="7b83b-115">This contract was generated by using **Add Service Reference** in Visual Studio.</span></span> <span data-ttu-id="7b83b-116">基本的には、GettingStartedLib プロジェクトで定義されているコントラクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="7b83b-116">It is essentially a copy of the contract that was defined in the GettingStartedLib project.</span></span> <span data-ttu-id="7b83b-117"><xref:System.ServiceModel.WSHttpBinding> バインディングは、トランスポートとして HTTP を指定し、相互運用可能なセキュリティ、およびその他の構成詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="7b83b-117">The <xref:System.ServiceModel.WSHttpBinding> binding specifies HTTP as the transport, interoperable security, and other configuration details.</span></span>

<span data-ttu-id="7b83b-118">この構成で生成されたクライアントを使用する方法の詳細については、次を参照してください。[方法: クライアントを使用して](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)します。</span><span class="sxs-lookup"><span data-stu-id="7b83b-118">For more information about how to use the generated client with this configuration, see [How to: Use a Client](../../../docs/framework/wcf/how-to-use-a-wcf-client.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="7b83b-119">次の手順</span><span class="sxs-lookup"><span data-stu-id="7b83b-119">Next steps</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="7b83b-120">方法: WCF クライアントを使用</span><span class="sxs-lookup"><span data-stu-id="7b83b-120">How to: Use a WCF client</span></span>](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)

## <a name="see-also"></a><span data-ttu-id="7b83b-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="7b83b-121">See also</span></span>

- [<span data-ttu-id="7b83b-122">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="7b83b-122">Using Bindings to Configure Services and Clients</span></span>](../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="7b83b-123">ServiceModel メタデータ ユーティリティ ツール (Svcutil.exe)</span><span class="sxs-lookup"><span data-stu-id="7b83b-123">ServiceModel Metadata Utility Tool (Svcutil.exe)</span></span>](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [<span data-ttu-id="7b83b-124">方法: クライアントを作成する</span><span class="sxs-lookup"><span data-stu-id="7b83b-124">How to: Create a Client</span></span>](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)
- [<span data-ttu-id="7b83b-125">はじめに</span><span class="sxs-lookup"><span data-stu-id="7b83b-125">Getting Started</span></span>](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [<span data-ttu-id="7b83b-126">自己ホスト</span><span class="sxs-lookup"><span data-stu-id="7b83b-126">Self-Host</span></span>](../../../docs/framework/wcf/samples/self-host.md)