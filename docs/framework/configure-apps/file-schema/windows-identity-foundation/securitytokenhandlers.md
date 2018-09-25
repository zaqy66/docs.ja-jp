---
title: '&lt;securityTokenHandlers&gt;'
ms.date: 03/30/2017
ms.assetid: f11a631d-4094-4e11-bb03-4ede74b30281
author: BrucePerlerMS
ms.openlocfilehash: e63f02add81495e474b59b6c5cc090bd69add3d2
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47082988"
---
# <a name="ltsecuritytokenhandlersgt"></a><span data-ttu-id="e73db-102">&lt;securityTokenHandlers&gt;</span><span class="sxs-lookup"><span data-stu-id="e73db-102">&lt;securityTokenHandlers&gt;</span></span>
<span data-ttu-id="e73db-103">エンドポイントに登録されているセキュリティ トークン ハンドラーのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="e73db-103">Specifies a collection of security token handlers that are registered with the endpoint.</span></span>  
  
 <span data-ttu-id="e73db-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="e73db-104">\<system.identityModel></span></span>  
<span data-ttu-id="e73db-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="e73db-105">\<identityConfiguration></span></span>  
<span data-ttu-id="e73db-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="e73db-106">\<securityTokenHandlers></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e73db-107">構文</span><span class="sxs-lookup"><span data-stu-id="e73db-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e73db-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="e73db-108">Attributes and Elements</span></span>  
 <span data-ttu-id="e73db-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="e73db-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e73db-110">属性</span><span class="sxs-lookup"><span data-stu-id="e73db-110">Attributes</span></span>  
  
|<span data-ttu-id="e73db-111">属性</span><span class="sxs-lookup"><span data-stu-id="e73db-111">Attribute</span></span>|<span data-ttu-id="e73db-112">説明</span><span class="sxs-lookup"><span data-stu-id="e73db-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e73db-113">name</span><span class="sxs-lookup"><span data-stu-id="e73db-113">name</span></span>|<span data-ttu-id="e73db-114">トークン ハンドラー コレクションの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e73db-114">Specifies the name of a token handler collection.</span></span> <span data-ttu-id="e73db-115">フレームワークによって認識される唯一の値は、"ActAs"と"OnBehalfOf"です。</span><span class="sxs-lookup"><span data-stu-id="e73db-115">The only values recognized by the framework are "ActAs" and "OnBehalfOf".</span></span> <span data-ttu-id="e73db-116">トークン ハンドラー コレクションにこれらの名前のいずれかを指定する場合、コレクションをそれぞれトークン ActAs または OnBehalfOf を処理するときに使用します。</span><span class="sxs-lookup"><span data-stu-id="e73db-116">If token handler collections are specified with either of these names, the collection will be used when processing ActAs or OnBehalfOf tokens respectively.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e73db-117">子要素</span><span class="sxs-lookup"><span data-stu-id="e73db-117">Child Elements</span></span>  
  
