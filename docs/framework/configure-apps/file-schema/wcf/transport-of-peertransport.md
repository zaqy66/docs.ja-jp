---
title: '&lt;peerTransport&gt; の &lt;transport&gt;'
ms.date: 03/30/2017
ms.assetid: d7116240-845c-4b6f-b203-262de6b597ef
ms.openlocfilehash: c82e91543920522f0ed6232036ec1b5a94189fa8
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148944"
---
# <a name="lttransportgt-of-ltpeertransportgt"></a><span data-ttu-id="bdb9c-102">&lt;peerTransport&gt; の &lt;transport&gt;</span><span class="sxs-lookup"><span data-stu-id="bdb9c-102">&lt;transport&gt; of &lt;peerTransport&gt;</span></span>
<span data-ttu-id="bdb9c-103">このバインドで構成されたピアが送信する、セキュリティで保護されたメッセージのトランスポートの型を指定します。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-103">Specifies the transport type for secured messages sent by peers configured with this binding.</span></span>  
  
 <span data-ttu-id="bdb9c-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="bdb9c-104">\<system.serviceModel></span></span>  
<span data-ttu-id="bdb9c-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="bdb9c-105">\<bindings></span></span>  
<span data-ttu-id="bdb9c-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="bdb9c-106">\<customBinding></span></span>  
<span data-ttu-id="bdb9c-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="bdb9c-107">\<binding></span></span>  
<span data-ttu-id="bdb9c-108">\<peerTransport ></span><span class="sxs-lookup"><span data-stu-id="bdb9c-108">\<peerTransport></span></span>  
<span data-ttu-id="bdb9c-109">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="bdb9c-109">\<security></span></span>  
<span data-ttu-id="bdb9c-110">\<transport></span><span class="sxs-lookup"><span data-stu-id="bdb9c-110">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bdb9c-111">構文</span><span class="sxs-lookup"><span data-stu-id="bdb9c-111">Syntax</span></span>  
  
```xml  
<security>
  <transport credentialType="Certificate/Password" />
</security>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bdb9c-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="bdb9c-112">Attributes and Elements</span></span>  
 <span data-ttu-id="bdb9c-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-113">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bdb9c-114">属性</span><span class="sxs-lookup"><span data-stu-id="bdb9c-114">Attributes</span></span>  
  
|<span data-ttu-id="bdb9c-115">属性</span><span class="sxs-lookup"><span data-stu-id="bdb9c-115">Attribute</span></span>|<span data-ttu-id="bdb9c-116">説明</span><span class="sxs-lookup"><span data-stu-id="bdb9c-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="bdb9c-117">credentialType</span><span class="sxs-lookup"><span data-stu-id="bdb9c-117">credentialType</span></span>|<span data-ttu-id="bdb9c-118">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-118">Optional.</span></span> <span data-ttu-id="bdb9c-119">ピア トランスポートにより送信されるメッセージの検証に使用される資格情報の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-119">Specifies the type of credentials used to verify messages sent with the peer transport.</span></span> <span data-ttu-id="bdb9c-120">この属性は <xref:System.ServiceModel.PeerTransportCredentialType> 型です。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-120">This attribute is of type <xref:System.ServiceModel.PeerTransportCredentialType>.</span></span>|  
  
## <a name="credentialtype-attribute"></a><span data-ttu-id="bdb9c-121">credentialType 属性</span><span class="sxs-lookup"><span data-stu-id="bdb9c-121">credentialType Attribute</span></span>  
  
|<span data-ttu-id="bdb9c-122">値</span><span class="sxs-lookup"><span data-stu-id="bdb9c-122">Value</span></span>|<span data-ttu-id="bdb9c-123">説明</span><span class="sxs-lookup"><span data-stu-id="bdb9c-123">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="bdb9c-124">証明書</span><span class="sxs-lookup"><span data-stu-id="bdb9c-124">Certificate</span></span>|<span data-ttu-id="bdb9c-125">ピア チャネル トランスポートの認証には X 509 証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-125">Authentication of the peer channel transport requires an X509 certificate.</span></span>|  
|<span data-ttu-id="bdb9c-126">[Password]</span><span class="sxs-lookup"><span data-stu-id="bdb9c-126">Password</span></span>|<span data-ttu-id="bdb9c-127">ピア チャネル トランスポートの認証には正しいパスワードが必要です。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-127">Authentication of the peer channel transport requires a correct password.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bdb9c-128">子要素</span><span class="sxs-lookup"><span data-stu-id="bdb9c-128">Child Elements</span></span>  
 <span data-ttu-id="bdb9c-129">なし</span><span class="sxs-lookup"><span data-stu-id="bdb9c-129">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="bdb9c-130">親要素</span><span class="sxs-lookup"><span data-stu-id="bdb9c-130">Parent Elements</span></span>  
  
|<span data-ttu-id="bdb9c-131">要素</span><span class="sxs-lookup"><span data-stu-id="bdb9c-131">Element</span></span>|<span data-ttu-id="bdb9c-132">説明</span><span class="sxs-lookup"><span data-stu-id="bdb9c-132">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bdb9c-133">\<security></span><span class="sxs-lookup"><span data-stu-id="bdb9c-133">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-peertransport.md)|<span data-ttu-id="bdb9c-134">ピア トランスポートのセキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-134">Defines the security settings for a peer transport.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bdb9c-135">Remarks</span><span class="sxs-lookup"><span data-stu-id="bdb9c-135">Remarks</span></span>  
 <span data-ttu-id="bdb9c-136">場合にのみこの要素は、設定の mode 属性[\<セキュリティ >](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-peertransport.md)に設定されている`Transport`または`TransportWithMessageCredential`します。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-136">This element is set only if the mode attribute of [\<security>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-peertransport.md) is set to `Transport` or `TransportWithMessageCredential`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bdb9c-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="bdb9c-137">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>  
 <xref:System.ServiceModel.PeerSecuritySettings.Transport%2A>  
 <xref:System.ServiceModel.PeerTransportSecuritySettings>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="bdb9c-138">トランスポート セキュリティ</span><span class="sxs-lookup"><span data-stu-id="bdb9c-138">Transport Security</span></span>](../../../../../docs/framework/wcf/feature-details/transport-security.md)  
 [<span data-ttu-id="bdb9c-139">トランスポート</span><span class="sxs-lookup"><span data-stu-id="bdb9c-139">Transports</span></span>](../../../../../docs/framework/wcf/feature-details/transports.md)  
 [<span data-ttu-id="bdb9c-140">トランスポートの選択</span><span class="sxs-lookup"><span data-stu-id="bdb9c-140">Choosing a Transport</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)  
 [<span data-ttu-id="bdb9c-141">バインディング</span><span class="sxs-lookup"><span data-stu-id="bdb9c-141">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="bdb9c-142">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="bdb9c-142">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="bdb9c-143">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="bdb9c-143">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="bdb9c-144">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="bdb9c-144">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
