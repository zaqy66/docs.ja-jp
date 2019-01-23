---
title: '&lt;allowedAudienceUris&gt;'
ms.date: 03/30/2017
ms.assetid: 0f4dc73d-d95d-4193-9755-7df4cf2b8e1c
ms.openlocfilehash: 5d1c1207486be3c6bfe25e7862a5674106ec5214
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498061"
---
# <a name="ltallowedaudienceurisgt"></a><span data-ttu-id="9cd42-102">&lt;allowedAudienceUris&gt;</span><span class="sxs-lookup"><span data-stu-id="9cd42-102">&lt;allowedAudienceUris&gt;</span></span>
<span data-ttu-id="9cd42-103"><xref:System.IdentityModel.Tokens.SamlSecurityToken> インスタンスにより有効と見なされるように、<xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> セキュリティ トークンのターゲットとなる URI のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="9cd42-103">Represents a collection of target URIs for which the <xref:System.IdentityModel.Tokens.SamlSecurityToken> security token can be targeted for in order to be considered valid by a <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> instance.</span></span>  
  
 <span data-ttu-id="9cd42-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="9cd42-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="9cd42-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="9cd42-105">\<behaviors></span></span>  
<span data-ttu-id="9cd42-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="9cd42-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="9cd42-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="9cd42-107">\<behavior></span></span>  
<span data-ttu-id="9cd42-108">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="9cd42-108">\<serviceCredentials></span></span>  
<span data-ttu-id="9cd42-109">\<issuedTokenAuthentication></span><span class="sxs-lookup"><span data-stu-id="9cd42-109">\<issuedTokenAuthentication></span></span>  
<span data-ttu-id="9cd42-110">\<allowedAudienceUris></span><span class="sxs-lookup"><span data-stu-id="9cd42-110">\<allowedAudienceUris></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9cd42-111">構文</span><span class="sxs-lookup"><span data-stu-id="9cd42-111">Syntax</span></span>  
  
