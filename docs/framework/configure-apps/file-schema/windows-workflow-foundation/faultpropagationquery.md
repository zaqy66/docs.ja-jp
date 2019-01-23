---
title: '&lt;faultPropagationQuery&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 4fb5c2b1-3dad-4eca-9c7f-3efb51899813
ms.openlocfilehash: a91a6f61b39a780ed48ad8d5f5e0dfb9ef60da39
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54538337"
---
# <a name="ltfaultpropagationquerygt"></a><span data-ttu-id="98fdc-102">&lt;faultPropagationQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="98fdc-102">&lt;faultPropagationQuery&gt;</span></span>
<span data-ttu-id="98fdc-103">1 つのアクティビティ内で発生するエラーの処理を追跡するために使用するクエリを表します。</span><span class="sxs-lookup"><span data-stu-id="98fdc-103">Represents a query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="98fdc-104">このイベントは、FaultHandler がエラーを処理するたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="98fdc-104">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="98fdc-105">1 つのアクティビティ内で発生したエラーの処理は、このようなクエリを使用して追跡する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98fdc-105">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="98fdc-106">追跡参加要素がエラー伝達レコードを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="98fdc-106">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
 <span data-ttu-id="98fdc-107">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="98fdc-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="98fdc-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="98fdc-108">\<system.serviceModel></span></span>  
<span data-ttu-id="98fdc-109">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="98fdc-109">\<tracking></span></span>  
<span data-ttu-id="98fdc-110">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="98fdc-110">\<trackingProfile></span></span>  
<span data-ttu-id="98fdc-111">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="98fdc-111">\<workflow></span></span>  
<span data-ttu-id="98fdc-112">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="98fdc-112">\<faultPropagationQueries></span></span>  
<span data-ttu-id="98fdc-113">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="98fdc-113">\<faultPropagationQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="98fdc-114">構文</span><span class="sxs-lookup"><span data-stu-id="98fdc-114">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <faultPropagationQueries>
        <faultPropagationQuery activityName="String" 
                               faultHandlerActivityName="String" />
      </faultPropagationQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="98fdc-115">属性および要素</span><span class="sxs-lookup"><span data-stu-id="98fdc-115">Attributes and Elements</span></span>  
 <span data-ttu-id="98fdc-116">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="98fdc-116">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="98fdc-117">属性</span><span class="sxs-lookup"><span data-stu-id="98fdc-117">Attributes</span></span>  
  
|<span data-ttu-id="98fdc-118">属性</span><span class="sxs-lookup"><span data-stu-id="98fdc-118">Attribute</span></span>|<span data-ttu-id="98fdc-119">説明</span><span class="sxs-lookup"><span data-stu-id="98fdc-119">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="98fdc-120">activityName</span><span class="sxs-lookup"><span data-stu-id="98fdc-120">activityName</span></span>|<span data-ttu-id="98fdc-121">エラーを伝達したエラー ハンドラー アクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="98fdc-121">A string that specifies the name of the fault hander activity that propagated the fault.</span></span> <span data-ttu-id="98fdc-122">既定値は \* で、すべてのアクティビティについてエラー伝達レコードが返されることを示します。</span><span class="sxs-lookup"><span data-stu-id="98fdc-122">The default is \*, which indicates that fault propagation records are returned for all activities.</span></span>|  
|<span data-ttu-id="98fdc-123">faultHandlerActivityName</span><span class="sxs-lookup"><span data-stu-id="98fdc-123">faultHandlerActivityName</span></span>|<span data-ttu-id="98fdc-124">エラーの原因となったアクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="98fdc-124">A string that specifies the name of the activity that was the source of the fault.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="98fdc-125">子要素</span><span class="sxs-lookup"><span data-stu-id="98fdc-125">Child Elements</span></span>  
 <span data-ttu-id="98fdc-126">なし。</span><span class="sxs-lookup"><span data-stu-id="98fdc-126">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="98fdc-127">親要素</span><span class="sxs-lookup"><span data-stu-id="98fdc-127">Parent Elements</span></span>  
  
|<span data-ttu-id="98fdc-128">要素</span><span class="sxs-lookup"><span data-stu-id="98fdc-128">Element</span></span>|<span data-ttu-id="98fdc-129">説明</span><span class="sxs-lookup"><span data-stu-id="98fdc-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="98fdc-130">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="98fdc-130">\<faultPropagationQueries></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationqueries.md)|<span data-ttu-id="98fdc-131">1 つのアクティビティ内で発生するエラーの処理を追跡するために使用する、構成要素の一覧を表します。</span><span class="sxs-lookup"><span data-stu-id="98fdc-131">Represents a list of configuration elements that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="98fdc-132">このイベントは、FaultHandler がエラーを処理するたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="98fdc-132">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="98fdc-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="98fdc-133">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="98fdc-134">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="98fdc-134">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="98fdc-135">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="98fdc-135">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
