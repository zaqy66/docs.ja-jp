---
title: WCF の &lt;cancelRequestedQueries&gt;
ms.date: 03/30/2017
ms.assetid: a7cc7125-9ea3-4d3f-99c0-878cdeb1258a
ms.openlocfilehash: 40fbcafd641e93be6ba21635f4f6e6428be62c12
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/26/2018
ms.locfileid: "50032706"
---
# <a name="ltcancelrequestedqueriesgt-of-wcf"></a><span data-ttu-id="f2b0c-102">WCF の &lt;cancelRequestedQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="f2b0c-102">&lt;cancelRequestedQueries&gt; of WCF</span></span>
<span data-ttu-id="f2b0c-103">親アクティビティが子アクティビティを取り消すための要求を追跡するのに使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="f2b0c-103">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="f2b0c-104">追跡参加要素がキャンセル要求レコード オブジェクトを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="f2b0c-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
<span data-ttu-id="f2b0c-105">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="f2b0c-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="f2b0c-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="f2b0c-106">\<system.serviceModel></span></span>  
<span data-ttu-id="f2b0c-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="f2b0c-107">\<tracking></span></span>  
<span data-ttu-id="f2b0c-108">\<プロファイル > \<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="f2b0c-108">\<profiles> \<trackingProfile></span></span>  
<span data-ttu-id="f2b0c-109">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="f2b0c-109">\<workflow></span></span>  
<span data-ttu-id="f2b0c-110">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="f2b0c-110">\<cancelRequestedQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2b0c-111">構文</span><span class="sxs-lookup"><span data-stu-id="f2b0c-111">Syntax</span></span>  
  
```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <cancelRequestQueries>
          <cancelRequestQuery activityName="String"
                              childActivityName="String"/>
        </cancelRequestQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>  
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f2b0c-112">属性と要素</span><span class="sxs-lookup"><span data-stu-id="f2b0c-112">Attributes and elements</span></span>  

<span data-ttu-id="f2b0c-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="f2b0c-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f2b0c-114">属性</span><span class="sxs-lookup"><span data-stu-id="f2b0c-114">Attributes</span></span>

<span data-ttu-id="f2b0c-115">なし。</span><span class="sxs-lookup"><span data-stu-id="f2b0c-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2b0c-116">子要素</span><span class="sxs-lookup"><span data-stu-id="f2b0c-116">Child elements</span></span>
  
|<span data-ttu-id="f2b0c-117">要素</span><span class="sxs-lookup"><span data-stu-id="f2b0c-117">Element</span></span>|<span data-ttu-id="f2b0c-118">説明</span><span class="sxs-lookup"><span data-stu-id="f2b0c-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f2b0c-119">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="f2b0c-119">\<cancelRequestedQuery></span></span>](cancelrequestedquery-of-wcf.md)|<span data-ttu-id="f2b0c-120">親アクティビティが子アクティビティを取り消すための要求を追跡するのに使用するクエリ。</span><span class="sxs-lookup"><span data-stu-id="f2b0c-120">A query that is used to track requests to cancel a child activity by the parent activity</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f2b0c-121">親要素</span><span class="sxs-lookup"><span data-stu-id="f2b0c-121">Parent elements</span></span>  
  
|<span data-ttu-id="f2b0c-122">要素</span><span class="sxs-lookup"><span data-stu-id="f2b0c-122">Element</span></span>|<span data-ttu-id="f2b0c-123">説明</span><span class="sxs-lookup"><span data-stu-id="f2b0c-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f2b0c-124">\<workflow></span><span class="sxs-lookup"><span data-stu-id="f2b0c-124">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="f2b0c-125"><xref:System.ServiceModel.Activities.Tracking.Configuration.ProfileWorkflowElement.ActivityDefinitionId> プロパティによって識別される特定のワークフローのすべてのクエリを格納する構成要素。</span><span class="sxs-lookup"><span data-stu-id="f2b0c-125">A configuration element that contains all queries for a specific workflow identified by the <xref:System.ServiceModel.Activities.Tracking.Configuration.ProfileWorkflowElement.ActivityDefinitionId> property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f2b0c-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2b0c-126">See also</span></span>

- <xref:System.Activities.Tracking.CancelRequestedQuery>
- [<span data-ttu-id="f2b0c-127">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="f2b0c-127">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="f2b0c-128">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="f2b0c-128">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
