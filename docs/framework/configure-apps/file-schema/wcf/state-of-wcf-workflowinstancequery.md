---
title: WCF の &lt;state&gt;、&lt;workflowInstanceQuery&gt;
ms.date: 03/30/2017
ms.assetid: 40f21055-766c-4be9-86c4-d1d899007098
ms.openlocfilehash: 427cba7a51bfb908171e476cd703c6a40fd6e144
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2018
ms.locfileid: "49123216"
---
# <a name="ltstategt-of-wcf-ltworkflowinstancequerygt"></a><span data-ttu-id="87d4d-102">WCF の &lt;state&gt;、&lt;workflowInstanceQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="87d4d-102">&lt;state&gt; of WCF, &lt;workflowInstanceQuery&gt;</span></span>
<span data-ttu-id="87d4d-103">追跡レコードが作成されたときの追跡ワークフロー インスタンスの定期受信済み状態のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="87d4d-103">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
 <span data-ttu-id="87d4d-104">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="87d4d-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="87d4d-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="87d4d-105">\<system.serviceModel></span></span>  
<span data-ttu-id="87d4d-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="87d4d-106">\<tracking></span></span>  
<span data-ttu-id="87d4d-107">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="87d4d-107">\<profiles></span></span>  
<span data-ttu-id="87d4d-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="87d4d-108">\<trackingProfile></span></span>  
<span data-ttu-id="87d4d-109">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="87d4d-109">\<workflow></span></span>  
<span data-ttu-id="87d4d-110">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="87d4d-110">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="87d4d-111">\<workflowInstanceQuery ></span><span class="sxs-lookup"><span data-stu-id="87d4d-111">\<workflowInstanceQuery></span></span>  
<span data-ttu-id="87d4d-112">\<状態 ></span><span class="sxs-lookup"><span data-stu-id="87d4d-112">\<states></span></span>  
<span data-ttu-id="87d4d-113">\<状態 ></span><span class="sxs-lookup"><span data-stu-id="87d4d-113">\<state></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="87d4d-114">構文</span><span class="sxs-lookup"><span data-stu-id="87d4d-114">Syntax</span></span>  
  
```xml
<tracking>
  <profiles>
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
  </profiles>
</tracking>  
```
  
## <a name="attributes-and-elements"></a><span data-ttu-id="87d4d-115">属性と要素</span><span class="sxs-lookup"><span data-stu-id="87d4d-115">Attributes and elements</span></span>

<span data-ttu-id="87d4d-116">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="87d4d-116">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="87d4d-117">属性</span><span class="sxs-lookup"><span data-stu-id="87d4d-117">Attributes</span></span>

|<span data-ttu-id="87d4d-118">属性</span><span class="sxs-lookup"><span data-stu-id="87d4d-118">Attribute</span></span>|<span data-ttu-id="87d4d-119">説明</span><span class="sxs-lookup"><span data-stu-id="87d4d-119">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="87d4d-120">追跡レコードが作成されたときの追跡ワークフロー インスタンスの定期受信済み状態を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="87d4d-120">A string that specifies a subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="87d4d-121">子要素</span><span class="sxs-lookup"><span data-stu-id="87d4d-121">Child elements</span></span>

<span data-ttu-id="87d4d-122">なし。</span><span class="sxs-lookup"><span data-stu-id="87d4d-122">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="87d4d-123">親要素</span><span class="sxs-lookup"><span data-stu-id="87d4d-123">Parent elements</span></span>

|<span data-ttu-id="87d4d-124">要素</span><span class="sxs-lookup"><span data-stu-id="87d4d-124">Element</span></span>|<span data-ttu-id="87d4d-125">説明</span><span class="sxs-lookup"><span data-stu-id="87d4d-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="87d4d-126">\<状態 ></span><span class="sxs-lookup"><span data-stu-id="87d4d-126">\<states></span></span>](states-of-wcf-workflowinstancequery.md)|<span data-ttu-id="87d4d-127">追跡レコードが作成されたときの追跡ワークフロー インスタンスの定期受信済み状態のコレクション。</span><span class="sxs-lookup"><span data-stu-id="87d4d-127">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="87d4d-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="87d4d-128">Remarks</span></span>  

<span data-ttu-id="87d4d-129">返されたレコードは、このコレクションの状態でフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="87d4d-129">The returned records are filtered by the states in this collection.</span></span>  
  
<span data-ttu-id="87d4d-130">可能な状態の値は、次の表で説明します。</span><span class="sxs-lookup"><span data-stu-id="87d4d-130">Possible state values are described in the following table:</span></span>
  
