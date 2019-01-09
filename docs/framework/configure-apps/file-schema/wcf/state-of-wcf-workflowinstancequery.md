---
title: WCF の &lt;state&gt;、&lt;workflowInstanceQuery&gt;
ms.date: 03/30/2017
ms.assetid: 40f21055-766c-4be9-86c4-d1d899007098
ms.openlocfilehash: 168a6980e955f602ee60bff26461f06cb16c836a
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145927"
---
# <a name="ltstategt-of-wcf-ltworkflowinstancequerygt"></a><span data-ttu-id="f00d0-102">WCF の &lt;state&gt;、&lt;workflowInstanceQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="f00d0-102">&lt;state&gt; of WCF, &lt;workflowInstanceQuery&gt;</span></span>
<span data-ttu-id="f00d0-103">追跡レコードが作成されたときの追跡ワークフロー インスタンスの定期受信済み状態のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="f00d0-103">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
 <span data-ttu-id="f00d0-104">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="f00d0-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="f00d0-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="f00d0-105">\<system.serviceModel></span></span>  
<span data-ttu-id="f00d0-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="f00d0-106">\<tracking></span></span>  
<span data-ttu-id="f00d0-107">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="f00d0-107">\<profiles></span></span>  
<span data-ttu-id="f00d0-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="f00d0-108">\<trackingProfile></span></span>  
<span data-ttu-id="f00d0-109">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="f00d0-109">\<workflow></span></span>  
<span data-ttu-id="f00d0-110">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="f00d0-110">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="f00d0-111">\<workflowInstanceQuery ></span><span class="sxs-lookup"><span data-stu-id="f00d0-111">\<workflowInstanceQuery></span></span>  
<span data-ttu-id="f00d0-112">\<状態 ></span><span class="sxs-lookup"><span data-stu-id="f00d0-112">\<states></span></span>  
<span data-ttu-id="f00d0-113">\<状態 ></span><span class="sxs-lookup"><span data-stu-id="f00d0-113">\<state></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f00d0-114">構文</span><span class="sxs-lookup"><span data-stu-id="f00d0-114">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f00d0-115">属性と要素</span><span class="sxs-lookup"><span data-stu-id="f00d0-115">Attributes and elements</span></span>

<span data-ttu-id="f00d0-116">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="f00d0-116">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f00d0-117">属性</span><span class="sxs-lookup"><span data-stu-id="f00d0-117">Attributes</span></span>

|<span data-ttu-id="f00d0-118">属性</span><span class="sxs-lookup"><span data-stu-id="f00d0-118">Attribute</span></span>|<span data-ttu-id="f00d0-119">説明</span><span class="sxs-lookup"><span data-stu-id="f00d0-119">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="f00d0-120">追跡レコードが作成されたときの追跡ワークフロー インスタンスの定期受信済み状態を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="f00d0-120">A string that specifies a subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f00d0-121">子要素</span><span class="sxs-lookup"><span data-stu-id="f00d0-121">Child elements</span></span>

<span data-ttu-id="f00d0-122">なし。</span><span class="sxs-lookup"><span data-stu-id="f00d0-122">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="f00d0-123">親要素</span><span class="sxs-lookup"><span data-stu-id="f00d0-123">Parent elements</span></span>

|<span data-ttu-id="f00d0-124">要素</span><span class="sxs-lookup"><span data-stu-id="f00d0-124">Element</span></span>|<span data-ttu-id="f00d0-125">説明</span><span class="sxs-lookup"><span data-stu-id="f00d0-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f00d0-126">\<状態 ></span><span class="sxs-lookup"><span data-stu-id="f00d0-126">\<states></span></span>](states-of-wcf-workflowinstancequery.md)|<span data-ttu-id="f00d0-127">追跡レコードが作成されたときの追跡ワークフロー インスタンスの定期受信済み状態のコレクション。</span><span class="sxs-lookup"><span data-stu-id="f00d0-127">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f00d0-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="f00d0-128">Remarks</span></span>  

<span data-ttu-id="f00d0-129">返されたレコードは、このコレクションの状態でフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="f00d0-129">The returned records are filtered by the states in this collection.</span></span>  
  
<span data-ttu-id="f00d0-130">可能な状態の値は、次の表で説明します。</span><span class="sxs-lookup"><span data-stu-id="f00d0-130">Possible state values are described in the following table:</span></span>
  
