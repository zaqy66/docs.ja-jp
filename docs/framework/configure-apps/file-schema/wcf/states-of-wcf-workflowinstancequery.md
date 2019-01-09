---
title: WCF の &lt;states&gt;、&lt;workflowInstanceQuery&gt;
ms.date: 03/30/2017
ms.assetid: d17f7525-8035-4e9e-85a0-4cddae59f85d
ms.openlocfilehash: d67f4143619b72826f8fef4adbf66ff8782e4a34
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151440"
---
# <a name="ltstatesgt-of-wcf-ltworkflowinstancequerygt"></a><span data-ttu-id="6701e-102">WCF の &lt;states&gt;、&lt;workflowInstanceQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="6701e-102">&lt;states&gt; of WCF, &lt;workflowInstanceQuery&gt;</span></span>

<span data-ttu-id="6701e-103">追跡レコードが作成されたときの追跡ワークフロー インスタンスの定期受信済み状態のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="6701e-103">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
<span data-ttu-id="6701e-104">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="6701e-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="6701e-105">\<system.serviceModel >\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="6701e-105">\<system.serviceModel> \<tracking></span></span>  
<span data-ttu-id="6701e-106">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="6701e-106">\<profiles></span></span>  
<span data-ttu-id="6701e-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="6701e-107">\<trackingProfile></span></span>  
<span data-ttu-id="6701e-108">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="6701e-108">\<workflow></span></span>  
<span data-ttu-id="6701e-109">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="6701e-109">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="6701e-110">\<workflowInstanceQuery ></span><span class="sxs-lookup"><span data-stu-id="6701e-110">\<workflowInstanceQuery></span></span>  
<span data-ttu-id="6701e-111">\<状態 ></span><span class="sxs-lookup"><span data-stu-id="6701e-111">\<states></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6701e-112">構文</span><span class="sxs-lookup"><span data-stu-id="6701e-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6701e-113">属性と要素</span><span class="sxs-lookup"><span data-stu-id="6701e-113">Attributes and elements</span></span>

<span data-ttu-id="6701e-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="6701e-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6701e-115">属性</span><span class="sxs-lookup"><span data-stu-id="6701e-115">Attributes</span></span>  

<span data-ttu-id="6701e-116">なし。</span><span class="sxs-lookup"><span data-stu-id="6701e-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="6701e-117">子要素</span><span class="sxs-lookup"><span data-stu-id="6701e-117">Child elements</span></span>
  
|<span data-ttu-id="6701e-118">要素</span><span class="sxs-lookup"><span data-stu-id="6701e-118">Element</span></span>|<span data-ttu-id="6701e-119">説明</span><span class="sxs-lookup"><span data-stu-id="6701e-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6701e-120">\<状態 ></span><span class="sxs-lookup"><span data-stu-id="6701e-120">\<states></span></span>](state-of-wcf-workflowinstancequery.md)|<span data-ttu-id="6701e-121">追跡レコードが作成されたときの追跡ワークフロー インスタンスの定期受信済み状態。</span><span class="sxs-lookup"><span data-stu-id="6701e-121">A subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6701e-122">親要素</span><span class="sxs-lookup"><span data-stu-id="6701e-122">Parent elements</span></span>  
  
|<span data-ttu-id="6701e-123">要素</span><span class="sxs-lookup"><span data-stu-id="6701e-123">Element</span></span>|<span data-ttu-id="6701e-124">説明</span><span class="sxs-lookup"><span data-stu-id="6701e-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6701e-125">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="6701e-125">\<workflowInstanceQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflowinstancequery.md)|<span data-ttu-id="6701e-126">開始したイベントや完了したイベントなど、ワークフロー インスタンスのライフサイクルの変化を追跡するクエリ。</span><span class="sxs-lookup"><span data-stu-id="6701e-126">A query that tracks workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6701e-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="6701e-127">Remarks</span></span>

<span data-ttu-id="6701e-128">返されたレコードは、このコレクションの状態でフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="6701e-128">The returned records are filtered by the states in this collection.</span></span>  
  
<span data-ttu-id="6701e-129">次の表に、有効な状態の値を示します。</span><span class="sxs-lookup"><span data-stu-id="6701e-129">Possible state values are described in the following table.</span></span>  
  
