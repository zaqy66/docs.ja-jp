---
title: <security> の <peerTransport>
ms.date: 03/30/2017
ms.assetid: f73634ed-f896-4968-bf74-5e5ac52d3b6b
ms.openlocfilehash: aadf2058c66cea4919d5dc9aa5aeab7850fcc395
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55283765"
---
# <a name="security-of-peertransport"></a><span data-ttu-id="0b0d2-102">\<セキュリティ > の\<peerTransport ></span><span class="sxs-lookup"><span data-stu-id="0b0d2-102">\<security> of \<peerTransport></span></span>
<span data-ttu-id="0b0d2-103">ピア チャネルに関連付けられたセキュリティ設定を格納します。使用される認証の種類とメッセージ トランスポートで使用されるセキュリティを含みます。</span><span class="sxs-lookup"><span data-stu-id="0b0d2-103">Contains the security settings associated with a peer channel, including the type of authentication used and the security used for the message transport.</span></span>  
  
 <span data-ttu-id="0b0d2-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="0b0d2-104">\<system.serviceModel></span></span>  
<span data-ttu-id="0b0d2-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="0b0d2-105">\<bindings></span></span>  
<span data-ttu-id="0b0d2-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="0b0d2-106">\<customBinding></span></span>  
<span data-ttu-id="0b0d2-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="0b0d2-107">\<binding></span></span>  
<span data-ttu-id="0b0d2-108">\<peerTransport ></span><span class="sxs-lookup"><span data-stu-id="0b0d2-108">\<peerTransport></span></span>  
<span data-ttu-id="0b0d2-109">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="0b0d2-109">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0b0d2-110">構文</span><span class="sxs-lookup"><span data-stu-id="0b0d2-110">Syntax</span></span>  
  
