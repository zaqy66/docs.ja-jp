---
title: '&lt;netPeerTcpBinding&gt; の &lt;transport&gt;'
ms.date: 03/30/2017
ms.assetid: c44d86d2-1160-44d7-9c7a-297b12eccc7f
ms.openlocfilehash: 62ba3b27b10afe182623f3be0f6738940e194579
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "48579791"
---
# <a name="lttransportgt-of-ltnetpeertcpbindinggt"></a><span data-ttu-id="b7ec8-102">&lt;netPeerTcpBinding&gt; の &lt;transport&gt;</span><span class="sxs-lookup"><span data-stu-id="b7ec8-102">&lt;transport&gt; of &lt;netPeerTcpBinding&gt;</span></span>
<span data-ttu-id="b7ec8-103">使用する場合は、トランスポート レベルのセキュリティの設定を指定、 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="b7ec8-103">Specifies settings for transport level security when using the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>  
  
 <span data-ttu-id="b7ec8-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="b7ec8-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="b7ec8-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="b7ec8-105">\<bindings></span></span>  
<span data-ttu-id="b7ec8-106">\<netPeerTcpBinding></span><span class="sxs-lookup"><span data-stu-id="b7ec8-106">\<netPeerTcpBinding></span></span>  
<span data-ttu-id="b7ec8-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="b7ec8-107">\<binding></span></span>  
<span data-ttu-id="b7ec8-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="b7ec8-108">\<security></span></span>  
<span data-ttu-id="b7ec8-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="b7ec8-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7ec8-110">構文</span><span class="sxs-lookup"><span data-stu-id="b7ec8-110">Syntax</span></span>  
  
```xml  
<netPeerTcpBinding>  
    <binding>  
        <security>  
            <transport credentialType="Certificate/Password" />  
        </security>         
    </binding>  
</netPeerTcpBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b7ec8-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="b7ec8-111">Attributes and Elements</span></span>  
 <span data-ttu-id="b7ec8-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="b7ec8-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b7ec8-113">属性</span><span class="sxs-lookup"><span data-stu-id="b7ec8-113">Attributes</span></span>  
  
|<span data-ttu-id="b7ec8-114">属性</span><span class="sxs-lookup"><span data-stu-id="b7ec8-114">Attribute</span></span>|<span data-ttu-id="b7ec8-115">説明</span><span class="sxs-lookup"><span data-stu-id="b7ec8-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b7ec8-116">credentialType</span><span class="sxs-lookup"><span data-stu-id="b7ec8-116">credentialType</span></span>|<span data-ttu-id="b7ec8-117">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="b7ec8-117">Optional.</span></span> <span data-ttu-id="b7ec8-118">ピア トランスポートにより送信されるメッセージの検証に使用される資格情報の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="b7ec8-118">Specifies the type of credentials used to verify messages sent with the peer transport.</span></span> <span data-ttu-id="b7ec8-119">この属性は <xref:System.ServiceModel.PeerTransportCredentialType> 型です。</span><span class="sxs-lookup"><span data-stu-id="b7ec8-119">This attribute is of type <xref:System.ServiceModel.PeerTransportCredentialType>.</span></span>|  
  
## <a name="credentialtype-attribute"></a><span data-ttu-id="b7ec8-120">credentialType 属性</span><span class="sxs-lookup"><span data-stu-id="b7ec8-120">credentialType Attribute</span></span>  
  
|<span data-ttu-id="b7ec8-121">値</span><span class="sxs-lookup"><span data-stu-id="b7ec8-121">Value</span></span>|<span data-ttu-id="b7ec8-122">説明</span><span class="sxs-lookup"><span data-stu-id="b7ec8-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="b7ec8-123">証明書</span><span class="sxs-lookup"><span data-stu-id="b7ec8-123">Certificate</span></span>|<span data-ttu-id="b7ec8-124">ピア チャネル トランスポートの認証には X 509 証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="b7ec8-124">Authentication of the peer channel transport requires an X509 certificate.</span></span>|  
|<span data-ttu-id="b7ec8-125">[Password]</span><span class="sxs-lookup"><span data-stu-id="b7ec8-125">Password</span></span>|<span data-ttu-id="b7ec8-126">ピア チャネル トランスポートの認証には正しいパスワードが必要です。</span><span class="sxs-lookup"><span data-stu-id="b7ec8-126">Authentication of the peer channel transport requires a correct password.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b7ec8-127">子要素</span><span class="sxs-lookup"><span data-stu-id="b7ec8-127">Child Elements</span></span>  
 <span data-ttu-id="b7ec8-128">なし</span><span class="sxs-lookup"><span data-stu-id="b7ec8-128">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b7ec8-129">親要素</span><span class="sxs-lookup"><span data-stu-id="b7ec8-129">Parent Elements</span></span>  
  
|<span data-ttu-id="b7ec8-130">要素</span><span class="sxs-lookup"><span data-stu-id="b7ec8-130">Element</span></span>|<span data-ttu-id="b7ec8-131">説明</span><span class="sxs-lookup"><span data-stu-id="b7ec8-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b7ec8-132">\<security></span><span class="sxs-lookup"><span data-stu-id="b7ec8-132">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netpeerbinding.md)|<span data-ttu-id="b7ec8-133">セキュリティ設定を定義、 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="b7ec8-133">Defines the security settings for the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b7ec8-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7ec8-134">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>  
 <xref:System.ServiceModel.PeerSecuritySettings.Transport%2A>  
 <xref:System.ServiceModel.Configuration.PeerSecurityElement.Transport%2A>  
 <xref:System.ServiceModel.PeerTransportSecuritySettings>  
 [<span data-ttu-id="b7ec8-135">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="b7ec8-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="b7ec8-136">バインディング</span><span class="sxs-lookup"><span data-stu-id="b7ec8-136">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="b7ec8-137">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="b7ec8-137">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="b7ec8-138">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="b7ec8-138">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="b7ec8-139">\<binding></span><span class="sxs-lookup"><span data-stu-id="b7ec8-139">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
