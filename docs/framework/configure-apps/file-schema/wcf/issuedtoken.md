---
title: '&lt;issuedToken&gt;'
ms.date: 03/30/2017
ms.assetid: b6eae4b7-a6cd-4e1a-b0f6-f407022550b0
ms.openlocfilehash: ca2e1db2c9894163c113541ac4366c638d0e1df0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54501534"
---
# <a name="ltissuedtokengt"></a><span data-ttu-id="95c32-102">&lt;issuedToken&gt;</span><span class="sxs-lookup"><span data-stu-id="95c32-102">&lt;issuedToken&gt;</span></span>
<span data-ttu-id="95c32-103">サービスに対するクライアントの認証に使用されるカスタム トークンを指定します。</span><span class="sxs-lookup"><span data-stu-id="95c32-103">Specifies a custom token used to authenticate a client to a service.</span></span>  
  
 <span data-ttu-id="95c32-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="95c32-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="95c32-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="95c32-105">\<behaviors></span></span>  
<span data-ttu-id="95c32-106">endpointBehaviors セクション</span><span class="sxs-lookup"><span data-stu-id="95c32-106">endpointBehaviors section</span></span>  
<span data-ttu-id="95c32-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="95c32-107">\<behavior></span></span>  
<span data-ttu-id="95c32-108">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="95c32-108">\<clientCredentials></span></span>  
<span data-ttu-id="95c32-109">\<issuedToken ></span><span class="sxs-lookup"><span data-stu-id="95c32-109">\<issuedToken></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="95c32-110">構文</span><span class="sxs-lookup"><span data-stu-id="95c32-110">Syntax</span></span>  
  
