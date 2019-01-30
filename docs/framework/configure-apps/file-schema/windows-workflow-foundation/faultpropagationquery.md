---
title: <faultPropagationQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 4fb5c2b1-3dad-4eca-9c7f-3efb51899813
ms.openlocfilehash: 1a6899eaa04ad16192e07f4bc2ad1abe6e4aedd5
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55257370"
---
# <a name="faultpropagationquery"></a><span data-ttu-id="50c65-101">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="50c65-101">\<faultPropagationQuery></span></span>
<span data-ttu-id="50c65-102">1 つのアクティビティ内で発生するエラーの処理を追跡するために使用するクエリを表します。</span><span class="sxs-lookup"><span data-stu-id="50c65-102">Represents a query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="50c65-103">このイベントは、FaultHandler がエラーを処理するたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="50c65-103">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="50c65-104">1 つのアクティビティ内で発生したエラーの処理は、このようなクエリを使用して追跡する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c65-104">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="50c65-105">追跡参加要素がエラー伝達レコードを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="50c65-105">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
 <span data-ttu-id="50c65-106">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="50c65-106">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="50c65-107">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="50c65-107">\<system.serviceModel></span></span>  
<span data-ttu-id="50c65-108">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="50c65-108">\<tracking></span></span>  
<span data-ttu-id="50c65-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="50c65-109">\<trackingProfile></span></span>  
<span data-ttu-id="50c65-110">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="50c65-110">\<workflow></span></span>  
<span data-ttu-id="50c65-111">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="50c65-111">\<faultPropagationQueries></span></span>  
<span data-ttu-id="50c65-112">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="50c65-112">\<faultPropagationQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="50c65-113">構文</span><span class="sxs-lookup"><span data-stu-id="50c65-113">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="50c65-114">属性および要素</span><span class="sxs-lookup"><span data-stu-id="50c65-114">Attributes and Elements</span></span>  
 <span data-ttu-id="50c65-115">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="50c65-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="50c65-116">属性</span><span class="sxs-lookup"><span data-stu-id="50c65-116">Attributes</span></span>  
  
|<span data-ttu-id="50c65-117">属性</span><span class="sxs-lookup"><span data-stu-id="50c65-117">Attribute</span></span>|<span data-ttu-id="50c65-118">説明</span><span class="sxs-lookup"><span data-stu-id="50c65-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="50c65-119">activityName</span><span class="sxs-lookup"><span data-stu-id="50c65-119">activityName</span></span>|<span data-ttu-id="50c65-120">エラーを伝達したエラー ハンドラー アクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="50c65-120">A string that specifies the name of the fault hander activity that propagated the fault.</span></span> <span data-ttu-id="50c65-121">既定値は \* で、すべてのアクティビティについてエラー伝達レコードが返されることを示します。</span><span class="sxs-lookup"><span data-stu-id="50c65-121">The default is \*, which indicates that fault propagation records are returned for all activities.</span></span>|  
|<span data-ttu-id="50c65-122">faultHandlerActivityName</span><span class="sxs-lookup"><span data-stu-id="50c65-122">faultHandlerActivityName</span></span>|<span data-ttu-id="50c65-123">エラーの原因となったアクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="50c65-123">A string that specifies the name of the activity that was the source of the fault.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="50c65-124">子要素</span><span class="sxs-lookup"><span data-stu-id="50c65-124">Child Elements</span></span>  
 <span data-ttu-id="50c65-125">なし。</span><span class="sxs-lookup"><span data-stu-id="50c65-125">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="50c65-126">親要素</span><span class="sxs-lookup"><span data-stu-id="50c65-126">Parent Elements</span></span>  
  
|<span data-ttu-id="50c65-127">要素</span><span class="sxs-lookup"><span data-stu-id="50c65-127">Element</span></span>|<span data-ttu-id="50c65-128">説明</span><span class="sxs-lookup"><span data-stu-id="50c65-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="50c65-129">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="50c65-129">\<faultPropagationQueries></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationqueries.md)|<span data-ttu-id="50c65-130">1 つのアクティビティ内で発生するエラーの処理を追跡するために使用する、構成要素の一覧を表します。</span><span class="sxs-lookup"><span data-stu-id="50c65-130">Represents a list of configuration elements that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="50c65-131">このイベントは、FaultHandler がエラーを処理するたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="50c65-131">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="50c65-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="50c65-132">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="50c65-133">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="50c65-133">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="50c65-134">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="50c65-134">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
