---
title: <entries>
ms.date: 03/30/2017
ms.assetid: 202e430c-c1b9-4343-abe2-ac78c181a3b7
ms.openlocfilehash: 9c4c7fa4f778642d549deebce6e7476f4da13a0d
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55283687"
---
# <a name="entries"></a><span data-ttu-id="422fb-101">\<entries></span><span class="sxs-lookup"><span data-stu-id="422fb-101">\<entries></span></span>
<span data-ttu-id="422fb-102">ルーティング フィルターとターゲット エンドポイントとのマッピングを格納するルーティング エントリ。フィルターが一致したときにメッセージを送信するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="422fb-102">A routing entry that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
 <span data-ttu-id="422fb-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="422fb-103">\<system.serviceModel></span></span>  
<span data-ttu-id="422fb-104">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="422fb-104">\<routing></span></span>  
<span data-ttu-id="422fb-105">\<routingTables></span><span class="sxs-lookup"><span data-stu-id="422fb-105">\<routingTables></span></span>  
<span data-ttu-id="422fb-106">\<table></span><span class="sxs-lookup"><span data-stu-id="422fb-106">\<table></span></span>  
<span data-ttu-id="422fb-107">\<entries></span><span class="sxs-lookup"><span data-stu-id="422fb-107">\<entries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="422fb-108">構文</span><span class="sxs-lookup"><span data-stu-id="422fb-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="422fb-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="422fb-109">Attributes and Elements</span></span>  
 <span data-ttu-id="422fb-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="422fb-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="422fb-111">属性</span><span class="sxs-lookup"><span data-stu-id="422fb-111">Attributes</span></span>  
 <span data-ttu-id="422fb-112">なし。</span><span class="sxs-lookup"><span data-stu-id="422fb-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="422fb-113">子要素</span><span class="sxs-lookup"><span data-stu-id="422fb-113">Child Elements</span></span>  
  
|<span data-ttu-id="422fb-114">要素</span><span class="sxs-lookup"><span data-stu-id="422fb-114">Element</span></span>|<span data-ttu-id="422fb-115">説明</span><span class="sxs-lookup"><span data-stu-id="422fb-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="422fb-116">\<filters></span><span class="sxs-lookup"><span data-stu-id="422fb-116">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="422fb-117">以前に定義されたクライアント エンドポイントにフィルターをマップします。</span><span class="sxs-lookup"><span data-stu-id="422fb-117">Maps a filter to a client endpoint that was previously defined.</span></span> <span data-ttu-id="422fb-118">このフィルターに一致するメッセージは、この宛先に送信されます。</span><span class="sxs-lookup"><span data-stu-id="422fb-118">Messages matching this filter will be sent to this destination.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="422fb-119">親要素</span><span class="sxs-lookup"><span data-stu-id="422fb-119">Parent Elements</span></span>  
  
|<span data-ttu-id="422fb-120">要素</span><span class="sxs-lookup"><span data-stu-id="422fb-120">Element</span></span>|<span data-ttu-id="422fb-121">説明</span><span class="sxs-lookup"><span data-stu-id="422fb-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="422fb-122">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="422fb-122">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="422fb-123">ルーティング テーブルを含む構成セクション。</span><span class="sxs-lookup"><span data-stu-id="422fb-123">A configuration section that contains a routing table.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="422fb-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="422fb-124">See also</span></span>
- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType>
