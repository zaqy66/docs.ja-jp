---
title: '&lt;追加&gt;要素&lt;namedCaches&gt;'
ms.date: 03/30/2017
helpviewer_keywords:
- add element for <namedCaches>
- <add> element for <namedCaches>
ms.assetid: ce2a63a8-c829-4742-a6ea-72ee5d89f169
ms.openlocfilehash: 0a292d5bdde019c4c01385a2126de29c3eea7afb
ms.sourcegitcommit: b351b0781a035616c90c68ccae6dd60aae66a953
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/26/2019
ms.locfileid: "55084082"
---
# <a name="ltaddgt-element-for-ltnamedcachesgt"></a><span data-ttu-id="fbf78-102">&lt;追加&gt;要素&lt;namedCaches&gt;</span><span class="sxs-lookup"><span data-stu-id="fbf78-102">&lt;add&gt; Element for &lt;namedCaches&gt;</span></span>
<span data-ttu-id="fbf78-103">追加、`namedCache`エントリを`namedCaches`メモリ キャッシュのコレクション。</span><span class="sxs-lookup"><span data-stu-id="fbf78-103">Adds a `namedCache` entry to the `namedCaches` collection for a memory cache.</span></span>  
  
 <span data-ttu-id="fbf78-104">\<system.runtime.caching></span><span class="sxs-lookup"><span data-stu-id="fbf78-104">\<system.runtime.caching></span></span>  
<span data-ttu-id="fbf78-105">\<memoryCache></span><span class="sxs-lookup"><span data-stu-id="fbf78-105">\<memoryCache></span></span>  
<span data-ttu-id="fbf78-106">\<namedCaches></span><span class="sxs-lookup"><span data-stu-id="fbf78-106">\<namedCaches></span></span>  
<span data-ttu-id="fbf78-107">\<add></span><span class="sxs-lookup"><span data-stu-id="fbf78-107">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fbf78-108">構文</span><span class="sxs-lookup"><span data-stu-id="fbf78-108">Syntax</span></span>  
  
```xml  
<namedCaches>  
    <add name="default" />  
      <!-- child elements -->  
 </namedCaches>  
```  
  
## <a name="type"></a><span data-ttu-id="fbf78-109">型</span><span class="sxs-lookup"><span data-stu-id="fbf78-109">Type</span></span>  
 `None`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fbf78-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="fbf78-110">Attributes and Elements</span></span>  
 <span data-ttu-id="fbf78-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="fbf78-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fbf78-112">属性</span><span class="sxs-lookup"><span data-stu-id="fbf78-112">Attributes</span></span>  
  
|<span data-ttu-id="fbf78-113">属性</span><span class="sxs-lookup"><span data-stu-id="fbf78-113">Attribute</span></span>|<span data-ttu-id="fbf78-114">説明</span><span class="sxs-lookup"><span data-stu-id="fbf78-114">Description</span></span>|  
|-|-|  
|`CacheMemoryLimitMegabytes`|<span data-ttu-id="fbf78-115">(メガバイト) 単位の最大サイズを指定する整数値のインスタンスを<xref:System.Runtime.Caching.MemoryCache>まで拡張できます。</span><span class="sxs-lookup"><span data-stu-id="fbf78-115">An integer value that specifies the maximum allowed size (in megabytes) that an instance of a <xref:System.Runtime.Caching.MemoryCache> can grow to.</span></span> <span data-ttu-id="fbf78-116">既定値は 0、つまり、<xref:System.Runtime.Caching.MemoryCache>クラスの自動サイズ調整ヒューリスティックが既定で使用されます。</span><span class="sxs-lookup"><span data-stu-id="fbf78-116">The default value is 0, which means that the <xref:System.Runtime.Caching.MemoryCache> class's autosizing heuristics are used by default.</span></span>|  
|`Name`|<span data-ttu-id="fbf78-117">キャッシュの名前。</span><span class="sxs-lookup"><span data-stu-id="fbf78-117">The name of the cache.</span></span>|  
|`PhysicalMemoryLimitPercentage`|<span data-ttu-id="fbf78-118">キャッシュで使用できるコンピューターを物理的にインストールされているメモリの最大パーセンテージを指定する整数 0 ~ 100 の値。</span><span class="sxs-lookup"><span data-stu-id="fbf78-118">An integer value between 0 and 100 that specifies the maximum percentage of physically installed computer memory that can be consumed by the cache.</span></span> <span data-ttu-id="fbf78-119">既定値は 0、つまり、<xref:System.Runtime.Caching.MemoryCache>クラスの自動サイズ調整ヒューリスティックが既定で使用されます。</span><span class="sxs-lookup"><span data-stu-id="fbf78-119">The default value is 0, which means that the <xref:System.Runtime.Caching.MemoryCache> class's autosizing heuristics are used by default.</span></span>|  
|`PollingInterval`|<span data-ttu-id="fbf78-120">時間間隔を示す値。この値を超えると、キャッシュの実装によりキャッシュ インスタンスに設定されている絶対およびパーセントのメモリ制限と現在のメモリ負荷が比較されます。</span><span class="sxs-lookup"><span data-stu-id="fbf78-120">A value that indicates the time interval after which the cache implementation compares the current memory load against the absolute and percentage-based memory limits that are set for the cache instance.</span></span> <span data-ttu-id="fbf78-121">この値は"HH:MM:SS"形式で入力します。</span><span class="sxs-lookup"><span data-stu-id="fbf78-121">This value is entered in "HH:MM:SS" format.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="fbf78-122">子要素</span><span class="sxs-lookup"><span data-stu-id="fbf78-122">Child Elements</span></span>  
 `None`  
  
