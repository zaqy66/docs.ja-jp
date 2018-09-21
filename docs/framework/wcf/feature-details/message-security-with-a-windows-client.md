---
title: Windows クライアントとのメッセージ セキュリティ
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 01e7d0b8-10f9-45c3-a4c5-53d44dc61eb8
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 34f6078baba86868fa03f37873731c39e73ac81f
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2018
ms.locfileid: "46481664"
---
# <a name="message-security-with-a-windows-client"></a><span data-ttu-id="e13d4-102">Windows クライアントとのメッセージ セキュリティ</span><span class="sxs-lookup"><span data-stu-id="e13d4-102">Message Security with a Windows Client</span></span>
<span data-ttu-id="e13d4-103">このシナリオでは、Windows Communication Foundation (WCF) クライアントとメッセージ セキュリティ モードによって保護されたサーバーを示します。</span><span class="sxs-lookup"><span data-stu-id="e13d4-103">This scenario shows a Windows Communication Foundation (WCF) client and server secured by message security mode.</span></span> <span data-ttu-id="e13d4-104">クライアントとサービスは、Windows 資格情報を使用して認証します。</span><span class="sxs-lookup"><span data-stu-id="e13d4-104">The client and service are authenticated using Windows credentials.</span></span>  
  
 <span data-ttu-id="e13d4-105">![メッセージのセキュリティと Windows クライアント](../../../../docs/framework/wcf/feature-details/media/1c8618d4-0005-4022-beb6-32fd087a8c3c.gif "1c8618d4-0005-4022-beb6-32fd087a8c3c")</span><span class="sxs-lookup"><span data-stu-id="e13d4-105">![Message security with a Windows client](../../../../docs/framework/wcf/feature-details/media/1c8618d4-0005-4022-beb6-32fd087a8c3c.gif "1c8618d4-0005-4022-beb6-32fd087a8c3c")</span></span>  
  
|<span data-ttu-id="e13d4-106">特徴</span><span class="sxs-lookup"><span data-stu-id="e13d4-106">Characteristic</span></span>|<span data-ttu-id="e13d4-107">説明</span><span class="sxs-lookup"><span data-stu-id="e13d4-107">Description</span></span>|  
|--------------------|-----------------|  
|<span data-ttu-id="e13d4-108">セキュリティ モード</span><span class="sxs-lookup"><span data-stu-id="e13d4-108">Security Mode</span></span>|<span data-ttu-id="e13d4-109">メッセージ</span><span class="sxs-lookup"><span data-stu-id="e13d4-109">Message</span></span>|  
|<span data-ttu-id="e13d4-110">相互運用性</span><span class="sxs-lookup"><span data-stu-id="e13d4-110">Interoperability</span></span>|<span data-ttu-id="e13d4-111">WCF のみ</span><span class="sxs-lookup"><span data-stu-id="e13d4-111">WCF Only</span></span>|  
|<span data-ttu-id="e13d4-112">認証 (サーバー)</span><span class="sxs-lookup"><span data-stu-id="e13d4-112">Authentication (Server)</span></span>|<span data-ttu-id="e13d4-113">サーバーとクライアントの相互認証</span><span class="sxs-lookup"><span data-stu-id="e13d4-113">Mutual authentication of the server and client</span></span>|  
|<span data-ttu-id="e13d4-114">認証 (クライアント)</span><span class="sxs-lookup"><span data-stu-id="e13d4-114">Authentication (Client)</span></span>|<span data-ttu-id="e13d4-115">サーバーとクライアントの相互認証</span><span class="sxs-lookup"><span data-stu-id="e13d4-115">Mutual authentication of the server and client</span></span>|  
|<span data-ttu-id="e13d4-116">整合性</span><span class="sxs-lookup"><span data-stu-id="e13d4-116">Integrity</span></span>|<span data-ttu-id="e13d4-117">はい、共有のセキュリティ コンテキストを使用します</span><span class="sxs-lookup"><span data-stu-id="e13d4-117">Yes, using shared security context</span></span>|  
|<span data-ttu-id="e13d4-118">機密性</span><span class="sxs-lookup"><span data-stu-id="e13d4-118">Confidentiality</span></span>|<span data-ttu-id="e13d4-119">はい、共有のセキュリティ コンテキストを使用します</span><span class="sxs-lookup"><span data-stu-id="e13d4-119">Yes, using shared security context</span></span>|  
|<span data-ttu-id="e13d4-120">Transport</span><span class="sxs-lookup"><span data-stu-id="e13d4-120">Transport</span></span>|<span data-ttu-id="e13d4-121">NET.TCP</span><span class="sxs-lookup"><span data-stu-id="e13d4-121">NET.TCP</span></span>|  
|<span data-ttu-id="e13d4-122">バインド</span><span class="sxs-lookup"><span data-stu-id="e13d4-122">Binding</span></span>|<xref:System.ServiceModel.NetTcpBinding>|  
  
## <a name="service"></a><span data-ttu-id="e13d4-123">サービス</span><span class="sxs-lookup"><span data-stu-id="e13d4-123">Service</span></span>  
 <span data-ttu-id="e13d4-124">次のコードと構成は、別々に実行します。</span><span class="sxs-lookup"><span data-stu-id="e13d4-124">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="e13d4-125">次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="e13d4-125">Do one of the following:</span></span>  
  
-   <span data-ttu-id="e13d4-126">構成を使用せずに、コードを使用してスタンドアロン サービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e13d4-126">Create a stand-alone service using the code with no configuration.</span></span>  
  
