---
title: '&lt;削除&gt;要素&lt;namedCaches&gt;'
ms.date: 03/30/2017
helpviewer_keywords:
- remove element for namedCaches
- <remove> element for namedCaches
ms.assetid: 24211ea5-163e-4fe5-aed8-004d8499760c
author: mcleblanc
ms.author: markl
ms.openlocfilehash: f885416629ae58949cc688f4e6fbd41e77e872aa
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "48781675"
---
# <a name="ltremovegt-element-for-ltnamedcachesgt"></a><span data-ttu-id="bd434-102">&lt;削除&gt;要素&lt;namedCaches&gt;</span><span class="sxs-lookup"><span data-stu-id="bd434-102">&lt;remove&gt; Element for &lt;namedCaches&gt;</span></span>
<span data-ttu-id="bd434-103">名前付きキャッシュ エントリを、メモリ キャッシュの `namedCaches` コレクションから削除します。</span><span class="sxs-lookup"><span data-stu-id="bd434-103">Removes a named cache entry from the `namedCaches` collection for a memory cache.</span></span>  
  
 <span data-ttu-id="bd434-104">\<system.runtime.caching></span><span class="sxs-lookup"><span data-stu-id="bd434-104">\<system.runtime.caching></span></span>  
<span data-ttu-id="bd434-105">\<memoryCache></span><span class="sxs-lookup"><span data-stu-id="bd434-105">\<memoryCache></span></span>  
<span data-ttu-id="bd434-106">\<namedCaches ></span><span class="sxs-lookup"><span data-stu-id="bd434-106">\<namedCaches></span></span>  
<span data-ttu-id="bd434-107">\<remove></span><span class="sxs-lookup"><span data-stu-id="bd434-107">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bd434-108">構文</span><span class="sxs-lookup"><span data-stu-id="bd434-108">Syntax</span></span>  
  
```xml  
<namedCaches>  
    <remove name="default" />  
    <!-- child elements -->  
 </namedCaches>  
```  
  
## <a name="type"></a><span data-ttu-id="bd434-109">型</span><span class="sxs-lookup"><span data-stu-id="bd434-109">Type</span></span>  
 `None`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bd434-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="bd434-110">Attributes and Elements</span></span>  
 <span data-ttu-id="bd434-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="bd434-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bd434-112">属性</span><span class="sxs-lookup"><span data-stu-id="bd434-112">Attributes</span></span>  
 `None`  
  
### <a name="child-elements"></a><span data-ttu-id="bd434-113">子要素</span><span class="sxs-lookup"><span data-stu-id="bd434-113">Child Elements</span></span>  
 `None`  
  
### <a name="parent-elements"></a><span data-ttu-id="bd434-114">親要素</span><span class="sxs-lookup"><span data-stu-id="bd434-114">Parent Elements</span></span>  
  
|<span data-ttu-id="bd434-115">要素</span><span class="sxs-lookup"><span data-stu-id="bd434-115">Element</span></span>|<span data-ttu-id="bd434-116">説明</span><span class="sxs-lookup"><span data-stu-id="bd434-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bd434-117">\<namedCaches></span><span class="sxs-lookup"><span data-stu-id="bd434-117">\<namedCaches></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)|<span data-ttu-id="bd434-118">名前付きの構成設定のコレクションを含む<xref:System.Runtime.Caching.MemoryCache>インスタンス。</span><span class="sxs-lookup"><span data-stu-id="bd434-118">Contains a collection of configuration settings for the named <xref:System.Runtime.Caching.MemoryCache> instances.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bd434-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="bd434-119">Remarks</span></span>  
 <span data-ttu-id="bd434-120">`remove`要素は、削除、`namedCache`メモリ キャッシュの名前付きキャッシュのコレクションからエントリ。</span><span class="sxs-lookup"><span data-stu-id="bd434-120">The `remove` element removes a `namedCache` entry from the named cache collection for a memory cache.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bd434-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd434-121">See Also</span></span>  
 [<span data-ttu-id="bd434-122">\<namedCaches > 要素 (キャッシュ設定)</span><span class="sxs-lookup"><span data-stu-id="bd434-122">\<namedCaches> Element (Cache Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)
