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
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47071728"
---
# <a name="ltremovegt-element-for-ltnamedcachesgt"></a><span data-ttu-id="6c71e-102">&lt;削除&gt;要素&lt;namedCaches&gt;</span><span class="sxs-lookup"><span data-stu-id="6c71e-102">&lt;remove&gt; Element for &lt;namedCaches&gt;</span></span>
<span data-ttu-id="6c71e-103">名前付きキャッシュ エントリを、メモリ キャッシュの `namedCaches` コレクションから削除します。</span><span class="sxs-lookup"><span data-stu-id="6c71e-103">Removes a named cache entry from the `namedCaches` collection for a memory cache.</span></span>  
  
 <span data-ttu-id="6c71e-104">\<system.runtime.caching></span><span class="sxs-lookup"><span data-stu-id="6c71e-104">\<system.runtime.caching></span></span>  
<span data-ttu-id="6c71e-105">\<memoryCache></span><span class="sxs-lookup"><span data-stu-id="6c71e-105">\<memoryCache></span></span>  
<span data-ttu-id="6c71e-106">\<namedCaches ></span><span class="sxs-lookup"><span data-stu-id="6c71e-106">\<namedCaches></span></span>  
<span data-ttu-id="6c71e-107">\<remove></span><span class="sxs-lookup"><span data-stu-id="6c71e-107">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c71e-108">構文</span><span class="sxs-lookup"><span data-stu-id="6c71e-108">Syntax</span></span>  
  
```xml  
<namedCaches>  
    <remove name="default" />  
    <!-- child elements -->  
 </namedCaches>  
```  
  
## <a name="type"></a><span data-ttu-id="6c71e-109">型</span><span class="sxs-lookup"><span data-stu-id="6c71e-109">Type</span></span>  
 `None`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6c71e-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="6c71e-110">Attributes and Elements</span></span>  
 <span data-ttu-id="6c71e-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="6c71e-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6c71e-112">属性</span><span class="sxs-lookup"><span data-stu-id="6c71e-112">Attributes</span></span>  
 `None`  
  
### <a name="child-elements"></a><span data-ttu-id="6c71e-113">子要素</span><span class="sxs-lookup"><span data-stu-id="6c71e-113">Child Elements</span></span>  
 `None`  
  
### <a name="parent-elements"></a><span data-ttu-id="6c71e-114">親要素</span><span class="sxs-lookup"><span data-stu-id="6c71e-114">Parent Elements</span></span>  
  
|<span data-ttu-id="6c71e-115">要素</span><span class="sxs-lookup"><span data-stu-id="6c71e-115">Element</span></span>|<span data-ttu-id="6c71e-116">説明</span><span class="sxs-lookup"><span data-stu-id="6c71e-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6c71e-117">\<namedCaches></span><span class="sxs-lookup"><span data-stu-id="6c71e-117">\<namedCaches></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)|<span data-ttu-id="6c71e-118">名前付きの構成設定のコレクションを含む<xref:System.Runtime.Caching.MemoryCache>インスタンス。</span><span class="sxs-lookup"><span data-stu-id="6c71e-118">Contains a collection of configuration settings for the named <xref:System.Runtime.Caching.MemoryCache> instances.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6c71e-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="6c71e-119">Remarks</span></span>  
 <span data-ttu-id="6c71e-120">`remove`要素は、削除、`namedCache`メモリ キャッシュの名前付きキャッシュのコレクションからエントリ。</span><span class="sxs-lookup"><span data-stu-id="6c71e-120">The `remove` element removes a `namedCache` entry from the named cache collection for a memory cache.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c71e-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="6c71e-121">See Also</span></span>  
 [<span data-ttu-id="6c71e-122">\<namedCaches > 要素 (キャッシュ設定)</span><span class="sxs-lookup"><span data-stu-id="6c71e-122">\<namedCaches> Element (Cache Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)