### <a name="parent-elements"></a><span data-ttu-id="fbf78-123">親要素</span><span class="sxs-lookup"><span data-stu-id="fbf78-123">Parent Elements</span></span>  
  
|<span data-ttu-id="fbf78-124">要素</span><span class="sxs-lookup"><span data-stu-id="fbf78-124">Element</span></span>|<span data-ttu-id="fbf78-125">説明</span><span class="sxs-lookup"><span data-stu-id="fbf78-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fbf78-126">\<namedCaches></span><span class="sxs-lookup"><span data-stu-id="fbf78-126">\<namedCaches></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)|<span data-ttu-id="fbf78-127">名前付きの構成設定のコレクションを含む<xref:System.Runtime.Caching.MemoryCache>インスタンス。</span><span class="sxs-lookup"><span data-stu-id="fbf78-127">Contains a collection of configuration settings for the named <xref:System.Runtime.Caching.MemoryCache> instances.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fbf78-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="fbf78-128">Remarks</span></span>  
 <span data-ttu-id="fbf78-129">`add`要素へのエントリを追加する、`namedCaches`メモリ キャッシュのコレクション。</span><span class="sxs-lookup"><span data-stu-id="fbf78-129">The `add` element adds an entry to the `namedCaches` collection for a memory cache.</span></span> <span data-ttu-id="fbf78-130">使用することができます、[オフ](../../../../../docs/framework/configure-apps/file-schema/runtime/clear-element-for-namedcaches.md)要素を使用する前に、`add`という名前のコレクション内のキャッシュのあるものがあることの他の要素。</span><span class="sxs-lookup"><span data-stu-id="fbf78-130">You can use the [clear](../../../../../docs/framework/configure-apps/file-schema/runtime/clear-element-for-namedcaches.md) element before you use the `add` element to be certain that there are no other named caches in the collection.</span></span> <span data-ttu-id="fbf78-131">この要素は、machine.config ファイルでは、Web.config ファイルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="fbf78-131">This element can be used in the machine.config file and in the Web.config file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fbf78-132">例</span><span class="sxs-lookup"><span data-stu-id="fbf78-132">Example</span></span>  
 <span data-ttu-id="fbf78-133">次の例は、既定の設定を定義する方法を示します`namedCache`エントリを`namedCaches`メモリ キャッシュのコレクション。</span><span class="sxs-lookup"><span data-stu-id="fbf78-133">The following example shows how to define settings for the default `namedCache` entry to the `namedCaches` collection for a memory cache.</span></span>  
  
```xml  
<configuration>  
  
  <system.runtime.caching>  
    <memoryCache>  
      <namedCaches>  
          <add name="default"   
               cacheMemoryLimitMegabytes="0"   
               physicalMemoryPercentage="0"  
               pollingInterval="00:02:00" />  
      </namedCaches>  
    </memoryCache>  
  </system.runtime.caching>  
  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="fbf78-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="fbf78-134">See also</span></span>
- [<span data-ttu-id="fbf78-135">\<namedCaches > 要素 (キャッシュ設定)</span><span class="sxs-lookup"><span data-stu-id="fbf78-135">\<namedCaches> Element (Cache Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)
