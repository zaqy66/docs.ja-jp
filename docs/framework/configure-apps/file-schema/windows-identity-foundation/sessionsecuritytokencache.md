---
title: '&lt;sessionSecurityTokenCache&gt;'
ms.date: 03/30/2017
ms.assetid: d43e676c-0153-485c-ab31-0257a2db7507
author: BrucePerlerMS
ms.openlocfilehash: b812673ac1c015adde357d3c0707d85643aad3e9
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47084333"
---
# <a name="ltsessionsecuritytokencachegt"></a><span data-ttu-id="1d850-102">&lt;sessionSecurityTokenCache&gt;</span><span class="sxs-lookup"><span data-stu-id="1d850-102">&lt;sessionSecurityTokenCache&gt;</span></span>
<span data-ttu-id="1d850-103">サービスまたはセキュリティ トークン ハンドラー コレクションのセッション トークン キャッシュに登録します。</span><span class="sxs-lookup"><span data-stu-id="1d850-103">Registers a cache for session tokens with a service or a security token handler collection.</span></span>  
  
 <span data-ttu-id="1d850-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="1d850-104">\<system.identityModel></span></span>  
<span data-ttu-id="1d850-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="1d850-105">\<identityConfiguration></span></span>  
<span data-ttu-id="1d850-106">\<キャッシュ ></span><span class="sxs-lookup"><span data-stu-id="1d850-106">\<caches></span></span>  
<span data-ttu-id="1d850-107">\<sessionSecurityTokenCache ></span><span class="sxs-lookup"><span data-stu-id="1d850-107">\<sessionSecurityTokenCache></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1d850-108">構文</span><span class="sxs-lookup"><span data-stu-id="1d850-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1d850-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="1d850-109">Attributes and Elements</span></span>  
 <span data-ttu-id="1d850-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="1d850-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1d850-111">属性</span><span class="sxs-lookup"><span data-stu-id="1d850-111">Attributes</span></span>  
  
|<span data-ttu-id="1d850-112">属性</span><span class="sxs-lookup"><span data-stu-id="1d850-112">Attribute</span></span>|<span data-ttu-id="1d850-113">説明</span><span class="sxs-lookup"><span data-stu-id="1d850-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="1d850-114">型</span><span class="sxs-lookup"><span data-stu-id="1d850-114">type</span></span>|<span data-ttu-id="1d850-115">派生した型、<xref:System.IdentityModel.Tokens.SessionSecurityTokenCache>クラス。</span><span class="sxs-lookup"><span data-stu-id="1d850-115">A type that derives from the <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache> class.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1d850-116">子要素</span><span class="sxs-lookup"><span data-stu-id="1d850-116">Child Elements</span></span>  
 <span data-ttu-id="1d850-117">なし</span><span class="sxs-lookup"><span data-stu-id="1d850-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1d850-118">親要素</span><span class="sxs-lookup"><span data-stu-id="1d850-118">Parent Elements</span></span>  
  
|<span data-ttu-id="1d850-119">要素</span><span class="sxs-lookup"><span data-stu-id="1d850-119">Element</span></span>|<span data-ttu-id="1d850-120">説明</span><span class="sxs-lookup"><span data-stu-id="1d850-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1d850-121">\<キャッシュ ></span><span class="sxs-lookup"><span data-stu-id="1d850-121">\<caches></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|<span data-ttu-id="1d850-122">サービスまたはセキュリティ トークン ハンドラー コレクションで使用されるキャッシュを登録します。</span><span class="sxs-lookup"><span data-stu-id="1d850-122">Registers the caches used by a service or a security token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="1d850-123">例</span><span class="sxs-lookup"><span data-stu-id="1d850-123">Example</span></span>  
 <span data-ttu-id="1d850-124">次の XML はセッション セキュリティ トークンを保持するためのカスタム キャッシュの構成 (<xref:System.IdentityModel.Tokens.SessionSecurityToken>)。</span><span class="sxs-lookup"><span data-stu-id="1d850-124">The following XML shows the configuration of a custom cache for holding session security tokens (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span></span> <span data-ttu-id="1d850-125">構成から取得されますが、`ClaimsAwareWebFarm`サンプル。</span><span class="sxs-lookup"><span data-stu-id="1d850-125">The configuration is taken from the `ClaimsAwareWebFarm` sample.</span></span> <span data-ttu-id="1d850-126">このサンプルの詳細については、次を参照してください。 [WIF コード サンプル インデックス](../../../../../docs/framework/security/wif-code-sample-index.md)します。</span><span class="sxs-lookup"><span data-stu-id="1d850-126">For more information about this sample, see [WIF Code Sample Index](../../../../../docs/framework/security/wif-code-sample-index.md).</span></span>  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```  
  
## <a name="see-also"></a><span data-ttu-id="1d850-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="1d850-127">See Also</span></span>  
 <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache>
