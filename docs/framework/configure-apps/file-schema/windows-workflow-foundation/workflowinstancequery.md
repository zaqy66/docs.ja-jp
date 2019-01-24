---
title: '&lt;workflowInstanceQuery&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 9096e812-626a-409a-9eda-c31a60b84c55
ms.openlocfilehash: bef9ddcee2e373f4588d6aed06b7c51e4c6ed4b6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54662050"
---
# <a name="ltworkflowinstancequerygt"></a><span data-ttu-id="523e3-102">&lt;workflowInstanceQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="523e3-102">&lt;workflowInstanceQuery&gt;</span></span>
<span data-ttu-id="523e3-103">開始したイベントや完了したイベントなど、ワークフロー インスタンスのライフサイクルの変化を追跡するクエリを表します。</span><span class="sxs-lookup"><span data-stu-id="523e3-103">Represents a query that tracks workflow instance life cycle changes such as a started or completed event.</span></span>  
  
 <span data-ttu-id="523e3-104">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="523e3-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="523e3-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="523e3-105">\<system.serviceModel></span></span>  
<span data-ttu-id="523e3-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="523e3-106">\<tracking></span></span>  
<span data-ttu-id="523e3-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="523e3-107">\<trackingProfile></span></span>  
<span data-ttu-id="523e3-108">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="523e3-108">\<workflow></span></span>  
<span data-ttu-id="523e3-109">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="523e3-109">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="523e3-110">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="523e3-110">\<workflowInstanceQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="523e3-111">構文</span><span class="sxs-lookup"><span data-stu-id="523e3-111">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <workflowInstanceQueries>
        <workflowInstanceQuery>
          <states>
            <state name="Name" />
          </states>
        </workflowInstanceQuery>
      </workflowInstanceQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="523e3-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="523e3-112">Attributes and Elements</span></span>  
 <span data-ttu-id="523e3-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="523e3-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="523e3-114">属性</span><span class="sxs-lookup"><span data-stu-id="523e3-114">Attributes</span></span>  
 <span data-ttu-id="523e3-115">なし。</span><span class="sxs-lookup"><span data-stu-id="523e3-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="523e3-116">子要素</span><span class="sxs-lookup"><span data-stu-id="523e3-116">Child Elements</span></span>  
  
|<span data-ttu-id="523e3-117">要素</span><span class="sxs-lookup"><span data-stu-id="523e3-117">Element</span></span>|<span data-ttu-id="523e3-118">説明</span><span class="sxs-lookup"><span data-stu-id="523e3-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="523e3-119">\<states></span><span class="sxs-lookup"><span data-stu-id="523e3-119">\<states></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)|<span data-ttu-id="523e3-120">追跡レコードが作成されたときの追跡ワークフロー インスタンスの定期受信済み状態のコレクション。</span><span class="sxs-lookup"><span data-stu-id="523e3-120">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="523e3-121">親要素</span><span class="sxs-lookup"><span data-stu-id="523e3-121">Parent Elements</span></span>  
  
|<span data-ttu-id="523e3-122">要素</span><span class="sxs-lookup"><span data-stu-id="523e3-122">Element</span></span>|<span data-ttu-id="523e3-123">説明</span><span class="sxs-lookup"><span data-stu-id="523e3-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="523e3-124">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="523e3-124">\<workflowInstanceQueries></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflowinstancequeries.md)|<span data-ttu-id="523e3-125">開始したイベントや完了したイベントなど、ワークフロー インスタンスのライフサイクルの変化を追跡する構成要素のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="523e3-125">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="523e3-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="523e3-126">Remarks</span></span>  
 <span data-ttu-id="523e3-127"><xref:System.Activities.Tracking.WorkflowInstanceQuery> は、次の <xref:System.Activities.Tracking.TrackingRecord> オブジェクトの定期受信に使用されます。</span><span class="sxs-lookup"><span data-stu-id="523e3-127">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="523e3-128">例</span><span class="sxs-lookup"><span data-stu-id="523e3-128">Example</span></span>  
 <span data-ttu-id="523e3-129">次の構成は、このクエリを使用して、`Started` インスタンス状態のワークフロー インスタンス レベルの追跡レコードを定期受信します。</span><span class="sxs-lookup"><span data-stu-id="523e3-129">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="523e3-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="523e3-130">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="523e3-131">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="523e3-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="523e3-132">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="523e3-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
