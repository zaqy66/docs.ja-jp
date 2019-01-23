---
title: WCF の &lt;cancelRequestedQuery&gt;
ms.date: 03/30/2017
ms.assetid: b690d870-02eb-4c56-8bc3-e5ca99d7097b
ms.openlocfilehash: 72fd23097760375738c2116b4535940873436986
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498269"
---
# <a name="ltcancelrequestedquerygt-of-wcf"></a><span data-ttu-id="2cfc4-102">WCF の &lt;cancelRequestedQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="2cfc4-102">&lt;cancelRequestedQuery&gt; of WCF</span></span>

<span data-ttu-id="2cfc4-103">親アクティビティが子アクティビティを取り消すための要求を追跡するのに使用するクエリを表します。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-103">Represents a query that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="2cfc4-104">追跡参加要素がキャンセル要求レコード オブジェクトを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
<span data-ttu-id="2cfc4-105">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>
  
<span data-ttu-id="2cfc4-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="2cfc4-106">\<system.serviceModel></span></span>  
<span data-ttu-id="2cfc4-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="2cfc4-107">\<tracking></span></span>  
<span data-ttu-id="2cfc4-108">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="2cfc4-108">\<profiles></span></span>  
<span data-ttu-id="2cfc4-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="2cfc4-109">\<trackingProfile></span></span>  
<span data-ttu-id="2cfc4-110">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="2cfc4-110">\<workflow></span></span>  
<span data-ttu-id="2cfc4-111">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="2cfc4-111">\<cancelRequestedQueries></span></span>  
<span data-ttu-id="2cfc4-112">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="2cfc4-112">\<cancelRequestedQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2cfc4-113">構文</span><span class="sxs-lookup"><span data-stu-id="2cfc4-113">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2cfc4-114">属性と要素</span><span class="sxs-lookup"><span data-stu-id="2cfc4-114">Attributes and elements</span></span>

<span data-ttu-id="2cfc4-115">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-115">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="2cfc4-116">属性</span><span class="sxs-lookup"><span data-stu-id="2cfc4-116">Attributes</span></span>  
  
|<span data-ttu-id="2cfc4-117">属性</span><span class="sxs-lookup"><span data-stu-id="2cfc4-117">Attribute</span></span>|<span data-ttu-id="2cfc4-118">説明</span><span class="sxs-lookup"><span data-stu-id="2cfc4-118">Description</span></span>|  
|---------------|-----------------|  
|`activityName`|<span data-ttu-id="2cfc4-119">キャンセルを要求しているアクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|`childActivityName`|<span data-ttu-id="2cfc4-120">キャンセルが要求された子アクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-120">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2cfc4-121">子要素</span><span class="sxs-lookup"><span data-stu-id="2cfc4-121">Child elements</span></span>

<span data-ttu-id="2cfc4-122">なし。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2cfc4-123">親要素</span><span class="sxs-lookup"><span data-stu-id="2cfc4-123">Parent elements</span></span>
  
|<span data-ttu-id="2cfc4-124">要素</span><span class="sxs-lookup"><span data-stu-id="2cfc4-124">Element</span></span>|<span data-ttu-id="2cfc4-125">説明</span><span class="sxs-lookup"><span data-stu-id="2cfc4-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2cfc4-126">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="2cfc4-126">\<cancelRequestedQueries></span></span>](cancelrequestedqueries-of-wcf.md)|<span data-ttu-id="2cfc4-127">親アクティビティが子アクティビティを取り消すための要求を追跡するのに使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="2cfc4-127">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="2cfc4-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="2cfc4-128">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CancelRequestedQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CancelRequestedQuery?displayProperty=nameWithType>
- [<span data-ttu-id="2cfc4-129">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="2cfc4-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="2cfc4-130">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="2cfc4-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
