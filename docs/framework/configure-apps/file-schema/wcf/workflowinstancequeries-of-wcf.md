---
title: <workflowInstanceQueries> WCF の
ms.date: 03/30/2017
ms.assetid: b0852f77-16e4-4d55-8eb7-a19feb0e8fc4
ms.openlocfilehash: 544ca868485a409554ece9d9b000beb1a472d344
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255303"
---
# <a name="workflowinstancequeries-of-wcf"></a><span data-ttu-id="47183-102">\<workflowInstanceQueries > の WCF</span><span class="sxs-lookup"><span data-stu-id="47183-102">\<workflowInstanceQueries> of WCF</span></span>

<span data-ttu-id="47183-103">開始したイベントや完了したイベントなど、ワークフロー インスタンスのライフサイクルの変化を追跡する構成要素のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="47183-103">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>  
  
<span data-ttu-id="47183-104">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="47183-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="47183-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="47183-105">\<system.serviceModel></span></span>  
<span data-ttu-id="47183-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="47183-106">\<tracking></span></span>  
<span data-ttu-id="47183-107">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="47183-107">\<profiles></span></span>  
<span data-ttu-id="47183-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="47183-108">\<trackingProfile></span></span>  
<span data-ttu-id="47183-109">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="47183-109">\<workflow></span></span>  
<span data-ttu-id="47183-110">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="47183-110">\<workflowInstanceQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="47183-111">構文</span><span class="sxs-lookup"><span data-stu-id="47183-111">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="47183-112">属性と要素</span><span class="sxs-lookup"><span data-stu-id="47183-112">Attributes and elements</span></span>

<span data-ttu-id="47183-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="47183-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="47183-114">属性</span><span class="sxs-lookup"><span data-stu-id="47183-114">Attributes</span></span>  

<span data-ttu-id="47183-115">なし。</span><span class="sxs-lookup"><span data-stu-id="47183-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="47183-116">子要素</span><span class="sxs-lookup"><span data-stu-id="47183-116">Child elements</span></span>  
  
|<span data-ttu-id="47183-117">要素</span><span class="sxs-lookup"><span data-stu-id="47183-117">Element</span></span>|<span data-ttu-id="47183-118">説明</span><span class="sxs-lookup"><span data-stu-id="47183-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="47183-119">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="47183-119">\<workflowInstanceQuery></span></span>](workflowinstancequery-of-wcf.md)|<span data-ttu-id="47183-120">ワークフロー インスタンスのライフサイクルの変化を追跡するために使用されるクエリ。</span><span class="sxs-lookup"><span data-stu-id="47183-120">A query that is used to track workflow instance life cycle changes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="47183-121">親要素</span><span class="sxs-lookup"><span data-stu-id="47183-121">Parent elements</span></span>  
  
|<span data-ttu-id="47183-122">要素</span><span class="sxs-lookup"><span data-stu-id="47183-122">Element</span></span>|<span data-ttu-id="47183-123">説明</span><span class="sxs-lookup"><span data-stu-id="47183-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="47183-124">\<workflow></span><span class="sxs-lookup"><span data-stu-id="47183-124">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="47183-125">識別される特定のワークフローのすべてのクエリを格納する構成要素、 [activityDefinitionId](https://msdn.microsoft.com/library/system.servicemodel.activities.tracking.configuration.profileworkflowelement.activitydefinitionid(VS.100).aspx)プロパティ。</span><span class="sxs-lookup"><span data-stu-id="47183-125">A configuration element that contains all queries for a specific workflow identified by the [activityDefinitionId](https://msdn.microsoft.com/library/system.servicemodel.activities.tracking.configuration.profileworkflowelement.activitydefinitionid(VS.100).aspx) property.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="47183-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="47183-126">Remarks</span></span>

<span data-ttu-id="47183-127"><xref:System.Activities.Tracking.WorkflowInstanceQuery> は、次の <xref:System.Activities.Tracking.TrackingRecord> オブジェクトの定期受信に使用されます。</span><span class="sxs-lookup"><span data-stu-id="47183-127">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="47183-128">例</span><span class="sxs-lookup"><span data-stu-id="47183-128">Example</span></span>  

<span data-ttu-id="47183-129">次の構成は、このクエリを使用して、`Started` インスタンス状態のワークフロー インスタンス レベルの追跡レコードを定期受信します。</span><span class="sxs-lookup"><span data-stu-id="47183-129">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>
  <workflowInstanceQuery>
    <states>
      <state name="Started" />
    </states>
  </workflowInstanceQuery>
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a><span data-ttu-id="47183-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="47183-130">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="47183-131">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="47183-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="47183-132">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="47183-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
