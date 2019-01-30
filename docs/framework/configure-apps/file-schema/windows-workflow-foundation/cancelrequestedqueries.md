---
title: <cancelRequestedQueries>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: eab5af7e-76fa-434d-9d36-873e995cee05
ms.openlocfilehash: 989d6e99457108336c38fb1eece4c9ac2444c974
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271500"
---
# <a name="cancelrequestedqueries"></a><span data-ttu-id="1fd44-101">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="1fd44-101">\<cancelRequestedQueries></span></span>
<span data-ttu-id="1fd44-102">親アクティビティが子アクティビティを取り消すための要求を追跡するのに使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="1fd44-102">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="1fd44-103">追跡参加要素がキャンセル要求レコード オブジェクトを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="1fd44-103">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
 <span data-ttu-id="1fd44-104">追跡プロファイルのクエリの詳細については、次を参照してください[追跡プロファイル。](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="1fd44-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="1fd44-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="1fd44-105">\<system.serviceModel></span></span>  
<span data-ttu-id="1fd44-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="1fd44-106">\<tracking></span></span>  
<span data-ttu-id="1fd44-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="1fd44-107">\<trackingProfile></span></span>  
<span data-ttu-id="1fd44-108">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="1fd44-108">\<workflow></span></span>  
<span data-ttu-id="1fd44-109">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="1fd44-109">\<cancelRequestedQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1fd44-110">構文</span><span class="sxs-lookup"><span data-stu-id="1fd44-110">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1fd44-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="1fd44-111">Attributes and Elements</span></span>  
 <span data-ttu-id="1fd44-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="1fd44-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1fd44-113">属性</span><span class="sxs-lookup"><span data-stu-id="1fd44-113">Attributes</span></span>  
 <span data-ttu-id="1fd44-114">なし。</span><span class="sxs-lookup"><span data-stu-id="1fd44-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="1fd44-115">子要素</span><span class="sxs-lookup"><span data-stu-id="1fd44-115">Child Elements</span></span>  
  
|<span data-ttu-id="1fd44-116">要素</span><span class="sxs-lookup"><span data-stu-id="1fd44-116">Element</span></span>|<span data-ttu-id="1fd44-117">説明</span><span class="sxs-lookup"><span data-stu-id="1fd44-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1fd44-118">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="1fd44-118">\<cancelRequestedQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/cancelrequestedquery.md)|<span data-ttu-id="1fd44-119">親アクティビティが子アクティビティを取り消すための要求を追跡するのに使用するクエリ。</span><span class="sxs-lookup"><span data-stu-id="1fd44-119">A query that is used to track requests to cancel a child activity by the parent activity</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="1fd44-120">親要素</span><span class="sxs-lookup"><span data-stu-id="1fd44-120">Parent Elements</span></span>  
  
|<span data-ttu-id="1fd44-121">要素</span><span class="sxs-lookup"><span data-stu-id="1fd44-121">Element</span></span>|<span data-ttu-id="1fd44-122">説明</span><span class="sxs-lookup"><span data-stu-id="1fd44-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1fd44-123">\<workflow></span><span class="sxs-lookup"><span data-stu-id="1fd44-123">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="1fd44-124">識別される特定のワークフローのすべてのクエリを格納する構成要素、 **activityDefinitionId**プロパティ。</span><span class="sxs-lookup"><span data-stu-id="1fd44-124">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1fd44-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="1fd44-125">See also</span></span>
- [<span data-ttu-id="1fd44-126">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="1fd44-126">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="1fd44-127">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="1fd44-127">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
