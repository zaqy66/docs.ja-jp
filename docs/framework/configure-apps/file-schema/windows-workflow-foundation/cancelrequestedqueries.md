---
title: '&lt;cancelRequestedQueries&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: eab5af7e-76fa-434d-9d36-873e995cee05
ms.openlocfilehash: 5bc2e3ffeb93bdfcd45638d6b50e218c03706f42
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54520686"
---
# <a name="ltcancelrequestedqueriesgt"></a><span data-ttu-id="9ca70-102">&lt;cancelRequestedQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="9ca70-102">&lt;cancelRequestedQueries&gt;</span></span>
<span data-ttu-id="9ca70-103">親アクティビティが子アクティビティを取り消すための要求を追跡するのに使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="9ca70-103">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="9ca70-104">追跡参加要素がキャンセル要求レコード オブジェクトを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="9ca70-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
 <span data-ttu-id="9ca70-105">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="9ca70-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="9ca70-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="9ca70-106">\<system.serviceModel></span></span>  
<span data-ttu-id="9ca70-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="9ca70-107">\<tracking></span></span>  
<span data-ttu-id="9ca70-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="9ca70-108">\<trackingProfile></span></span>  
<span data-ttu-id="9ca70-109">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="9ca70-109">\<workflow></span></span>  
<span data-ttu-id="9ca70-110">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="9ca70-110">\<cancelRequestedQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ca70-111">構文</span><span class="sxs-lookup"><span data-stu-id="9ca70-111">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <cancelRequestQueries>
        <cancelRequestQuery activityName="String" 
                            childActivityName="String"/>
      </cancelRequestQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9ca70-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="9ca70-112">Attributes and Elements</span></span>  
 <span data-ttu-id="9ca70-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="9ca70-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9ca70-114">属性</span><span class="sxs-lookup"><span data-stu-id="9ca70-114">Attributes</span></span>  
 <span data-ttu-id="9ca70-115">なし。</span><span class="sxs-lookup"><span data-stu-id="9ca70-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="9ca70-116">子要素</span><span class="sxs-lookup"><span data-stu-id="9ca70-116">Child Elements</span></span>  
  
|<span data-ttu-id="9ca70-117">要素</span><span class="sxs-lookup"><span data-stu-id="9ca70-117">Element</span></span>|<span data-ttu-id="9ca70-118">説明</span><span class="sxs-lookup"><span data-stu-id="9ca70-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9ca70-119">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="9ca70-119">\<cancelRequestedQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/cancelrequestedquery.md)|<span data-ttu-id="9ca70-120">親アクティビティが子アクティビティを取り消すための要求を追跡するのに使用するクエリ。</span><span class="sxs-lookup"><span data-stu-id="9ca70-120">A query that is used to track requests to cancel a child activity by the parent activity</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9ca70-121">親要素</span><span class="sxs-lookup"><span data-stu-id="9ca70-121">Parent Elements</span></span>  
  
|<span data-ttu-id="9ca70-122">要素</span><span class="sxs-lookup"><span data-stu-id="9ca70-122">Element</span></span>|<span data-ttu-id="9ca70-123">説明</span><span class="sxs-lookup"><span data-stu-id="9ca70-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9ca70-124">\<workflow></span><span class="sxs-lookup"><span data-stu-id="9ca70-124">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="9ca70-125">識別される特定のワークフローのすべてのクエリを格納する構成要素、 **activityDefinitionId**プロパティ。</span><span class="sxs-lookup"><span data-stu-id="9ca70-125">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9ca70-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="9ca70-126">See also</span></span>
- [<span data-ttu-id="9ca70-127">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="9ca70-127">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="9ca70-128">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="9ca70-128">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
