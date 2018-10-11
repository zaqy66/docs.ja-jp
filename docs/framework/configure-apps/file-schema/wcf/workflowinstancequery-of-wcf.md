---
title: WCF の &lt;workflowInstanceQuery&gt;
ms.date: 03/30/2017
ms.assetid: 35c73f9d-474e-42eb-874d-ddc04b1987f3
ms.openlocfilehash: bb4b3e37bd8e8e4f47fd7a0cd6d493d985c2536e
ms.sourcegitcommit: 2eb5ca4956231c1a0efd34b6a9cab6153a5438af
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/11/2018
ms.locfileid: "49087636"
---
# <a name="ltworkflowinstancequerygt-of-wcf"></a><span data-ttu-id="ef877-102">WCF の &lt;workflowInstanceQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="ef877-102">&lt;workflowInstanceQuery&gt; of WCF</span></span>
<span data-ttu-id="ef877-103">開始したイベントや完了したイベントなど、ワークフロー インスタンスのライフサイクルの変化を追跡するクエリを表します。</span><span class="sxs-lookup"><span data-stu-id="ef877-103">Represents a query that tracks workflow instance life cycle changes such as a started or completed event.</span></span>  
  
 <span data-ttu-id="ef877-104">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="ef877-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
 <span data-ttu-id="ef877-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="ef877-105">\<system.serviceModel></span></span>  
<span data-ttu-id="ef877-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="ef877-106">\<tracking></span></span>  
<span data-ttu-id="ef877-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="ef877-107">\<trackingProfile></span></span>  
<span data-ttu-id="ef877-108">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="ef877-108">\<workflow></span></span>  
<span data-ttu-id="ef877-109">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="ef877-109">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="ef877-110">\<workflowInstanceQuery ></span><span class="sxs-lookup"><span data-stu-id="ef877-110">\<workflowInstanceQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ef877-111">構文</span><span class="sxs-lookup"><span data-stu-id="ef877-111">Syntax</span></span>  
  
```xml
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <workflowInstanceQueries>
        <workflowInstanceQuery>
          <states>
            <state name="Name"/>
          </states>
        </workflowInstanceQuery>
      </workflowInstanceQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ef877-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="ef877-112">Attributes and Elements</span></span>  
 <span data-ttu-id="ef877-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="ef877-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ef877-114">属性</span><span class="sxs-lookup"><span data-stu-id="ef877-114">Attributes</span></span>  
 <span data-ttu-id="ef877-115">なし。</span><span class="sxs-lookup"><span data-stu-id="ef877-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="ef877-116">子要素</span><span class="sxs-lookup"><span data-stu-id="ef877-116">Child Elements</span></span>  
  
|<span data-ttu-id="ef877-117">要素</span><span class="sxs-lookup"><span data-stu-id="ef877-117">Element</span></span>|<span data-ttu-id="ef877-118">説明</span><span class="sxs-lookup"><span data-stu-id="ef877-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ef877-119">\<状態 ></span><span class="sxs-lookup"><span data-stu-id="ef877-119">\<states></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)|<span data-ttu-id="ef877-120">追跡レコードが作成されたときの追跡ワークフロー インスタンスの定期受信済み状態のコレクション。</span><span class="sxs-lookup"><span data-stu-id="ef877-120">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ef877-121">親要素</span><span class="sxs-lookup"><span data-stu-id="ef877-121">Parent Elements</span></span>  
  
|<span data-ttu-id="ef877-122">要素</span><span class="sxs-lookup"><span data-stu-id="ef877-122">Element</span></span>|<span data-ttu-id="ef877-123">説明</span><span class="sxs-lookup"><span data-stu-id="ef877-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ef877-124">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="ef877-124">\<workflowInstanceQueries></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflowinstancequeries.md)|<span data-ttu-id="ef877-125">開始したイベントや完了したイベントなど、ワークフロー インスタンスのライフサイクルの変化を追跡する構成要素のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="ef877-125">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ef877-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="ef877-126">Remarks</span></span>  
 <span data-ttu-id="ef877-127"><xref:System.Activities.Tracking.WorkflowInstanceQuery> は、次の <xref:System.Activities.Tracking.TrackingRecord> オブジェクトの定期受信に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ef877-127">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
-   <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="ef877-128">例</span><span class="sxs-lookup"><span data-stu-id="ef877-128">Example</span></span>  
 <span data-ttu-id="ef877-129">次の構成は、このクエリを使用して、`Started` インスタンス状態のワークフロー インスタンス レベルの追跡レコードを定期受信します。</span><span class="sxs-lookup"><span data-stu-id="ef877-129">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="ef877-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="ef877-130">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="ef877-131">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="ef877-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="ef877-132">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="ef877-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