|<span data-ttu-id="6701e-130">状態</span><span class="sxs-lookup"><span data-stu-id="6701e-130">State</span></span>|<span data-ttu-id="6701e-131">説明</span><span class="sxs-lookup"><span data-stu-id="6701e-131">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="6701e-132">Aborted</span><span class="sxs-lookup"><span data-stu-id="6701e-132">Aborted</span></span>|<span data-ttu-id="6701e-133">ワークフロー インスタンスは中止されました。</span><span class="sxs-lookup"><span data-stu-id="6701e-133">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="6701e-134">Completed</span><span class="sxs-lookup"><span data-stu-id="6701e-134">Completed</span></span>|<span data-ttu-id="6701e-135">ワークフロー インスタンスは完了しました。</span><span class="sxs-lookup"><span data-stu-id="6701e-135">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="6701e-136">Deleted</span><span class="sxs-lookup"><span data-stu-id="6701e-136">Deleted</span></span>|<span data-ttu-id="6701e-137">ワークフロー インスタンスは削除されました。</span><span class="sxs-lookup"><span data-stu-id="6701e-137">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="6701e-138">Idle</span><span class="sxs-lookup"><span data-stu-id="6701e-138">Idle</span></span>|<span data-ttu-id="6701e-139">ワークフロー インスタンスはアイドル状態です。</span><span class="sxs-lookup"><span data-stu-id="6701e-139">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="6701e-140">Persisted</span><span class="sxs-lookup"><span data-stu-id="6701e-140">Persisted</span></span>|<span data-ttu-id="6701e-141">ワークフロー インスタンスは永続化されました。</span><span class="sxs-lookup"><span data-stu-id="6701e-141">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="6701e-142">Resumed</span><span class="sxs-lookup"><span data-stu-id="6701e-142">Resumed</span></span>|<span data-ttu-id="6701e-143">ワークフロー インスタンスが再開されました。</span><span class="sxs-lookup"><span data-stu-id="6701e-143">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="6701e-144">Started</span><span class="sxs-lookup"><span data-stu-id="6701e-144">Started</span></span>|<span data-ttu-id="6701e-145">ワークフロー インスタンスが開始されました。</span><span class="sxs-lookup"><span data-stu-id="6701e-145">The workflow instance is started.</span></span>|  
|<span data-ttu-id="6701e-146">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="6701e-146">UnhandledException</span></span>|<span data-ttu-id="6701e-147">ワークフロー インスタンスで未処理の例外が発生しました。</span><span class="sxs-lookup"><span data-stu-id="6701e-147">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="6701e-148">アンロード</span><span class="sxs-lookup"><span data-stu-id="6701e-148">Unloaded</span></span>|<span data-ttu-id="6701e-149">ワークフロー インスタンスはアンロードされました。</span><span class="sxs-lookup"><span data-stu-id="6701e-149">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="6701e-150">Canceled</span><span class="sxs-lookup"><span data-stu-id="6701e-150">Canceled</span></span>|<span data-ttu-id="6701e-151">ワークフロー インスタンスは取り消されました。</span><span class="sxs-lookup"><span data-stu-id="6701e-151">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="6701e-152">Suspended</span><span class="sxs-lookup"><span data-stu-id="6701e-152">Suspended</span></span>|<span data-ttu-id="6701e-153">ワークフロー インスタンスが中断されています。</span><span class="sxs-lookup"><span data-stu-id="6701e-153">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="6701e-154">Terminated</span><span class="sxs-lookup"><span data-stu-id="6701e-154">Terminated</span></span>|<span data-ttu-id="6701e-155">ワークフロー インスタンスは終了しました。</span><span class="sxs-lookup"><span data-stu-id="6701e-155">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="6701e-156">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="6701e-156">Unsuspended</span></span>|<span data-ttu-id="6701e-157">ワークフロー インスタンスの中断が解除されました。</span><span class="sxs-lookup"><span data-stu-id="6701e-157">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="6701e-158">例</span><span class="sxs-lookup"><span data-stu-id="6701e-158">Example</span></span>

<span data-ttu-id="6701e-159">次の構成は、このクエリを使用して、`Started` インスタンス状態のワークフロー インスタンス レベルの追跡レコードを定期受信します。</span><span class="sxs-lookup"><span data-stu-id="6701e-159">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>
  <workflowInstanceQuery>
    <states>
      <state name="Started" />
    </states>
  </workflowInstanceQuery>
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a><span data-ttu-id="6701e-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="6701e-160">See also</span></span>  

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>       
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElementCollection?displayProperty=nameWithType>       
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>       
- [<span data-ttu-id="6701e-161">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="6701e-161">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
- [<span data-ttu-id="6701e-162">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="6701e-162">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
