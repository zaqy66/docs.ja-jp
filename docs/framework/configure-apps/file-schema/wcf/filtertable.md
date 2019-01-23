---
title: '&lt;filterTable&gt;'
ms.date: 03/30/2017
ms.assetid: e9f05441-3ad1-49b9-a267-71724aa094b4
ms.openlocfilehash: 83339eebef9a4f1b7f69e0bd1dd16b8278a68258
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54534606"
---
# <a name="ltfiltertablegt"></a><span data-ttu-id="ee0b6-102">&lt;filterTable&gt;</span><span class="sxs-lookup"><span data-stu-id="ee0b6-102">&lt;filterTable&gt;</span></span>
<span data-ttu-id="ee0b6-103">フィルターが true に評価された場合、メッセージと照合し、クライアントのエンドポイントにメッセージをルーティングを評価するフィルターの一覧を含むルーティング テーブルを表します。</span><span class="sxs-lookup"><span data-stu-id="ee0b6-103">Represents a routing table that contains a list of filters to evaluate messages against and the client endpoint to route messages to if the filter evaluates to true.</span></span>  
  
 <span data-ttu-id="ee0b6-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="ee0b6-104">\<system.serviceModel></span></span>  
<span data-ttu-id="ee0b6-105">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="ee0b6-105">\<routing></span></span>  
<span data-ttu-id="ee0b6-106">\<routingTables></span><span class="sxs-lookup"><span data-stu-id="ee0b6-106">\<routingTables></span></span>  
<span data-ttu-id="ee0b6-107">\<table></span><span class="sxs-lookup"><span data-stu-id="ee0b6-107">\<table></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ee0b6-108">構文</span><span class="sxs-lookup"><span data-stu-id="ee0b6-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ee0b6-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="ee0b6-109">Attributes and Elements</span></span>  
 <span data-ttu-id="ee0b6-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="ee0b6-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ee0b6-111">属性</span><span class="sxs-lookup"><span data-stu-id="ee0b6-111">Attributes</span></span>  
  
|<span data-ttu-id="ee0b6-112">要素</span><span class="sxs-lookup"><span data-stu-id="ee0b6-112">Element</span></span>|<span data-ttu-id="ee0b6-113">説明</span><span class="sxs-lookup"><span data-stu-id="ee0b6-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ee0b6-114">name</span><span class="sxs-lookup"><span data-stu-id="ee0b6-114">name</span></span>|<span data-ttu-id="ee0b6-115">この構成要素の一意の名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="ee0b6-115">A string that contains the unique name of this configuration element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ee0b6-116">子要素</span><span class="sxs-lookup"><span data-stu-id="ee0b6-116">Child Elements</span></span>  
  
|<span data-ttu-id="ee0b6-117">要素</span><span class="sxs-lookup"><span data-stu-id="ee0b6-117">Element</span></span>|<span data-ttu-id="ee0b6-118">説明</span><span class="sxs-lookup"><span data-stu-id="ee0b6-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ee0b6-119">\<filters></span><span class="sxs-lookup"><span data-stu-id="ee0b6-119">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="ee0b6-120">ルーティング フィルターとターゲット エンドポイントとのマッピング。フィルターが一致したときにメッセージを送信するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee0b6-120">Mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ee0b6-121">親要素</span><span class="sxs-lookup"><span data-stu-id="ee0b6-121">Parent Elements</span></span>  
  
|<span data-ttu-id="ee0b6-122">要素</span><span class="sxs-lookup"><span data-stu-id="ee0b6-122">Element</span></span>|<span data-ttu-id="ee0b6-123">説明</span><span class="sxs-lookup"><span data-stu-id="ee0b6-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ee0b6-124">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="ee0b6-124">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="ee0b6-125">ルーティング テーブルを含む構成セクション。</span><span class="sxs-lookup"><span data-stu-id="ee0b6-125">A configuration section that contains routing tables.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ee0b6-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="ee0b6-126">See also</span></span>
- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
