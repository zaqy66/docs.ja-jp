---
title: WCF の &lt;activityScheduledQueries&gt;
ms.date: 03/30/2017
ms.assetid: e351329f-9676-4f11-9b19-f4bac82f36fc
ms.openlocfilehash: 35bcb0dc0c33d30eee566869579edb32f131f495
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452697"
---
# <a name="ltactivityscheduledqueriesgt-of-wcf"></a><span data-ttu-id="96e2f-102">WCF の &lt;activityScheduledQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="96e2f-102">&lt;activityScheduledQueries&gt; of WCF</span></span>
<span data-ttu-id="96e2f-103">親アクティビティによる実行がスケジュールされているアクティビティを追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="96e2f-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="96e2f-104">アクティビティがスケジュールされたレコードを追跡参加要素が定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="96e2f-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
<span data-ttu-id="96e2f-105">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="96e2f-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="96e2f-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="96e2f-106">\<system.serviceModel></span></span>  
<span data-ttu-id="96e2f-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="96e2f-107">\<tracking></span></span>  
<span data-ttu-id="96e2f-108">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="96e2f-108">\<profiles></span></span>  
<span data-ttu-id="96e2f-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="96e2f-109">\<trackingProfile></span></span>  
<span data-ttu-id="96e2f-110">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="96e2f-110">\<workflow></span></span>  
<span data-ttu-id="96e2f-111">\<activityScheduledQueries ></span><span class="sxs-lookup"><span data-stu-id="96e2f-111">\<activityScheduledQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="96e2f-112">構文</span><span class="sxs-lookup"><span data-stu-id="96e2f-112">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <activityScheduledQueries>
          <activityScheduledQuery activityName="String"   
                                  childActivityName="String"/>
        </activityScheduledQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="96e2f-113">属性と要素</span><span class="sxs-lookup"><span data-stu-id="96e2f-113">Attributes and elements</span></span>  

<span data-ttu-id="96e2f-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="96e2f-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="96e2f-115">属性</span><span class="sxs-lookup"><span data-stu-id="96e2f-115">Attributes</span></span>  

<span data-ttu-id="96e2f-116">なし。</span><span class="sxs-lookup"><span data-stu-id="96e2f-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="96e2f-117">子要素</span><span class="sxs-lookup"><span data-stu-id="96e2f-117">Child elements</span></span>  
  
|<span data-ttu-id="96e2f-118">要素</span><span class="sxs-lookup"><span data-stu-id="96e2f-118">Element</span></span>|<span data-ttu-id="96e2f-119">説明</span><span class="sxs-lookup"><span data-stu-id="96e2f-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="96e2f-120">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="96e2f-120">\<activityScheduledQuery></span></span>](activityscheduledquery-of-wcf.md)|<span data-ttu-id="96e2f-121">親アクティビティによる実行がスケジュールされているアクティビティを追跡するために使用するクエリ。</span><span class="sxs-lookup"><span data-stu-id="96e2f-121">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="96e2f-122">親要素</span><span class="sxs-lookup"><span data-stu-id="96e2f-122">Parent elements</span></span>  
  
|<span data-ttu-id="96e2f-123">要素</span><span class="sxs-lookup"><span data-stu-id="96e2f-123">Element</span></span>|<span data-ttu-id="96e2f-124">説明</span><span class="sxs-lookup"><span data-stu-id="96e2f-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="96e2f-125">\<workflow></span><span class="sxs-lookup"><span data-stu-id="96e2f-125">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="96e2f-126">`activityDefinitionId` プロパティによって識別される特定のワークフローのすべてのクエリを格納する構成要素。</span><span class="sxs-lookup"><span data-stu-id="96e2f-126">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="96e2f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="96e2f-127">See also</span></span>  

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElementCollection>
- <xref:System.Activities.Tracking.ActivityScheduledQuery>
- [<span data-ttu-id="96e2f-128">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="96e2f-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="96e2f-129">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="96e2f-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
