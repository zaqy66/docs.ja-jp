---
title: '&lt;netPeerTcpBinding&gt; の &lt;transport&gt;'
ms.date: 03/30/2017
ms.assetid: c44d86d2-1160-44d7-9c7a-297b12eccc7f
ms.openlocfilehash: 2b89ae090d24ff6aad1aae1b39a0a18961bd2537
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/13/2018
ms.locfileid: "45519222"
---
# <a name="lttransportgt-of-ltnetpeertcpbindinggt"></a><span data-ttu-id="f916f-102">&lt;netPeerTcpBinding&gt; の &lt;transport&gt;</span><span class="sxs-lookup"><span data-stu-id="f916f-102">&lt;transport&gt; of &lt;netPeerTcpBinding&gt;</span></span>
<span data-ttu-id="f916f-103">使用する場合は、トランスポート レベルのセキュリティの設定を指定、 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="f916f-103">Specifies settings for transport level security when using the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>  
  
 <span data-ttu-id="f916f-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="f916f-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="f916f-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="f916f-105">\<bindings></span></span>  
<span data-ttu-id="f916f-106">\<netPeerTcpBinding></span><span class="sxs-lookup"><span data-stu-id="f916f-106">\<netPeerTcpBinding></span></span>  
<span data-ttu-id="f916f-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="f916f-107">\<binding></span></span>  
<span data-ttu-id="f916f-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="f916f-108">\<security></span></span>  
<span data-ttu-id="f916f-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="f916f-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f916f-110">構文</span><span class="sxs-lookup"><span data-stu-id="f916f-110">Syntax</span></span>  
  
```xml  
<netPeerTcpBinding>  
    <binding>  
        <security>  
            <transport credentialType="Certificate/Password" />  
        </security>         
    </binding>  
</netPeerTcpBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f916f-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="f916f-111">Attributes and Elements</span></span>  
 <span data-ttu-id="f916f-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="f916f-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f916f-113">属性</span><span class="sxs-lookup"><span data-stu-id="f916f-113">Attributes</span></span>  
  
|<span data-ttu-id="f916f-114">属性</span><span class="sxs-lookup"><span data-stu-id="f916f-114">Attribute</span></span>|<span data-ttu-id="f916f-115">説明</span><span class="sxs-lookup"><span data-stu-id="f916f-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f916f-116">credentialType</span><span class="sxs-lookup"><span data-stu-id="f916f-116">credentialType</span></span>|<span data-ttu-id="f916f-117">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="f916f-117">Optional.</span></span> <span data-ttu-id="f916f-118">ピア トランスポートにより送信されるメッセージの検証に使用される資格情報の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="f916f-118">Specifies the type of credentials used to verify messages sent with the peer transport.</span></span> <span data-ttu-id="f916f-119">この属性は <xref:System.ServiceModel.PeerTransportCredentialType> 型です。</span><span class="sxs-lookup"><span data-stu-id="f916f-119">This attribute is of type <xref:System.ServiceModel.PeerTransportCredentialType>.</span></span>|  
  
## <a name="credentialtype-attribute"></a><span data-ttu-id="f916f-120">credentialType 属性</span><span class="sxs-lookup"><span data-stu-id="f916f-120">credentialType Attribute</span></span>  
  
|<span data-ttu-id="f916f-121">値</span><span class="sxs-lookup"><span data-stu-id="f916f-121">Value</span></span>|<span data-ttu-id="f916f-122">説明</span><span class="sxs-lookup"><span data-stu-id="f916f-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="f916f-123">証明書</span><span class="sxs-lookup"><span data-stu-id="f916f-123">Certificate</span></span>|<span data-ttu-id="f916f-124">ピア チャネル トランスポートの認証には X 509 証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="f916f-124">Authentication of the peer channel transport requires an X509 certificate.</span></span>|  
|<span data-ttu-id="f916f-125">[Password]</span><span class="sxs-lookup"><span data-stu-id="f916f-125">Password</span></span>|<span data-ttu-id="f916f-126">ピア チャネル トランスポートの認証には正しいパスワードが必要です。</span><span class="sxs-lookup"><span data-stu-id="f916f-126">Authentication of the peer channel transport requires a correct password.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f916f-127">子要素</span><span class="sxs-lookup"><span data-stu-id="f916f-127">Child Elements</span></span>  
 <span data-ttu-id="f916f-128">なし</span><span class="sxs-lookup"><span data-stu-id="f916f-128">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f916f-129">親要素</span><span class="sxs-lookup"><span data-stu-id="f916f-129">Parent Elements</span></span>  
  
|<span data-ttu-id="f916f-130">要素</span><span class="sxs-lookup"><span data-stu-id="f916f-130">Element</span></span>|<span data-ttu-id="f916f-131">説明</span><span class="sxs-lookup"><span data-stu-id="f916f-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f916f-132">\<security></span><span class="sxs-lookup"><span data-stu-id="f916f-132">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netpeerbinding.md)|<span data-ttu-id="f916f-133">セキュリティ設定を定義、 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="f916f-133">Defines the security settings for the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f916f-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="f916f-134">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>  
 <xref:System.ServiceModel.PeerSecuritySettings.Transport%2A>  
 <xref:System.ServiceModel.Configuration.PeerSecurityElement.Transport%2A>  
 <xref:System.ServiceModel.PeerTransportSecuritySettings>  
 [<span data-ttu-id="f916f-135">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="f916f-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="f916f-136">バインディング</span><span class="sxs-lookup"><span data-stu-id="f916f-136">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="f916f-137">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="f916f-137">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="f916f-138">バインドを使用して、Windows Communication Foundation サービスとクライアントを構成するには</span><span class="sxs-lookup"><span data-stu-id="f916f-138">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="f916f-139">\<binding></span><span class="sxs-lookup"><span data-stu-id="f916f-139">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