|<span data-ttu-id="f00d0-131">状態</span><span class="sxs-lookup"><span data-stu-id="f00d0-131">State</span></span>|<span data-ttu-id="f00d0-132">説明</span><span class="sxs-lookup"><span data-stu-id="f00d0-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="f00d0-133">Aborted</span><span class="sxs-lookup"><span data-stu-id="f00d0-133">Aborted</span></span>|<span data-ttu-id="f00d0-134">ワークフロー インスタンスは中止されました。</span><span class="sxs-lookup"><span data-stu-id="f00d0-134">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="f00d0-135">Completed</span><span class="sxs-lookup"><span data-stu-id="f00d0-135">Completed</span></span>|<span data-ttu-id="f00d0-136">ワークフロー インスタンスは完了しました。</span><span class="sxs-lookup"><span data-stu-id="f00d0-136">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="f00d0-137">Deleted</span><span class="sxs-lookup"><span data-stu-id="f00d0-137">Deleted</span></span>|<span data-ttu-id="f00d0-138">ワークフロー インスタンスは削除されました。</span><span class="sxs-lookup"><span data-stu-id="f00d0-138">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="f00d0-139">Idle</span><span class="sxs-lookup"><span data-stu-id="f00d0-139">Idle</span></span>|<span data-ttu-id="f00d0-140">ワークフロー インスタンスはアイドル状態です。</span><span class="sxs-lookup"><span data-stu-id="f00d0-140">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="f00d0-141">Persisted</span><span class="sxs-lookup"><span data-stu-id="f00d0-141">Persisted</span></span>|<span data-ttu-id="f00d0-142">ワークフロー インスタンスは永続化されました。</span><span class="sxs-lookup"><span data-stu-id="f00d0-142">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="f00d0-143">Resumed</span><span class="sxs-lookup"><span data-stu-id="f00d0-143">Resumed</span></span>|<span data-ttu-id="f00d0-144">ワークフロー インスタンスが再開されました。</span><span class="sxs-lookup"><span data-stu-id="f00d0-144">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="f00d0-145">Started</span><span class="sxs-lookup"><span data-stu-id="f00d0-145">Started</span></span>|<span data-ttu-id="f00d0-146">ワークフロー インスタンスが開始されました。</span><span class="sxs-lookup"><span data-stu-id="f00d0-146">The workflow instance is started.</span></span>|  
|<span data-ttu-id="f00d0-147">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="f00d0-147">UnhandledException</span></span>|<span data-ttu-id="f00d0-148">ワークフロー インスタンスで未処理の例外が発生しました。</span><span class="sxs-lookup"><span data-stu-id="f00d0-148">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="f00d0-149">アンロード</span><span class="sxs-lookup"><span data-stu-id="f00d0-149">Unloaded</span></span>|<span data-ttu-id="f00d0-150">ワークフロー インスタンスはアンロードされました。</span><span class="sxs-lookup"><span data-stu-id="f00d0-150">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="f00d0-151">Canceled</span><span class="sxs-lookup"><span data-stu-id="f00d0-151">Canceled</span></span>|<span data-ttu-id="f00d0-152">ワークフロー インスタンスは取り消されました。</span><span class="sxs-lookup"><span data-stu-id="f00d0-152">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="f00d0-153">Suspended</span><span class="sxs-lookup"><span data-stu-id="f00d0-153">Suspended</span></span>|<span data-ttu-id="f00d0-154">ワークフロー インスタンスが中断されています。</span><span class="sxs-lookup"><span data-stu-id="f00d0-154">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="f00d0-155">Terminated</span><span class="sxs-lookup"><span data-stu-id="f00d0-155">Terminated</span></span>|<span data-ttu-id="f00d0-156">ワークフロー インスタンスは終了しました。</span><span class="sxs-lookup"><span data-stu-id="f00d0-156">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="f00d0-157">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="f00d0-157">Unsuspended</span></span>|<span data-ttu-id="f00d0-158">ワークフロー インスタンスの中断が解除されました。</span><span class="sxs-lookup"><span data-stu-id="f00d0-158">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="f00d0-159">例</span><span class="sxs-lookup"><span data-stu-id="f00d0-159">Example</span></span>

<span data-ttu-id="f00d0-160">次の構成は、このクエリを使用して、`Started` インスタンス状態のワークフロー インスタンス レベルの追跡レコードを定期受信します。</span><span class="sxs-lookup"><span data-stu-id="f00d0-160">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>
  <workflowInstanceQuery>
    <states>
      <state name="Started" />
    </states>
  </workflowInstanceQuery>
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a><span data-ttu-id="f00d0-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="f00d0-161">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="f00d0-162">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="f00d0-162">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="f00d0-163">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="f00d0-163">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
