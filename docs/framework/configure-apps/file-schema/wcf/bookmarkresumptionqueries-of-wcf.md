---
title: WCF の &lt;bookmarkResumptionQueries&gt;
ms.date: 03/30/2017
ms.assetid: ed086712-1dc7-4932-a592-d1116a0155f3
ms.openlocfilehash: ba8c98557a859f4bd37b9aaca80a44c393429da4
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146083"
---
# <a name="ltbookmarkresumptionqueriesgt-of-wcf"></a><span data-ttu-id="3fcc1-102">WCF の &lt;bookmarkResumptionQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="3fcc1-102">&lt;bookmarkResumptionQueries&gt; of WCF</span></span>
  
<span data-ttu-id="3fcc1-103">ワークフロー インスタンス内のブックマークの再開を追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="3fcc1-103">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="3fcc1-104">追跡参加要素がブックマーク再開レコードを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="3fcc1-104">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
<span data-ttu-id="3fcc1-105">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="3fcc1-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>
  
<span data-ttu-id="3fcc1-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="3fcc1-106">\<system.serviceModel></span></span>  
<span data-ttu-id="3fcc1-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="3fcc1-107">\<tracking></span></span>  
<span data-ttu-id="3fcc1-108">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="3fcc1-108">\<profiles></span></span>  
<span data-ttu-id="3fcc1-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="3fcc1-109">\<trackingProfile></span></span>  
<span data-ttu-id="3fcc1-110">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="3fcc1-110">\<workflow></span></span>  
<span data-ttu-id="3fcc1-111">\<bookmarkResumptionQueries ></span><span class="sxs-lookup"><span data-stu-id="3fcc1-111">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="3fcc1-112">\<bookmarkResumptionQuery ></span><span class="sxs-lookup"><span data-stu-id="3fcc1-112">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3fcc1-113">構文</span><span class="sxs-lookup"><span data-stu-id="3fcc1-113">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3fcc1-114">属性と要素</span><span class="sxs-lookup"><span data-stu-id="3fcc1-114">Attributes and elements</span></span>  
  
<span data-ttu-id="3fcc1-115">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="3fcc1-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3fcc1-116">属性</span><span class="sxs-lookup"><span data-stu-id="3fcc1-116">Attributes</span></span>  
  
<span data-ttu-id="3fcc1-117">なし。</span><span class="sxs-lookup"><span data-stu-id="3fcc1-117">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="3fcc1-118">子要素</span><span class="sxs-lookup"><span data-stu-id="3fcc1-118">Child elements</span></span>  
  
|<span data-ttu-id="3fcc1-119">要素</span><span class="sxs-lookup"><span data-stu-id="3fcc1-119">Element</span></span>|<span data-ttu-id="3fcc1-120">説明</span><span class="sxs-lookup"><span data-stu-id="3fcc1-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3fcc1-121">\<bookmarkResumptionQuery ></span><span class="sxs-lookup"><span data-stu-id="3fcc1-121">\<bookmarkResumptionQuery></span></span>](bookmarkresumptionquery-of-wcf.md)|<span data-ttu-id="3fcc1-122">ワークフロー インスタンス内のブックマークの再開を追跡するために使用されるクエリ。</span><span class="sxs-lookup"><span data-stu-id="3fcc1-122">A query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="3fcc1-123">追跡参加要素がブックマーク再開レコードを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="3fcc1-123">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="3fcc1-124">親要素</span><span class="sxs-lookup"><span data-stu-id="3fcc1-124">Parent elements</span></span>  
  
|<span data-ttu-id="3fcc1-125">要素</span><span class="sxs-lookup"><span data-stu-id="3fcc1-125">Element</span></span>|<span data-ttu-id="3fcc1-126">説明</span><span class="sxs-lookup"><span data-stu-id="3fcc1-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3fcc1-127">\<workflow></span><span class="sxs-lookup"><span data-stu-id="3fcc1-127">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="3fcc1-128">`activityDefinitionId` プロパティによって識別される特定のワークフローのすべてのクエリを格納する構成要素。</span><span class="sxs-lookup"><span data-stu-id="3fcc1-128">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3fcc1-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="3fcc1-129">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType> 
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>       
- [<span data-ttu-id="3fcc1-130">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="3fcc1-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
- [<span data-ttu-id="3fcc1-131">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="3fcc1-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
