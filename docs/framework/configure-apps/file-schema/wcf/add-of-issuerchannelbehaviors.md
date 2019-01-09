---
title: '&lt;issuerChannelBehaviors&gt; の &lt;add&gt;'
ms.date: 03/30/2017
ms.assetid: 50710506-e28f-45dd-ab7e-bff6f44173db
ms.openlocfilehash: 072e3f4e961f6bf45e7c8b48c64cda36d385cf2b
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149541"
---
# <a name="ltaddgt-of-ltissuerchannelbehaviorsgt"></a><span data-ttu-id="61e77-102">&lt;issuerChannelBehaviors&gt; の &lt;add&gt;</span><span class="sxs-lookup"><span data-stu-id="61e77-102">&lt;add&gt; of &lt;issuerChannelBehaviors&gt;</span></span>
<span data-ttu-id="61e77-103">STS と通信するときに使用されるエンドポイントの動作を追加します。</span><span class="sxs-lookup"><span data-stu-id="61e77-103">Adds an endpoint behavior to be used when communicating with an STS.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="61e77-104">エンドポイントの動作が含まれている場合、 [ \<clientCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)要素、例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="61e77-104">If any endpoint behavior contains a [\<clientCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) element, an exception will be thrown.</span></span>  
  
 <span data-ttu-id="61e77-105">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="61e77-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="61e77-106">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="61e77-106">\<behaviors></span></span>  
<span data-ttu-id="61e77-107">endpointBehaviors セクション</span><span class="sxs-lookup"><span data-stu-id="61e77-107">endpointBehaviors section</span></span>  
<span data-ttu-id="61e77-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="61e77-108">\<behavior></span></span>  
<span data-ttu-id="61e77-109">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="61e77-109">\<clientCredentials></span></span>  
<span data-ttu-id="61e77-110">\<issuedToken ></span><span class="sxs-lookup"><span data-stu-id="61e77-110">\<issuedToken></span></span>  
<span data-ttu-id="61e77-111">\<issuerChannelBehaviors > 要素</span><span class="sxs-lookup"><span data-stu-id="61e77-111">\<issuerChannelBehaviors> Element</span></span>  
<span data-ttu-id="61e77-112">\<add></span><span class="sxs-lookup"><span data-stu-id="61e77-112">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61e77-113">構文</span><span class="sxs-lookup"><span data-stu-id="61e77-113">Syntax</span></span>  
  
```xml  
<add issuerAddress="string"
     behaviorConfiguraton="string" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="61e77-114">属性および要素</span><span class="sxs-lookup"><span data-stu-id="61e77-114">Attributes and Elements</span></span>  
 <span data-ttu-id="61e77-115">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="61e77-115">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="61e77-116">属性</span><span class="sxs-lookup"><span data-stu-id="61e77-116">Attributes</span></span>  
  
|<span data-ttu-id="61e77-117">属性</span><span class="sxs-lookup"><span data-stu-id="61e77-117">Attribute</span></span>|<span data-ttu-id="61e77-118">説明</span><span class="sxs-lookup"><span data-stu-id="61e77-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="61e77-119">issuerAddress</span><span class="sxs-lookup"><span data-stu-id="61e77-119">issuerAddress</span></span>|<span data-ttu-id="61e77-120">通信するためのセキュリティ トークン発行者の URI。</span><span class="sxs-lookup"><span data-stu-id="61e77-120">The URI of the security token issuer to communicate with.</span></span>|  
|<span data-ttu-id="61e77-121">behaviorConfiguration</span><span class="sxs-lookup"><span data-stu-id="61e77-121">behaviorConfiguration</span></span>|<span data-ttu-id="61e77-122">同じ構成ファイルに定義されたエンドポイントの動作の名前。</span><span class="sxs-lookup"><span data-stu-id="61e77-122">The name of an endpoint behavior defined in the same configuration file.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="61e77-123">子要素</span><span class="sxs-lookup"><span data-stu-id="61e77-123">Child Elements</span></span>  
 <span data-ttu-id="61e77-124">なし。</span><span class="sxs-lookup"><span data-stu-id="61e77-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="61e77-125">親要素</span><span class="sxs-lookup"><span data-stu-id="61e77-125">Parent Elements</span></span>  
  
|<span data-ttu-id="61e77-126">要素</span><span class="sxs-lookup"><span data-stu-id="61e77-126">Element</span></span>|<span data-ttu-id="61e77-127">説明</span><span class="sxs-lookup"><span data-stu-id="61e77-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="61e77-128">\<issuerChannelBehaviors ></span><span class="sxs-lookup"><span data-stu-id="61e77-128">\<issuerChannelBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuerchannelbehaviors-element.md)|<span data-ttu-id="61e77-129">指定されたサービス トークン サービスと通信するときに使用する Windows Communication Foundation (WCF) クライアント エンドポイントの動作のコレクションを含みます。</span><span class="sxs-lookup"><span data-stu-id="61e77-129">Contains a collection of Windows Communication Foundation (WCF) client endpoint behaviors to be used when communicating with the specified Service Token Services.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="61e77-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="61e77-130">Remarks</span></span>  
 <span data-ttu-id="61e77-131">`issuerAddress` には、クライアントの通信相手となるセキュリティ トークン サービスの URI が含まれます。</span><span class="sxs-lookup"><span data-stu-id="61e77-131">`issuerAddress` contains the URI of the Security Token Service that the client wants to communicate with.</span></span> <span data-ttu-id="61e77-132">`behaviorConfiguration` アプリケーションがセキュリティ トークン サービスから発行されたトークンを取得する Windows Communication Foundation (WCF) によって作成されたチャネルで使用するエンドポイントの動作を指します。</span><span class="sxs-lookup"><span data-stu-id="61e77-132">`behaviorConfiguration` points to an endpoint behavior that the application uses in the channels created by Windows Communication Foundation (WCF) to get the issued tokens from the Security Token Services.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61e77-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="61e77-133">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.IssuerChannelBehaviors%2A>  
 <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElement>  
 <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElementCollection>  
 <xref:System.ServiceModel.Security.IssuedTokenClientCredential.IssuerChannelBehaviors%2A>  
 [<span data-ttu-id="61e77-134">サービス ID と認証</span><span class="sxs-lookup"><span data-stu-id="61e77-134">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="61e77-135">セキュリティ動作</span><span class="sxs-lookup"><span data-stu-id="61e77-135">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)  
 [<span data-ttu-id="61e77-136">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="61e77-136">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="61e77-137">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="61e77-137">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="61e77-138">クライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="61e77-138">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)  
 [<span data-ttu-id="61e77-139">方法: フェデレーション クライアントを作成します。</span><span class="sxs-lookup"><span data-stu-id="61e77-139">How to: Create a Federated Client</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)  
 [<span data-ttu-id="61e77-140">方法: ローカル発行者を構成します。</span><span class="sxs-lookup"><span data-stu-id="61e77-140">How to: Configure a Local Issuer</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)  
 [<span data-ttu-id="61e77-141">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="61e77-141">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="61e77-142">\<issuerChannelBehaviors ></span><span class="sxs-lookup"><span data-stu-id="61e77-142">\<issuerChannelBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuerchannelbehaviors-element.md)
