---
title: '&lt;エントリ&gt;'
ms.date: 03/30/2017
ms.assetid: 202e430c-c1b9-4343-abe2-ac78c181a3b7
ms.openlocfilehash: 8c442990ee736c17b71b625e06d961230a8ceed2
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146434"
---
# <a name="ltentriesgt"></a><span data-ttu-id="29b18-102">&lt;エントリ&gt;</span><span class="sxs-lookup"><span data-stu-id="29b18-102">&lt;entries&gt;</span></span>
<span data-ttu-id="29b18-103">ルーティング フィルターとターゲット エンドポイントとのマッピングを格納するルーティング エントリ。フィルターが一致したときにメッセージを送信するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="29b18-103">A routing entry that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
 <span data-ttu-id="29b18-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="29b18-104">\<system.serviceModel></span></span>  
<span data-ttu-id="29b18-105">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="29b18-105">\<routing></span></span>  
<span data-ttu-id="29b18-106">\<routingTables ></span><span class="sxs-lookup"><span data-stu-id="29b18-106">\<routingTables></span></span>  
<span data-ttu-id="29b18-107">\<テーブル ></span><span class="sxs-lookup"><span data-stu-id="29b18-107">\<table></span></span>  
<span data-ttu-id="29b18-108">\<エントリ ></span><span class="sxs-lookup"><span data-stu-id="29b18-108">\<entries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="29b18-109">構文</span><span class="sxs-lookup"><span data-stu-id="29b18-109">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="29b18-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="29b18-110">Attributes and Elements</span></span>  
 <span data-ttu-id="29b18-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="29b18-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="29b18-112">属性</span><span class="sxs-lookup"><span data-stu-id="29b18-112">Attributes</span></span>  
 <span data-ttu-id="29b18-113">なし。</span><span class="sxs-lookup"><span data-stu-id="29b18-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="29b18-114">子要素</span><span class="sxs-lookup"><span data-stu-id="29b18-114">Child Elements</span></span>  
  
|<span data-ttu-id="29b18-115">要素</span><span class="sxs-lookup"><span data-stu-id="29b18-115">Element</span></span>|<span data-ttu-id="29b18-116">説明</span><span class="sxs-lookup"><span data-stu-id="29b18-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="29b18-117">\<フィルター ></span><span class="sxs-lookup"><span data-stu-id="29b18-117">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="29b18-118">以前に定義されたクライアント エンドポイントにフィルターをマップします。</span><span class="sxs-lookup"><span data-stu-id="29b18-118">Maps a filter to a client endpoint that was previously defined.</span></span> <span data-ttu-id="29b18-119">このフィルターに一致するメッセージは、この宛先に送信されます。</span><span class="sxs-lookup"><span data-stu-id="29b18-119">Messages matching this filter will be sent to this destination.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="29b18-120">親要素</span><span class="sxs-lookup"><span data-stu-id="29b18-120">Parent Elements</span></span>  
  
|<span data-ttu-id="29b18-121">要素</span><span class="sxs-lookup"><span data-stu-id="29b18-121">Element</span></span>|<span data-ttu-id="29b18-122">説明</span><span class="sxs-lookup"><span data-stu-id="29b18-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="29b18-123">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="29b18-123">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="29b18-124">ルーティング テーブルを含む構成セクション。</span><span class="sxs-lookup"><span data-stu-id="29b18-124">A configuration section that contains a routing table.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="29b18-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="29b18-125">See Also</span></span>  
 <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>       
 <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType>    
