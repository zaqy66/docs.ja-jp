---
title: <workflowInstanceQuery> WCF の
ms.date: 03/30/2017
ms.assetid: 35c73f9d-474e-42eb-874d-ddc04b1987f3
ms.openlocfilehash: 726d4db3bad9f57663790e2bb4e081faba28f1ef
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55278773"
---
# <a name="workflowinstancequery-of-wcf"></a><span data-ttu-id="8376c-102">\<workflowInstanceQuery > の WCF</span><span class="sxs-lookup"><span data-stu-id="8376c-102">\<workflowInstanceQuery> of WCF</span></span>

<span data-ttu-id="8376c-103">開始したイベントや完了したイベントなど、ワークフロー インスタンスのライフサイクルの変化を追跡するクエリを表します。</span><span class="sxs-lookup"><span data-stu-id="8376c-103">Represents a query that tracks workflow instance life cycle changes such as a started or completed event.</span></span>  
  
<span data-ttu-id="8376c-104">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="8376c-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="8376c-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="8376c-105">\<system.serviceModel></span></span>  
<span data-ttu-id="8376c-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="8376c-106">\<tracking></span></span>  
<span data-ttu-id="8376c-107">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="8376c-107">\<profiles></span></span>  
<span data-ttu-id="8376c-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="8376c-108">\<trackingProfile></span></span>  
<span data-ttu-id="8376c-109">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="8376c-109">\<workflow></span></span>  
<span data-ttu-id="8376c-110">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="8376c-110">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="8376c-111">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="8376c-111">\<workflowInstanceQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8376c-112">構文</span><span class="sxs-lookup"><span data-stu-id="8376c-112">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
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
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8376c-113">属性と要素</span><span class="sxs-lookup"><span data-stu-id="8376c-113">Attributes and elements</span></span>  

<span data-ttu-id="8376c-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="8376c-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8376c-115">属性</span><span class="sxs-lookup"><span data-stu-id="8376c-115">Attributes</span></span>  

<span data-ttu-id="8376c-116">なし。</span><span class="sxs-lookup"><span data-stu-id="8376c-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="8376c-117">子要素</span><span class="sxs-lookup"><span data-stu-id="8376c-117">Child elements</span></span>  
  
|<span data-ttu-id="8376c-118">要素</span><span class="sxs-lookup"><span data-stu-id="8376c-118">Element</span></span>|<span data-ttu-id="8376c-119">説明</span><span class="sxs-lookup"><span data-stu-id="8376c-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8376c-120">\<states></span><span class="sxs-lookup"><span data-stu-id="8376c-120">\<states></span></span>](states-of-wcf-workflowinstancequery.md)|<span data-ttu-id="8376c-121">追跡レコードが作成されたときの追跡ワークフロー インスタンスの定期受信済み状態のコレクション。</span><span class="sxs-lookup"><span data-stu-id="8376c-121">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="8376c-122">親要素</span><span class="sxs-lookup"><span data-stu-id="8376c-122">Parent elements</span></span>  
  
|<span data-ttu-id="8376c-123">要素</span><span class="sxs-lookup"><span data-stu-id="8376c-123">Element</span></span>|<span data-ttu-id="8376c-124">説明</span><span class="sxs-lookup"><span data-stu-id="8376c-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8376c-125">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="8376c-125">\<workflowInstanceQueries></span></span>](workflowinstancequeries-of-wcf.md)|<span data-ttu-id="8376c-126">開始したイベントや完了したイベントなど、ワークフロー インスタンスのライフサイクルの変化を追跡する構成要素のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="8376c-126">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8376c-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="8376c-127">Remarks</span></span>  

<span data-ttu-id="8376c-128"><xref:System.Activities.Tracking.WorkflowInstanceQuery> は、次の <xref:System.Activities.Tracking.TrackingRecord> オブジェクトの定期受信に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8376c-128">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="8376c-129">例</span><span class="sxs-lookup"><span data-stu-id="8376c-129">Example</span></span>  

<span data-ttu-id="8376c-130">次の構成は、このクエリを使用して、`Started` インスタンス状態のワークフロー インスタンス レベルの追跡レコードを定期受信します。</span><span class="sxs-lookup"><span data-stu-id="8376c-130">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>
  <workflowInstanceQuery>
    <states>
      <state name="Started" />
    </states>
  </workflowInstanceQuery>
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a><span data-ttu-id="8376c-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="8376c-131">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="8376c-132">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="8376c-132">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="8376c-133">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="8376c-133">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