|<span data-ttu-id="e73db-118">要素</span><span class="sxs-lookup"><span data-stu-id="e73db-118">Element</span></span>|<span data-ttu-id="e73db-119">説明</span><span class="sxs-lookup"><span data-stu-id="e73db-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e73db-120">\<add></span><span class="sxs-lookup"><span data-stu-id="e73db-120">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="e73db-121">トークン ハンドラー コレクションには、セキュリティ トークン ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="e73db-121">Adds a security token handler to the token handler collection.</span></span>|  
|[<span data-ttu-id="e73db-122">\<clear></span><span class="sxs-lookup"><span data-stu-id="e73db-122">\<clear></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/clear.md)|<span data-ttu-id="e73db-123">トークン ハンドラー コレクションからすべてのセキュリティ トークン ハンドラーをクリアします。</span><span class="sxs-lookup"><span data-stu-id="e73db-123">Clears all security token handlers from the token handler collection.</span></span>|  
|[<span data-ttu-id="e73db-124">\<remove></span><span class="sxs-lookup"><span data-stu-id="e73db-124">\<remove></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/remove.md)|<span data-ttu-id="e73db-125">トークン ハンドラー コレクションからセキュリティ トークン ハンドラーを削除します。</span><span class="sxs-lookup"><span data-stu-id="e73db-125">Removes a security token handler from the token handler collection.</span></span>|  
|[<span data-ttu-id="e73db-126">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="e73db-126">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="e73db-127">トークン ハンドラーのコレクションの構成を提供します。</span><span class="sxs-lookup"><span data-stu-id="e73db-127">Provides configuration for the collection of token handlers.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e73db-128">親要素</span><span class="sxs-lookup"><span data-stu-id="e73db-128">Parent Elements</span></span>  
  
|<span data-ttu-id="e73db-129">要素</span><span class="sxs-lookup"><span data-stu-id="e73db-129">Element</span></span>|<span data-ttu-id="e73db-130">説明</span><span class="sxs-lookup"><span data-stu-id="e73db-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e73db-131">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="e73db-131">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="e73db-132">サービス レベルの id の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="e73db-132">Specifies service-level identity settings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e73db-133">Remarks</span><span class="sxs-lookup"><span data-stu-id="e73db-133">Remarks</span></span>  
 <span data-ttu-id="e73db-134">サービス構成では、セキュリティ トークン ハンドラーの 1 つまたは複数の名前付きコレクションを指定できます。</span><span class="sxs-lookup"><span data-stu-id="e73db-134">You can specify one or more named collections of security token handlers in a service configuration.</span></span> <span data-ttu-id="e73db-135">使用してコレクションの名前を指定することができます、`name`属性。</span><span class="sxs-lookup"><span data-stu-id="e73db-135">You can specify a name for a collection by using the `name` attribute.</span></span> <span data-ttu-id="e73db-136">フレームワークを処理する唯一の名前とは、"ActAs"と"OnBehalfOf"です。</span><span class="sxs-lookup"><span data-stu-id="e73db-136">The only names that the framework handles are "ActAs" and "OnBehalfOf".</span></span> <span data-ttu-id="e73db-137">ハンドラーは、これらのコレクションに存在する場合で使用されるセキュリティ トークン サービス (STS)、既定のハンドラーではなく処理するときに`ActAs`と`OnBehalfOf`トークンです。</span><span class="sxs-lookup"><span data-stu-id="e73db-137">If handlers exist in these collections, they are used by a security token service (STS) instead of the default handlers when processing `ActAs` and `OnBehalfOf` tokens.</span></span>  
  
 <span data-ttu-id="e73db-138">既定では、コレクションは、次の種類のハンドラーで設定されます: <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler>、 <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>、 <xref:System.IdentityModel.Tokens.KerberosSecurityTokenHandler>、 <xref:System.IdentityModel.Tokens.WindowsUserNameSecurityTokenHandler>、 <xref:System.IdentityModel.Tokens.RsaSecurityTokenHandler>、 <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler>、および<xref:System.IdentityModel.Tokens.EncryptedSecurityTokenHandler>します。</span><span class="sxs-lookup"><span data-stu-id="e73db-138">By default, the collection is populated with the following handler types: <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>, <xref:System.IdentityModel.Tokens.KerberosSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.WindowsUserNameSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.RsaSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler>, and <xref:System.IdentityModel.Tokens.EncryptedSecurityTokenHandler>.</span></span> <span data-ttu-id="e73db-139">使用して、コレクションを変更することができます、 `<add>`、 `<remove>`、および`<clear>`要素。</span><span class="sxs-lookup"><span data-stu-id="e73db-139">You can modify the collection by using the `<add>`, `<remove>`, and `<clear>` elements.</span></span> <span data-ttu-id="e73db-140">特定の型の 1 つのハンドラーのみがコレクションに存在することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e73db-140">You must ensure that only a single handler of any particular type exists in the collection.</span></span> <span data-ttu-id="e73db-141">たとえば、次のハンドラーからの派生、<xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>クラスか、ハンドラーまたは<xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>両方ではなく 1 つのコレクションで構成することがあります。</span><span class="sxs-lookup"><span data-stu-id="e73db-141">For example, if you derive a handler from the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class, either your handler or the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> may be configured in a single collection, but not both.</span></span>  
  
 <span data-ttu-id="e73db-142">使用して、`<securityTokenHandlerConfiguration>`要素をコレクション内で、ハンドラーの構成設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="e73db-142">Use the `<securityTokenHandlerConfiguration>` element to specify configuration settings for the handlers in the collection.</span></span> <span data-ttu-id="e73db-143">この要素で指定された設定をオーバーライドを通じてサービスに指定されている、 [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)要素。</span><span class="sxs-lookup"><span data-stu-id="e73db-143">Settings specified through this element override those specified on the service through the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element.</span></span> <span data-ttu-id="e73db-144">いくつかのハンドラー (いくつかの組み込みハンドラー型を含む) の子要素を追加の構成をサポートできる、`<add>`要素。</span><span class="sxs-lookup"><span data-stu-id="e73db-144">Some handlers (including several of the built-in handler types) can support additional configuration through a child element of the `<add>` element.</span></span> <span data-ttu-id="e73db-145">ハンドラーで指定した設定では、コレクションまたはサービスに指定した同等の設定をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="e73db-145">Settings specified on a handler override equivalent settings specified on the collection or the service.</span></span>
