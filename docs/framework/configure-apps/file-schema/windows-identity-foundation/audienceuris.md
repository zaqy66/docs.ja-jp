---
title: '&lt;audienceUris&gt;'
ms.date: 03/30/2017
ms.assetid: 7a3d8515-d756-4afe-a22d-07cbe2217ee3
author: BrucePerlerMS
ms.openlocfilehash: af138a4da49a48ed43e1bc8f2c2c81c56892feed
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47216651"
---
# <a name="ltaudienceurisgt"></a><span data-ttu-id="64b58-102">&lt;audienceUris&gt;</span><span class="sxs-lookup"><span data-stu-id="64b58-102">&lt;audienceUris&gt;</span></span>
<span data-ttu-id="64b58-103">利用者 (RP) の許容可能な識別子 Uri のセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="64b58-103">Specifies the set of URIs that are acceptable identifiers of the relying party (RP).</span></span> <span data-ttu-id="64b58-104">許可された対象 Uri のいずれかのスコープがない限り、トークンは受け入れられません。</span><span class="sxs-lookup"><span data-stu-id="64b58-104">Tokens will not be accepted unless they are scoped for one of the allowed audience URIs.</span></span>  
  
 <span data-ttu-id="64b58-105">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="64b58-105">\<system.identityModel></span></span>  
<span data-ttu-id="64b58-106">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="64b58-106">\<identityConfiguration></span></span>  
<span data-ttu-id="64b58-107">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="64b58-107">\<securityTokenHandlers></span></span>  
<span data-ttu-id="64b58-108">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="64b58-108">\<securityTokenHandlerConfiguration></span></span>  
<span data-ttu-id="64b58-109">\<audienceUris ></span><span class="sxs-lookup"><span data-stu-id="64b58-109">\<audienceUris></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64b58-110">構文</span><span class="sxs-lookup"><span data-stu-id="64b58-110">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <audienceUris mode=xs:string>  
          <add value=xs:string />  
          <clear />  
          <remove value=xs:string />  
        </audienceUris>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="64b58-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="64b58-111">Attributes and Elements</span></span>  
 <span data-ttu-id="64b58-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="64b58-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="64b58-113">属性</span><span class="sxs-lookup"><span data-stu-id="64b58-113">Attributes</span></span>  
  
|<span data-ttu-id="64b58-114">属性</span><span class="sxs-lookup"><span data-stu-id="64b58-114">Attribute</span></span>|<span data-ttu-id="64b58-115">説明</span><span class="sxs-lookup"><span data-stu-id="64b58-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="64b58-116">モード</span><span class="sxs-lookup"><span data-stu-id="64b58-116">mode</span></span>|<span data-ttu-id="64b58-117"><xref:System.IdentityModel.Selectors.AudienceUriMode>受信トークンに対象者制限を適用するかどうかを指定する値。</span><span class="sxs-lookup"><span data-stu-id="64b58-117">An <xref:System.IdentityModel.Selectors.AudienceUriMode> value that specifies whether the audience restriction should be applied to an incoming token.</span></span> <span data-ttu-id="64b58-118">使用可能な値は、「常に」、"Never"、"BearerKeyOnly"。</span><span class="sxs-lookup"><span data-stu-id="64b58-118">The possible values are "Always", "Never", and "BearerKeyOnly".</span></span> <span data-ttu-id="64b58-119">既定では 常にです"。</span><span class="sxs-lookup"><span data-stu-id="64b58-119">The default is "Always".</span></span> <span data-ttu-id="64b58-120">任意。</span><span class="sxs-lookup"><span data-stu-id="64b58-120">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="64b58-121">子要素</span><span class="sxs-lookup"><span data-stu-id="64b58-121">Child Elements</span></span>  
  
