---
title: WCF の &lt;bookmarkResumptionQueries&gt;
ms.date: 03/30/2017
ms.assetid: ed086712-1dc7-4932-a592-d1116a0155f3
ms.openlocfilehash: 80d1c1e4bc61972d44c27bcbdd0eba14d97c2d6c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54493951"
---
# <a name="ltbookmarkresumptionqueriesgt-of-wcf"></a><span data-ttu-id="261b8-102">WCF の &lt;bookmarkResumptionQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="261b8-102">&lt;bookmarkResumptionQueries&gt; of WCF</span></span>
  
<span data-ttu-id="261b8-103">ワークフロー インスタンス内のブックマークの再開を追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="261b8-103">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="261b8-104">追跡参加要素がブックマーク再開レコードを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="261b8-104">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
<span data-ttu-id="261b8-105">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="261b8-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>
  
<span data-ttu-id="261b8-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="261b8-106">\<system.serviceModel></span></span>  
<span data-ttu-id="261b8-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="261b8-107">\<tracking></span></span>  
<span data-ttu-id="261b8-108">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="261b8-108">\<profiles></span></span>  
<span data-ttu-id="261b8-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="261b8-109">\<trackingProfile></span></span>  
<span data-ttu-id="261b8-110">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="261b8-110">\<workflow></span></span>  
<span data-ttu-id="261b8-111">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="261b8-111">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="261b8-112">\<bookmarkResumptionQuery></span><span class="sxs-lookup"><span data-stu-id="261b8-112">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="261b8-113">構文</span><span class="sxs-lookup"><span data-stu-id="261b8-113">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <bookmarkResumptionQueries>
          <bookmarkResumptionQuery name="String" />
        </bookmarkResumptionQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="261b8-114">属性と要素</span><span class="sxs-lookup"><span data-stu-id="261b8-114">Attributes and elements</span></span>  
  
<span data-ttu-id="261b8-115">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="261b8-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="261b8-116">属性</span><span class="sxs-lookup"><span data-stu-id="261b8-116">Attributes</span></span>  
  
<span data-ttu-id="261b8-117">なし。</span><span class="sxs-lookup"><span data-stu-id="261b8-117">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="261b8-118">子要素</span><span class="sxs-lookup"><span data-stu-id="261b8-118">Child elements</span></span>  
  
|<span data-ttu-id="261b8-119">要素</span><span class="sxs-lookup"><span data-stu-id="261b8-119">Element</span></span>|<span data-ttu-id="261b8-120">説明</span><span class="sxs-lookup"><span data-stu-id="261b8-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="261b8-121">\<bookmarkResumptionQuery></span><span class="sxs-lookup"><span data-stu-id="261b8-121">\<bookmarkResumptionQuery></span></span>](bookmarkresumptionquery-of-wcf.md)|<span data-ttu-id="261b8-122">ワークフロー インスタンス内のブックマークの再開を追跡するために使用されるクエリ。</span><span class="sxs-lookup"><span data-stu-id="261b8-122">A query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="261b8-123">追跡参加要素がブックマーク再開レコードを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="261b8-123">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="261b8-124">親要素</span><span class="sxs-lookup"><span data-stu-id="261b8-124">Parent elements</span></span>  
  
|<span data-ttu-id="261b8-125">要素</span><span class="sxs-lookup"><span data-stu-id="261b8-125">Element</span></span>|<span data-ttu-id="261b8-126">説明</span><span class="sxs-lookup"><span data-stu-id="261b8-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="261b8-127">\<workflow></span><span class="sxs-lookup"><span data-stu-id="261b8-127">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="261b8-128">`activityDefinitionId` プロパティによって識別される特定のワークフローのすべてのクエリを格納する構成要素。</span><span class="sxs-lookup"><span data-stu-id="261b8-128">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="261b8-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="261b8-129">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [<span data-ttu-id="261b8-130">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="261b8-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="261b8-131">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="261b8-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
