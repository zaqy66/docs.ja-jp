---
title: '&lt;peerTransport&gt; の &lt;security&gt;'
ms.date: 03/30/2017
ms.assetid: f73634ed-f896-4968-bf74-5e5ac52d3b6b
ms.openlocfilehash: 901a1d0b29fa6ea7d9e520b379dc7c7ff1d1e522
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151957"
---
# <a name="ltsecuritygt-of-ltpeertransportgt"></a><span data-ttu-id="d61ca-102">&lt;peerTransport&gt; の &lt;security&gt;</span><span class="sxs-lookup"><span data-stu-id="d61ca-102">&lt;security&gt; of &lt;peerTransport&gt;</span></span>
<span data-ttu-id="d61ca-103">ピア チャネルに関連付けられたセキュリティ設定を格納します。使用される認証の種類とメッセージ トランスポートで使用されるセキュリティを含みます。</span><span class="sxs-lookup"><span data-stu-id="d61ca-103">Contains the security settings associated with a peer channel, including the type of authentication used and the security used for the message transport.</span></span>  
  
 <span data-ttu-id="d61ca-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="d61ca-104">\<system.serviceModel></span></span>  
<span data-ttu-id="d61ca-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="d61ca-105">\<bindings></span></span>  
<span data-ttu-id="d61ca-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="d61ca-106">\<customBinding></span></span>  
<span data-ttu-id="d61ca-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="d61ca-107">\<binding></span></span>  
<span data-ttu-id="d61ca-108">\<peerTransport ></span><span class="sxs-lookup"><span data-stu-id="d61ca-108">\<peerTransport></span></span>  
<span data-ttu-id="d61ca-109">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="d61ca-109">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d61ca-110">構文</span><span class="sxs-lookup"><span data-stu-id="d61ca-110">Syntax</span></span>  
  
