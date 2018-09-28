---
title: '&lt;netPeerBinding&gt; の &lt;security&gt;'
ms.date: 03/30/2017
ms.assetid: 1ef40d8c-f903-4426-9b08-da81462766d8
author: BrucePerlerMS
ms.openlocfilehash: d17d063ffdd354327c2523415b7d9394e723135a
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2018
ms.locfileid: "47436298"
---
# <a name="ltsecuritygt-of-ltnetpeerbindinggt"></a><span data-ttu-id="4f9f5-102">&lt;netPeerBinding&gt; の &lt;security&gt;</span><span class="sxs-lookup"><span data-stu-id="4f9f5-102">&lt;security&gt; of &lt;netPeerBinding&gt;</span></span>
<span data-ttu-id="4f9f5-103">セキュリティ設定を定義、 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md)メッセージ トランスポートで使用されるセキュリティ、認証の種類などを使用します。</span><span class="sxs-lookup"><span data-stu-id="4f9f5-103">Defines the security settings of the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md), including the type of authentication used and the security used for the message transport.</span></span>  
  
 <span data-ttu-id="4f9f5-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="4f9f5-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="4f9f5-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="4f9f5-105">\<bindings></span></span>  
<span data-ttu-id="4f9f5-106">\<netPeerBinding></span><span class="sxs-lookup"><span data-stu-id="4f9f5-106">\<netPeerBinding></span></span>  
<span data-ttu-id="4f9f5-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="4f9f5-107">\<binding></span></span>  
<span data-ttu-id="4f9f5-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="4f9f5-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f9f5-109">構文</span><span class="sxs-lookup"><span data-stu-id="4f9f5-109">Syntax</span></span>  
  
