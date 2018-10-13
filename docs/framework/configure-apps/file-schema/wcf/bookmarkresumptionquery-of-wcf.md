---
title: WCF の &lt;bookmarkResumptionQuery&gt;
ms.date: 03/30/2017
ms.assetid: 755a34f0-87c9-4a1e-ae4d-0fb8a6fbdc0e
ms.openlocfilehash: f0721e7e14d543b1ff212fe59ed6a2de0a8a9968
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2018
ms.locfileid: "49308433"
---
# <a name="ltbookmarkresumptionquerygt-of-wcf"></a><span data-ttu-id="7d01d-102">WCF の &lt;bookmarkResumptionQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="7d01d-102">&lt;bookmarkResumptionQuery&gt; of WCF</span></span>

<span data-ttu-id="7d01d-103">ワークフロー インスタンス内のブックマークの再開を追跡するために使用されるクエリを表します。</span><span class="sxs-lookup"><span data-stu-id="7d01d-103">Represents a query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="7d01d-104">追跡参加要素がブックマーク再開レコードを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="7d01d-104">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
<span data-ttu-id="7d01d-105">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="7d01d-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>
  
<span data-ttu-id="7d01d-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="7d01d-106">\<system.serviceModel></span></span>  
<span data-ttu-id="7d01d-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="7d01d-107">\<tracking></span></span>  
<span data-ttu-id="7d01d-108">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="7d01d-108">\<profiles></span></span>  
<span data-ttu-id="7d01d-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="7d01d-109">\<trackingProfile></span></span>  
<span data-ttu-id="7d01d-110">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="7d01d-110">\<workflow></span></span>  
<span data-ttu-id="7d01d-111">\<bookmarkResumptionQueries ></span><span class="sxs-lookup"><span data-stu-id="7d01d-111">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="7d01d-112">\<bookmarkResumptionQuery ></span><span class="sxs-lookup"><span data-stu-id="7d01d-112">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7d01d-113">構文</span><span class="sxs-lookup"><span data-stu-id="7d01d-113">Syntax</span></span>  
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="7d01d-114">属性と要素</span><span class="sxs-lookup"><span data-stu-id="7d01d-114">Attributes and elements</span></span>

<span data-ttu-id="7d01d-115">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="7d01d-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7d01d-116">属性</span><span class="sxs-lookup"><span data-stu-id="7d01d-116">Attributes</span></span>  
  
|<span data-ttu-id="7d01d-117">属性</span><span class="sxs-lookup"><span data-stu-id="7d01d-117">Attribute</span></span>|<span data-ttu-id="7d01d-118">説明</span><span class="sxs-lookup"><span data-stu-id="7d01d-118">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="7d01d-119">定期受信するブックマーク レコードの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="7d01d-119">A string that specifies the name of the bookmark record to subscribe to.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7d01d-120">子要素</span><span class="sxs-lookup"><span data-stu-id="7d01d-120">Child elements</span></span>

<span data-ttu-id="7d01d-121">なし。</span><span class="sxs-lookup"><span data-stu-id="7d01d-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7d01d-122">親要素</span><span class="sxs-lookup"><span data-stu-id="7d01d-122">Parent elements</span></span>  
  
|<span data-ttu-id="7d01d-123">要素</span><span class="sxs-lookup"><span data-stu-id="7d01d-123">Element</span></span>|<span data-ttu-id="7d01d-124">説明</span><span class="sxs-lookup"><span data-stu-id="7d01d-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7d01d-125">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="7d01d-125">\<bookmarkResumptionQueries></span></span>](bookmarkresumptionqueries-of-wcf.md)|<span data-ttu-id="7d01d-126">ワークフロー インスタンス内のブックマークの再開を追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="7d01d-126">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7d01d-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="7d01d-127">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [<span data-ttu-id="7d01d-128">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="7d01d-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="7d01d-129">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="7d01d-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
