---
title: <customTrackingQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 4e108e89-1132-46b7-868a-c7f5c69dc89f
ms.openlocfilehash: 4e525bc4c77649a6c6d70ddb2408b6ecce4a0f09
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55263767"
---
# <a name="customtrackingquery"></a><span data-ttu-id="5ca3b-101">\<customTrackingQuery></span><span class="sxs-lookup"><span data-stu-id="5ca3b-101">\<customTrackingQuery></span></span>
<span data-ttu-id="5ca3b-102">コード アクティビティで定義するイベントを追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="5ca3b-102">Represents a collection of queries that are used to track events that you define in your code activities.</span></span> <span data-ttu-id="5ca3b-103">追跡参加要素がカスタム追跡レコードを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="5ca3b-103">The query is necessary for a tracking participant to subscribe to custom tracking records.</span></span>  
  
 <span data-ttu-id="5ca3b-104">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="5ca3b-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="5ca3b-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="5ca3b-105">\<system.serviceModel></span></span>  
<span data-ttu-id="5ca3b-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="5ca3b-106">\<tracking></span></span>  
<span data-ttu-id="5ca3b-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="5ca3b-107">\<trackingProfile></span></span>  
<span data-ttu-id="5ca3b-108">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="5ca3b-108">\<workflow></span></span>  
<span data-ttu-id="5ca3b-109">\<customTrackingQueries></span><span class="sxs-lookup"><span data-stu-id="5ca3b-109">\<customTrackingQueries></span></span>  
<span data-ttu-id="5ca3b-110">\<customTrackingQuery></span><span class="sxs-lookup"><span data-stu-id="5ca3b-110">\<customTrackingQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5ca3b-111">構文</span><span class="sxs-lookup"><span data-stu-id="5ca3b-111">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <customTrackingQueries>
        <customTrackingQuery activityName="String" 
                             name="String" />
      </customTrackingQueries>
    </workflow>
 </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5ca3b-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="5ca3b-112">Attributes and Elements</span></span>  
 <span data-ttu-id="5ca3b-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="5ca3b-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5ca3b-114">属性</span><span class="sxs-lookup"><span data-stu-id="5ca3b-114">Attributes</span></span>  
  
|<span data-ttu-id="5ca3b-115">属性</span><span class="sxs-lookup"><span data-stu-id="5ca3b-115">Attribute</span></span>|<span data-ttu-id="5ca3b-116">説明</span><span class="sxs-lookup"><span data-stu-id="5ca3b-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5ca3b-117">activityName</span><span class="sxs-lookup"><span data-stu-id="5ca3b-117">activityName</span></span>|<span data-ttu-id="5ca3b-118">追跡レコードを生成したアクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="5ca3b-118">A string that specifies the name of the activity that generated the tracking record.</span></span>|  
|<span data-ttu-id="5ca3b-119">name</span><span class="sxs-lookup"><span data-stu-id="5ca3b-119">name</span></span>|<span data-ttu-id="5ca3b-120">生成されたカスタム追跡レコードの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="5ca3b-120">A string that specifies the name of the custom tracking record that is emitted.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5ca3b-121">子要素</span><span class="sxs-lookup"><span data-stu-id="5ca3b-121">Child Elements</span></span>  
 <span data-ttu-id="5ca3b-122">なし。</span><span class="sxs-lookup"><span data-stu-id="5ca3b-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5ca3b-123">親要素</span><span class="sxs-lookup"><span data-stu-id="5ca3b-123">Parent Elements</span></span>  
  
|<span data-ttu-id="5ca3b-124">要素</span><span class="sxs-lookup"><span data-stu-id="5ca3b-124">Element</span></span>|<span data-ttu-id="5ca3b-125">説明</span><span class="sxs-lookup"><span data-stu-id="5ca3b-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5ca3b-126">\<customTrackingQuery></span><span class="sxs-lookup"><span data-stu-id="5ca3b-126">\<customTrackingQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/customtrackingquery.md)|<span data-ttu-id="5ca3b-127">コード アクティビティで定義するイベントを追跡するために使用するクエリ。</span><span class="sxs-lookup"><span data-stu-id="5ca3b-127">A query that is used to track events that you define in your code activities.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5ca3b-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ca3b-128">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.CustomTrackingQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CustomTrackingQuery?displayProperty=nameWithType>
- [<span data-ttu-id="5ca3b-129">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="5ca3b-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="5ca3b-130">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="5ca3b-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