```xml  
<security mode="None/Transport/Message/TransportWithMessageCredential">
  <transport clientCredentialType="None/Windows/UserName/Certificate/CardSpace" />
</security
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d61ca-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="d61ca-111">Attributes and Elements</span></span>  
 <span data-ttu-id="d61ca-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="d61ca-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d61ca-113">属性</span><span class="sxs-lookup"><span data-stu-id="d61ca-113">Attributes</span></span>  
  
|<span data-ttu-id="d61ca-114">属性</span><span class="sxs-lookup"><span data-stu-id="d61ca-114">Attribute</span></span>|<span data-ttu-id="d61ca-115">説明</span><span class="sxs-lookup"><span data-stu-id="d61ca-115">Description</span></span>|  
|---------------|-----------------|  
|`mode`|<span data-ttu-id="d61ca-116">適用するセキュリティの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="d61ca-116">Specifies the type of security to be applied.</span></span> <span data-ttu-id="d61ca-117">既定値は Message です。</span><span class="sxs-lookup"><span data-stu-id="d61ca-117">The default value is Message.</span></span> <span data-ttu-id="d61ca-118">この属性は <xref:System.ServiceModel.SecurityMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="d61ca-118">This attribute is of type <xref:System.ServiceModel.SecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="d61ca-119">mode 属性</span><span class="sxs-lookup"><span data-stu-id="d61ca-119">mode Attribute</span></span>  
  
|<span data-ttu-id="d61ca-120">値</span><span class="sxs-lookup"><span data-stu-id="d61ca-120">Value</span></span>|<span data-ttu-id="d61ca-121">説明</span><span class="sxs-lookup"><span data-stu-id="d61ca-121">Description</span></span>|  
|-----------|-----------------|  
|`None`|<span data-ttu-id="d61ca-122">セキュリティを無効にします。</span><span class="sxs-lookup"><span data-stu-id="d61ca-122">Security is disabled.</span></span>|  
|`Transport`|<span data-ttu-id="d61ca-123">セキュリティは、HTTPS を使用して確保されます。</span><span class="sxs-lookup"><span data-stu-id="d61ca-123">Security is provided using HTTPS.</span></span>|  
|`Message`|<span data-ttu-id="d61ca-124">SOAP セキュリティにより、認証、整合性、および機密性が実現します。</span><span class="sxs-lookup"><span data-stu-id="d61ca-124">SOAP security provides authentication, integrity and confidentiality.</span></span>|  
|`TransportWithMessageCredential`|<span data-ttu-id="d61ca-125">HTTPS により、認証および機密性が実現します。</span><span class="sxs-lookup"><span data-stu-id="d61ca-125">HTTPS provides authentication and confidentiality.</span></span> <span data-ttu-id="d61ca-126">SOAP メッセージには、豊富な資格情報の種類が用意されています。</span><span class="sxs-lookup"><span data-stu-id="d61ca-126">SOAP messages provide rich credential types.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d61ca-127">子要素</span><span class="sxs-lookup"><span data-stu-id="d61ca-127">Child Elements</span></span>  
  
|<span data-ttu-id="d61ca-128">要素</span><span class="sxs-lookup"><span data-stu-id="d61ca-128">Element</span></span>|<span data-ttu-id="d61ca-129">説明</span><span class="sxs-lookup"><span data-stu-id="d61ca-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d61ca-130">\<transport></span><span class="sxs-lookup"><span data-stu-id="d61ca-130">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-peertransport.md)|<span data-ttu-id="d61ca-131">カスタム バインドのピア トランスポートを定義します。</span><span class="sxs-lookup"><span data-stu-id="d61ca-131">Defines a peer transport for a custom binding.</span></span> <span data-ttu-id="d61ca-132">この要素には、サービスと対話するときに使用される資格情報を指定する `clientCredentialType` 属性があります。</span><span class="sxs-lookup"><span data-stu-id="d61ca-132">This element has a `clientCredentialType` attribute that specifies the credentials to be used when interacting with a service.</span></span> <span data-ttu-id="d61ca-133">この属性は <xref:System.ServiceModel.PeerTransportCredentialType> 型です。</span><span class="sxs-lookup"><span data-stu-id="d61ca-133">This attribute is of type <xref:System.ServiceModel.PeerTransportCredentialType>.</span></span><br /><br /> <span data-ttu-id="d61ca-134">この要素は <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="d61ca-134">This element is of type <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d61ca-135">親要素</span><span class="sxs-lookup"><span data-stu-id="d61ca-135">Parent Elements</span></span>  
  
|<span data-ttu-id="d61ca-136">要素</span><span class="sxs-lookup"><span data-stu-id="d61ca-136">Element</span></span>|<span data-ttu-id="d61ca-137">説明</span><span class="sxs-lookup"><span data-stu-id="d61ca-137">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d61ca-138">\<peerTransport ></span><span class="sxs-lookup"><span data-stu-id="d61ca-138">\<peerTransport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peertransport.md)|<span data-ttu-id="d61ca-139">カスタム バインドのピア トランスポートを定義します。</span><span class="sxs-lookup"><span data-stu-id="d61ca-139">Defines a peer transport for a custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d61ca-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="d61ca-140">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PeerSecurityElement>  
 <xref:System.ServiceModel.PeerSecuritySettings>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="d61ca-141">トランスポート セキュリティ</span><span class="sxs-lookup"><span data-stu-id="d61ca-141">Transport Security</span></span>](../../../../../docs/framework/wcf/feature-details/transport-security.md)  
 [<span data-ttu-id="d61ca-142">トランスポート</span><span class="sxs-lookup"><span data-stu-id="d61ca-142">Transports</span></span>](../../../../../docs/framework/wcf/feature-details/transports.md)  
 [<span data-ttu-id="d61ca-143">トランスポートの選択</span><span class="sxs-lookup"><span data-stu-id="d61ca-143">Choosing a Transport</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)  
 [<span data-ttu-id="d61ca-144">バインディング</span><span class="sxs-lookup"><span data-stu-id="d61ca-144">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="d61ca-145">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="d61ca-145">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="d61ca-146">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="d61ca-146">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="d61ca-147">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="d61ca-147">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
