---
title: '&lt;system.runtime.caching&gt;要素 (キャッシュ設定)'
ms.date: 03/30/2017
helpviewer_keywords:
- <system.runtime.caching> element
- caching [.NET Framework], configuration
- system.runtime.caching element
ms.assetid: 9b44daee-874a-4bd1-954e-83bf53565590
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: daa08bb8a92a13941093a77f580318558dc14e9c
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2018
ms.locfileid: "53610373"
---
# <a name="ltsystemruntimecachinggt-element-cache-settings"></a><span data-ttu-id="51fab-102">&lt;system.runtime.caching&gt;要素 (キャッシュ設定)</span><span class="sxs-lookup"><span data-stu-id="51fab-102">&lt;system.runtime.caching&gt; Element (Cache Settings)</span></span>
<span data-ttu-id="51fab-103">構成ファイル内の <xref:System.Runtime.Caching.ObjectCache> エントリを使用して既定のメモリ内の `memoryCache` の実装の構成を提供します。</span><span class="sxs-lookup"><span data-stu-id="51fab-103">Provides configuration for the default in-memory <xref:System.Runtime.Caching.ObjectCache> implementation through the `memoryCache` entry in the configuration file.</span></span>  
  
 <span data-ttu-id="51fab-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="51fab-104">\<configuration></span></span>  
<span data-ttu-id="51fab-105">\<system.runtime.caching></span><span class="sxs-lookup"><span data-stu-id="51fab-105">\<system.runtime.caching></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="51fab-106">構文</span><span class="sxs-lookup"><span data-stu-id="51fab-106">Syntax</span></span>  
  
