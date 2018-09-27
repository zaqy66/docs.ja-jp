---
title: '&lt;webHttpBinding&gt; の &lt;security&gt;'
ms.date: 03/30/2017
ms.assetid: 727cf3d2-6f56-48ad-a59f-ba423edb9c83
author: BrucePerlerMS
ms.openlocfilehash: 28cff66cfd50229eacbb7c7c4b1d65678efb40ea
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47236203"
---
# <a name="ltsecuritygt-of-ltwebhttpbindinggt"></a><span data-ttu-id="f295d-102">&lt;webHttpBinding&gt; の &lt;security&gt;</span><span class="sxs-lookup"><span data-stu-id="f295d-102">&lt;security&gt; of &lt;webHttpBinding&gt;</span></span>
<span data-ttu-id="f295d-103">構成されているエンドポイントのセキュリティ要件を指定します、 [ \<wsHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="f295d-103">Specifies the security requirements for an endpoint configured with a [\<wsHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md).</span></span>  
  
 <span data-ttu-id="f295d-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="f295d-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="f295d-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="f295d-105">\<bindings></span></span>  
<span data-ttu-id="f295d-106">\<webHttpBinding></span><span class="sxs-lookup"><span data-stu-id="f295d-106">\<webHttpBinding></span></span>  
<span data-ttu-id="f295d-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="f295d-107">\<binding></span></span>  
<span data-ttu-id="f295d-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="f295d-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f295d-109">構文</span><span class="sxs-lookup"><span data-stu-id="f295d-109">Syntax</span></span>  
  
```xml  
<system.ServiceModel>  
    <bindings>  
        <webHttpBinding>  
            <binding name = "string">  
              <security mode="None/Transport/TransportCredentialOnly">  
                                    <transport clientCredentialType =   
                                     "Basic/Certificate/Digest/None/Ntlm/Windows"  
                                     proxyCredentialType="Basic/Digest/None/Ntlm/Windows"  
                                     realm="string" />  
              </security>  
        </webHttpBinding>  
    </bindings>  
</system.ServiceModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f295d-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="f295d-110">Attributes and Elements</span></span>  
 <span data-ttu-id="f295d-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="f295d-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f295d-112">属性</span><span class="sxs-lookup"><span data-stu-id="f295d-112">Attributes</span></span>  
  
|<span data-ttu-id="f295d-113">属性</span><span class="sxs-lookup"><span data-stu-id="f295d-113">Attribute</span></span>|<span data-ttu-id="f295d-114">説明</span><span class="sxs-lookup"><span data-stu-id="f295d-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f295d-115">モード</span><span class="sxs-lookup"><span data-stu-id="f295d-115">mode</span></span>|<span data-ttu-id="f295d-116">トランスポート レベルのセキュリティをエンドポイントで使用するか、セキュリティを使用しないかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f295d-116">Specifies whether transport-level security or no security is used by an endpoint.</span></span> <span data-ttu-id="f295d-117">既定値は、`None` です。</span><span class="sxs-lookup"><span data-stu-id="f295d-117">The default is `None`.</span></span> <span data-ttu-id="f295d-118">この属性は <xref:System.ServiceModel.WebHttpSecurityMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="f295d-118">This attribute is of type <xref:System.ServiceModel.WebHttpSecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="f295d-119">Mode 属性</span><span class="sxs-lookup"><span data-stu-id="f295d-119">Mode Attribute</span></span>  
  
|<span data-ttu-id="f295d-120">値</span><span class="sxs-lookup"><span data-stu-id="f295d-120">Value</span></span>|<span data-ttu-id="f295d-121">説明</span><span class="sxs-lookup"><span data-stu-id="f295d-121">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="f295d-122">なし</span><span class="sxs-lookup"><span data-stu-id="f295d-122">None</span></span>|<span data-ttu-id="f295d-123">セキュリティを無効にします。</span><span class="sxs-lookup"><span data-stu-id="f295d-123">Security is disabled.</span></span>|  
|<span data-ttu-id="f295d-124">Transport</span><span class="sxs-lookup"><span data-stu-id="f295d-124">Transport</span></span>|<span data-ttu-id="f295d-125">セキュリティは、HTTPS を使用して確保されます。</span><span class="sxs-lookup"><span data-stu-id="f295d-125">Security is provided using HTTPS.</span></span> <span data-ttu-id="f295d-126">サービスは、SSL 証明書を使用して構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f295d-126">The service needs to be configured with SSL certificates.</span></span> <span data-ttu-id="f295d-127">メッセージは、HTTPS およびサービスを使用して完全にセキュリティで保護され、サービスの SSL 証明書を使用するクライアントによって認証されます。</span><span class="sxs-lookup"><span data-stu-id="f295d-127">The message is entirely secured using HTTPS and the service is authenticated by the client using the service’s SSL certificate.</span></span> <span data-ttu-id="f295d-128">クライアント認証はによって制御されます、`ClientCredentialType`の属性、 [\<トランスポート >](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-webhttpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="f295d-128">The client authentication is controlled through the `ClientCredentialType` attribute of the [\<transport>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-webhttpbinding.md).</span></span>|  
|<span data-ttu-id="f295d-129">TransportCredentialOnly</span><span class="sxs-lookup"><span data-stu-id="f295d-129">TransportCredentialOnly</span></span>|<span data-ttu-id="f295d-130">このモードは、メッセージの整合性と機密性を提供しません。</span><span class="sxs-lookup"><span data-stu-id="f295d-130">This mode does not provide message integrity and confidentiality.</span></span> <span data-ttu-id="f295d-131">HTTP ベースのクライアント認証を提供します。</span><span class="sxs-lookup"><span data-stu-id="f295d-131">It provides HTTP-based client authentication.</span></span> <span data-ttu-id="f295d-132">このモードを使用するときは、十分に注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f295d-132">This mode should be used with caution.</span></span> <span data-ttu-id="f295d-133">これは、トランスポート セキュリティ (IPSec) などの他の方法で提供されるされ、クライアント認証だけが、WCF インフラストラクチャによって提供される環境で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f295d-133">It should be used in environments where the transport security is being provided by other means (such as IPSec) and only client authentication is provided by the WCF infrastructure.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f295d-134">子要素</span><span class="sxs-lookup"><span data-stu-id="f295d-134">Child Elements</span></span>  
  
|<span data-ttu-id="f295d-135">要素</span><span class="sxs-lookup"><span data-stu-id="f295d-135">Element</span></span>|<span data-ttu-id="f295d-136">説明</span><span class="sxs-lookup"><span data-stu-id="f295d-136">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f295d-137">\<transport></span><span class="sxs-lookup"><span data-stu-id="f295d-137">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-webhttpbinding.md)|<span data-ttu-id="f295d-138">トランスポートのセキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="f295d-138">Defines the transport security settings.</span></span> <span data-ttu-id="f295d-139">この要素は、<xref:System.ServiceModel.Configuration.HttpTransportSecurityElement> 型に対応しています。</span><span class="sxs-lookup"><span data-stu-id="f295d-139">This element corresponds to the <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement> type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f295d-140">親要素</span><span class="sxs-lookup"><span data-stu-id="f295d-140">Parent Elements</span></span>  
  
|<span data-ttu-id="f295d-141">要素</span><span class="sxs-lookup"><span data-stu-id="f295d-141">Element</span></span>|<span data-ttu-id="f295d-142">説明</span><span class="sxs-lookup"><span data-stu-id="f295d-142">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f295d-143">\<webHttpBinding></span><span class="sxs-lookup"><span data-stu-id="f295d-143">\<webHttpBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md)|<span data-ttu-id="f295d-144">Windows Communication Foundation (WCF) Web サービスの SOAP メッセージに代わって HTTP 要求に応答するエンドポイントを構成するために使用するバインド要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="f295d-144">A binding element that is used to configure endpoints for Windows Communication Foundation (WCF) Web services that respond to HTTP requests instead of SOAP messages.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f295d-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="f295d-145">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.WebHttpBindingElement>  
 <xref:System.ServiceModel.Configuration.WSHttpSecurityElement>  
 <xref:System.ServiceModel.WebHttpBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.WebHttpBindingElement.Security%2A>  
 <xref:System.ServiceModel.WebHttpSecurity>  
 [<span data-ttu-id="f295d-146">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="f295d-146">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="f295d-147">資格情報の種類の選択</span><span class="sxs-lookup"><span data-stu-id="f295d-147">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)  
 [<span data-ttu-id="f295d-148">バインディング</span><span class="sxs-lookup"><span data-stu-id="f295d-148">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="f295d-149">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="f295d-149">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="f295d-150">バインドを使用して、Windows Communication Foundation サービスとクライアントを構成するには</span><span class="sxs-lookup"><span data-stu-id="f295d-150">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="f295d-151">\<binding></span><span class="sxs-lookup"><span data-stu-id="f295d-151">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)  
 [<span data-ttu-id="f295d-152">WCF Web HTTP プログラミング モデル</span><span class="sxs-lookup"><span data-stu-id="f295d-152">WCF Web HTTP Programming Model</span></span>](../../../../../docs/framework/wcf/feature-details/wcf-web-http-programming-model.md)
