---
title: '&lt;エントリ&gt;'
ms.date: 03/30/2017
ms.assetid: 202e430c-c1b9-4343-abe2-ac78c181a3b7
ms.openlocfilehash: 33f98cb4b138307622a14463ce5a3008058b6e31
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54587061"
---
# <a name="ltentriesgt"></a><span data-ttu-id="6cbbb-102">&lt;エントリ&gt;</span><span class="sxs-lookup"><span data-stu-id="6cbbb-102">&lt;entries&gt;</span></span>
<span data-ttu-id="6cbbb-103">ルーティング フィルターとターゲット エンドポイントとのマッピングを格納するルーティング エントリ。フィルターが一致したときにメッセージを送信するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6cbbb-103">A routing entry that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
 <span data-ttu-id="6cbbb-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="6cbbb-104">\<system.serviceModel></span></span>  
<span data-ttu-id="6cbbb-105">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="6cbbb-105">\<routing></span></span>  
<span data-ttu-id="6cbbb-106">\<routingTables></span><span class="sxs-lookup"><span data-stu-id="6cbbb-106">\<routingTables></span></span>  
<span data-ttu-id="6cbbb-107">\<table></span><span class="sxs-lookup"><span data-stu-id="6cbbb-107">\<table></span></span>  
<span data-ttu-id="6cbbb-108">\<entries></span><span class="sxs-lookup"><span data-stu-id="6cbbb-108">\<entries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6cbbb-109">構文</span><span class="sxs-lookup"><span data-stu-id="6cbbb-109">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6cbbb-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="6cbbb-110">Attributes and Elements</span></span>  
 <span data-ttu-id="6cbbb-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="6cbbb-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6cbbb-112">属性</span><span class="sxs-lookup"><span data-stu-id="6cbbb-112">Attributes</span></span>  
 <span data-ttu-id="6cbbb-113">なし。</span><span class="sxs-lookup"><span data-stu-id="6cbbb-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="6cbbb-114">子要素</span><span class="sxs-lookup"><span data-stu-id="6cbbb-114">Child Elements</span></span>  
  
|<span data-ttu-id="6cbbb-115">要素</span><span class="sxs-lookup"><span data-stu-id="6cbbb-115">Element</span></span>|<span data-ttu-id="6cbbb-116">説明</span><span class="sxs-lookup"><span data-stu-id="6cbbb-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6cbbb-117">\<filters></span><span class="sxs-lookup"><span data-stu-id="6cbbb-117">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="6cbbb-118">以前に定義されたクライアント エンドポイントにフィルターをマップします。</span><span class="sxs-lookup"><span data-stu-id="6cbbb-118">Maps a filter to a client endpoint that was previously defined.</span></span> <span data-ttu-id="6cbbb-119">このフィルターに一致するメッセージは、この宛先に送信されます。</span><span class="sxs-lookup"><span data-stu-id="6cbbb-119">Messages matching this filter will be sent to this destination.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6cbbb-120">親要素</span><span class="sxs-lookup"><span data-stu-id="6cbbb-120">Parent Elements</span></span>  
  
|<span data-ttu-id="6cbbb-121">要素</span><span class="sxs-lookup"><span data-stu-id="6cbbb-121">Element</span></span>|<span data-ttu-id="6cbbb-122">説明</span><span class="sxs-lookup"><span data-stu-id="6cbbb-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6cbbb-123">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="6cbbb-123">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="6cbbb-124">ルーティング テーブルを含む構成セクション。</span><span class="sxs-lookup"><span data-stu-id="6cbbb-124">A configuration section that contains a routing table.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6cbbb-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="6cbbb-125">See also</span></span>
- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType>
