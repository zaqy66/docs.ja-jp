---
title: WCF の &lt;cancelRequestedQuery&gt;
ms.date: 03/30/2017
ms.assetid: b690d870-02eb-4c56-8bc3-e5ca99d7097b
ms.openlocfilehash: 6b41721dcc0c489377c59bfccdd0b1a617f551b0
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149073"
---
# <a name="ltcancelrequestedquerygt-of-wcf"></a><span data-ttu-id="34de0-102">WCF の &lt;cancelRequestedQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="34de0-102">&lt;cancelRequestedQuery&gt; of WCF</span></span>

<span data-ttu-id="34de0-103">親アクティビティが子アクティビティを取り消すための要求を追跡するのに使用するクエリを表します。</span><span class="sxs-lookup"><span data-stu-id="34de0-103">Represents a query that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="34de0-104">追跡参加要素がキャンセル要求レコード オブジェクトを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="34de0-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
<span data-ttu-id="34de0-105">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="34de0-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>
  
<span data-ttu-id="34de0-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="34de0-106">\<system.serviceModel></span></span>  
<span data-ttu-id="34de0-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="34de0-107">\<tracking></span></span>  
<span data-ttu-id="34de0-108">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="34de0-108">\<profiles></span></span>  
<span data-ttu-id="34de0-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="34de0-109">\<trackingProfile></span></span>  
<span data-ttu-id="34de0-110">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="34de0-110">\<workflow></span></span>  
<span data-ttu-id="34de0-111">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="34de0-111">\<cancelRequestedQueries></span></span>  
<span data-ttu-id="34de0-112">\<cancelRequestedQuery ></span><span class="sxs-lookup"><span data-stu-id="34de0-112">\<cancelRequestedQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="34de0-113">構文</span><span class="sxs-lookup"><span data-stu-id="34de0-113">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <cancelRequestedQueries>
          <cancelRequestedQuery activityName="String"
                                childActivityName="String" />
        </cancelRequestedQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="34de0-114">属性と要素</span><span class="sxs-lookup"><span data-stu-id="34de0-114">Attributes and elements</span></span>

<span data-ttu-id="34de0-115">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="34de0-115">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="34de0-116">属性</span><span class="sxs-lookup"><span data-stu-id="34de0-116">Attributes</span></span>  
  
|<span data-ttu-id="34de0-117">属性</span><span class="sxs-lookup"><span data-stu-id="34de0-117">Attribute</span></span>|<span data-ttu-id="34de0-118">説明</span><span class="sxs-lookup"><span data-stu-id="34de0-118">Description</span></span>|  
|---------------|-----------------|  
|`activityName`|<span data-ttu-id="34de0-119">キャンセルを要求しているアクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="34de0-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|`childActivityName`|<span data-ttu-id="34de0-120">キャンセルが要求された子アクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="34de0-120">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="34de0-121">子要素</span><span class="sxs-lookup"><span data-stu-id="34de0-121">Child elements</span></span>

<span data-ttu-id="34de0-122">なし。</span><span class="sxs-lookup"><span data-stu-id="34de0-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="34de0-123">親要素</span><span class="sxs-lookup"><span data-stu-id="34de0-123">Parent elements</span></span>
  
|<span data-ttu-id="34de0-124">要素</span><span class="sxs-lookup"><span data-stu-id="34de0-124">Element</span></span>|<span data-ttu-id="34de0-125">説明</span><span class="sxs-lookup"><span data-stu-id="34de0-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="34de0-126">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="34de0-126">\<cancelRequestedQueries></span></span>](cancelrequestedqueries-of-wcf.md)|<span data-ttu-id="34de0-127">親アクティビティが子アクティビティを取り消すための要求を追跡するのに使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="34de0-127">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="34de0-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="34de0-128">See also</span></span>  

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CancelRequestedQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CancelRequestedQuery?displayProperty=nameWithType>
- [<span data-ttu-id="34de0-129">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="34de0-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="34de0-130">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="34de0-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