```xml  
<netPeerBinding>  
    <binding>  
        <security mode="Message/None/Transport//TransportWithMessageCredential">  
            <transport credentialType="Certificate/Password" />  
        </security>  
    </binding>  
</netPeerBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4f9f5-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="4f9f5-110">Attributes and Elements</span></span>  
 <span data-ttu-id="4f9f5-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f9f5-111">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4f9f5-112">属性</span><span class="sxs-lookup"><span data-stu-id="4f9f5-112">Attributes</span></span>  
  
|<span data-ttu-id="4f9f5-113">属性</span><span class="sxs-lookup"><span data-stu-id="4f9f5-113">Attribute</span></span>|<span data-ttu-id="4f9f5-114">説明</span><span class="sxs-lookup"><span data-stu-id="4f9f5-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4f9f5-115">モード</span><span class="sxs-lookup"><span data-stu-id="4f9f5-115">mode</span></span>|<span data-ttu-id="4f9f5-116">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="4f9f5-116">Optional.</span></span> <span data-ttu-id="4f9f5-117">このバインディングで構成されたピアが使用するセキュリティの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="4f9f5-117">Specifies the type of security used by peers configured with this binding.</span></span> <span data-ttu-id="4f9f5-118">既定値は `Message` です。</span><span class="sxs-lookup"><span data-stu-id="4f9f5-118">The default value is `Message`.</span></span> <span data-ttu-id="4f9f5-119">この属性は <xref:System.ServiceModel.SecurityMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="4f9f5-119">This attribute is of type <xref:System.ServiceModel.SecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="4f9f5-120">mode 属性</span><span class="sxs-lookup"><span data-stu-id="4f9f5-120">mode Attribute</span></span>  
  
|<span data-ttu-id="4f9f5-121">値</span><span class="sxs-lookup"><span data-stu-id="4f9f5-121">Value</span></span>|<span data-ttu-id="4f9f5-122">説明</span><span class="sxs-lookup"><span data-stu-id="4f9f5-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="4f9f5-123">メッセージ</span><span class="sxs-lookup"><span data-stu-id="4f9f5-123">Message</span></span>|<span data-ttu-id="4f9f5-124">SOAP セキュリティにより、認証、整合性、および機密性が実現します。</span><span class="sxs-lookup"><span data-stu-id="4f9f5-124">SOAP security provides authentication, integrity and confidentiality.</span></span>|  
|<span data-ttu-id="4f9f5-125">なし</span><span class="sxs-lookup"><span data-stu-id="4f9f5-125">None</span></span>|<span data-ttu-id="4f9f5-126">セキュリティを無効にします。</span><span class="sxs-lookup"><span data-stu-id="4f9f5-126">Security is disabled.</span></span>|  
|<span data-ttu-id="4f9f5-127">Transport</span><span class="sxs-lookup"><span data-stu-id="4f9f5-127">Transport</span></span>|<span data-ttu-id="4f9f5-128">セキュリティは、HTTPS を使用して確保されます。</span><span class="sxs-lookup"><span data-stu-id="4f9f5-128">Security is provided using HTTPS.</span></span>|  
|<span data-ttu-id="4f9f5-129">TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="4f9f5-129">TransportWithMessageCredential</span></span>|<span data-ttu-id="4f9f5-130">HTTPS により、認証および機密性が実現します。</span><span class="sxs-lookup"><span data-stu-id="4f9f5-130">HTTPS provides authentication and confidentiality.</span></span> <span data-ttu-id="4f9f5-131">SOAP メッセージには、豊富な資格情報の種類が用意されています。</span><span class="sxs-lookup"><span data-stu-id="4f9f5-131">SOAP messages provide rich credential types.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4f9f5-132">子要素</span><span class="sxs-lookup"><span data-stu-id="4f9f5-132">Child Elements</span></span>  
  
|<span data-ttu-id="4f9f5-133">要素</span><span class="sxs-lookup"><span data-stu-id="4f9f5-133">Element</span></span>|<span data-ttu-id="4f9f5-134">説明</span><span class="sxs-lookup"><span data-stu-id="4f9f5-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4f9f5-135">\<transport></span><span class="sxs-lookup"><span data-stu-id="4f9f5-135">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-netpeertcpbinding.md)|<span data-ttu-id="4f9f5-136">このバインディングで構成されたピアが送信するセキュリティで保護されたメッセージのトランスポートの型を定義します。</span><span class="sxs-lookup"><span data-stu-id="4f9f5-136">Defines the transport type for secured messages sent by peers configured with this binding.</span></span> <span data-ttu-id="4f9f5-137">この要素は <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="4f9f5-137">This element is of type <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4f9f5-138">親要素</span><span class="sxs-lookup"><span data-stu-id="4f9f5-138">Parent Elements</span></span>  
  
|<span data-ttu-id="4f9f5-139">要素</span><span class="sxs-lookup"><span data-stu-id="4f9f5-139">Element</span></span>|<span data-ttu-id="4f9f5-140">説明</span><span class="sxs-lookup"><span data-stu-id="4f9f5-140">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4f9f5-141">\<binding></span><span class="sxs-lookup"><span data-stu-id="4f9f5-141">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="4f9f5-142">すべてのバインド機能を定義、 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="4f9f5-142">Defines all binding capabilities of the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4f9f5-143">Remarks</span><span class="sxs-lookup"><span data-stu-id="4f9f5-143">Remarks</span></span>  
 <span data-ttu-id="4f9f5-144">セキュリティは、メッセージ固有にすることも、トランスポート固有にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="4f9f5-144">Security can be either message- or transport-specific.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4f9f5-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f9f5-145">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PeerSecurityElement>  
 <xref:System.ServiceModel.NetPeerTcpBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.NetPeerTcpBindingElement.Security%2A>  
 <xref:System.ServiceModel.PeerSecuritySettings>  
 [<span data-ttu-id="4f9f5-146">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="4f9f5-146">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="4f9f5-147">資格情報の種類の選択</span><span class="sxs-lookup"><span data-stu-id="4f9f5-147">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)  
 [<span data-ttu-id="4f9f5-148">バインディング</span><span class="sxs-lookup"><span data-stu-id="4f9f5-148">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="4f9f5-149">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="4f9f5-149">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="4f9f5-150">バインドを使用して、Windows Communication Foundation サービスとクライアントを構成するには</span><span class="sxs-lookup"><span data-stu-id="4f9f5-150">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="4f9f5-151">\<binding></span><span class="sxs-lookup"><span data-stu-id="4f9f5-151">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
