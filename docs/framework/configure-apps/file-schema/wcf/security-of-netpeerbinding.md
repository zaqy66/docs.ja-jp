---
title: '&lt;netPeerBinding&gt; の &lt;security&gt;'
ms.date: 03/30/2017
ms.assetid: 1ef40d8c-f903-4426-9b08-da81462766d8
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 45000554226fcde753041fca283bfc8b1eeba5ce
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43489761"
---
# <a name="ltsecuritygt-of-ltnetpeerbindinggt"></a><span data-ttu-id="7bc3c-102">&lt;netPeerBinding&gt; の &lt;security&gt;</span><span class="sxs-lookup"><span data-stu-id="7bc3c-102">&lt;security&gt; of &lt;netPeerBinding&gt;</span></span>
<span data-ttu-id="7bc3c-103">セキュリティ設定を定義、 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md)メッセージ トランスポートで使用されるセキュリティ、認証の種類などを使用します。</span><span class="sxs-lookup"><span data-stu-id="7bc3c-103">Defines the security settings of the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md), including the type of authentication used and the security used for the message transport.</span></span>  
  
 <span data-ttu-id="7bc3c-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="7bc3c-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="7bc3c-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="7bc3c-105">\<bindings></span></span>  
<span data-ttu-id="7bc3c-106">\<netPeerBinding></span><span class="sxs-lookup"><span data-stu-id="7bc3c-106">\<netPeerBinding></span></span>  
<span data-ttu-id="7bc3c-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="7bc3c-107">\<binding></span></span>  
<span data-ttu-id="7bc3c-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="7bc3c-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7bc3c-109">構文</span><span class="sxs-lookup"><span data-stu-id="7bc3c-109">Syntax</span></span>  
  
