---
title: '&lt;serviceCredentials&gt; の &lt;peer&gt;'
ms.date: 03/30/2017
ms.assetid: b134e21d-e5b5-458e-9309-626dbf8db4ed
ms.openlocfilehash: 94f93a7955af3bff1c17e59a11af3fad85c9134d
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43399844"
---
# <a name="ltpeergt-of-ltservicecredentialsgt"></a><span data-ttu-id="a502b-102">&lt;serviceCredentials&gt; の &lt;peer&gt;</span><span class="sxs-lookup"><span data-stu-id="a502b-102">&lt;peer&gt; of &lt;serviceCredentials&gt;</span></span>
<span data-ttu-id="a502b-103">ピア ノードの現在の資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="a502b-103">Specifies the current credentials for a peer node.</span></span>  
  
 <span data-ttu-id="a502b-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="a502b-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="a502b-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="a502b-105">\<behaviors></span></span>  
<span data-ttu-id="a502b-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="a502b-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="a502b-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="a502b-107">\<behavior></span></span>  
<span data-ttu-id="a502b-108">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="a502b-108">\<serviceCredentials></span></span>  
<span data-ttu-id="a502b-109">\<ピア ></span><span class="sxs-lookup"><span data-stu-id="a502b-109">\<peer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a502b-110">構文</span><span class="sxs-lookup"><span data-stu-id="a502b-110">Syntax</span></span>  
  
```xml  
<peer>  
  <certificate/>  
  <peerAuthentication/>  
  <messageSenderAuthentication/>  
</peer>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a502b-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="a502b-111">Attributes and Elements</span></span>  
 <span data-ttu-id="a502b-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="a502b-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a502b-113">属性</span><span class="sxs-lookup"><span data-stu-id="a502b-113">Attributes</span></span>  
 <span data-ttu-id="a502b-114">なし。</span><span class="sxs-lookup"><span data-stu-id="a502b-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="a502b-115">子要素</span><span class="sxs-lookup"><span data-stu-id="a502b-115">Child Elements</span></span>  
  
|<span data-ttu-id="a502b-116">要素</span><span class="sxs-lookup"><span data-stu-id="a502b-116">Element</span></span>|<span data-ttu-id="a502b-117">説明</span><span class="sxs-lookup"><span data-stu-id="a502b-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a502b-118">\<certificate></span><span class="sxs-lookup"><span data-stu-id="a502b-118">\<certificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-of-peer.md)|<span data-ttu-id="a502b-119">ピアツーピア サービスのメッセージの署名と暗号化に使用する X.509 証明書を指定します。</span><span class="sxs-lookup"><span data-stu-id="a502b-119">Specifies an X.509 certificate to use for signing and encrypting messages for peer-to-peer services.</span></span> <span data-ttu-id="a502b-120">.</span><span class="sxs-lookup"><span data-stu-id="a502b-120">.</span></span>|  
|[<span data-ttu-id="a502b-121">\<messageSenderAuthentication></span><span class="sxs-lookup"><span data-stu-id="a502b-121">\<messageSenderAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/messagesenderauthentication.md)|<span data-ttu-id="a502b-122">メッセージ送信者の認証オプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="a502b-122">Specifies authentication options for message senders.</span></span>|  
|[<span data-ttu-id="a502b-123">\<peerAuthentication></span><span class="sxs-lookup"><span data-stu-id="a502b-123">\<peerAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peerauthentication.md)|<span data-ttu-id="a502b-124">ピア サービスの認証オプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="a502b-124">Specifies authentication options for peer services.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a502b-125">親要素</span><span class="sxs-lookup"><span data-stu-id="a502b-125">Parent Elements</span></span>  
  
|<span data-ttu-id="a502b-126">要素</span><span class="sxs-lookup"><span data-stu-id="a502b-126">Element</span></span>|<span data-ttu-id="a502b-127">説明</span><span class="sxs-lookup"><span data-stu-id="a502b-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a502b-128">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="a502b-128">\<serviceCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md)|<span data-ttu-id="a502b-129">サービスの認証に使用される資格情報と、クライアントの資格情報検証関連の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="a502b-129">Specifies the credential to be used in authenticating the service, and the client credential validation-related settings.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a502b-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="a502b-130">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PeerCredentialElement>  
 <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.Peer%2A>  
 <xref:System.ServiceModel.Description.ServiceCredentials.Peer%2A>  
 <xref:System.ServiceModel.Security.PeerCredential>  
 [<span data-ttu-id="a502b-131">ピアツーピア ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a502b-131">Peer-to-Peer Networking</span></span>](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)  
 [<span data-ttu-id="a502b-132">ピア チャネル メッセージの認証</span><span class="sxs-lookup"><span data-stu-id="a502b-132">Peer Channel Message Authentication</span></span>](https://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95)  
 [<span data-ttu-id="a502b-133">ピア チャネル カスタム認証</span><span class="sxs-lookup"><span data-stu-id="a502b-133">Peer Channel Custom Authentication</span></span>](https://msdn.microsoft.com/library/4aa8a82e-41a8-48e2-8621-7e1cbabdca7c)  
 [<span data-ttu-id="a502b-134">セキュリティによるピア チャネル アプリケーションの保護</span><span class="sxs-lookup"><span data-stu-id="a502b-134">Securing Peer Channel Applications</span></span>](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)  
 [<span data-ttu-id="a502b-135">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="a502b-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
