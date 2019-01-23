---
title: '&lt;sessionSecurityTokenCache&gt;'
ms.date: 03/30/2017
ms.assetid: d43e676c-0153-485c-ab31-0257a2db7507
author: BrucePerlerMS
ms.openlocfilehash: 024375cb114bb080c576ea033e5588526350ecdf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54510092"
---
# <a name="ltsessionsecuritytokencachegt"></a><span data-ttu-id="cadd4-102">&lt;sessionSecurityTokenCache&gt;</span><span class="sxs-lookup"><span data-stu-id="cadd4-102">&lt;sessionSecurityTokenCache&gt;</span></span>
<span data-ttu-id="cadd4-103">サービスまたはセキュリティ トークン ハンドラー コレクションのセッション トークン キャッシュに登録します。</span><span class="sxs-lookup"><span data-stu-id="cadd4-103">Registers a cache for session tokens with a service or a security token handler collection.</span></span>  
  
 <span data-ttu-id="cadd4-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="cadd4-104">\<system.identityModel></span></span>  
<span data-ttu-id="cadd4-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="cadd4-105">\<identityConfiguration></span></span>  
<span data-ttu-id="cadd4-106">\<caches></span><span class="sxs-lookup"><span data-stu-id="cadd4-106">\<caches></span></span>  
<span data-ttu-id="cadd4-107">\<sessionSecurityTokenCache></span><span class="sxs-lookup"><span data-stu-id="cadd4-107">\<sessionSecurityTokenCache></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cadd4-108">構文</span><span class="sxs-lookup"><span data-stu-id="cadd4-108">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
      <sessionSecurityTokenCache type=xs:string>  
      </sessionSecurityTokenCache>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cadd4-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="cadd4-109">Attributes and Elements</span></span>  
 <span data-ttu-id="cadd4-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="cadd4-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cadd4-111">属性</span><span class="sxs-lookup"><span data-stu-id="cadd4-111">Attributes</span></span>  
  
|<span data-ttu-id="cadd4-112">属性</span><span class="sxs-lookup"><span data-stu-id="cadd4-112">Attribute</span></span>|<span data-ttu-id="cadd4-113">説明</span><span class="sxs-lookup"><span data-stu-id="cadd4-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="cadd4-114">型</span><span class="sxs-lookup"><span data-stu-id="cadd4-114">type</span></span>|<span data-ttu-id="cadd4-115">派生した型、<xref:System.IdentityModel.Tokens.SessionSecurityTokenCache>クラス。</span><span class="sxs-lookup"><span data-stu-id="cadd4-115">A type that derives from the <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache> class.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cadd4-116">子要素</span><span class="sxs-lookup"><span data-stu-id="cadd4-116">Child Elements</span></span>  
 <span data-ttu-id="cadd4-117">なし</span><span class="sxs-lookup"><span data-stu-id="cadd4-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="cadd4-118">親要素</span><span class="sxs-lookup"><span data-stu-id="cadd4-118">Parent Elements</span></span>  
  
|<span data-ttu-id="cadd4-119">要素</span><span class="sxs-lookup"><span data-stu-id="cadd4-119">Element</span></span>|<span data-ttu-id="cadd4-120">説明</span><span class="sxs-lookup"><span data-stu-id="cadd4-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cadd4-121">\<caches></span><span class="sxs-lookup"><span data-stu-id="cadd4-121">\<caches></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|<span data-ttu-id="cadd4-122">サービスまたはセキュリティ トークン ハンドラー コレクションで使用されるキャッシュを登録します。</span><span class="sxs-lookup"><span data-stu-id="cadd4-122">Registers the caches used by a service or a security token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="cadd4-123">例</span><span class="sxs-lookup"><span data-stu-id="cadd4-123">Example</span></span>  
 <span data-ttu-id="cadd4-124">次の XML はセッション セキュリティ トークンを保持するためのカスタム キャッシュの構成 (<xref:System.IdentityModel.Tokens.SessionSecurityToken>)。</span><span class="sxs-lookup"><span data-stu-id="cadd4-124">The following XML shows the configuration of a custom cache for holding session security tokens (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span></span> <span data-ttu-id="cadd4-125">構成から取得されますが、`ClaimsAwareWebFarm`サンプル。</span><span class="sxs-lookup"><span data-stu-id="cadd4-125">The configuration is taken from the `ClaimsAwareWebFarm` sample.</span></span> <span data-ttu-id="cadd4-126">このサンプルの詳細については、次を参照してください。 [WIF コード サンプル インデックス](../../../../../docs/framework/security/wif-code-sample-index.md)します。</span><span class="sxs-lookup"><span data-stu-id="cadd4-126">For more information about this sample, see [WIF Code Sample Index](../../../../../docs/framework/security/wif-code-sample-index.md).</span></span>  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```  
  
## <a name="see-also"></a><span data-ttu-id="cadd4-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="cadd4-127">See also</span></span>
- <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache>