-   <span data-ttu-id="e13d4-127">提供された構成を使用してサービスを作成しますが、エンドポイントを定義しません。</span><span class="sxs-lookup"><span data-stu-id="e13d4-127">Create a service using the supplied configuration, but do not define any endpoints.</span></span>  
  
### <a name="code"></a><span data-ttu-id="e13d4-128">コード</span><span class="sxs-lookup"><span data-stu-id="e13d4-128">Code</span></span>  
 <span data-ttu-id="e13d4-129">次のコードでは、メッセージ セキュリティを使用するサービス エンドポイントを作成し、Windows コンピューターとの間にセキュリティで保護されたコンテキストを確立する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e13d4-129">The following code shows how to create a service endpoint that uses message security to establish a secure context with a Windows machine.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#11](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#11)]
 [!code-vb[C_SecurityScenarios#11](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#11)]  
  
### <a name="configuration"></a><span data-ttu-id="e13d4-130">構成</span><span class="sxs-lookup"><span data-stu-id="e13d4-130">Configuration</span></span>  
 <span data-ttu-id="e13d4-131">コードの代わりに次の構成を使用して、サービスをセットアップできます。</span><span class="sxs-lookup"><span data-stu-id="e13d4-131">The following configuration can be used instead of the code to set up the service:</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <services>  
      <service behaviorConfiguration=""  
               name="ServiceModel.Calculator">  
        <endpoint address="net.tcp://localhost:8008/Calculator"  
                  binding="netTcpBinding"  
                  bindingConfiguration="Windows"  
                  name="WindowsOverMessage"  
                  contract="ServiceModel.ICalculator" />  
      </service>  
    </services>  
    <bindings>  
      <netTcpBinding>  
        <binding name="Windows">  
          <security mode="Message">  
            <message clientCredentialType="Windows" />  
          </security>  
        </binding>  
      </netTcpBinding>  
    </bindings>  
    <client />  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="client"></a><span data-ttu-id="e13d4-132">クライアント</span><span class="sxs-lookup"><span data-stu-id="e13d4-132">Client</span></span>  
 <span data-ttu-id="e13d4-133">次のコードと構成は、別々に実行します。</span><span class="sxs-lookup"><span data-stu-id="e13d4-133">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="e13d4-134">次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="e13d4-134">Do one of the following:</span></span>  
  
-   <span data-ttu-id="e13d4-135">コード (およびクライアント コード) を使用してスタンドアロン クライアントを作成します。</span><span class="sxs-lookup"><span data-stu-id="e13d4-135">Create a stand-alone client using the code (and client code).</span></span>  
  
-   <span data-ttu-id="e13d4-136">エンドポイント アドレスを定義しないクライアントを作成します。</span><span class="sxs-lookup"><span data-stu-id="e13d4-136">Create a client that does not define any endpoint addresses.</span></span> <span data-ttu-id="e13d4-137">代わりに、引数として構成名を受け取るクライアント コンストラクターを使用します。</span><span class="sxs-lookup"><span data-stu-id="e13d4-137">Instead, use the client constructor that takes the configuration name as an argument.</span></span> <span data-ttu-id="e13d4-138">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="e13d4-138">For example:</span></span>  
  
     [!code-csharp[C_SecurityScenarios#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#0)]
     [!code-vb[C_SecurityScenarios#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#0)]  
  
### <a name="code"></a><span data-ttu-id="e13d4-139">コード</span><span class="sxs-lookup"><span data-stu-id="e13d4-139">Code</span></span>  
 <span data-ttu-id="e13d4-140">クライアントを作成する場合のコード例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e13d4-140">The following code creates a client.</span></span> <span data-ttu-id="e13d4-141">バインディングはメッセージ モード セキュリティに対して行い、クライアント資格情報の種類は `Windows` に設定します。</span><span class="sxs-lookup"><span data-stu-id="e13d4-141">The binding is to Message mode security, and the client credential type is set to `Windows`.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#18](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#18)]
 [!code-vb[C_SecurityScenarios#18](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#18)]  
  
### <a name="configuration"></a><span data-ttu-id="e13d4-142">構成</span><span class="sxs-lookup"><span data-stu-id="e13d4-142">Configuration</span></span>  
 <span data-ttu-id="e13d4-143">次の構成を使用してクライアントのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e13d4-143">The following configuration is used to set the client properties.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <bindings>  
      <netTcpBinding>  
        <binding name="NetTcpBinding_ICalculator" >  
         <security mode="Message">  
            <message clientCredentialType="Windows" />  
          </security>  
        </binding>  
      </netTcpBinding>  
    </bindings>  
    <client>  
      <endpoint address="net.tcp://machineName:8008/Calculator"   
                binding="netTcpBinding"  
                bindingConfiguration="NetTcpBinding_ICalculator"  
                contract="ICalculator"  
                name="NetTcpBinding_ICalculator">          
      </endpoint>  
    </client>  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="e13d4-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="e13d4-144">See Also</span></span>  
 [<span data-ttu-id="e13d4-145">セキュリティの概要</span><span class="sxs-lookup"><span data-stu-id="e13d4-145">Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/security-overview.md)  
 [<span data-ttu-id="e13d4-146">Windows Server App Fabric のセキュリティ モデル</span><span class="sxs-lookup"><span data-stu-id="e13d4-146">Security Model for Windows Server App Fabric</span></span>](https://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