```xml  
<system.runtime.caching >  
   <!-- child elements -->  
</system.runtime.caching >  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="51fab-107">属性および要素</span><span class="sxs-lookup"><span data-stu-id="51fab-107">Attributes and Elements</span></span>  
 <span data-ttu-id="51fab-108">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="51fab-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="51fab-109">属性</span><span class="sxs-lookup"><span data-stu-id="51fab-109">Attributes</span></span>  
 `None`  
  
### <a name="child-elements"></a><span data-ttu-id="51fab-110">子要素</span><span class="sxs-lookup"><span data-stu-id="51fab-110">Child Elements</span></span>  
  
|<span data-ttu-id="51fab-111">要素</span><span class="sxs-lookup"><span data-stu-id="51fab-111">Element</span></span>|<span data-ttu-id="51fab-112">説明</span><span class="sxs-lookup"><span data-stu-id="51fab-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="51fab-113">\<memoryCache></span><span class="sxs-lookup"><span data-stu-id="51fab-113">\<memoryCache></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/memorycache-element-cache-settings.md)|<span data-ttu-id="51fab-114"><xref:System.Runtime.Caching.MemoryCache> クラスに基づくキャッシュを構成するために使用される要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="51fab-114">Defines an element that is used to configure a cache that is based on the <xref:System.Runtime.Caching.MemoryCache> class.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="51fab-115">親要素</span><span class="sxs-lookup"><span data-stu-id="51fab-115">Parent Elements</span></span>  
  
|<span data-ttu-id="51fab-116">要素</span><span class="sxs-lookup"><span data-stu-id="51fab-116">Element</span></span>|<span data-ttu-id="51fab-117">説明</span><span class="sxs-lookup"><span data-stu-id="51fab-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="51fab-118">\<configuration></span><span class="sxs-lookup"><span data-stu-id="51fab-118">\<configuration></span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|<span data-ttu-id="51fab-119">共通言語ランタイムおよび [!INCLUDE[dnprdnshort](../../../../../includes/dnprdnshort-md.md)] アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="51fab-119">Specifies the root element in every configuration file that is used by the common language runtime and [!INCLUDE[dnprdnshort](../../../../../includes/dnprdnshort-md.md)] applications.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="51fab-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="51fab-120">Remarks</span></span>  
 <span data-ttu-id="51fab-121">この名前空間のクラスは、ASP.NET のキャッシュ機能と同様のキャッシュ機能を使用する方法を提供しますが、 `System.Web` アセンブリに依存しません。</span><span class="sxs-lookup"><span data-stu-id="51fab-121">The classes in this namespace provide a way to use caching facilities like those in ASP.NET, but without a dependency on the `System.Web` assembly.</span></span> <span data-ttu-id="51fab-122">詳細については、「 [Caching in .NET Framework Applications](../../../../../docs/framework/performance/caching-in-net-framework-applications.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="51fab-122">For more information, see [Caching in .NET Framework Applications](../../../../../docs/framework/performance/caching-in-net-framework-applications.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="51fab-123"><xref:System.Runtime.Caching> 名前空間の出力キャッシュ機能と型は、 [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)]の新機能です。</span><span class="sxs-lookup"><span data-stu-id="51fab-123">The output caching functionality and types in the <xref:System.Runtime.Caching> namespace are new in [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="example"></a><span data-ttu-id="51fab-124">例</span><span class="sxs-lookup"><span data-stu-id="51fab-124">Example</span></span>  
 <span data-ttu-id="51fab-125">次の例では、 <xref:System.Runtime.Caching.MemoryCache> クラスを元にしたキャッシュの構成方法を紹介します。</span><span class="sxs-lookup"><span data-stu-id="51fab-125">The following example shows how to configure a cache that is based on the <xref:System.Runtime.Caching.MemoryCache> class.</span></span> <span data-ttu-id="51fab-126">この例では、メモリ キャッシュ用の `namedCaches` エントリのインスタンスの構成を方法を示します。</span><span class="sxs-lookup"><span data-stu-id="51fab-126">The example shows how to configure an instance of the `namedCaches` entry for memory cache.</span></span> <span data-ttu-id="51fab-127">キャッシュの名前は、 `name` 属性を "default" に設定することによって、既定のキャッシュ エントリ名に設定されます。</span><span class="sxs-lookup"><span data-stu-id="51fab-127">The name of the cache is set to the default cache entry name by setting the `name` attribute to "default".</span></span>  
  
 <span data-ttu-id="51fab-128">`cacheMemoryLimitMegabytes` 属性および `physicalMemoryPercentage` 属性はゼロに設定されます。</span><span class="sxs-lookup"><span data-stu-id="51fab-128">The `cacheMemoryLimitMegabytes` attribute and the `physicalMemoryPercentage` attribute are set to zero.</span></span> <span data-ttu-id="51fab-129">これらの属性をゼロに設定すると、 <xref:System.Runtime.Caching.MemoryCache> の自動サイズ調整ヒューリスティックが既定で使用されることになります。</span><span class="sxs-lookup"><span data-stu-id="51fab-129">Setting these attributes to zero means that the <xref:System.Runtime.Caching.MemoryCache> autosizing heuristics are used by default.</span></span> <span data-ttu-id="51fab-130">キャッシュの実装では、現在のメモリ負荷と絶対およびパーセントのメモリ制限を 2 分ごとに比較する必要があります。</span><span class="sxs-lookup"><span data-stu-id="51fab-130">The cache implementation should compare the current memory load against the absolute and percentage-based memory limits every two minutes.</span></span>  
  
```xml  
<configuration>  
  <system.runtime.caching>  
    <memoryCache>  
      <namedCaches>  
          <add name="default"   
               cacheMemoryLimitMegabytes="0"   
               physicalMemoryLimitPercentage="0"  
               pollingInterval="00:02:00" />  
      </namedCaches>  
    </memoryCache>  
  </system.runtime.caching>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="51fab-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="51fab-131">See Also</span></span>  
- [<span data-ttu-id="51fab-132">\<memoryCache > 要素 (キャッシュ設定)</span><span class="sxs-lookup"><span data-stu-id="51fab-132">\<memoryCache> Element (Cache Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/memorycache-element-cache-settings.md)
