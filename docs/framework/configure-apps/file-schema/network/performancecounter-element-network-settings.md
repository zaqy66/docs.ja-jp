---
title: '&lt;performanceCounter&gt;要素 (ネットワーク設定)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings/performanceCounters
- http://schemas.microsoft.com/.NetConfiguration/v2.0#performanceCounters
helpviewer_keywords:
- performanceCounter element
- <performanceCounter> element
ms.assetid: 3afa1586-e1b8-473d-8985-c3fc90cf561b
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 564cef8ae53bf4a455a2e8032a296aa36e309917
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43402200"
---
# <a name="ltperformancecountergt-element-network-settings"></a><span data-ttu-id="0fc77-102">&lt;performanceCounter&gt;要素 (ネットワーク設定)</span><span class="sxs-lookup"><span data-stu-id="0fc77-102">&lt;performanceCounter&gt; Element (Network Settings)</span></span>
<span data-ttu-id="0fc77-103">有効または、ネットワーク パフォーマンス カウンターを無効にします。</span><span class="sxs-lookup"><span data-stu-id="0fc77-103">Enables or disables networking performance counters.</span></span>  
  
 <span data-ttu-id="0fc77-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="0fc77-104">\<configuration></span></span>  
<span data-ttu-id="0fc77-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="0fc77-105">\<system.net></span></span>  
<span data-ttu-id="0fc77-106">\<settings></span><span class="sxs-lookup"><span data-stu-id="0fc77-106">\<settings></span></span>  
<span data-ttu-id="0fc77-107">\<performanceCounters></span><span class="sxs-lookup"><span data-stu-id="0fc77-107">\<performanceCounters></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0fc77-108">構文</span><span class="sxs-lookup"><span data-stu-id="0fc77-108">Syntax</span></span>  
  
```xml  
<performanceCounters  
  enabled="true|false"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0fc77-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="0fc77-109">Attributes and Elements</span></span>  
 <span data-ttu-id="0fc77-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="0fc77-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0fc77-111">属性</span><span class="sxs-lookup"><span data-stu-id="0fc77-111">Attributes</span></span>  
  
|<span data-ttu-id="0fc77-112">属性</span><span class="sxs-lookup"><span data-stu-id="0fc77-112">Attribute</span></span>|<span data-ttu-id="0fc77-113">説明</span><span class="sxs-lookup"><span data-stu-id="0fc77-113">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="0fc77-114">ネットワークのパフォーマンス カウンターが有効になっているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="0fc77-114">Specifies whether the networking performance counters are enabled.</span></span> <span data-ttu-id="0fc77-115">既定値は `false` です。</span><span class="sxs-lookup"><span data-stu-id="0fc77-115">The default value is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0fc77-116">子要素</span><span class="sxs-lookup"><span data-stu-id="0fc77-116">Child Elements</span></span>  
 <span data-ttu-id="0fc77-117">なし。</span><span class="sxs-lookup"><span data-stu-id="0fc77-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0fc77-118">親要素</span><span class="sxs-lookup"><span data-stu-id="0fc77-118">Parent Elements</span></span>  
  
|<span data-ttu-id="0fc77-119">要素</span><span class="sxs-lookup"><span data-stu-id="0fc77-119">Element</span></span>|<span data-ttu-id="0fc77-120">説明</span><span class="sxs-lookup"><span data-stu-id="0fc77-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0fc77-121">settings</span><span class="sxs-lookup"><span data-stu-id="0fc77-121">settings</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/settings-element-network-settings.md)|<span data-ttu-id="0fc77-122"><xref:System.Net> 名前空間の基本的なネットワーク オプションを構成します。</span><span class="sxs-lookup"><span data-stu-id="0fc77-122">Configures basic network options for the <xref:System.Net> namespace.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0fc77-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="0fc77-123">Remarks</span></span>  
 <span data-ttu-id="0fc77-124">この要素は、アプリケーション構成ファイルまたはマシン構成ファイル (Machine.config) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="0fc77-124">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
 <span data-ttu-id="0fc77-125">ネットワーク パフォーマンス カウンターは、使用される構成ファイルで有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fc77-125">Networking performance counters need to be enabled in the configuration file to be used.</span></span> <span data-ttu-id="0fc77-126">すべてのネットワーク パフォーマンス カウンターは、構成ファイル内の 1 つの設定で有効または無効にされます。</span><span class="sxs-lookup"><span data-stu-id="0fc77-126">All networking performance counters are enabled or disabled with a single setting in the configuration file.</span></span> <span data-ttu-id="0fc77-127">ネットワーク パフォーマンス カウンターを個別に有効または無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="0fc77-127">Individual networking performance counters cannot be enabled or disabled.</span></span> <span data-ttu-id="0fc77-128">特定のネットワーク パフォーマンス カウンターの詳細については、次を参照してください。[ネットワーク パフォーマンス カウンター](https://msdn.microsoft.com/library/d1860235-f643-46ae-846c-ff0ed8b0e3cd)します。</span><span class="sxs-lookup"><span data-stu-id="0fc77-128">For more information on the specific networking performance counters, see [Networking Performance Counters](https://msdn.microsoft.com/library/d1860235-f643-46ae-846c-ff0ed8b0e3cd).</span></span>  
  
 <span data-ttu-id="0fc77-129">既定値は、そのネットワークのパフォーマンス カウンターが無効です。</span><span class="sxs-lookup"><span data-stu-id="0fc77-129">The default value is that networking performance counters are disabled.</span></span>  
  
 <span data-ttu-id="0fc77-130"><xref:System.Net.Configuration.PerformanceCountersElement.Enabled%2A?displayProperty=nameWithType>プロパティを使用しての現在の値を取得すること、**有効になっている**該当する構成ファイルからの属性。</span><span class="sxs-lookup"><span data-stu-id="0fc77-130">The <xref:System.Net.Configuration.PerformanceCountersElement.Enabled%2A?displayProperty=nameWithType> property can be used to get the current value of the **enabled** attribute from applicable configuration files.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0fc77-131">例</span><span class="sxs-lookup"><span data-stu-id="0fc77-131">Example</span></span>  
 <span data-ttu-id="0fc77-132">次の例は、構成する方法を示します、<xref:System.Net>と関連するネットワークのパフォーマンス カウンターを有効にする名前空間。</span><span class="sxs-lookup"><span data-stu-id="0fc77-132">The following example shows how to configure the <xref:System.Net> and related namespaces to enable networking performance counters.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <settings>  
      <performanceCounters  
        enabled="true"  
      />  
    </settings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="0fc77-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="0fc77-133">See Also</span></span>  
 <xref:System.Net.Configuration.PerformanceCountersElement?displayProperty=nameWithType>  
 <xref:System.Net.Configuration.PerformanceCountersElement.Enabled%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="0fc77-134">ネットワーク設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="0fc77-134">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)  
 [<span data-ttu-id="0fc77-135">ネットワーク パフォーマンス カウンター</span><span class="sxs-lookup"><span data-stu-id="0fc77-135">Networking Performance Counters</span></span>](https://msdn.microsoft.com/library/d1860235-f643-46ae-846c-ff0ed8b0e3cd)
