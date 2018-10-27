---
title: '&lt;設定&gt;要素 (ネットワーク設定)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#settings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings
helpviewer_keywords:
- settings element
- <settings> element
ms.assetid: 189ce989-c39b-427d-b004-6b82a668b931
ms.openlocfilehash: 87a944eca6ea4158f15c9911c6b13fd4d3c0921d
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50191954"
---
# <a name="ltsettingsgt-element-network-settings"></a><span data-ttu-id="01ba1-102">&lt;設定&gt;要素 (ネットワーク設定)</span><span class="sxs-lookup"><span data-stu-id="01ba1-102">&lt;settings&gt; Element (Network Settings)</span></span>
<span data-ttu-id="01ba1-103"><xref:System.Net?displayProperty=nameWithType> 名前空間の基本的なネットワーク オプションを構成します。</span><span class="sxs-lookup"><span data-stu-id="01ba1-103">Configures basic network options for the <xref:System.Net?displayProperty=nameWithType> namespace.</span></span>  
  
 <span data-ttu-id="01ba1-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="01ba1-104">\<configuration></span></span>  
<span data-ttu-id="01ba1-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="01ba1-105">\<system.net></span></span>  
<span data-ttu-id="01ba1-106">\<settings></span><span class="sxs-lookup"><span data-stu-id="01ba1-106">\<settings></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="01ba1-107">構文</span><span class="sxs-lookup"><span data-stu-id="01ba1-107">Syntax</span></span>  
  
```xml  
<settings>  
  <httpListener> … </httpListener>  
  <httpWebRequest> … </httpWebRequest>  
  <ipv6> … </ipv6>  
  <performanceCounters> … </performanceCounters>  
  <servicePointManager> … </servicePointManager>  
  <socket> … </socket>  
  <webProxyScript> … </webProxyScript>  
</settings>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="01ba1-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="01ba1-108">Attributes and Elements</span></span>  
 <span data-ttu-id="01ba1-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="01ba1-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="01ba1-110">属性</span><span class="sxs-lookup"><span data-stu-id="01ba1-110">Attributes</span></span>  
 <span data-ttu-id="01ba1-111">なし。</span><span class="sxs-lookup"><span data-stu-id="01ba1-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="01ba1-112">子要素</span><span class="sxs-lookup"><span data-stu-id="01ba1-112">Child Elements</span></span>  
  
|<span data-ttu-id="01ba1-113">要素</span><span class="sxs-lookup"><span data-stu-id="01ba1-113">Element</span></span>|<span data-ttu-id="01ba1-114">説明</span><span class="sxs-lookup"><span data-stu-id="01ba1-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="01ba1-115">httpListener</span><span class="sxs-lookup"><span data-stu-id="01ba1-115">httpListener</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/httplistener-element-network-settings.md)|<span data-ttu-id="01ba1-116">によって使用されるパラメーターのカスタマイズ、<xref:System.Net.HttpListener>クラス。</span><span class="sxs-lookup"><span data-stu-id="01ba1-116">Customizes parameters used by the <xref:System.Net.HttpListener> class.</span></span>|  
|[<span data-ttu-id="01ba1-117">httpWebRequest</span><span class="sxs-lookup"><span data-stu-id="01ba1-117">httpWebRequest</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/httpwebrequest-element-network-settings.md)|<span data-ttu-id="01ba1-118">Web 要求のパラメーターをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="01ba1-118">Customizes Web request parameters.</span></span>|  
|[<span data-ttu-id="01ba1-119">ipv6</span><span class="sxs-lookup"><span data-stu-id="01ba1-119">ipv6</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/ipv6-element-network-settings.md)|<span data-ttu-id="01ba1-120">により、インターネット プロトコル バージョン 6 (IPv6) をサポートします。</span><span class="sxs-lookup"><span data-stu-id="01ba1-120">Enables Internet Protocol version 6 (IPv6) support.</span></span>|  
|[<span data-ttu-id="01ba1-121">\<performanceCounter > 要素 (ネットワーク設定)</span><span class="sxs-lookup"><span data-stu-id="01ba1-121">\<performanceCounter> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/performancecounter-element-network-settings.md)|<span data-ttu-id="01ba1-122">ネットワーク パフォーマンス カウンターを有効にします。</span><span class="sxs-lookup"><span data-stu-id="01ba1-122">Enables network performance counters.</span></span>|  
|[<span data-ttu-id="01ba1-123">servicePointManager</span><span class="sxs-lookup"><span data-stu-id="01ba1-123">servicePointManager</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/servicepointmanager-element-network-settings.md)|<span data-ttu-id="01ba1-124">ネットワーク リソースへの接続を構成します。</span><span class="sxs-lookup"><span data-stu-id="01ba1-124">Configures connections to network resources.</span></span>|  
|[<span data-ttu-id="01ba1-125">ソケット</span><span class="sxs-lookup"><span data-stu-id="01ba1-125">socket</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/socket-element-network-settings.md)|<span data-ttu-id="01ba1-126">ソケット操作が完了ポートを使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="01ba1-126">Specifies whether socket operations use completion ports.</span></span>|  
|[<span data-ttu-id="01ba1-127">\<webProxyScript > 要素 (ネットワーク設定)</span><span class="sxs-lookup"><span data-stu-id="01ba1-127">\<webProxyScript> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/webproxyscript-element-network-settings.md)|<span data-ttu-id="01ba1-128">Web プロキシを検出するために使用するスクリプトの特性を構成します。</span><span class="sxs-lookup"><span data-stu-id="01ba1-128">Configures the characteristics of the script used to discover Web proxies.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="01ba1-129">親要素</span><span class="sxs-lookup"><span data-stu-id="01ba1-129">Parent Elements</span></span>  
  
|<span data-ttu-id="01ba1-130">要素</span><span class="sxs-lookup"><span data-stu-id="01ba1-130">Element</span></span>|<span data-ttu-id="01ba1-131">説明</span><span class="sxs-lookup"><span data-stu-id="01ba1-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="01ba1-132">system.net</span><span class="sxs-lookup"><span data-stu-id="01ba1-132">system.net</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="01ba1-133">.NET Framework がネットワークに接続する方法を指定するための設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="01ba1-133">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="01ba1-134">Remarks</span><span class="sxs-lookup"><span data-stu-id="01ba1-134">Remarks</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="01ba1-135">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="01ba1-135">Configuration Files</span></span>  
 <span data-ttu-id="01ba1-136">この要素は、アプリケーション構成ファイルまたはマシン構成ファイル (Machine.config) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="01ba1-136">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01ba1-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="01ba1-137">See Also</span></span>  
- <xref:System.Net?displayProperty=nameWithType>  
- [<span data-ttu-id="01ba1-138">ネットワーク設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="01ba1-138">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
