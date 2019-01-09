---
title: WCF の &lt;activityScheduledQueries&gt;
ms.date: 03/30/2017
ms.assetid: e351329f-9676-4f11-9b19-f4bac82f36fc
ms.openlocfilehash: d6bc2360ccdeebe291de495e6ee5c7e22f26590a
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145576"
---
# <a name="ltactivityscheduledqueriesgt-of-wcf"></a><span data-ttu-id="4b490-102">WCF の &lt;activityScheduledQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="4b490-102">&lt;activityScheduledQueries&gt; of WCF</span></span>
<span data-ttu-id="4b490-103">親アクティビティによる実行がスケジュールされているアクティビティを追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="4b490-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="4b490-104">アクティビティがスケジュールされたレコードを追跡参加要素が定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="4b490-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
<span data-ttu-id="4b490-105">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="4b490-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="4b490-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="4b490-106">\<system.serviceModel></span></span>  
<span data-ttu-id="4b490-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="4b490-107">\<tracking></span></span>  
<span data-ttu-id="4b490-108">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="4b490-108">\<profiles></span></span>  
<span data-ttu-id="4b490-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="4b490-109">\<trackingProfile></span></span>  
<span data-ttu-id="4b490-110">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="4b490-110">\<workflow></span></span>  
<span data-ttu-id="4b490-111">\<activityScheduledQueries ></span><span class="sxs-lookup"><span data-stu-id="4b490-111">\<activityScheduledQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b490-112">構文</span><span class="sxs-lookup"><span data-stu-id="4b490-112">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <activityScheduledQueries>
          <activityScheduledQuery activityName="String"
                                  childActivityName="String" />
        </activityScheduledQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4b490-113">属性と要素</span><span class="sxs-lookup"><span data-stu-id="4b490-113">Attributes and elements</span></span>  

<span data-ttu-id="4b490-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="4b490-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4b490-115">属性</span><span class="sxs-lookup"><span data-stu-id="4b490-115">Attributes</span></span>  

<span data-ttu-id="4b490-116">なし。</span><span class="sxs-lookup"><span data-stu-id="4b490-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4b490-117">子要素</span><span class="sxs-lookup"><span data-stu-id="4b490-117">Child elements</span></span>  
  
|<span data-ttu-id="4b490-118">要素</span><span class="sxs-lookup"><span data-stu-id="4b490-118">Element</span></span>|<span data-ttu-id="4b490-119">説明</span><span class="sxs-lookup"><span data-stu-id="4b490-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4b490-120">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="4b490-120">\<activityScheduledQuery></span></span>](activityscheduledquery-of-wcf.md)|<span data-ttu-id="4b490-121">親アクティビティによる実行がスケジュールされているアクティビティを追跡するために使用するクエリ。</span><span class="sxs-lookup"><span data-stu-id="4b490-121">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4b490-122">親要素</span><span class="sxs-lookup"><span data-stu-id="4b490-122">Parent elements</span></span>  
  
|<span data-ttu-id="4b490-123">要素</span><span class="sxs-lookup"><span data-stu-id="4b490-123">Element</span></span>|<span data-ttu-id="4b490-124">説明</span><span class="sxs-lookup"><span data-stu-id="4b490-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4b490-125">\<workflow></span><span class="sxs-lookup"><span data-stu-id="4b490-125">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="4b490-126">`activityDefinitionId` プロパティによって識別される特定のワークフローのすべてのクエリを格納する構成要素。</span><span class="sxs-lookup"><span data-stu-id="4b490-126">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4b490-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b490-127">See also</span></span>  

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElementCollection>
- <xref:System.Activities.Tracking.ActivityScheduledQuery>
- [<span data-ttu-id="4b490-128">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="4b490-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="4b490-129">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="4b490-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
