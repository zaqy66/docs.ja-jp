---
title: <caches>
ms.date: 03/30/2017
ms.assetid: 4651091b-3a20-40d8-b293-4408c0710143
author: BrucePerlerMS
ms.openlocfilehash: b1d04280ef993297102d446ba5a7db54e8404dd8
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55285663"
---
# <a name="caches"></a><span data-ttu-id="2dceb-101">\<caches></span><span class="sxs-lookup"><span data-stu-id="2dceb-101">\<caches></span></span>
<span data-ttu-id="2dceb-102">セッション トークンやトークン リプレイ検出のために使用されるキャッシュを登録します。</span><span class="sxs-lookup"><span data-stu-id="2dceb-102">Registers the caches used for session tokens and token replay detection.</span></span>  
  
 <span data-ttu-id="2dceb-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="2dceb-103">\<system.identityModel></span></span>  
<span data-ttu-id="2dceb-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="2dceb-104">\<identityConfiguration></span></span>  
<span data-ttu-id="2dceb-105">\<caches></span><span class="sxs-lookup"><span data-stu-id="2dceb-105">\<caches></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2dceb-106">構文</span><span class="sxs-lookup"><span data-stu-id="2dceb-106">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2dceb-107">属性および要素</span><span class="sxs-lookup"><span data-stu-id="2dceb-107">Attributes and Elements</span></span>  
 <span data-ttu-id="2dceb-108">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="2dceb-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2dceb-109">属性</span><span class="sxs-lookup"><span data-stu-id="2dceb-109">Attributes</span></span>  
 <span data-ttu-id="2dceb-110">なし</span><span class="sxs-lookup"><span data-stu-id="2dceb-110">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="2dceb-111">子要素</span><span class="sxs-lookup"><span data-stu-id="2dceb-111">Child Elements</span></span>  
  
|<span data-ttu-id="2dceb-112">要素</span><span class="sxs-lookup"><span data-stu-id="2dceb-112">Element</span></span>|<span data-ttu-id="2dceb-113">説明</span><span class="sxs-lookup"><span data-stu-id="2dceb-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2dceb-114">\<sessionSecurityTokenCache></span><span class="sxs-lookup"><span data-stu-id="2dceb-114">\<sessionSecurityTokenCache></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/sessionsecuritytokencache.md)|<span data-ttu-id="2dceb-115">サービスまたはセキュリティ トークン ハンドラー コレクションのセッション トークン キャッシュに登録します。</span><span class="sxs-lookup"><span data-stu-id="2dceb-115">Registers a cache for session tokens with a service or a security token handler collection.</span></span>|  
|[<span data-ttu-id="2dceb-116">\<tokenReplayCache></span><span class="sxs-lookup"><span data-stu-id="2dceb-116">\<tokenReplayCache></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md)|<span data-ttu-id="2dceb-117">トークン再生キャッシュ サービスまたはセキュリティ トークン ハンドラー コレクションに登録します。</span><span class="sxs-lookup"><span data-stu-id="2dceb-117">Registers a token replay cache with a service or a security token handler collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="2dceb-118">親要素</span><span class="sxs-lookup"><span data-stu-id="2dceb-118">Parent Elements</span></span>  
  
|<span data-ttu-id="2dceb-119">要素</span><span class="sxs-lookup"><span data-stu-id="2dceb-119">Element</span></span>|<span data-ttu-id="2dceb-120">説明</span><span class="sxs-lookup"><span data-stu-id="2dceb-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2dceb-121">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="2dceb-121">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="2dceb-122">サービス レベルの id の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="2dceb-122">Specifies service-level identity settings.</span></span>|  
|[<span data-ttu-id="2dceb-123">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="2dceb-123">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="2dceb-124">トークン ハンドラー コレクションのセキュリティの構成を提供します。</span><span class="sxs-lookup"><span data-stu-id="2dceb-124">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2dceb-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="2dceb-125">Remarks</span></span>  
 <span data-ttu-id="2dceb-126">A`<caches>`下で、サービス レベルで要素を指定することができます、`<identityConfiguration>`要素またはセキュリティ トークン ハンドラー コレクション レベルの下で、`<securityTokenHandlerConfiguration>`要素。</span><span class="sxs-lookup"><span data-stu-id="2dceb-126">A `<caches>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="2dceb-127">トークン ハンドラー コレクションの設定は、サービスに指定されているものをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="2dceb-127">Settings on a token handler collection override those specified on the service.</span></span>  
  
 <span data-ttu-id="2dceb-128">`<caches>`要素が表される、<xref:System.IdentityModel.Configuration.IdentityModelCachesElement>クラス。</span><span class="sxs-lookup"><span data-stu-id="2dceb-128">The `<caches>` element is represented by the <xref:System.IdentityModel.Configuration.IdentityModelCachesElement> class.</span></span> <span data-ttu-id="2dceb-129">構成済みのキャッシュがによって表される、<xref:System.IdentityModel.Configuration.IdentityModelCaches>クラス。</span><span class="sxs-lookup"><span data-stu-id="2dceb-129">The configured caches are represented by the <xref:System.IdentityModel.Configuration.IdentityModelCaches> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2dceb-130">例</span><span class="sxs-lookup"><span data-stu-id="2dceb-130">Example</span></span>  
 <span data-ttu-id="2dceb-131">次の XML はセッション セキュリティ トークンを保持するためのカスタム キャッシュの構成 (<xref:System.IdentityModel.Tokens.SessionSecurityToken>)。</span><span class="sxs-lookup"><span data-stu-id="2dceb-131">The following XML shows the configuration of a custom cache for holding session security tokens (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span></span> <span data-ttu-id="2dceb-132">構成から取得されますが、`ClaimsAwareWebFarm`サンプル。</span><span class="sxs-lookup"><span data-stu-id="2dceb-132">The configuration is taken from the `ClaimsAwareWebFarm` sample.</span></span>  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```
