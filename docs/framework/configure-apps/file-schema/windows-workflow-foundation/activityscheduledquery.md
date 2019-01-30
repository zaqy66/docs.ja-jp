---
title: <activityScheduledQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: a8bcd6d4-b389-4daf-86bf-1ade85fec114
ms.openlocfilehash: 2199e66342c6fa3afca9d8ccd3b620560b123ede
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55260841"
---
# <a name="activityscheduledquery"></a><span data-ttu-id="ade3e-101">\<activityScheduledQuery></span><span class="sxs-lookup"><span data-stu-id="ade3e-101">\<activityScheduledQuery></span></span>
<span data-ttu-id="ade3e-102">親アクティビティによる実行がスケジュールされているアクティビティを追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="ade3e-102">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="ade3e-103">アクティビティがスケジュールされたレコードを追跡参加要素が定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="ade3e-103">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
 <span data-ttu-id="ade3e-104">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="ade3e-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="ade3e-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="ade3e-105">\<system.serviceModel></span></span>  
<span data-ttu-id="ade3e-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="ade3e-106">\<tracking></span></span>  
<span data-ttu-id="ade3e-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="ade3e-107">\<trackingProfile></span></span>  
<span data-ttu-id="ade3e-108">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="ade3e-108">\<workflow></span></span>  
<span data-ttu-id="ade3e-109">\<activityScheduledQueries></span><span class="sxs-lookup"><span data-stu-id="ade3e-109">\<activityScheduledQueries></span></span>  
<span data-ttu-id="ade3e-110">\<activityScheduledQuery></span><span class="sxs-lookup"><span data-stu-id="ade3e-110">\<activityScheduledQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ade3e-111">構文</span><span class="sxs-lookup"><span data-stu-id="ade3e-111">Syntax</span></span>  
  
```xml 
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityScheduledQueries>
        <activityScheduledQuery activityName="String" 
                                childActivityName="String"/>
      </activityScheduledQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ade3e-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="ade3e-112">Attributes and Elements</span></span>  
 <span data-ttu-id="ade3e-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="ade3e-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ade3e-114">属性</span><span class="sxs-lookup"><span data-stu-id="ade3e-114">Attributes</span></span>  
  
|<span data-ttu-id="ade3e-115">属性</span><span class="sxs-lookup"><span data-stu-id="ade3e-115">Attribute</span></span>|<span data-ttu-id="ade3e-116">説明</span><span class="sxs-lookup"><span data-stu-id="ade3e-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ade3e-117">activityName</span><span class="sxs-lookup"><span data-stu-id="ade3e-117">activityName</span></span>|<span data-ttu-id="ade3e-118">キャンセルを要求しているアクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="ade3e-118">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|<span data-ttu-id="ade3e-119">childActivityName</span><span class="sxs-lookup"><span data-stu-id="ade3e-119">childActivityName</span></span>|<span data-ttu-id="ade3e-120">キャンセルが要求された子アクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="ade3e-120">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ade3e-121">子要素</span><span class="sxs-lookup"><span data-stu-id="ade3e-121">Child Elements</span></span>  
 <span data-ttu-id="ade3e-122">なし。</span><span class="sxs-lookup"><span data-stu-id="ade3e-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ade3e-123">親要素</span><span class="sxs-lookup"><span data-stu-id="ade3e-123">Parent Elements</span></span>  
  
|<span data-ttu-id="ade3e-124">要素</span><span class="sxs-lookup"><span data-stu-id="ade3e-124">Element</span></span>|<span data-ttu-id="ade3e-125">説明</span><span class="sxs-lookup"><span data-stu-id="ade3e-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ade3e-126">\<activityScheduledQuery></span><span class="sxs-lookup"><span data-stu-id="ade3e-126">\<activityScheduledQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activityscheduledquery.md)|<span data-ttu-id="ade3e-127">親アクティビティによる実行がスケジュールされているアクティビティを追跡するために使用するクエリ。</span><span class="sxs-lookup"><span data-stu-id="ade3e-127">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ade3e-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="ade3e-128">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityScheduledQuery?displayProperty=nameWithType>
- [<span data-ttu-id="ade3e-129">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="ade3e-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="ade3e-130">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="ade3e-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