```xml  
<allowedAudienceUris>
  <add allowedAudienceUri="String" />
</allowedAudienceUris>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9cd42-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="9cd42-112">Attributes and Elements</span></span>  
 <span data-ttu-id="9cd42-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="9cd42-113">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9cd42-114">属性</span><span class="sxs-lookup"><span data-stu-id="9cd42-114">Attributes</span></span>  
 <span data-ttu-id="9cd42-115">なし。</span><span class="sxs-lookup"><span data-stu-id="9cd42-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="9cd42-116">子要素</span><span class="sxs-lookup"><span data-stu-id="9cd42-116">Child Elements</span></span>  
  
|<span data-ttu-id="9cd42-117">要素</span><span class="sxs-lookup"><span data-stu-id="9cd42-117">Element</span></span>|<span data-ttu-id="9cd42-118">説明</span><span class="sxs-lookup"><span data-stu-id="9cd42-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9cd42-119">\<add></span><span class="sxs-lookup"><span data-stu-id="9cd42-119">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-allowedaudienceuris.md)|<span data-ttu-id="9cd42-120"><xref:System.IdentityModel.Tokens.SamlSecurityToken> インスタンスにより有効と見なされるように、<xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> セキュリティ トークンのターゲットとなる URI を追加します。</span><span class="sxs-lookup"><span data-stu-id="9cd42-120">Adds a target Uri for which the <xref:System.IdentityModel.Tokens.SamlSecurityToken> security token can be targeted for in order to be considered valid by a <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> instance.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9cd42-121">親要素</span><span class="sxs-lookup"><span data-stu-id="9cd42-121">Parent Elements</span></span>  
  
|<span data-ttu-id="9cd42-122">要素</span><span class="sxs-lookup"><span data-stu-id="9cd42-122">Element</span></span>|<span data-ttu-id="9cd42-123">説明</span><span class="sxs-lookup"><span data-stu-id="9cd42-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9cd42-124">\<issuedTokenAuthentication></span><span class="sxs-lookup"><span data-stu-id="9cd42-124">\<issuedTokenAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenauthentication-of-servicecredentials.md)|<span data-ttu-id="9cd42-125">サービス資格情報として発行されるトークンを指定します。</span><span class="sxs-lookup"><span data-stu-id="9cd42-125">Specifies a token issued as a service credential.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9cd42-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="9cd42-126">Remarks</span></span>  
 <span data-ttu-id="9cd42-127">このコレクションは、<xref:System.IdentityModel.Tokens.SamlSecurityToken> セキュリティ トークンを発行するセキュリティ トークン サービス (STS) を利用するフェデレーション アプリケーションで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cd42-127">You should use this collection in a federated application that utilizes a security token service (STS) that issues <xref:System.IdentityModel.Tokens.SamlSecurityToken> security tokens.</span></span> <span data-ttu-id="9cd42-128">STS がセキュリティ トークンを発行する場合、このセキュリティ トークンに <xref:System.IdentityModel.Tokens.SamlAudienceRestrictionCondition> を追加して、セキュリティ トークンの提供先となる Web サービスの URI を指定できます。</span><span class="sxs-lookup"><span data-stu-id="9cd42-128">When the STS issues the security token, it can specify the URI of the Web services for which the security token is intended by adding a <xref:System.IdentityModel.Tokens.SamlAudienceRestrictionCondition> to the security token.</span></span> <span data-ttu-id="9cd42-129">これにより、受け取り側 <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> Web サービスは、次のようにしてこのチェックが行われるように指定することで、発行されたセキュリティ トークンがこの Web サービスを対象としていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="9cd42-129">That allows the <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> for the recipient Web service to verify that the issued security token is intended for this Web service by specifying that this check should happen by doing the following:</span></span>  
  
-   <span data-ttu-id="9cd42-130">`audienceUriMode` の `<issuedTokenAuthentication>` 属性を <xref:System.IdentityModel.Selectors.AudienceUriMode.Always> または <xref:System.IdentityModel.Selectors.AudienceUriMode.BearerKeyOnly> に設定します。</span><span class="sxs-lookup"><span data-stu-id="9cd42-130">Set the `audienceUriMode` attribute of `<issuedTokenAuthentication>` to <xref:System.IdentityModel.Selectors.AudienceUriMode.Always> or <xref:System.IdentityModel.Selectors.AudienceUriMode.BearerKeyOnly>.</span></span>  
  
-   <span data-ttu-id="9cd42-131">このコレクションに URI を追加して、有効な URI のセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="9cd42-131">Specify the set of valid URIs, by adding the URIs to this collection.</span></span>  
  
 <span data-ttu-id="9cd42-132">詳細については、「 <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9cd42-132">For more information, see <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>.</span></span>  
  
 <span data-ttu-id="9cd42-133">この構成要素の使用に関する詳細については、次を参照してください。[方法。フェデレーション サービスで資格情報を構成](../../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md)します。</span><span class="sxs-lookup"><span data-stu-id="9cd42-133">For more information on using this configuration element, see [How to: Configure Credentials on a Federation Service](../../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9cd42-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="9cd42-134">See also</span></span>
- <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>
- <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator.AllowedAudienceUris%2A>
- <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator.AudienceUriMode%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenServiceElement.AllowedAudienceUris%2A>
- <xref:System.ServiceModel.Configuration.AllowedAudienceUriElementCollection>
- <xref:System.ServiceModel.Configuration.AllowedAudienceUriElement>
- <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.AllowedAudienceUris%2A>
- [<span data-ttu-id="9cd42-135">\<issuedTokenAuthentication></span><span class="sxs-lookup"><span data-stu-id="9cd42-135">\<issuedTokenAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenauthentication-of-servicecredentials.md)
- [<span data-ttu-id="9cd42-136">\<add></span><span class="sxs-lookup"><span data-stu-id="9cd42-136">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-allowedaudienceuris.md)
- [<span data-ttu-id="9cd42-137">セキュリティ動作</span><span class="sxs-lookup"><span data-stu-id="9cd42-137">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="9cd42-138">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="9cd42-138">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="9cd42-139">方法: フェデレーション サービスで資格情報を構成します。</span><span class="sxs-lookup"><span data-stu-id="9cd42-139">How to: Configure Credentials on a Federation Service</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md)
