---
title: '&lt;entries&gt; の &lt;add&gt;'
ms.date: 03/30/2017
ms.assetid: 3af4805b-dc72-4f68-b168-da4fba8c6170
ms.openlocfilehash: 5a61aefd92390eefb95d1f3e39236e53fa264990
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151504"
---
# <a name="ltaddgt-of-ltentriesgt"></a><span data-ttu-id="231a2-102">&lt;entries&gt; の &lt;add&gt;</span><span class="sxs-lookup"><span data-stu-id="231a2-102">&lt;add&gt; of &lt;entries&gt;</span></span>
<span data-ttu-id="231a2-103">以前に定義されたクライアント エンドポイントにフィルターをマップするルーティング エントリを表します。</span><span class="sxs-lookup"><span data-stu-id="231a2-103">Represents a routing entry that maps a filter to a client endpoint that was previously defined.</span></span> <span data-ttu-id="231a2-104">このフィルターに一致するメッセージは、この宛先に送信されます。</span><span class="sxs-lookup"><span data-stu-id="231a2-104">Messages matching this filter will be sent to this destination.</span></span>  
  
 <span data-ttu-id="231a2-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="231a2-105">\<system.serviceModel></span></span>  
<span data-ttu-id="231a2-106">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="231a2-106">\<routing></span></span>  
<span data-ttu-id="231a2-107">\<filterTables ></span><span class="sxs-lookup"><span data-stu-id="231a2-107">\<filterTables></span></span>  
<span data-ttu-id="231a2-108">\<filterTable ></span><span class="sxs-lookup"><span data-stu-id="231a2-108">\<filterTable></span></span>  
<span data-ttu-id="231a2-109">\<エントリ ></span><span class="sxs-lookup"><span data-stu-id="231a2-109">\<entries></span></span>  
<span data-ttu-id="231a2-110">\<add></span><span class="sxs-lookup"><span data-stu-id="231a2-110">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="231a2-111">構文</span><span class="sxs-lookup"><span data-stu-id="231a2-111">Syntax</span></span>  
  
```xml  
<routing>
  <filterTables>
    <filterTable name="String">
      <entries>
        <add backupList="String"
             endpointName="String"
             filterName="String"
             priority="Integer" />
      </entries>
    </filterTable>
  </filterTables>
</routing>
```  
  
```csharp  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="231a2-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="231a2-112">Attributes and Elements</span></span>  
 <span data-ttu-id="231a2-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="231a2-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="231a2-114">属性</span><span class="sxs-lookup"><span data-stu-id="231a2-114">Attributes</span></span>  
  
|<span data-ttu-id="231a2-115">属性</span><span class="sxs-lookup"><span data-stu-id="231a2-115">Attribute</span></span>|<span data-ttu-id="231a2-116">説明</span><span class="sxs-lookup"><span data-stu-id="231a2-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="231a2-117">backupList</span><span class="sxs-lookup"><span data-stu-id="231a2-117">backupList</span></span>|<span data-ttu-id="231a2-118">エンドポイントのバックアップ リストへの参照を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="231a2-118">A string that specifies a reference to a backup list of endpoints.</span></span>|  
|<span data-ttu-id="231a2-119">エンドポイント</span><span class="sxs-lookup"><span data-stu-id="231a2-119">endpoint</span></span>|<span data-ttu-id="231a2-120">`filterName` 属性で指定されたフィルターに一致するメッセージを受信するクライアント エンドポイントへの参照を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="231a2-120">A string that specifies a reference to a client endpoint that will receive messages that match the filter specified by the `filterName` attribute.</span></span>|  
|<span data-ttu-id="231a2-121">filterName</span><span class="sxs-lookup"><span data-stu-id="231a2-121">filterName</span></span>|<span data-ttu-id="231a2-122">フィルター要素への参照を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="231a2-122">A string that specifies a reference to a filter element.</span></span>|  
|<span data-ttu-id="231a2-123">priority</span><span class="sxs-lookup"><span data-stu-id="231a2-123">priority</span></span>|<span data-ttu-id="231a2-124">このエントリの優先順位を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="231a2-124">An integer that specifies the priority of this entry.</span></span><br /><br /> <span data-ttu-id="231a2-125">ルーティング テーブルのエントリは、優先順位に基づいて評価されます。0 が最下位の優先順位です。</span><span class="sxs-lookup"><span data-stu-id="231a2-125">Entries in the routing table will be evaluated based on priority, with 0 being the lowest priority.</span></span> <span data-ttu-id="231a2-126">特定の優先順位について、すべてのエントリが同時に評価されます。現在の優先順位について一致するエントリが見つからない場合は、次の優先順位が評価されます。</span><span class="sxs-lookup"><span data-stu-id="231a2-126">All entries for a specific priority are evaluated simultaneously, if no matching entry is found for the current priority, the next priority level will be evaluated.</span></span><br /><br /> <span data-ttu-id="231a2-127">この値はオプションです。</span><span class="sxs-lookup"><span data-stu-id="231a2-127">This value is optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="231a2-128">子要素</span><span class="sxs-lookup"><span data-stu-id="231a2-128">Child Elements</span></span>  
 <span data-ttu-id="231a2-129">なし。</span><span class="sxs-lookup"><span data-stu-id="231a2-129">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="231a2-130">親要素</span><span class="sxs-lookup"><span data-stu-id="231a2-130">Parent Elements</span></span>  
  
|<span data-ttu-id="231a2-131">要素</span><span class="sxs-lookup"><span data-stu-id="231a2-131">Element</span></span>|<span data-ttu-id="231a2-132">説明</span><span class="sxs-lookup"><span data-stu-id="231a2-132">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="231a2-133">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="231a2-133">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="231a2-134">ルーティング マッピング エントリを含む構成セクション。</span><span class="sxs-lookup"><span data-stu-id="231a2-134">A configuration section that contains routing mapping entries.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="231a2-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="231a2-135">See Also</span></span>  
 <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>      
 <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType> 
