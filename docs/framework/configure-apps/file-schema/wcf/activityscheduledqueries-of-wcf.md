---
title: WCF の &lt;activityScheduledQueries&gt;
ms.date: 03/30/2017
ms.assetid: e351329f-9676-4f11-9b19-f4bac82f36fc
ms.openlocfilehash: 35bcb0dc0c33d30eee566869579edb32f131f495
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "49374401"
---
# <a name="ltactivityscheduledqueriesgt-of-wcf"></a><span data-ttu-id="0ad78-102">WCF の &lt;activityScheduledQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="0ad78-102">&lt;activityScheduledQueries&gt; of WCF</span></span>
<span data-ttu-id="0ad78-103">親アクティビティによる実行がスケジュールされているアクティビティを追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="0ad78-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="0ad78-104">アクティビティがスケジュールされたレコードを追跡参加要素が定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="0ad78-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
<span data-ttu-id="0ad78-105">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="0ad78-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="0ad78-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="0ad78-106">\<system.serviceModel></span></span>  
<span data-ttu-id="0ad78-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="0ad78-107">\<tracking></span></span>  
<span data-ttu-id="0ad78-108">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="0ad78-108">\<profiles></span></span>  
<span data-ttu-id="0ad78-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="0ad78-109">\<trackingProfile></span></span>  
<span data-ttu-id="0ad78-110">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="0ad78-110">\<workflow></span></span>  
<span data-ttu-id="0ad78-111">\<activityScheduledQueries ></span><span class="sxs-lookup"><span data-stu-id="0ad78-111">\<activityScheduledQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ad78-112">構文</span><span class="sxs-lookup"><span data-stu-id="0ad78-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0ad78-113">属性と要素</span><span class="sxs-lookup"><span data-stu-id="0ad78-113">Attributes and elements</span></span>  

<span data-ttu-id="0ad78-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="0ad78-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0ad78-115">属性</span><span class="sxs-lookup"><span data-stu-id="0ad78-115">Attributes</span></span>  

<span data-ttu-id="0ad78-116">なし。</span><span class="sxs-lookup"><span data-stu-id="0ad78-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="0ad78-117">子要素</span><span class="sxs-lookup"><span data-stu-id="0ad78-117">Child elements</span></span>  
  
|<span data-ttu-id="0ad78-118">要素</span><span class="sxs-lookup"><span data-stu-id="0ad78-118">Element</span></span>|<span data-ttu-id="0ad78-119">説明</span><span class="sxs-lookup"><span data-stu-id="0ad78-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0ad78-120">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="0ad78-120">\<activityScheduledQuery></span></span>](activityscheduledquery-of-wcf.md)|<span data-ttu-id="0ad78-121">親アクティビティによる実行がスケジュールされているアクティビティを追跡するために使用するクエリ。</span><span class="sxs-lookup"><span data-stu-id="0ad78-121">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0ad78-122">親要素</span><span class="sxs-lookup"><span data-stu-id="0ad78-122">Parent elements</span></span>  
  
|<span data-ttu-id="0ad78-123">要素</span><span class="sxs-lookup"><span data-stu-id="0ad78-123">Element</span></span>|<span data-ttu-id="0ad78-124">説明</span><span class="sxs-lookup"><span data-stu-id="0ad78-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0ad78-125">\<workflow></span><span class="sxs-lookup"><span data-stu-id="0ad78-125">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="0ad78-126">`activityDefinitionId` プロパティによって識別される特定のワークフローのすべてのクエリを格納する構成要素。</span><span class="sxs-lookup"><span data-stu-id="0ad78-126">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0ad78-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="0ad78-127">See also</span></span>  

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElementCollection>
- <xref:System.Activities.Tracking.ActivityScheduledQuery>
- [<span data-ttu-id="0ad78-128">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="0ad78-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="0ad78-129">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="0ad78-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
