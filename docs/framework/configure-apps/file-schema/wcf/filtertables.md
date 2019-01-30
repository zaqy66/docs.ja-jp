---
title: <filterTables>
ms.date: 03/30/2017
ms.assetid: 41f1ac35-f559-473a-b2c3-8cc83a6a3831
ms.openlocfilehash: a54386de369a11a1958e4d81ab01f053a0bc5b36
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55253978"
---
# <a name="filtertables"></a><span data-ttu-id="078b7-101">\<filterTables></span><span class="sxs-lookup"><span data-stu-id="078b7-101">\<filterTables></span></span>
<span data-ttu-id="078b7-102">ルーティング フィルターとターゲット エンドポイントとのマッピングを格納するルーティング テーブルを定義する構成セクションを表します。フィルターが一致したときにメッセージを送信するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="078b7-102">Represents a configuration section for defining routing tables that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
 <span data-ttu-id="078b7-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="078b7-103">\<system.serviceModel></span></span>  
<span data-ttu-id="078b7-104">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="078b7-104">\<routing></span></span>  
<span data-ttu-id="078b7-105">\<routingTables></span><span class="sxs-lookup"><span data-stu-id="078b7-105">\<routingTables></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="078b7-106">構文</span><span class="sxs-lookup"><span data-stu-id="078b7-106">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="078b7-107">属性および要素</span><span class="sxs-lookup"><span data-stu-id="078b7-107">Attributes and Elements</span></span>  
 <span data-ttu-id="078b7-108">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="078b7-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="078b7-109">属性</span><span class="sxs-lookup"><span data-stu-id="078b7-109">Attributes</span></span>  
 <span data-ttu-id="078b7-110">なし。</span><span class="sxs-lookup"><span data-stu-id="078b7-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="078b7-111">子要素</span><span class="sxs-lookup"><span data-stu-id="078b7-111">Child Elements</span></span>  
  
|<span data-ttu-id="078b7-112">要素</span><span class="sxs-lookup"><span data-stu-id="078b7-112">Element</span></span>|<span data-ttu-id="078b7-113">説明</span><span class="sxs-lookup"><span data-stu-id="078b7-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="078b7-114">\<filters></span><span class="sxs-lookup"><span data-stu-id="078b7-114">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="078b7-115">ルーティング フィルターとターゲット エンドポイントとのマッピングを格納するルーティング テーブル。フィルターが一致したときにメッセージを送信するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="078b7-115">A routing table that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="078b7-116">親要素</span><span class="sxs-lookup"><span data-stu-id="078b7-116">Parent Elements</span></span>  
  
|<span data-ttu-id="078b7-117">要素</span><span class="sxs-lookup"><span data-stu-id="078b7-117">Element</span></span>|<span data-ttu-id="078b7-118">説明</span><span class="sxs-lookup"><span data-stu-id="078b7-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="078b7-119">\<ルーティング ></span><span class="sxs-lookup"><span data-stu-id="078b7-119">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="078b7-120">ルーティング フィルターおよびルーティング テーブルを含む構成セクション。</span><span class="sxs-lookup"><span data-stu-id="078b7-120">A configuration section that contains routing filters and routing tables.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="078b7-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="078b7-121">See also</span></span>
- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterTableCollection?displayProperty=nameWithType>
