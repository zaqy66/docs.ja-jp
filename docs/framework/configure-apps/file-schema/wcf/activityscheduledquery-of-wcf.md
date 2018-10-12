---
title: WCF の  &lt;activityScheduledQuery&gt;
ms.date: 03/30/2017
ms.assetid: 25f6eee1-3d98-4c39-b517-c0813f03f106
ms.openlocfilehash: a3c4c8b338921c9d949edd83deb4d6073eb26b55
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2018
ms.locfileid: "49123372"
---
# <a name="ltactivityscheduledquerygt-of-wcf"></a><span data-ttu-id="d2a59-102">WCF の  &lt;activityScheduledQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="d2a59-102">&lt;activityScheduledQuery&gt; of WCF</span></span>

<span data-ttu-id="d2a59-103">親アクティビティによる実行がスケジュールされているアクティビティを追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="d2a59-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="d2a59-104">アクティビティがスケジュールされたレコードを追跡参加要素が定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="d2a59-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
<span data-ttu-id="d2a59-105">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="d2a59-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="d2a59-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="d2a59-106">\<system.serviceModel></span></span>  
<span data-ttu-id="d2a59-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="d2a59-107">\<tracking></span></span>  
<span data-ttu-id="d2a59-108">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="d2a59-108">\<profiles></span></span>  
<span data-ttu-id="d2a59-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="d2a59-109">\<trackingProfile></span></span>  
<span data-ttu-id="d2a59-110">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="d2a59-110">\<workflow></span></span>  
<span data-ttu-id="d2a59-111">\<activityScheduledQueries ></span><span class="sxs-lookup"><span data-stu-id="d2a59-111">\<activityScheduledQueries></span></span>  
<span data-ttu-id="d2a59-112">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="d2a59-112">\<activityScheduledQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d2a59-113">構文</span><span class="sxs-lookup"><span data-stu-id="d2a59-113">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d2a59-114">属性と要素</span><span class="sxs-lookup"><span data-stu-id="d2a59-114">Attributes and elements</span></span>  

<span data-ttu-id="d2a59-115">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="d2a59-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d2a59-116">属性</span><span class="sxs-lookup"><span data-stu-id="d2a59-116">Attributes</span></span>  
  
|<span data-ttu-id="d2a59-117">属性</span><span class="sxs-lookup"><span data-stu-id="d2a59-117">Attribute</span></span>|<span data-ttu-id="d2a59-118">説明</span><span class="sxs-lookup"><span data-stu-id="d2a59-118">Description</span></span>|  
|---------------|-----------------|  
|`activityName`|<span data-ttu-id="d2a59-119">キャンセルを要求しているアクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="d2a59-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|`childActivityName`|<span data-ttu-id="d2a59-120">キャンセルが要求された子アクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="d2a59-120">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d2a59-121">子要素</span><span class="sxs-lookup"><span data-stu-id="d2a59-121">Child elements</span></span>

<span data-ttu-id="d2a59-122">なし。</span><span class="sxs-lookup"><span data-stu-id="d2a59-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d2a59-123">親要素</span><span class="sxs-lookup"><span data-stu-id="d2a59-123">Parent elements</span></span>  
  
|<span data-ttu-id="d2a59-124">要素</span><span class="sxs-lookup"><span data-stu-id="d2a59-124">Element</span></span>|<span data-ttu-id="d2a59-125">説明</span><span class="sxs-lookup"><span data-stu-id="d2a59-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d2a59-126">\<activityScheduledQueries></span><span class="sxs-lookup"><span data-stu-id="d2a59-126">\<activityScheduledQueries></span></span>](activityscheduledqueries-of-wcf.md)|<span data-ttu-id="d2a59-127">親アクティビティによる実行のスケジュールされたアクティビティを追跡するために使用されるクエリのコレクション。</span><span class="sxs-lookup"><span data-stu-id="d2a59-127">A collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d2a59-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2a59-128">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElement>
- <xref:System.Activities.Tracking.ActivityScheduledQuery>
- [<span data-ttu-id="d2a59-129">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="d2a59-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="d2a59-130">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2a59-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
