---
title: WCF の &lt;customTrackingQueries&gt;
ms.date: 03/30/2017
ms.assetid: 14cfe47e-9935-4120-84f1-8f38de8ca4c1
ms.openlocfilehash: f4f6186aa51ef1656f31fb0035f58a07e5c2447b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54700794"
---
# <a name="ltcustomtrackingqueriesgt-of-wcf"></a><span data-ttu-id="963e9-102">WCF の &lt;customTrackingQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="963e9-102">&lt;customTrackingQueries&gt; of WCF</span></span>

<span data-ttu-id="963e9-103">コード アクティビティで定義するイベントを追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="963e9-103">Represents a collection of queries that are used to track events that you define in your code activities.</span></span> <span data-ttu-id="963e9-104">追跡参加要素がカスタム追跡レコードを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="963e9-104">The query is necessary for a tracking participant to subscribe to custom tracking records.</span></span>  
  
 <span data-ttu-id="963e9-105">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="963e9-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>
  
<span data-ttu-id="963e9-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="963e9-106">\<system.serviceModel></span></span>  
<span data-ttu-id="963e9-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="963e9-107">\<tracking></span></span>  
<span data-ttu-id="963e9-108">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="963e9-108">\<profiles></span></span>  
<span data-ttu-id="963e9-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="963e9-109">\<trackingProfile></span></span>  
<span data-ttu-id="963e9-110">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="963e9-110">\<workflow></span></span>  
<span data-ttu-id="963e9-111">\<customTrackingQueries></span><span class="sxs-lookup"><span data-stu-id="963e9-111">\<customTrackingQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="963e9-112">構文</span><span class="sxs-lookup"><span data-stu-id="963e9-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="963e9-113">属性と要素</span><span class="sxs-lookup"><span data-stu-id="963e9-113">Attributes and elements</span></span>

<span data-ttu-id="963e9-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="963e9-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="963e9-115">属性</span><span class="sxs-lookup"><span data-stu-id="963e9-115">Attributes</span></span>

<span data-ttu-id="963e9-116">なし。</span><span class="sxs-lookup"><span data-stu-id="963e9-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="963e9-117">子要素</span><span class="sxs-lookup"><span data-stu-id="963e9-117">Child elements</span></span>
  
|<span data-ttu-id="963e9-118">要素</span><span class="sxs-lookup"><span data-stu-id="963e9-118">Element</span></span>|<span data-ttu-id="963e9-119">説明</span><span class="sxs-lookup"><span data-stu-id="963e9-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="963e9-120">\<customTrackingQuery></span><span class="sxs-lookup"><span data-stu-id="963e9-120">\<customTrackingQuery></span></span>](customtrackingquery-of-wcf.md)|<span data-ttu-id="963e9-121">コード アクティビティで定義するイベントを追跡するために使用するクエリ。</span><span class="sxs-lookup"><span data-stu-id="963e9-121">A query that is used to track events that you define in your code activities.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="963e9-122">親要素</span><span class="sxs-lookup"><span data-stu-id="963e9-122">Parent elements</span></span>  
  
|<span data-ttu-id="963e9-123">要素</span><span class="sxs-lookup"><span data-stu-id="963e9-123">Element</span></span>|<span data-ttu-id="963e9-124">説明</span><span class="sxs-lookup"><span data-stu-id="963e9-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="963e9-125">\<workflow></span><span class="sxs-lookup"><span data-stu-id="963e9-125">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="963e9-126">`activityDefinitionId` プロパティによって識別される特定のワークフローのすべてのクエリを格納する構成要素。</span><span class="sxs-lookup"><span data-stu-id="963e9-126">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="963e9-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="963e9-127">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CustomTrackingQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CustomTrackingQuery?displayProperty=nameWithType>
- [<span data-ttu-id="963e9-128">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="963e9-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="963e9-129">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="963e9-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
