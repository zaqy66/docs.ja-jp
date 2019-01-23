---
title: '&lt;activityScheduledQueries&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: ca6e82f1-54f2-48d6-899c-9873065b5547
ms.openlocfilehash: 2285dfae84f078483c03d85801051e29b79e74c3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54561843"
---
# <a name="ltactivityscheduledqueriesgt"></a><span data-ttu-id="89720-102">&lt;activityScheduledQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="89720-102">&lt;activityScheduledQueries&gt;</span></span>
<span data-ttu-id="89720-103">親アクティビティによる実行がスケジュールされているアクティビティを追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="89720-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="89720-104">アクティビティがスケジュールされたレコードを追跡参加要素が定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="89720-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
 <span data-ttu-id="89720-105">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="89720-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="89720-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="89720-106">\<system.serviceModel></span></span>  
<span data-ttu-id="89720-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="89720-107">\<tracking></span></span>  
<span data-ttu-id="89720-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="89720-108">\<trackingProfile></span></span>  
<span data-ttu-id="89720-109">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="89720-109">\<workflow></span></span>  
<span data-ttu-id="89720-110">\<activityScheduledQueries></span><span class="sxs-lookup"><span data-stu-id="89720-110">\<activityScheduledQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="89720-111">構文</span><span class="sxs-lookup"><span data-stu-id="89720-111">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityScheduledQueries>
        <activityScheduledQuery activityName="String" 
                                childActivityName="String" />
      </activityScheduledQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="89720-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="89720-112">Attributes and Elements</span></span>  
 <span data-ttu-id="89720-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="89720-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="89720-114">属性</span><span class="sxs-lookup"><span data-stu-id="89720-114">Attributes</span></span>  
 <span data-ttu-id="89720-115">なし。</span><span class="sxs-lookup"><span data-stu-id="89720-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="89720-116">子要素</span><span class="sxs-lookup"><span data-stu-id="89720-116">Child Elements</span></span>  
  
|<span data-ttu-id="89720-117">要素</span><span class="sxs-lookup"><span data-stu-id="89720-117">Element</span></span>|<span data-ttu-id="89720-118">説明</span><span class="sxs-lookup"><span data-stu-id="89720-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="89720-119">\<activityScheduledQuery></span><span class="sxs-lookup"><span data-stu-id="89720-119">\<activityScheduledQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activityscheduledquery.md)|<span data-ttu-id="89720-120">親アクティビティによる実行がスケジュールされているアクティビティを追跡するために使用するクエリ。</span><span class="sxs-lookup"><span data-stu-id="89720-120">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="89720-121">親要素</span><span class="sxs-lookup"><span data-stu-id="89720-121">Parent Elements</span></span>  
  
|<span data-ttu-id="89720-122">要素</span><span class="sxs-lookup"><span data-stu-id="89720-122">Element</span></span>|<span data-ttu-id="89720-123">説明</span><span class="sxs-lookup"><span data-stu-id="89720-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="89720-124">\<workflow></span><span class="sxs-lookup"><span data-stu-id="89720-124">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="89720-125">識別される特定のワークフローのすべてのクエリを格納する構成要素、 **activityDefinitionId**プロパティ。</span><span class="sxs-lookup"><span data-stu-id="89720-125">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="89720-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="89720-126">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityScheduledQuery?displayProperty=nameWithType>
- [<span data-ttu-id="89720-127">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="89720-127">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="89720-128">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="89720-128">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
