---
title: <filterTable>
ms.date: 03/30/2017
ms.assetid: e9f05441-3ad1-49b9-a267-71724aa094b4
ms.openlocfilehash: ba65d3858cdbdf6b49c50e60f4e3cc9624fef136
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55254406"
---
# <a name="filtertable"></a><span data-ttu-id="78b56-101">\<filterTable></span><span class="sxs-lookup"><span data-stu-id="78b56-101">\<filterTable></span></span>
<span data-ttu-id="78b56-102">フィルターが true に評価された場合、メッセージと照合し、クライアントのエンドポイントにメッセージをルーティングを評価するフィルターの一覧を含むルーティング テーブルを表します。</span><span class="sxs-lookup"><span data-stu-id="78b56-102">Represents a routing table that contains a list of filters to evaluate messages against and the client endpoint to route messages to if the filter evaluates to true.</span></span>  
  
 <span data-ttu-id="78b56-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="78b56-103">\<system.serviceModel></span></span>  
<span data-ttu-id="78b56-104">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="78b56-104">\<routing></span></span>  
<span data-ttu-id="78b56-105">\<routingTables></span><span class="sxs-lookup"><span data-stu-id="78b56-105">\<routingTables></span></span>  
<span data-ttu-id="78b56-106">\<table></span><span class="sxs-lookup"><span data-stu-id="78b56-106">\<table></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="78b56-107">構文</span><span class="sxs-lookup"><span data-stu-id="78b56-107">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="78b56-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="78b56-108">Attributes and Elements</span></span>  
 <span data-ttu-id="78b56-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="78b56-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="78b56-110">属性</span><span class="sxs-lookup"><span data-stu-id="78b56-110">Attributes</span></span>  
  
|<span data-ttu-id="78b56-111">要素</span><span class="sxs-lookup"><span data-stu-id="78b56-111">Element</span></span>|<span data-ttu-id="78b56-112">説明</span><span class="sxs-lookup"><span data-stu-id="78b56-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="78b56-113">name</span><span class="sxs-lookup"><span data-stu-id="78b56-113">name</span></span>|<span data-ttu-id="78b56-114">この構成要素の一意の名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="78b56-114">A string that contains the unique name of this configuration element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="78b56-115">子要素</span><span class="sxs-lookup"><span data-stu-id="78b56-115">Child Elements</span></span>  
  
|<span data-ttu-id="78b56-116">要素</span><span class="sxs-lookup"><span data-stu-id="78b56-116">Element</span></span>|<span data-ttu-id="78b56-117">説明</span><span class="sxs-lookup"><span data-stu-id="78b56-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="78b56-118">\<filters></span><span class="sxs-lookup"><span data-stu-id="78b56-118">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="78b56-119">ルーティング フィルターとターゲット エンドポイントとのマッピング。フィルターが一致したときにメッセージを送信するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="78b56-119">Mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="78b56-120">親要素</span><span class="sxs-lookup"><span data-stu-id="78b56-120">Parent Elements</span></span>  
  
|<span data-ttu-id="78b56-121">要素</span><span class="sxs-lookup"><span data-stu-id="78b56-121">Element</span></span>|<span data-ttu-id="78b56-122">説明</span><span class="sxs-lookup"><span data-stu-id="78b56-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="78b56-123">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="78b56-123">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="78b56-124">ルーティング テーブルを含む構成セクション。</span><span class="sxs-lookup"><span data-stu-id="78b56-124">A configuration section that contains routing tables.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="78b56-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="78b56-125">See also</span></span>
- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
