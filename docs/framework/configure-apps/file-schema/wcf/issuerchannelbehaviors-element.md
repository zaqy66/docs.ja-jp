---
title: '&lt;issuerChannelBehaviors&gt; 要素'
ms.date: 03/30/2017
ms.assetid: f7378673-8e9b-45b2-98d1-cf5dccdd8c40
ms.openlocfilehash: b77d0ce79557dff4b5a243da4d24703ed45fde07
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54677109"
---
# <a name="ltissuerchannelbehaviorsgt-element"></a><span data-ttu-id="8032f-102">&lt;issuerChannelBehaviors&gt; 要素</span><span class="sxs-lookup"><span data-stu-id="8032f-102">&lt;issuerChannelBehaviors&gt; Element</span></span>
<span data-ttu-id="8032f-103">指定されたサービス トークン サービスと通信するときに使用するには、Windows Communication Foundation (WCF) クライアント エンドポイントの動作 (構成で定義されている) のコレクションを含みます。</span><span class="sxs-lookup"><span data-stu-id="8032f-103">Contains a collection of Windows Communication Foundation (WCF) client endpoint behaviors (defined in the configuration) to be used when communicating with the specified Service Token Services.</span></span> <span data-ttu-id="8032f-104">定義された動作は、いずれかを含めることはできません[ \<clientCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)要素。</span><span class="sxs-lookup"><span data-stu-id="8032f-104">The defined behaviors cannot include any [\<clientCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) elements.</span></span>  
  
 <span data-ttu-id="8032f-105">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="8032f-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="8032f-106">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="8032f-106">\<behaviors></span></span>  
<span data-ttu-id="8032f-107">endpointBehaviors セクション</span><span class="sxs-lookup"><span data-stu-id="8032f-107">endpointBehaviors section</span></span>  
<span data-ttu-id="8032f-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="8032f-108">\<behavior></span></span>  
<span data-ttu-id="8032f-109">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="8032f-109">\<clientCredentials></span></span>  
<span data-ttu-id="8032f-110">\<issuedToken ></span><span class="sxs-lookup"><span data-stu-id="8032f-110">\<issuedToken></span></span>  
<span data-ttu-id="8032f-111">\<issuerChannelBehaviors></span><span class="sxs-lookup"><span data-stu-id="8032f-111">\<issuerChannelBehaviors></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8032f-112">構文</span><span class="sxs-lookup"><span data-stu-id="8032f-112">Syntax</span></span>  
  
```xml  
<issuerChannelBehaviors>
  <add behaviorConfiguraton="string"
       issuerAddress="string" />
</issuerChannelBehaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8032f-113">属性および要素</span><span class="sxs-lookup"><span data-stu-id="8032f-113">Attributes and Elements</span></span>  
 <span data-ttu-id="8032f-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="8032f-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8032f-115">属性</span><span class="sxs-lookup"><span data-stu-id="8032f-115">Attributes</span></span>  
 <span data-ttu-id="8032f-116">なし。</span><span class="sxs-lookup"><span data-stu-id="8032f-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="8032f-117">子要素</span><span class="sxs-lookup"><span data-stu-id="8032f-117">Child Elements</span></span>  
  
|<span data-ttu-id="8032f-118">要素</span><span class="sxs-lookup"><span data-stu-id="8032f-118">Element</span></span>|<span data-ttu-id="8032f-119">説明</span><span class="sxs-lookup"><span data-stu-id="8032f-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8032f-120">\<add></span><span class="sxs-lookup"><span data-stu-id="8032f-120">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-issuerchannelbehaviors.md)|<span data-ttu-id="8032f-121">コレクションに動作を追加します。</span><span class="sxs-lookup"><span data-stu-id="8032f-121">Adds a behavior to the collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="8032f-122">親要素</span><span class="sxs-lookup"><span data-stu-id="8032f-122">Parent Elements</span></span>  
  
|<span data-ttu-id="8032f-123">要素</span><span class="sxs-lookup"><span data-stu-id="8032f-123">Element</span></span>|<span data-ttu-id="8032f-124">説明</span><span class="sxs-lookup"><span data-stu-id="8032f-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8032f-125">\<issuedToken ></span><span class="sxs-lookup"><span data-stu-id="8032f-125">\<issuedToken></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtoken.md)|<span data-ttu-id="8032f-126">サービスに対するクライアントの認証に使用されるカスタム トークンを指定します。</span><span class="sxs-lookup"><span data-stu-id="8032f-126">Specifies a custom token used to authenticate a client to a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8032f-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="8032f-127">Remarks</span></span>  
 <span data-ttu-id="8032f-128">この要素を使用するのは、なんらかの動作 (`<clientCredentials>` 要素を含む動作以外) を使用してサービスと通信する必要がある場合です。</span><span class="sxs-lookup"><span data-stu-id="8032f-128">Use this element when any behaviors (other than behaviors that include `<clientCredentials>` elements) must be used to communicate with a service.</span></span> <span data-ttu-id="8032f-129">たとえば場合、 [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)動作要素を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="8032f-129">For example, if a [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) behavior element must be included.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8032f-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="8032f-130">See also</span></span>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.IssuerChannelBehaviors%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElement>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElementCollection>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential.IssuerChannelBehaviors%2A>
- [<span data-ttu-id="8032f-131">サービス ID と認証</span><span class="sxs-lookup"><span data-stu-id="8032f-131">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="8032f-132">セキュリティ動作</span><span class="sxs-lookup"><span data-stu-id="8032f-132">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="8032f-133">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="8032f-133">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="8032f-134">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="8032f-134">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="8032f-135">クライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="8032f-135">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
- [<span data-ttu-id="8032f-136">方法: フェデレーション クライアントを作成します。</span><span class="sxs-lookup"><span data-stu-id="8032f-136">How to: Create a Federated Client</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)
- [<span data-ttu-id="8032f-137">方法: ローカル発行者を構成します。</span><span class="sxs-lookup"><span data-stu-id="8032f-137">How to: Configure a Local Issuer</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)
- [<span data-ttu-id="8032f-138">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="8032f-138">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