|<span data-ttu-id="87d4d-131">状態</span><span class="sxs-lookup"><span data-stu-id="87d4d-131">State</span></span>|<span data-ttu-id="87d4d-132">説明</span><span class="sxs-lookup"><span data-stu-id="87d4d-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="87d4d-133">Aborted</span><span class="sxs-lookup"><span data-stu-id="87d4d-133">Aborted</span></span>|<span data-ttu-id="87d4d-134">ワークフロー インスタンスは中止されました。</span><span class="sxs-lookup"><span data-stu-id="87d4d-134">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="87d4d-135">Completed</span><span class="sxs-lookup"><span data-stu-id="87d4d-135">Completed</span></span>|<span data-ttu-id="87d4d-136">ワークフロー インスタンスは完了しました。</span><span class="sxs-lookup"><span data-stu-id="87d4d-136">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="87d4d-137">Deleted</span><span class="sxs-lookup"><span data-stu-id="87d4d-137">Deleted</span></span>|<span data-ttu-id="87d4d-138">ワークフロー インスタンスは削除されました。</span><span class="sxs-lookup"><span data-stu-id="87d4d-138">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="87d4d-139">Idle</span><span class="sxs-lookup"><span data-stu-id="87d4d-139">Idle</span></span>|<span data-ttu-id="87d4d-140">ワークフロー インスタンスはアイドル状態です。</span><span class="sxs-lookup"><span data-stu-id="87d4d-140">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="87d4d-141">Persisted</span><span class="sxs-lookup"><span data-stu-id="87d4d-141">Persisted</span></span>|<span data-ttu-id="87d4d-142">ワークフロー インスタンスは永続化されました。</span><span class="sxs-lookup"><span data-stu-id="87d4d-142">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="87d4d-143">Resumed</span><span class="sxs-lookup"><span data-stu-id="87d4d-143">Resumed</span></span>|<span data-ttu-id="87d4d-144">ワークフロー インスタンスが再開されました。</span><span class="sxs-lookup"><span data-stu-id="87d4d-144">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="87d4d-145">Started</span><span class="sxs-lookup"><span data-stu-id="87d4d-145">Started</span></span>|<span data-ttu-id="87d4d-146">ワークフロー インスタンスが開始されました。</span><span class="sxs-lookup"><span data-stu-id="87d4d-146">The workflow instance is started.</span></span>|  
|<span data-ttu-id="87d4d-147">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="87d4d-147">UnhandledException</span></span>|<span data-ttu-id="87d4d-148">ワークフロー インスタンスで未処理の例外が発生しました。</span><span class="sxs-lookup"><span data-stu-id="87d4d-148">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="87d4d-149">アンロード</span><span class="sxs-lookup"><span data-stu-id="87d4d-149">Unloaded</span></span>|<span data-ttu-id="87d4d-150">ワークフロー インスタンスはアンロードされました。</span><span class="sxs-lookup"><span data-stu-id="87d4d-150">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="87d4d-151">Canceled</span><span class="sxs-lookup"><span data-stu-id="87d4d-151">Canceled</span></span>|<span data-ttu-id="87d4d-152">ワークフロー インスタンスは取り消されました。</span><span class="sxs-lookup"><span data-stu-id="87d4d-152">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="87d4d-153">Suspended</span><span class="sxs-lookup"><span data-stu-id="87d4d-153">Suspended</span></span>|<span data-ttu-id="87d4d-154">ワークフロー インスタンスが中断されています。</span><span class="sxs-lookup"><span data-stu-id="87d4d-154">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="87d4d-155">Terminated</span><span class="sxs-lookup"><span data-stu-id="87d4d-155">Terminated</span></span>|<span data-ttu-id="87d4d-156">ワークフロー インスタンスは終了しました。</span><span class="sxs-lookup"><span data-stu-id="87d4d-156">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="87d4d-157">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="87d4d-157">Unsuspended</span></span>|<span data-ttu-id="87d4d-158">ワークフロー インスタンスの中断が解除されました。</span><span class="sxs-lookup"><span data-stu-id="87d4d-158">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="87d4d-159">例</span><span class="sxs-lookup"><span data-stu-id="87d4d-159">Example</span></span>

<span data-ttu-id="87d4d-160">次の構成は、このクエリを使用して、`Started` インスタンス状態のワークフロー インスタンス レベルの追跡レコードを定期受信します。</span><span class="sxs-lookup"><span data-stu-id="87d4d-160">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml
<workflowInstanceQueries>
  <workflowInstanceQuery>  
    <states>  
      <state name="Started"/>  
    </states>  
  </workflowInstanceQuery>  
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a><span data-ttu-id="87d4d-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="87d4d-161">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="87d4d-162">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="87d4d-162">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="87d4d-163">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="87d4d-163">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
