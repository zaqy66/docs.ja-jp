---
title: '&lt;state&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 619414f2-61c2-4427-9977-d05009e343db
ms.openlocfilehash: 8e381671d9282218a4e5bf0ae979bec79c7cfe78
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54523052"
---
# <a name="ltstategt"></a><span data-ttu-id="7a4f1-102">&lt;state&gt;</span><span class="sxs-lookup"><span data-stu-id="7a4f1-102">&lt;state&gt;</span></span>
<span data-ttu-id="7a4f1-103">追跡レコードが作成されたときの追跡ワークフロー インスタンスの定期受信済み状態のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-103">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
 <span data-ttu-id="7a4f1-104">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="7a4f1-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="7a4f1-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="7a4f1-105">\<system.serviceModel></span></span>  
<span data-ttu-id="7a4f1-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="7a4f1-106">\<tracking></span></span>  
<span data-ttu-id="7a4f1-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="7a4f1-107">\<trackingProfile></span></span>  
<span data-ttu-id="7a4f1-108">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="7a4f1-108">\<workflow></span></span>  
<span data-ttu-id="7a4f1-109">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="7a4f1-109">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="7a4f1-110">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="7a4f1-110">\<workflowInstanceQuery></span></span>  
<span data-ttu-id="7a4f1-111">\<states></span><span class="sxs-lookup"><span data-stu-id="7a4f1-111">\<states></span></span>  
<span data-ttu-id="7a4f1-112">\<state></span><span class="sxs-lookup"><span data-stu-id="7a4f1-112">\<state></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7a4f1-113">構文</span><span class="sxs-lookup"><span data-stu-id="7a4f1-113">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7a4f1-114">属性および要素</span><span class="sxs-lookup"><span data-stu-id="7a4f1-114">Attributes and Elements</span></span>  
 <span data-ttu-id="7a4f1-115">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7a4f1-116">属性</span><span class="sxs-lookup"><span data-stu-id="7a4f1-116">Attributes</span></span>  
  
|<span data-ttu-id="7a4f1-117">属性</span><span class="sxs-lookup"><span data-stu-id="7a4f1-117">Attribute</span></span>|<span data-ttu-id="7a4f1-118">説明</span><span class="sxs-lookup"><span data-stu-id="7a4f1-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="7a4f1-119">name</span><span class="sxs-lookup"><span data-stu-id="7a4f1-119">name</span></span>|<span data-ttu-id="7a4f1-120">追跡レコードが作成されたときの追跡ワークフロー インスタンスの定期受信済み状態を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-120">A string that specifies a subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7a4f1-121">子要素</span><span class="sxs-lookup"><span data-stu-id="7a4f1-121">Child Elements</span></span>  
 <span data-ttu-id="7a4f1-122">なし。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7a4f1-123">親要素</span><span class="sxs-lookup"><span data-stu-id="7a4f1-123">Parent Elements</span></span>  
  
|<span data-ttu-id="7a4f1-124">要素</span><span class="sxs-lookup"><span data-stu-id="7a4f1-124">Element</span></span>|<span data-ttu-id="7a4f1-125">説明</span><span class="sxs-lookup"><span data-stu-id="7a4f1-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7a4f1-126">\<states></span><span class="sxs-lookup"><span data-stu-id="7a4f1-126">\<states></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)|<span data-ttu-id="7a4f1-127">追跡レコードが作成されたときの追跡ワークフロー インスタンスの定期受信済み状態のコレクション。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-127">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7a4f1-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="7a4f1-128">Remarks</span></span>  
 <span data-ttu-id="7a4f1-129">返されたレコードは、このコレクションの状態でフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-129">The returned records are filtered by the states in this collection.</span></span>  
  
 <span data-ttu-id="7a4f1-130">次の表に、有効な状態の値を示します。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-130">Possible state values are described in the following table.</span></span>  
  
|<span data-ttu-id="7a4f1-131">状態</span><span class="sxs-lookup"><span data-stu-id="7a4f1-131">State</span></span>|<span data-ttu-id="7a4f1-132">説明</span><span class="sxs-lookup"><span data-stu-id="7a4f1-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="7a4f1-133">Aborted</span><span class="sxs-lookup"><span data-stu-id="7a4f1-133">Aborted</span></span>|<span data-ttu-id="7a4f1-134">ワークフロー インスタンスは中止されました。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-134">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="7a4f1-135">Completed</span><span class="sxs-lookup"><span data-stu-id="7a4f1-135">Completed</span></span>|<span data-ttu-id="7a4f1-136">ワークフロー インスタンスは完了しました。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-136">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="7a4f1-137">Deleted</span><span class="sxs-lookup"><span data-stu-id="7a4f1-137">Deleted</span></span>|<span data-ttu-id="7a4f1-138">ワークフロー インスタンスは削除されました。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-138">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="7a4f1-139">Idle</span><span class="sxs-lookup"><span data-stu-id="7a4f1-139">Idle</span></span>|<span data-ttu-id="7a4f1-140">ワークフロー インスタンスはアイドル状態です。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-140">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="7a4f1-141">Persisted</span><span class="sxs-lookup"><span data-stu-id="7a4f1-141">Persisted</span></span>|<span data-ttu-id="7a4f1-142">ワークフロー インスタンスは永続化されました。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-142">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="7a4f1-143">Resumed</span><span class="sxs-lookup"><span data-stu-id="7a4f1-143">Resumed</span></span>|<span data-ttu-id="7a4f1-144">ワークフロー インスタンスが再開されました。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-144">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="7a4f1-145">Started</span><span class="sxs-lookup"><span data-stu-id="7a4f1-145">Started</span></span>|<span data-ttu-id="7a4f1-146">ワークフロー インスタンスが開始されました。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-146">The workflow instance is started.</span></span>|  
|<span data-ttu-id="7a4f1-147">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="7a4f1-147">UnhandledException</span></span>|<span data-ttu-id="7a4f1-148">ワークフロー インスタンスで未処理の例外が発生しました。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-148">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="7a4f1-149">アンロード</span><span class="sxs-lookup"><span data-stu-id="7a4f1-149">Unloaded</span></span>|<span data-ttu-id="7a4f1-150">ワークフロー インスタンスはアンロードされました。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-150">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="7a4f1-151">Canceled</span><span class="sxs-lookup"><span data-stu-id="7a4f1-151">Canceled</span></span>|<span data-ttu-id="7a4f1-152">ワークフロー インスタンスは取り消されました。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-152">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="7a4f1-153">Suspended</span><span class="sxs-lookup"><span data-stu-id="7a4f1-153">Suspended</span></span>|<span data-ttu-id="7a4f1-154">ワークフロー インスタンスが中断されています。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-154">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="7a4f1-155">Terminated</span><span class="sxs-lookup"><span data-stu-id="7a4f1-155">Terminated</span></span>|<span data-ttu-id="7a4f1-156">ワークフロー インスタンスは終了しました。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-156">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="7a4f1-157">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="7a4f1-157">Unsuspended</span></span>|<span data-ttu-id="7a4f1-158">ワークフロー インスタンスの中断が解除されました。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-158">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="7a4f1-159">例</span><span class="sxs-lookup"><span data-stu-id="7a4f1-159">Example</span></span>  
 <span data-ttu-id="7a4f1-160">次の構成は、このクエリを使用して、`Started` インスタンス状態のワークフロー インスタンス レベルの追跡レコードを定期受信します。</span><span class="sxs-lookup"><span data-stu-id="7a4f1-160">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="7a4f1-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a4f1-161">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="7a4f1-162">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="7a4f1-162">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="7a4f1-163">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="7a4f1-163">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
