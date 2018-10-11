---
title: WCF の  &lt;activityScheduledQuery&gt;
ms.date: 03/30/2017
ms.assetid: 25f6eee1-3d98-4c39-b517-c0813f03f106
ms.openlocfilehash: 9a53d72316dad0178f24e05656a4fb4531b88aec
ms.sourcegitcommit: 2eb5ca4956231c1a0efd34b6a9cab6153a5438af
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/11/2018
ms.locfileid: "49087766"
---
# <a name="ltactivityscheduledquerygt-of-wcf"></a><span data-ttu-id="0c471-102">WCF の  &lt;activityScheduledQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="0c471-102">&lt;activityScheduledQuery&gt; of WCF</span></span>
<span data-ttu-id="0c471-103">親アクティビティによる実行がスケジュールされているアクティビティを追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="0c471-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="0c471-104">アクティビティがスケジュールされたレコードを追跡参加要素が定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="0c471-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
 <span data-ttu-id="0c471-105">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="0c471-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
 <span data-ttu-id="0c471-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="0c471-106">\<system.serviceModel></span></span>  
<span data-ttu-id="0c471-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="0c471-107">\<tracking></span></span>  
<span data-ttu-id="0c471-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="0c471-108">\<trackingProfile></span></span>  
<span data-ttu-id="0c471-109">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="0c471-109">\<workflow></span></span>  
<span data-ttu-id="0c471-110">\<activityScheduledQueries ></span><span class="sxs-lookup"><span data-stu-id="0c471-110">\<activityScheduledQueries></span></span>  
<span data-ttu-id="0c471-111">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="0c471-111">\<activityScheduledQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c471-112">構文</span><span class="sxs-lookup"><span data-stu-id="0c471-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0c471-113">属性および要素</span><span class="sxs-lookup"><span data-stu-id="0c471-113">Attributes and Elements</span></span>  
 <span data-ttu-id="0c471-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="0c471-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0c471-115">属性</span><span class="sxs-lookup"><span data-stu-id="0c471-115">Attributes</span></span>  
  
|<span data-ttu-id="0c471-116">属性</span><span class="sxs-lookup"><span data-stu-id="0c471-116">Attribute</span></span>|<span data-ttu-id="0c471-117">説明</span><span class="sxs-lookup"><span data-stu-id="0c471-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0c471-118">activityName</span><span class="sxs-lookup"><span data-stu-id="0c471-118">activityName</span></span>|<span data-ttu-id="0c471-119">キャンセルを要求しているアクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="0c471-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|<span data-ttu-id="0c471-120">childActivityName</span><span class="sxs-lookup"><span data-stu-id="0c471-120">childActivityName</span></span>|<span data-ttu-id="0c471-121">キャンセルが要求された子アクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="0c471-121">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0c471-122">子要素</span><span class="sxs-lookup"><span data-stu-id="0c471-122">Child Elements</span></span>  
 <span data-ttu-id="0c471-123">なし。</span><span class="sxs-lookup"><span data-stu-id="0c471-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0c471-124">親要素</span><span class="sxs-lookup"><span data-stu-id="0c471-124">Parent Elements</span></span>  
  
|<span data-ttu-id="0c471-125">要素</span><span class="sxs-lookup"><span data-stu-id="0c471-125">Element</span></span>|<span data-ttu-id="0c471-126">説明</span><span class="sxs-lookup"><span data-stu-id="0c471-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0c471-127">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="0c471-127">\<activityScheduledQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activityscheduledquery.md)|<span data-ttu-id="0c471-128">親アクティビティによる実行がスケジュールされているアクティビティを追跡するために使用するクエリ。</span><span class="sxs-lookup"><span data-stu-id="0c471-128">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0c471-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c471-129">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElement>     
 <xref:System.Activities.Tracking.ActivityScheduledQuery>     
 [<span data-ttu-id="0c471-130">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="0c471-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="0c471-131">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="0c471-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
