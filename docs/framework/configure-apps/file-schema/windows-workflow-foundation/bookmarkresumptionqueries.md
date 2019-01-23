---
title: '&lt;bookmarkResumptionQueries&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 8ed61a7f-4254-439c-bdd8-b474971533f7
ms.openlocfilehash: ae6a81123379ecd0e7fdc72f4e115a462f81eb90
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54555038"
---
# <a name="ltbookmarkresumptionqueriesgt"></a><span data-ttu-id="9e022-102">&lt;bookmarkResumptionQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="9e022-102">&lt;bookmarkResumptionQueries&gt;</span></span>
<span data-ttu-id="9e022-103">ワークフロー インスタンス内のブックマークの再開を追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="9e022-103">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="9e022-104">追跡参加要素がブックマーク再開レコードを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="9e022-104">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
 <span data-ttu-id="9e022-105">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="9e022-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="9e022-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="9e022-106">\<system.serviceModel></span></span>  
<span data-ttu-id="9e022-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="9e022-107">\<tracking></span></span>  
<span data-ttu-id="9e022-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="9e022-108">\<trackingProfile></span></span>  
<span data-ttu-id="9e022-109">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="9e022-109">\<workflow></span></span>  
<span data-ttu-id="9e022-110">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="9e022-110">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="9e022-111">\<bookmarkResumptionQuery></span><span class="sxs-lookup"><span data-stu-id="9e022-111">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9e022-112">構文</span><span class="sxs-lookup"><span data-stu-id="9e022-112">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <bookmarkResumptionQueries>
        <bookmarkResumptionQuery name="String" />
      </bookmarkResumptionQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9e022-113">属性および要素</span><span class="sxs-lookup"><span data-stu-id="9e022-113">Attributes and Elements</span></span>  
 <span data-ttu-id="9e022-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="9e022-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9e022-115">属性</span><span class="sxs-lookup"><span data-stu-id="9e022-115">Attributes</span></span>  
 <span data-ttu-id="9e022-116">なし。</span><span class="sxs-lookup"><span data-stu-id="9e022-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="9e022-117">子要素</span><span class="sxs-lookup"><span data-stu-id="9e022-117">Child Elements</span></span>  
  
|<span data-ttu-id="9e022-118">要素</span><span class="sxs-lookup"><span data-stu-id="9e022-118">Element</span></span>|<span data-ttu-id="9e022-119">説明</span><span class="sxs-lookup"><span data-stu-id="9e022-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9e022-120">\<bookmarkResumptionQuery></span><span class="sxs-lookup"><span data-stu-id="9e022-120">\<bookmarkResumptionQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/bookmarkresumptionquery.md)|<span data-ttu-id="9e022-121">ワークフロー インスタンス内のブックマークの再開を追跡するために使用されるクエリ。</span><span class="sxs-lookup"><span data-stu-id="9e022-121">A query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="9e022-122">追跡参加要素がブックマーク再開レコードを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="9e022-122">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9e022-123">親要素</span><span class="sxs-lookup"><span data-stu-id="9e022-123">Parent Elements</span></span>  
  
|<span data-ttu-id="9e022-124">要素</span><span class="sxs-lookup"><span data-stu-id="9e022-124">Element</span></span>|<span data-ttu-id="9e022-125">説明</span><span class="sxs-lookup"><span data-stu-id="9e022-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9e022-126">\<workflow></span><span class="sxs-lookup"><span data-stu-id="9e022-126">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="9e022-127">識別される特定のワークフローのすべてのクエリを格納する構成要素、 **activityDefinitionId**プロパティ。</span><span class="sxs-lookup"><span data-stu-id="9e022-127">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9e022-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9e022-128">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [<span data-ttu-id="9e022-129">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="9e022-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="9e022-130">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="9e022-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
