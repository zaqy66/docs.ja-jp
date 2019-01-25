---
title: '&lt;netPeerTcpBinding&gt; の &lt;transport&gt;'
ms.date: 03/30/2017
ms.assetid: c44d86d2-1160-44d7-9c7a-297b12eccc7f
ms.openlocfilehash: b929c97d0b5d9e021a71e4b88dd3d8a5f2f909a7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54677005"
---
# <a name="lttransportgt-of-ltnetpeertcpbindinggt"></a><span data-ttu-id="ebce7-102">&lt;netPeerTcpBinding&gt; の &lt;transport&gt;</span><span class="sxs-lookup"><span data-stu-id="ebce7-102">&lt;transport&gt; of &lt;netPeerTcpBinding&gt;</span></span>
<span data-ttu-id="ebce7-103">使用する場合は、トランスポート レベルのセキュリティの設定を指定、 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="ebce7-103">Specifies settings for transport level security when using the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>  
  
 <span data-ttu-id="ebce7-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="ebce7-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="ebce7-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="ebce7-105">\<bindings></span></span>  
<span data-ttu-id="ebce7-106">\<netPeerTcpBinding></span><span class="sxs-lookup"><span data-stu-id="ebce7-106">\<netPeerTcpBinding></span></span>  
<span data-ttu-id="ebce7-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="ebce7-107">\<binding></span></span>  
<span data-ttu-id="ebce7-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="ebce7-108">\<security></span></span>  
<span data-ttu-id="ebce7-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="ebce7-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ebce7-110">構文</span><span class="sxs-lookup"><span data-stu-id="ebce7-110">Syntax</span></span>  
  
```xml  
<netPeerTcpBinding>
  <binding>
    <security>
      <transport credentialType="Certificate/Password" />
    </security>
  </binding>
</netPeerTcpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ebce7-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="ebce7-111">Attributes and Elements</span></span>  
 <span data-ttu-id="ebce7-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="ebce7-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ebce7-113">属性</span><span class="sxs-lookup"><span data-stu-id="ebce7-113">Attributes</span></span>  
  
|<span data-ttu-id="ebce7-114">属性</span><span class="sxs-lookup"><span data-stu-id="ebce7-114">Attribute</span></span>|<span data-ttu-id="ebce7-115">説明</span><span class="sxs-lookup"><span data-stu-id="ebce7-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ebce7-116">credentialType</span><span class="sxs-lookup"><span data-stu-id="ebce7-116">credentialType</span></span>|<span data-ttu-id="ebce7-117">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="ebce7-117">Optional.</span></span> <span data-ttu-id="ebce7-118">ピア トランスポートにより送信されるメッセージの検証に使用される資格情報の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="ebce7-118">Specifies the type of credentials used to verify messages sent with the peer transport.</span></span> <span data-ttu-id="ebce7-119">この属性は <xref:System.ServiceModel.PeerTransportCredentialType> 型です。</span><span class="sxs-lookup"><span data-stu-id="ebce7-119">This attribute is of type <xref:System.ServiceModel.PeerTransportCredentialType>.</span></span>|  
  
## <a name="credentialtype-attribute"></a><span data-ttu-id="ebce7-120">credentialType 属性</span><span class="sxs-lookup"><span data-stu-id="ebce7-120">credentialType Attribute</span></span>  
  
|<span data-ttu-id="ebce7-121">値</span><span class="sxs-lookup"><span data-stu-id="ebce7-121">Value</span></span>|<span data-ttu-id="ebce7-122">説明</span><span class="sxs-lookup"><span data-stu-id="ebce7-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="ebce7-123">証明書</span><span class="sxs-lookup"><span data-stu-id="ebce7-123">Certificate</span></span>|<span data-ttu-id="ebce7-124">ピア チャネル トランスポートの認証には X 509 証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="ebce7-124">Authentication of the peer channel transport requires an X509 certificate.</span></span>|  
|<span data-ttu-id="ebce7-125">[Password]</span><span class="sxs-lookup"><span data-stu-id="ebce7-125">Password</span></span>|<span data-ttu-id="ebce7-126">ピア チャネル トランスポートの認証には正しいパスワードが必要です。</span><span class="sxs-lookup"><span data-stu-id="ebce7-126">Authentication of the peer channel transport requires a correct password.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ebce7-127">子要素</span><span class="sxs-lookup"><span data-stu-id="ebce7-127">Child Elements</span></span>  
 <span data-ttu-id="ebce7-128">なし</span><span class="sxs-lookup"><span data-stu-id="ebce7-128">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ebce7-129">親要素</span><span class="sxs-lookup"><span data-stu-id="ebce7-129">Parent Elements</span></span>  
  
|<span data-ttu-id="ebce7-130">要素</span><span class="sxs-lookup"><span data-stu-id="ebce7-130">Element</span></span>|<span data-ttu-id="ebce7-131">説明</span><span class="sxs-lookup"><span data-stu-id="ebce7-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ebce7-132">\<security></span><span class="sxs-lookup"><span data-stu-id="ebce7-132">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netpeerbinding.md)|<span data-ttu-id="ebce7-133">セキュリティ設定を定義、 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="ebce7-133">Defines the security settings for the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ebce7-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="ebce7-134">See also</span></span>
- <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>
- <xref:System.ServiceModel.PeerSecuritySettings.Transport%2A>
- <xref:System.ServiceModel.Configuration.PeerSecurityElement.Transport%2A>
- <xref:System.ServiceModel.PeerTransportSecuritySettings>
- [<span data-ttu-id="ebce7-135">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="ebce7-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="ebce7-136">バインディング</span><span class="sxs-lookup"><span data-stu-id="ebce7-136">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="ebce7-137">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="ebce7-137">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="ebce7-138">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="ebce7-138">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="ebce7-139">\<binding></span><span class="sxs-lookup"><span data-stu-id="ebce7-139">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
