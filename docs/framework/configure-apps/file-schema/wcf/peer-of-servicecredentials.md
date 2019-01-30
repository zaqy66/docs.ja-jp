---
title: <peer> の <serviceCredentials>
ms.date: 03/30/2017
ms.assetid: b134e21d-e5b5-458e-9309-626dbf8db4ed
ms.openlocfilehash: 2090e79e6affe8ade6e2e52b94d2c4e1dafe8fa1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55266027"
---
# <a name="peer-of-servicecredentials"></a><span data-ttu-id="95123-102">\<ピア > の\<serviceCredentials ></span><span class="sxs-lookup"><span data-stu-id="95123-102">\<peer> of \<serviceCredentials></span></span>
<span data-ttu-id="95123-103">ピア ノードの現在の資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="95123-103">Specifies the current credentials for a peer node.</span></span>  
  
 <span data-ttu-id="95123-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="95123-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="95123-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="95123-105">\<behaviors></span></span>  
<span data-ttu-id="95123-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="95123-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="95123-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="95123-107">\<behavior></span></span>  
<span data-ttu-id="95123-108">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="95123-108">\<serviceCredentials></span></span>  
<span data-ttu-id="95123-109">\<ピア ></span><span class="sxs-lookup"><span data-stu-id="95123-109">\<peer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="95123-110">構文</span><span class="sxs-lookup"><span data-stu-id="95123-110">Syntax</span></span>  
  
```xml  
<peer>
  <certificate />
  <peerAuthentication />
  <messageSenderAuthentication />
</peer>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="95123-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="95123-111">Attributes and Elements</span></span>  
 <span data-ttu-id="95123-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="95123-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="95123-113">属性</span><span class="sxs-lookup"><span data-stu-id="95123-113">Attributes</span></span>  
 <span data-ttu-id="95123-114">なし。</span><span class="sxs-lookup"><span data-stu-id="95123-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="95123-115">子要素</span><span class="sxs-lookup"><span data-stu-id="95123-115">Child Elements</span></span>  
  
|<span data-ttu-id="95123-116">要素</span><span class="sxs-lookup"><span data-stu-id="95123-116">Element</span></span>|<span data-ttu-id="95123-117">説明</span><span class="sxs-lookup"><span data-stu-id="95123-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="95123-118">\<certificate></span><span class="sxs-lookup"><span data-stu-id="95123-118">\<certificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-of-peer.md)|<span data-ttu-id="95123-119">ピアツーピア サービスのメッセージの署名と暗号化に使用する X.509 証明書を指定します。</span><span class="sxs-lookup"><span data-stu-id="95123-119">Specifies an X.509 certificate to use for signing and encrypting messages for peer-to-peer services.</span></span> <span data-ttu-id="95123-120">.</span><span class="sxs-lookup"><span data-stu-id="95123-120">.</span></span>|  
|[<span data-ttu-id="95123-121">\<messageSenderAuthentication></span><span class="sxs-lookup"><span data-stu-id="95123-121">\<messageSenderAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/messagesenderauthentication.md)|<span data-ttu-id="95123-122">メッセージ送信者の認証オプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="95123-122">Specifies authentication options for message senders.</span></span>|  
|[<span data-ttu-id="95123-123">\<peerAuthentication></span><span class="sxs-lookup"><span data-stu-id="95123-123">\<peerAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peerauthentication.md)|<span data-ttu-id="95123-124">ピア サービスの認証オプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="95123-124">Specifies authentication options for peer services.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="95123-125">親要素</span><span class="sxs-lookup"><span data-stu-id="95123-125">Parent Elements</span></span>  
  
|<span data-ttu-id="95123-126">要素</span><span class="sxs-lookup"><span data-stu-id="95123-126">Element</span></span>|<span data-ttu-id="95123-127">説明</span><span class="sxs-lookup"><span data-stu-id="95123-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="95123-128">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="95123-128">\<serviceCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md)|<span data-ttu-id="95123-129">サービスの認証に使用される資格情報と、クライアントの資格情報検証関連の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="95123-129">Specifies the credential to be used in authenticating the service, and the client credential validation-related settings.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="95123-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="95123-130">See also</span></span>
- <xref:System.ServiceModel.Configuration.PeerCredentialElement>
- <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.Peer%2A>
- <xref:System.ServiceModel.Description.ServiceCredentials.Peer%2A>
- <xref:System.ServiceModel.Security.PeerCredential>
- [<span data-ttu-id="95123-131">ピアツーピア ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95123-131">Peer-to-Peer Networking</span></span>](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)
- [<span data-ttu-id="95123-132">ピア チャネル メッセージの認証</span><span class="sxs-lookup"><span data-stu-id="95123-132">Peer Channel Message Authentication</span></span>](https://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95)
- [<span data-ttu-id="95123-133">ピア チャネル カスタム認証</span><span class="sxs-lookup"><span data-stu-id="95123-133">Peer Channel Custom Authentication</span></span>](https://msdn.microsoft.com/library/4aa8a82e-41a8-48e2-8621-7e1cbabdca7c)
- [<span data-ttu-id="95123-134">セキュリティによるピア チャネル アプリケーションの保護</span><span class="sxs-lookup"><span data-stu-id="95123-134">Securing Peer Channel Applications</span></span>](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
- [<span data-ttu-id="95123-135">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="95123-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