```xml  
<netPeerBinding>  
    <binding>  
        <security mode="Message/None/Transport//TransportWithMessageCredential">  
            <transport credentialType="Certificate/Password" />  
        </security>  
    </binding>  
</netPeerBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7bc3c-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="7bc3c-110">Attributes and Elements</span></span>  
 <span data-ttu-id="7bc3c-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="7bc3c-111">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7bc3c-112">属性</span><span class="sxs-lookup"><span data-stu-id="7bc3c-112">Attributes</span></span>  
  
|<span data-ttu-id="7bc3c-113">属性</span><span class="sxs-lookup"><span data-stu-id="7bc3c-113">Attribute</span></span>|<span data-ttu-id="7bc3c-114">説明</span><span class="sxs-lookup"><span data-stu-id="7bc3c-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="7bc3c-115">モード</span><span class="sxs-lookup"><span data-stu-id="7bc3c-115">mode</span></span>|<span data-ttu-id="7bc3c-116">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="7bc3c-116">Optional.</span></span> <span data-ttu-id="7bc3c-117">このバインディングで構成されたピアが使用するセキュリティの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="7bc3c-117">Specifies the type of security used by peers configured with this binding.</span></span> <span data-ttu-id="7bc3c-118">既定値は `Message` です。</span><span class="sxs-lookup"><span data-stu-id="7bc3c-118">The default value is `Message`.</span></span> <span data-ttu-id="7bc3c-119">この属性は <xref:System.ServiceModel.SecurityMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="7bc3c-119">This attribute is of type <xref:System.ServiceModel.SecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="7bc3c-120">mode 属性</span><span class="sxs-lookup"><span data-stu-id="7bc3c-120">mode Attribute</span></span>  
  
|<span data-ttu-id="7bc3c-121">値</span><span class="sxs-lookup"><span data-stu-id="7bc3c-121">Value</span></span>|<span data-ttu-id="7bc3c-122">説明</span><span class="sxs-lookup"><span data-stu-id="7bc3c-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="7bc3c-123">メッセージ</span><span class="sxs-lookup"><span data-stu-id="7bc3c-123">Message</span></span>|<span data-ttu-id="7bc3c-124">SOAP セキュリティにより、認証、整合性、および機密性が実現します。</span><span class="sxs-lookup"><span data-stu-id="7bc3c-124">SOAP security provides authentication, integrity and confidentiality.</span></span>|  
|<span data-ttu-id="7bc3c-125">なし</span><span class="sxs-lookup"><span data-stu-id="7bc3c-125">None</span></span>|<span data-ttu-id="7bc3c-126">セキュリティを無効にします。</span><span class="sxs-lookup"><span data-stu-id="7bc3c-126">Security is disabled.</span></span>|  
|<span data-ttu-id="7bc3c-127">Transport</span><span class="sxs-lookup"><span data-stu-id="7bc3c-127">Transport</span></span>|<span data-ttu-id="7bc3c-128">セキュリティは、HTTPS を使用して確保されます。</span><span class="sxs-lookup"><span data-stu-id="7bc3c-128">Security is provided using HTTPS.</span></span>|  
|<span data-ttu-id="7bc3c-129">TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="7bc3c-129">TransportWithMessageCredential</span></span>|<span data-ttu-id="7bc3c-130">HTTPS により、認証および機密性が実現します。</span><span class="sxs-lookup"><span data-stu-id="7bc3c-130">HTTPS provides authentication and confidentiality.</span></span> <span data-ttu-id="7bc3c-131">SOAP メッセージには、豊富な資格情報の種類が用意されています。</span><span class="sxs-lookup"><span data-stu-id="7bc3c-131">SOAP messages provide rich credential types.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7bc3c-132">子要素</span><span class="sxs-lookup"><span data-stu-id="7bc3c-132">Child Elements</span></span>  
  
|<span data-ttu-id="7bc3c-133">要素</span><span class="sxs-lookup"><span data-stu-id="7bc3c-133">Element</span></span>|<span data-ttu-id="7bc3c-134">説明</span><span class="sxs-lookup"><span data-stu-id="7bc3c-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7bc3c-135">\<transport></span><span class="sxs-lookup"><span data-stu-id="7bc3c-135">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-netpeertcpbinding.md)|<span data-ttu-id="7bc3c-136">このバインディングで構成されたピアが送信するセキュリティで保護されたメッセージのトランスポートの型を定義します。</span><span class="sxs-lookup"><span data-stu-id="7bc3c-136">Defines the transport type for secured messages sent by peers configured with this binding.</span></span> <span data-ttu-id="7bc3c-137">この要素は <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="7bc3c-137">This element is of type <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="7bc3c-138">親要素</span><span class="sxs-lookup"><span data-stu-id="7bc3c-138">Parent Elements</span></span>  
  
|<span data-ttu-id="7bc3c-139">要素</span><span class="sxs-lookup"><span data-stu-id="7bc3c-139">Element</span></span>|<span data-ttu-id="7bc3c-140">説明</span><span class="sxs-lookup"><span data-stu-id="7bc3c-140">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7bc3c-141">\<binding></span><span class="sxs-lookup"><span data-stu-id="7bc3c-141">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="7bc3c-142">すべてのバインド機能を定義、 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="7bc3c-142">Defines all binding capabilities of the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7bc3c-143">Remarks</span><span class="sxs-lookup"><span data-stu-id="7bc3c-143">Remarks</span></span>  
 <span data-ttu-id="7bc3c-144">セキュリティは、メッセージ固有にすることも、トランスポート固有にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="7bc3c-144">Security can be either message- or transport-specific.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7bc3c-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="7bc3c-145">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PeerSecurityElement>  
 <xref:System.ServiceModel.NetPeerTcpBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.NetPeerTcpBindingElement.Security%2A>  
 <xref:System.ServiceModel.PeerSecuritySettings>  
 [<span data-ttu-id="7bc3c-146">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="7bc3c-146">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="7bc3c-147">資格情報の種類の選択</span><span class="sxs-lookup"><span data-stu-id="7bc3c-147">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)  
 [<span data-ttu-id="7bc3c-148">バインディング</span><span class="sxs-lookup"><span data-stu-id="7bc3c-148">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="7bc3c-149">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="7bc3c-149">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="7bc3c-150">バインドを使用して、Windows Communication Foundation サービスとクライアントを構成するには</span><span class="sxs-lookup"><span data-stu-id="7bc3c-150">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="7bc3c-151">\<binding></span><span class="sxs-lookup"><span data-stu-id="7bc3c-151">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