```xml  
<issuedToken cacheIssuedTokens="Boolean"
             defaultKeyEntropyMode="ClientEntropy/ServerEntropy/CombinedEntropy"
             issuedTokenRenewalThresholdPercentage = "0 to 100"
             issuerChannelBehaviors="String"
             localIssuerChannelBehaviors="String"
             maxIssuedTokenCachingTime="TimeSpan">
</issuedToken>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="95c32-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="95c32-111">Attributes and Elements</span></span>  
 <span data-ttu-id="95c32-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="95c32-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="95c32-113">属性</span><span class="sxs-lookup"><span data-stu-id="95c32-113">Attributes</span></span>  
  
|<span data-ttu-id="95c32-114">属性</span><span class="sxs-lookup"><span data-stu-id="95c32-114">Attribute</span></span>|<span data-ttu-id="95c32-115">説明</span><span class="sxs-lookup"><span data-stu-id="95c32-115">Description</span></span>|  
|---------------|-----------------|  
|`cacheIssuedTokens`|<span data-ttu-id="95c32-116">トークンがキャッシュされるかどうかを指定する省略可能なブール属性。</span><span class="sxs-lookup"><span data-stu-id="95c32-116">Optional Boolean attribute that specifies whether tokens are cached.</span></span> <span data-ttu-id="95c32-117">既定値は、`true` です。</span><span class="sxs-lookup"><span data-stu-id="95c32-117">The default is `true`.</span></span>|  
|`defaultKeyEntropyMode`|<span data-ttu-id="95c32-118">ハンドシェイク操作に使用されるランダム値 (エントロピ) を指定する省略可能な文字列属性。</span><span class="sxs-lookup"><span data-stu-id="95c32-118">Optional string attribute that specifies which random values (entropies) are used for handshake operations.</span></span> <span data-ttu-id="95c32-119">値には、`ClientEntropy`、`ServerEntropy`、および `CombinedEntropy` があります。既定値は `CombinedEntropy` です。</span><span class="sxs-lookup"><span data-stu-id="95c32-119">Values include `ClientEntropy`, `ServerEntropy`, and `CombinedEntropy`, The default is `CombinedEntropy`.</span></span> <span data-ttu-id="95c32-120">この属性は <xref:System.ServiceModel.Security.SecurityKeyEntropyMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="95c32-120">This attribute is of type <xref:System.ServiceModel.Security.SecurityKeyEntropyMode>.</span></span>|  
|`issuedTokenRenewalThresholdPercentage`|<span data-ttu-id="95c32-121">トークンが更新されるまでに待機できる有効な期間 (トークン発行者によって提供される) のパーセンテージを指定する省略可能な整数属性。</span><span class="sxs-lookup"><span data-stu-id="95c32-121">Optional integer attribute that specifies the percentage of a valid time frame (supplied by the token issuer) that can pass before a token is renewed.</span></span> <span data-ttu-id="95c32-122">値は 0 ～ 100 の範囲です。</span><span class="sxs-lookup"><span data-stu-id="95c32-122">Values are from 0 to 100.</span></span> <span data-ttu-id="95c32-123">既定値は 60 で、更新の実行までに待機できる期間の 60% を示します。</span><span class="sxs-lookup"><span data-stu-id="95c32-123">The default is 60, which specifies 60% of the time passes before a renewal is attempted.</span></span>|  
|`issuerChannelBehaviors`|<span data-ttu-id="95c32-124">発行者との通信時に使用するチャネル動作を指定する省略可能な属性。</span><span class="sxs-lookup"><span data-stu-id="95c32-124">Optional attribute that specifies the channel behaviors to use when communicating with the issuer.</span></span>|  
|`localIssuerChannelBehaviors`|<span data-ttu-id="95c32-125">ローカル発行者との通信時に使用するチャネル動作を指定する省略可能な属性。</span><span class="sxs-lookup"><span data-stu-id="95c32-125">Optional attribute that specifies the channel behaviors to use when communicating with the local issuer.</span></span>|  
|`maxIssuedTokenCachingTime`|<span data-ttu-id="95c32-126">トークン発行者 (STS) が期間を指定しない場合に、発行済みトークンがキャッシュされる期間を指定する省略可能な Timespan 属性。</span><span class="sxs-lookup"><span data-stu-id="95c32-126">Optional Timespan attribute that specifies the duration that issued tokens are cached when the token issuer (an STS) does not specify a time.</span></span> <span data-ttu-id="95c32-127">既定値は「10675199.02:48:05.4775807」</span><span class="sxs-lookup"><span data-stu-id="95c32-127">The default is "10675199.02:48:05.4775807."</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="95c32-128">子要素</span><span class="sxs-lookup"><span data-stu-id="95c32-128">Child Elements</span></span>  
  
|<span data-ttu-id="95c32-129">要素</span><span class="sxs-lookup"><span data-stu-id="95c32-129">Element</span></span>|<span data-ttu-id="95c32-130">説明</span><span class="sxs-lookup"><span data-stu-id="95c32-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="95c32-131">\<localIssuer></span><span class="sxs-lookup"><span data-stu-id="95c32-131">\<localIssuer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/localissuer.md)|<span data-ttu-id="95c32-132">トークンのローカル発行者のアドレスと、エンドポイントとの通信に使用されるバインディングを指定します。</span><span class="sxs-lookup"><span data-stu-id="95c32-132">Specifies the address of the local issuer of the token and the binding used to communicate with the endpoint.</span></span>|  
|[<span data-ttu-id="95c32-133">\<issuerChannelBehaviors></span><span class="sxs-lookup"><span data-stu-id="95c32-133">\<issuerChannelBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuerchannelbehaviors-element.md)|<span data-ttu-id="95c32-134">ローカル発行者に接続するときに使用するエンドポイント動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="95c32-134">Specifies the endpoint behaviors to use when contacting a local issuer.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="95c32-135">親要素</span><span class="sxs-lookup"><span data-stu-id="95c32-135">Parent Elements</span></span>  
  
|<span data-ttu-id="95c32-136">要素</span><span class="sxs-lookup"><span data-stu-id="95c32-136">Element</span></span>|<span data-ttu-id="95c32-137">説明</span><span class="sxs-lookup"><span data-stu-id="95c32-137">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="95c32-138">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="95c32-138">\<clientCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)|<span data-ttu-id="95c32-139">サービスに対するクライアントの認証に使用される資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="95c32-139">Specifies the credentials used to authenticate a client to a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="95c32-140">Remarks</span><span class="sxs-lookup"><span data-stu-id="95c32-140">Remarks</span></span>  
 <span data-ttu-id="95c32-141">発行済みトークンは、フェデレーション シナリオでセキュリティ トークン サービス (STS) を使用して認証するときに使用されるカスタム資格情報の種類です。</span><span class="sxs-lookup"><span data-stu-id="95c32-141">An issued token is a custom credential type used, for example, when authenticating with a Secure Token Service (STS) in a federated scenario.</span></span> <span data-ttu-id="95c32-142">既定ではトークンは、SAML トークンです。</span><span class="sxs-lookup"><span data-stu-id="95c32-142">By default, the token is a SAML token.</span></span> <span data-ttu-id="95c32-143">詳細については、次を参照してください。[フェデレーションと発行されたトークン](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)します。</span><span class="sxs-lookup"><span data-stu-id="95c32-143">For more information, see [Federation and Issued Tokens](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md).</span></span> <span data-ttu-id="95c32-144">[フェデレーションと発行済みトークン](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)します。</span><span class="sxs-lookup"><span data-stu-id="95c32-144">and [Federation and Issued Tokens](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md).</span></span>  
  
 <span data-ttu-id="95c32-145">このセクションには、トークンのローカル発行者やセキュリティ トークン サービスで使用する動作の構成に使用する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="95c32-145">This section contains the elements used to configure a local issuer of tokens, or behaviors used with an security token service.</span></span> <span data-ttu-id="95c32-146">ローカル発行者を使用するクライアントの構成については、次を参照してください。[方法。ローカル発行者を構成する](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)します。</span><span class="sxs-lookup"><span data-stu-id="95c32-146">For instructions on configuring a client to use a local issuer, see [How to: Configure a Local Issuer](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="95c32-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="95c32-147">See also</span></span>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement.IssuedToken%2A>
- <xref:System.ServiceModel.Description.ClientCredentials.IssuedToken%2A>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential>
- [<span data-ttu-id="95c32-148">セキュリティ動作</span><span class="sxs-lookup"><span data-stu-id="95c32-148">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="95c32-149">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="95c32-149">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="95c32-150">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="95c32-150">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="95c32-151">クライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="95c32-151">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
- [<span data-ttu-id="95c32-152">方法: フェデレーション クライアントを作成します。</span><span class="sxs-lookup"><span data-stu-id="95c32-152">How to: Create a Federated Client</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)
- [<span data-ttu-id="95c32-153">方法: ローカル発行者を構成します。</span><span class="sxs-lookup"><span data-stu-id="95c32-153">How to: Configure a Local Issuer</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)
- [<span data-ttu-id="95c32-154">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="95c32-154">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
