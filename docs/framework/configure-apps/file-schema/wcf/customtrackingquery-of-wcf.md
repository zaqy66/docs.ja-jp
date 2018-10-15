---
title: WCF の &lt;customTrackingQuery&gt;
ms.date: 03/30/2017
ms.assetid: 164446ae-8440-4b67-b217-6786cfae1e01
ms.openlocfilehash: e13064afbd9f5dbc8d7216eb384001e1e005785c
ms.sourcegitcommit: d88024e6d6d8b242feae5f4007a709379355aa24
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/15/2018
ms.locfileid: "49316234"
---
# <a name="ltcustomtrackingquerygt-of-wcf"></a><span data-ttu-id="e54d8-102">WCF の &lt;customTrackingQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="e54d8-102">&lt;customTrackingQuery&gt; of WCF</span></span>

<span data-ttu-id="e54d8-103">コード アクティビティで定義するイベントを追跡するために使用されるクエリを表します。</span><span class="sxs-lookup"><span data-stu-id="e54d8-103">Represents a query that is used to track events that you define in your code activities.</span></span> <span data-ttu-id="e54d8-104">追跡参加要素がカスタム追跡レコードを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="e54d8-104">The query is necessary for a tracking participant to subscribe to custom tracking records.</span></span>

<span data-ttu-id="e54d8-105">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="e54d8-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="e54d8-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="e54d8-106">\<system.serviceModel></span></span>  
<span data-ttu-id="e54d8-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="e54d8-107">\<tracking></span></span>  
<span data-ttu-id="e54d8-108">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="e54d8-108">\<profiles></span></span>  
<span data-ttu-id="e54d8-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="e54d8-109">\<trackingProfile></span></span>  
<span data-ttu-id="e54d8-110">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="e54d8-110">\<workflow></span></span>  
<span data-ttu-id="e54d8-111">\<customTrackingQueries ></span><span class="sxs-lookup"><span data-stu-id="e54d8-111">\<customTrackingQueries></span></span>  
<span data-ttu-id="e54d8-112">\<customTrackingQuery ></span><span class="sxs-lookup"><span data-stu-id="e54d8-112">\<customTrackingQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e54d8-113">構文</span><span class="sxs-lookup"><span data-stu-id="e54d8-113">Syntax</span></span>  
  
```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <customTrackingQueries>
          <customTrackingQuery activityName="String"
                               name="String"/>
        </customTrackingQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="e54d8-114">属性と要素</span><span class="sxs-lookup"><span data-stu-id="e54d8-114">Attributes and elements</span></span>  

<span data-ttu-id="e54d8-115">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="e54d8-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e54d8-116">属性</span><span class="sxs-lookup"><span data-stu-id="e54d8-116">Attributes</span></span>  
  
|<span data-ttu-id="e54d8-117">属性</span><span class="sxs-lookup"><span data-stu-id="e54d8-117">Attribute</span></span>|<span data-ttu-id="e54d8-118">説明</span><span class="sxs-lookup"><span data-stu-id="e54d8-118">Description</span></span>|  
|---------------|-----------------|  
|`activityName`|<span data-ttu-id="e54d8-119">追跡レコードを生成したアクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="e54d8-119">A string that specifies the name of the activity that generated the tracking record.</span></span>|  
|`name`|<span data-ttu-id="e54d8-120">生成されたカスタム追跡レコードの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="e54d8-120">A string that specifies the name of the custom tracking record that is emitted.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e54d8-121">子要素</span><span class="sxs-lookup"><span data-stu-id="e54d8-121">Child elements</span></span>

<span data-ttu-id="e54d8-122">なし。</span><span class="sxs-lookup"><span data-stu-id="e54d8-122">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="e54d8-123">親要素</span><span class="sxs-lookup"><span data-stu-id="e54d8-123">Parent elements</span></span>

|<span data-ttu-id="e54d8-124">要素</span><span class="sxs-lookup"><span data-stu-id="e54d8-124">Element</span></span>|<span data-ttu-id="e54d8-125">説明</span><span class="sxs-lookup"><span data-stu-id="e54d8-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e54d8-126">\<customTrackingQueries></span><span class="sxs-lookup"><span data-stu-id="e54d8-126">\<customTrackingQueries></span></span>](customtrackingqueries-of-wcf.md)|<span data-ttu-id="e54d8-127">コード アクティビティで定義するイベントを追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="e54d8-127">Represents a collection of queries that are used to track events that you define in your code activities.</span></span>|
  
## <a name="see-also"></a><span data-ttu-id="e54d8-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="e54d8-128">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CustomTrackingQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CustomTrackingQuery?displayProperty=nameWithType>
- [<span data-ttu-id="e54d8-129">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="e54d8-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="e54d8-130">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="e54d8-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
