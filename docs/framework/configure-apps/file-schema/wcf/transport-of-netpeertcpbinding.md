---
title: <transport> の <netPeerTcpBinding>
ms.date: 03/30/2017
ms.assetid: c44d86d2-1160-44d7-9c7a-297b12eccc7f
ms.openlocfilehash: f5feca232265cbcad7feff78c0c66e3606c8567e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55270373"
---
# <a name="transport-of-netpeertcpbinding"></a><span data-ttu-id="95eb0-102">\<トランスポート > の\<netPeerTcpBinding ></span><span class="sxs-lookup"><span data-stu-id="95eb0-102">\<transport> of \<netPeerTcpBinding></span></span>
<span data-ttu-id="95eb0-103">使用する場合は、トランスポート レベルのセキュリティの設定を指定、 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="95eb0-103">Specifies settings for transport level security when using the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>  
  
 <span data-ttu-id="95eb0-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="95eb0-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="95eb0-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="95eb0-105">\<bindings></span></span>  
<span data-ttu-id="95eb0-106">\<netPeerTcpBinding></span><span class="sxs-lookup"><span data-stu-id="95eb0-106">\<netPeerTcpBinding></span></span>  
<span data-ttu-id="95eb0-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="95eb0-107">\<binding></span></span>  
<span data-ttu-id="95eb0-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="95eb0-108">\<security></span></span>  
<span data-ttu-id="95eb0-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="95eb0-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="95eb0-110">構文</span><span class="sxs-lookup"><span data-stu-id="95eb0-110">Syntax</span></span>  
  
```xml  
<netPeerTcpBinding>
  <binding>
    <security>
      <transport credentialType="Certificate/Password" />
    </security>
  </binding>
</netPeerTcpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="95eb0-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="95eb0-111">Attributes and Elements</span></span>  
 <span data-ttu-id="95eb0-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="95eb0-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="95eb0-113">属性</span><span class="sxs-lookup"><span data-stu-id="95eb0-113">Attributes</span></span>  
  
|<span data-ttu-id="95eb0-114">属性</span><span class="sxs-lookup"><span data-stu-id="95eb0-114">Attribute</span></span>|<span data-ttu-id="95eb0-115">説明</span><span class="sxs-lookup"><span data-stu-id="95eb0-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="95eb0-116">credentialType</span><span class="sxs-lookup"><span data-stu-id="95eb0-116">credentialType</span></span>|<span data-ttu-id="95eb0-117">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="95eb0-117">Optional.</span></span> <span data-ttu-id="95eb0-118">ピア トランスポートにより送信されるメッセージの検証に使用される資格情報の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="95eb0-118">Specifies the type of credentials used to verify messages sent with the peer transport.</span></span> <span data-ttu-id="95eb0-119">この属性は <xref:System.ServiceModel.PeerTransportCredentialType> 型です。</span><span class="sxs-lookup"><span data-stu-id="95eb0-119">This attribute is of type <xref:System.ServiceModel.PeerTransportCredentialType>.</span></span>|  
  
## <a name="credentialtype-attribute"></a><span data-ttu-id="95eb0-120">credentialType 属性</span><span class="sxs-lookup"><span data-stu-id="95eb0-120">credentialType Attribute</span></span>  
  
|<span data-ttu-id="95eb0-121">値</span><span class="sxs-lookup"><span data-stu-id="95eb0-121">Value</span></span>|<span data-ttu-id="95eb0-122">説明</span><span class="sxs-lookup"><span data-stu-id="95eb0-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="95eb0-123">証明書</span><span class="sxs-lookup"><span data-stu-id="95eb0-123">Certificate</span></span>|<span data-ttu-id="95eb0-124">ピア チャネル トランスポートの認証には X 509 証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="95eb0-124">Authentication of the peer channel transport requires an X509 certificate.</span></span>|  
|<span data-ttu-id="95eb0-125">[Password]</span><span class="sxs-lookup"><span data-stu-id="95eb0-125">Password</span></span>|<span data-ttu-id="95eb0-126">ピア チャネル トランスポートの認証には正しいパスワードが必要です。</span><span class="sxs-lookup"><span data-stu-id="95eb0-126">Authentication of the peer channel transport requires a correct password.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="95eb0-127">子要素</span><span class="sxs-lookup"><span data-stu-id="95eb0-127">Child Elements</span></span>  
 <span data-ttu-id="95eb0-128">なし</span><span class="sxs-lookup"><span data-stu-id="95eb0-128">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="95eb0-129">親要素</span><span class="sxs-lookup"><span data-stu-id="95eb0-129">Parent Elements</span></span>  
  
|<span data-ttu-id="95eb0-130">要素</span><span class="sxs-lookup"><span data-stu-id="95eb0-130">Element</span></span>|<span data-ttu-id="95eb0-131">説明</span><span class="sxs-lookup"><span data-stu-id="95eb0-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="95eb0-132">\<security></span><span class="sxs-lookup"><span data-stu-id="95eb0-132">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netpeerbinding.md)|<span data-ttu-id="95eb0-133">セキュリティ設定を定義、 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="95eb0-133">Defines the security settings for the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="95eb0-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="95eb0-134">See also</span></span>
- <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>
- <xref:System.ServiceModel.PeerSecuritySettings.Transport%2A>
- <xref:System.ServiceModel.Configuration.PeerSecurityElement.Transport%2A>
- <xref:System.ServiceModel.PeerTransportSecuritySettings>
- [<span data-ttu-id="95eb0-135">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="95eb0-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="95eb0-136">バインディング</span><span class="sxs-lookup"><span data-stu-id="95eb0-136">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="95eb0-137">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="95eb0-137">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="95eb0-138">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="95eb0-138">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="95eb0-139">\<binding></span><span class="sxs-lookup"><span data-stu-id="95eb0-139">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