```xml  
<security mode="None/Transport/Message/TransportWithMessageCredential">
  <transport clientCredentialType="None/Windows/UserName/Certificate/CardSpace" />
</security
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0b0d2-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="0b0d2-111">Attributes and Elements</span></span>  
 <span data-ttu-id="0b0d2-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="0b0d2-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0b0d2-113">属性</span><span class="sxs-lookup"><span data-stu-id="0b0d2-113">Attributes</span></span>  
  
|<span data-ttu-id="0b0d2-114">属性</span><span class="sxs-lookup"><span data-stu-id="0b0d2-114">Attribute</span></span>|<span data-ttu-id="0b0d2-115">説明</span><span class="sxs-lookup"><span data-stu-id="0b0d2-115">Description</span></span>|  
|---------------|-----------------|  
|`mode`|<span data-ttu-id="0b0d2-116">適用するセキュリティの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b0d2-116">Specifies the type of security to be applied.</span></span> <span data-ttu-id="0b0d2-117">既定値は Message です。</span><span class="sxs-lookup"><span data-stu-id="0b0d2-117">The default value is Message.</span></span> <span data-ttu-id="0b0d2-118">この属性は <xref:System.ServiceModel.SecurityMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="0b0d2-118">This attribute is of type <xref:System.ServiceModel.SecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="0b0d2-119">mode 属性</span><span class="sxs-lookup"><span data-stu-id="0b0d2-119">mode Attribute</span></span>  
  
|<span data-ttu-id="0b0d2-120">値</span><span class="sxs-lookup"><span data-stu-id="0b0d2-120">Value</span></span>|<span data-ttu-id="0b0d2-121">説明</span><span class="sxs-lookup"><span data-stu-id="0b0d2-121">Description</span></span>|  
|-----------|-----------------|  
|`None`|<span data-ttu-id="0b0d2-122">セキュリティを無効にします。</span><span class="sxs-lookup"><span data-stu-id="0b0d2-122">Security is disabled.</span></span>|  
|`Transport`|<span data-ttu-id="0b0d2-123">セキュリティは、HTTPS を使用して確保されます。</span><span class="sxs-lookup"><span data-stu-id="0b0d2-123">Security is provided using HTTPS.</span></span>|  
|`Message`|<span data-ttu-id="0b0d2-124">SOAP セキュリティにより、認証、整合性、および機密性が実現します。</span><span class="sxs-lookup"><span data-stu-id="0b0d2-124">SOAP security provides authentication, integrity and confidentiality.</span></span>|  
|`TransportWithMessageCredential`|<span data-ttu-id="0b0d2-125">HTTPS により、認証および機密性が実現します。</span><span class="sxs-lookup"><span data-stu-id="0b0d2-125">HTTPS provides authentication and confidentiality.</span></span> <span data-ttu-id="0b0d2-126">SOAP メッセージには、豊富な資格情報の種類が用意されています。</span><span class="sxs-lookup"><span data-stu-id="0b0d2-126">SOAP messages provide rich credential types.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0b0d2-127">子要素</span><span class="sxs-lookup"><span data-stu-id="0b0d2-127">Child Elements</span></span>  
  
|<span data-ttu-id="0b0d2-128">要素</span><span class="sxs-lookup"><span data-stu-id="0b0d2-128">Element</span></span>|<span data-ttu-id="0b0d2-129">説明</span><span class="sxs-lookup"><span data-stu-id="0b0d2-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0b0d2-130">\<transport></span><span class="sxs-lookup"><span data-stu-id="0b0d2-130">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-peertransport.md)|<span data-ttu-id="0b0d2-131">カスタム バインドのピア トランスポートを定義します。</span><span class="sxs-lookup"><span data-stu-id="0b0d2-131">Defines a peer transport for a custom binding.</span></span> <span data-ttu-id="0b0d2-132">この要素には、サービスと対話するときに使用される資格情報を指定する `clientCredentialType` 属性があります。</span><span class="sxs-lookup"><span data-stu-id="0b0d2-132">This element has a `clientCredentialType` attribute that specifies the credentials to be used when interacting with a service.</span></span> <span data-ttu-id="0b0d2-133">この属性は <xref:System.ServiceModel.PeerTransportCredentialType> 型です。</span><span class="sxs-lookup"><span data-stu-id="0b0d2-133">This attribute is of type <xref:System.ServiceModel.PeerTransportCredentialType>.</span></span><br /><br /> <span data-ttu-id="0b0d2-134">この要素は <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="0b0d2-134">This element is of type <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0b0d2-135">親要素</span><span class="sxs-lookup"><span data-stu-id="0b0d2-135">Parent Elements</span></span>  
  
|<span data-ttu-id="0b0d2-136">要素</span><span class="sxs-lookup"><span data-stu-id="0b0d2-136">Element</span></span>|<span data-ttu-id="0b0d2-137">説明</span><span class="sxs-lookup"><span data-stu-id="0b0d2-137">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0b0d2-138">\<peerTransport></span><span class="sxs-lookup"><span data-stu-id="0b0d2-138">\<peerTransport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peertransport.md)|<span data-ttu-id="0b0d2-139">カスタム バインドのピア トランスポートを定義します。</span><span class="sxs-lookup"><span data-stu-id="0b0d2-139">Defines a peer transport for a custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0b0d2-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="0b0d2-140">See also</span></span>
- <xref:System.ServiceModel.Configuration.PeerSecurityElement>
- <xref:System.ServiceModel.PeerSecuritySettings>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="0b0d2-141">トランスポート セキュリティ</span><span class="sxs-lookup"><span data-stu-id="0b0d2-141">Transport Security</span></span>](../../../../../docs/framework/wcf/feature-details/transport-security.md)
- [<span data-ttu-id="0b0d2-142">トランスポート</span><span class="sxs-lookup"><span data-stu-id="0b0d2-142">Transports</span></span>](../../../../../docs/framework/wcf/feature-details/transports.md)
- [<span data-ttu-id="0b0d2-143">トランスポートの選択</span><span class="sxs-lookup"><span data-stu-id="0b0d2-143">Choosing a Transport</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)
- [<span data-ttu-id="0b0d2-144">バインディング</span><span class="sxs-lookup"><span data-stu-id="0b0d2-144">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="0b0d2-145">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="0b0d2-145">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="0b0d2-146">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="0b0d2-146">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="0b0d2-147">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="0b0d2-147">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
