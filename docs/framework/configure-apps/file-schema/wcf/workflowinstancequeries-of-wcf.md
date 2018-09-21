---
title: WCF の &lt;workflowInstanceQueries&gt;
ms.date: 03/30/2017
ms.assetid: b0852f77-16e4-4d55-8eb7-a19feb0e8fc4
ms.openlocfilehash: dfa75a7e4729244ba5887e6666c0fdfe840e9faf
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2018
ms.locfileid: "46470754"
---
# <a name="ltworkflowinstancequeriesgt-of-wcf"></a><span data-ttu-id="933db-102">WCF の &lt;workflowInstanceQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="933db-102">&lt;workflowInstanceQueries&gt; of WCF</span></span>
<span data-ttu-id="933db-103">開始したイベントや完了したイベントなど、ワークフロー インスタンスのライフサイクルの変化を追跡する構成要素のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="933db-103">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>  
  
 <span data-ttu-id="933db-104">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="933db-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
 <span data-ttu-id="933db-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="933db-105">\<system.serviceModel></span></span>  
<span data-ttu-id="933db-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="933db-106">\<tracking></span></span>  
<span data-ttu-id="933db-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="933db-107">\<trackingProfile></span></span>  
<span data-ttu-id="933db-108">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="933db-108">\<workflow></span></span>  
<span data-ttu-id="933db-109">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="933db-109">\<workflowInstanceQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="933db-110">構文</span><span class="sxs-lookup"><span data-stu-id="933db-110">Syntax</span></span>  
  
```xml
<tracking>   <trackingProfile name="Name">       <workflow>          <workflowInstanceQueries>             <workflowInstanceQuery>                <states>                   <state name="Name"/>                </states>            </workflowInstanceQuery>         </workflowInstanceQueries>       </workflow>   </trackingProfile></tracking>  
```
  
## <a name="attributes-and-elements"></a><span data-ttu-id="933db-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="933db-111">Attributes and Elements</span></span>  
 <span data-ttu-id="933db-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="933db-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="933db-113">属性</span><span class="sxs-lookup"><span data-stu-id="933db-113">Attributes</span></span>  
 <span data-ttu-id="933db-114">なし。</span><span class="sxs-lookup"><span data-stu-id="933db-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="933db-115">子要素</span><span class="sxs-lookup"><span data-stu-id="933db-115">Child Elements</span></span>  
  
|<span data-ttu-id="933db-116">要素</span><span class="sxs-lookup"><span data-stu-id="933db-116">Element</span></span>|<span data-ttu-id="933db-117">説明</span><span class="sxs-lookup"><span data-stu-id="933db-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="933db-118">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="933db-118">\<workflowInstanceQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflowinstancequery.md)|<span data-ttu-id="933db-119">ワークフロー インスタンスのライフサイクルの変化を追跡するために使用されるクエリ。</span><span class="sxs-lookup"><span data-stu-id="933db-119">A query that is used to track workflow instance life cycle changes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="933db-120">親要素</span><span class="sxs-lookup"><span data-stu-id="933db-120">Parent Elements</span></span>  
  
|<span data-ttu-id="933db-121">要素</span><span class="sxs-lookup"><span data-stu-id="933db-121">Element</span></span>|<span data-ttu-id="933db-122">説明</span><span class="sxs-lookup"><span data-stu-id="933db-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="933db-123">\<workflow></span><span class="sxs-lookup"><span data-stu-id="933db-123">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="933db-124">識別される特定のワークフローのすべてのクエリを格納する構成要素、 [activityDefinitionId](https://msdn.microsoft.com/library/system.servicemodel.activities.tracking.configuration.profileworkflowelement.activitydefinitionid(VS.100).aspx)プロパティ。</span><span class="sxs-lookup"><span data-stu-id="933db-124">A configuration element that contains all queries for a specific workflow identified by the [activityDefinitionId](https://msdn.microsoft.com/library/system.servicemodel.activities.tracking.configuration.profileworkflowelement.activitydefinitionid(VS.100).aspx) property.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="933db-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="933db-125">Remarks</span></span>  
 <span data-ttu-id="933db-126"><xref:System.Activities.Tracking.WorkflowInstanceQuery> は、次の <xref:System.Activities.Tracking.TrackingRecord> オブジェクトの定期受信に使用されます。</span><span class="sxs-lookup"><span data-stu-id="933db-126">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="933db-127">例</span><span class="sxs-lookup"><span data-stu-id="933db-127">Example</span></span>  
 <span data-ttu-id="933db-128">次の構成は、このクエリを使用して、`Started` インスタンス状態のワークフロー インスタンス レベルの追跡レコードを定期受信します。</span><span class="sxs-lookup"><span data-stu-id="933db-128">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="933db-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="933db-129">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElementCollection?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="933db-130">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="933db-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="933db-131">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="933db-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