|<span data-ttu-id="64b58-122">要素</span><span class="sxs-lookup"><span data-stu-id="64b58-122">Element</span></span>|<span data-ttu-id="64b58-123">説明</span><span class="sxs-lookup"><span data-stu-id="64b58-123">Description</span></span>|  
|-------------|-----------------|  
|`<add value=xs:string>`|<span data-ttu-id="64b58-124">指定された URI を追加、 `value` audienceUris のコレクションに属性します。</span><span class="sxs-lookup"><span data-stu-id="64b58-124">Adds the URI specified by the `value` attribute to the audienceUris collection.</span></span> <span data-ttu-id="64b58-125">`value` 属性は必須です。</span><span class="sxs-lookup"><span data-stu-id="64b58-125">The `value` attribute is required.</span></span> <span data-ttu-id="64b58-126">URI は、大文字小文字を区別します。</span><span class="sxs-lookup"><span data-stu-id="64b58-126">The URI is case-sensitive.</span></span>|  
|`<clear>`|<span data-ttu-id="64b58-127">AudienceUris のコレクションをクリアします。</span><span class="sxs-lookup"><span data-stu-id="64b58-127">Clears the audienceUris collection.</span></span> <span data-ttu-id="64b58-128">すべての識別子は、コレクションから削除されます。</span><span class="sxs-lookup"><span data-stu-id="64b58-128">All identifiers are removed from the collection.</span></span>|  
|`<remove value=xs:string>`|<span data-ttu-id="64b58-129">指定された URI を削除、 `value` audienceUris のコレクションから属性。</span><span class="sxs-lookup"><span data-stu-id="64b58-129">Removes the URI specified by the `value` attribute from the audienceUris collection.</span></span> <span data-ttu-id="64b58-130">`value` 属性は必須です。</span><span class="sxs-lookup"><span data-stu-id="64b58-130">The `value` attribute is required.</span></span> <span data-ttu-id="64b58-131">URI は、大文字小文字を区別します。</span><span class="sxs-lookup"><span data-stu-id="64b58-131">The URI is case-sensitive.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="64b58-132">親要素</span><span class="sxs-lookup"><span data-stu-id="64b58-132">Parent Elements</span></span>  
  
|<span data-ttu-id="64b58-133">要素</span><span class="sxs-lookup"><span data-stu-id="64b58-133">Element</span></span>|<span data-ttu-id="64b58-134">説明</span><span class="sxs-lookup"><span data-stu-id="64b58-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="64b58-135">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="64b58-135">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="64b58-136">トークン ハンドラー コレクションのセキュリティの構成を提供します。</span><span class="sxs-lookup"><span data-stu-id="64b58-136">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="64b58-137">Remarks</span><span class="sxs-lookup"><span data-stu-id="64b58-137">Remarks</span></span>  
 <span data-ttu-id="64b58-138">既定では、コレクションが空です。使用して、 `<add>`、 `<clear>`、および`<remove>`コレクションを変更する要素。</span><span class="sxs-lookup"><span data-stu-id="64b58-138">By default, the collection is empty; use `<add>`, `<clear>`, and `<remove>` elements to modify the collection.</span></span> <span data-ttu-id="64b58-139"><xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>オブジェクトでいずれかを構成する対象ユーザー URI のコレクション内の値が対象ユーザー URI 制限を許可されている使用<xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement>オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="64b58-139"><xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> and <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> objects use the values in the audience URI collection to configure any allowed audience URI restrictions in <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> objects.</span></span>  
  
 <span data-ttu-id="64b58-140">`<audienceUris>`要素が表される、<xref:System.IdentityModel.Configuration.AudienceUriElementCollection>クラス。</span><span class="sxs-lookup"><span data-stu-id="64b58-140">The `<audienceUris>` element is represented by the <xref:System.IdentityModel.Configuration.AudienceUriElementCollection> class.</span></span> <span data-ttu-id="64b58-141">によって表されるコレクションに追加された個々 の URI、<xref:System.IdentityModel.Configuration.AudienceUriElement>クラス。</span><span class="sxs-lookup"><span data-stu-id="64b58-141">An individual URI added to the collection is represented by the <xref:System.IdentityModel.Configuration.AudienceUriElement> class.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="64b58-142">使用、`<audienceUris>`要素の子要素として、 [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)要素は非推奨とされましたが、旧バージョンとの互換性もサポートします。</span><span class="sxs-lookup"><span data-stu-id="64b58-142">The use of the `<audienceUris>` element as a child element of the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element has been deprecated, but is still supported for backward compatibility.</span></span> <span data-ttu-id="64b58-143">上の設定、`<securityTokenHandlerConfiguration>`要素のオーバーライド、`<identityConfiguration>`要素。</span><span class="sxs-lookup"><span data-stu-id="64b58-143">Settings on the `<securityTokenHandlerConfiguration>` element override those on the `<identityConfiguration>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="64b58-144">例</span><span class="sxs-lookup"><span data-stu-id="64b58-144">Example</span></span>  
 <span data-ttu-id="64b58-145">次の XML では、アプリケーションの許容される対象ユーザー Uri を構成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="64b58-145">The following XML shows how to configure the acceptable audience URIs for an application.</span></span> <span data-ttu-id="64b58-146">この例では、単一の URI を設定します。</span><span class="sxs-lookup"><span data-stu-id="64b58-146">This example configures a single URI.</span></span> <span data-ttu-id="64b58-147">この URI のスコープのトークンが受け付けられます、他のすべてのユーザーは拒否されます。</span><span class="sxs-lookup"><span data-stu-id="64b58-147">Tokens scoped for this URI will be accepted, all others will be rejected.</span></span>  
  
```xml  
<audienceUris>  
  <add value="http://localhost:19851/"/>  
</audienceUris>  
```
