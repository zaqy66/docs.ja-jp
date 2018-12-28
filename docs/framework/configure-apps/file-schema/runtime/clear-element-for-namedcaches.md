---
title: '&lt;オフ&gt;要素&lt;namedCaches&gt;'
ms.date: 03/30/2017
helpviewer_keywords:
- <clear> element for <namedCaches>
- clear element for <namedCaches>
ms.assetid: ea01a858-65da-4348-800f-5e3df59d4d79
author: mcleblanc
ms.author: markl
ms.openlocfilehash: dd521e3afa7584cadb28829028a5ecfd1cb55a92
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2018
ms.locfileid: "53612304"
---
# <a name="ltcleargt-element-for-ltnamedcachesgt"></a><span data-ttu-id="6125f-102">&lt;オフ&gt;要素&lt;namedCaches&gt;</span><span class="sxs-lookup"><span data-stu-id="6125f-102">&lt;clear&gt; Element for &lt;namedCaches&gt;</span></span>
<span data-ttu-id="6125f-103">すべてクリア`namedCache`内のエントリ、`namedCaches`メモリ キャッシュのコレクション。</span><span class="sxs-lookup"><span data-stu-id="6125f-103">Clears all `namedCache` entries in the `namedCaches` collection for a memory cache.</span></span>  
  
 <span data-ttu-id="6125f-104">\<system.runtime.caching></span><span class="sxs-lookup"><span data-stu-id="6125f-104">\<system.runtime.caching></span></span>  
<span data-ttu-id="6125f-105">\<memoryCache></span><span class="sxs-lookup"><span data-stu-id="6125f-105">\<memoryCache></span></span>  
<span data-ttu-id="6125f-106">\<namedCaches ></span><span class="sxs-lookup"><span data-stu-id="6125f-106">\<namedCaches></span></span>  
<span data-ttu-id="6125f-107">\<add></span><span class="sxs-lookup"><span data-stu-id="6125f-107">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6125f-108">構文</span><span class="sxs-lookup"><span data-stu-id="6125f-108">Syntax</span></span>  
  
```xml  
<namedCaches>  
    <clear name="default" />  
    <!-- child elements -->  
 </namedCaches>  
```  
  
## <a name="type"></a><span data-ttu-id="6125f-109">型</span><span class="sxs-lookup"><span data-stu-id="6125f-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6125f-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="6125f-110">Attributes and Elements</span></span>  
 <span data-ttu-id="6125f-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="6125f-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6125f-112">属性</span><span class="sxs-lookup"><span data-stu-id="6125f-112">Attributes</span></span>  
 `None`  
  
### <a name="child-elements"></a><span data-ttu-id="6125f-113">子要素</span><span class="sxs-lookup"><span data-stu-id="6125f-113">Child Elements</span></span>  
 `None`  
  
### <a name="parent-elements"></a><span data-ttu-id="6125f-114">親要素</span><span class="sxs-lookup"><span data-stu-id="6125f-114">Parent Elements</span></span>  
  
|<span data-ttu-id="6125f-115">要素</span><span class="sxs-lookup"><span data-stu-id="6125f-115">Element</span></span>|<span data-ttu-id="6125f-116">説明</span><span class="sxs-lookup"><span data-stu-id="6125f-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6125f-117">\<namedCaches></span><span class="sxs-lookup"><span data-stu-id="6125f-117">\<namedCaches></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)|<span data-ttu-id="6125f-118">名前付きの構成設定のコレクションを含む<xref:System.Runtime.Caching.MemoryCache>インスタンス。</span><span class="sxs-lookup"><span data-stu-id="6125f-118">Contains a collection of configuration settings for the named <xref:System.Runtime.Caching.MemoryCache> instances.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6125f-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="6125f-119">Remarks</span></span>  
 <span data-ttu-id="6125f-120">`clear`要素がすべてクリア`namedCache`メモリ キャッシュの名前付きキャッシュのコレクション内のエントリ。</span><span class="sxs-lookup"><span data-stu-id="6125f-120">The `clear` element clears all `namedCache` entries in the named cache collection for a memory cache.</span></span> <span data-ttu-id="6125f-121">使用することができます、`clear`要素を使用する前に、`add`が他にないを特定するためには新しい名前付きキャッシュ エントリを追加する要素がコレクション内のキャッシュをという名前です。</span><span class="sxs-lookup"><span data-stu-id="6125f-121">You can use the `clear` element before you use the `add` element to add a new named cache entry in order to be certain there are no other named caches in the collection.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6125f-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="6125f-122">See Also</span></span>  
- [<span data-ttu-id="6125f-123">\<namedCaches > 要素 (キャッシュ設定)</span><span class="sxs-lookup"><span data-stu-id="6125f-123">\<namedCaches> Element (Cache Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)
