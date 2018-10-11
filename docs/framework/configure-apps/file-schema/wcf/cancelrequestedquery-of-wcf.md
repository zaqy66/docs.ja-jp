---
title: WCF の &lt;cancelRequestedQuery&gt;
ms.date: 03/30/2017
ms.assetid: b690d870-02eb-4c56-8bc3-e5ca99d7097b
ms.openlocfilehash: 38d946a213131e8dcb6f4100d0ad67f7c167f342
ms.sourcegitcommit: 2eb5ca4956231c1a0efd34b6a9cab6153a5438af
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/11/2018
ms.locfileid: "49086402"
---
# <a name="ltcancelrequestedquerygt-of-wcf"></a><span data-ttu-id="12963-102">WCF の &lt;cancelRequestedQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="12963-102">&lt;cancelRequestedQuery&gt; of WCF</span></span>
<span data-ttu-id="12963-103">親アクティビティが子アクティビティを取り消すための要求を追跡するのに使用するクエリを表します。</span><span class="sxs-lookup"><span data-stu-id="12963-103">Represents a query that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="12963-104">追跡参加要素がキャンセル要求レコード オブジェクトを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="12963-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
 <span data-ttu-id="12963-105">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="12963-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
 <span data-ttu-id="12963-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="12963-106">\<system.serviceModel></span></span>  
<span data-ttu-id="12963-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="12963-107">\<tracking></span></span>  
<span data-ttu-id="12963-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="12963-108">\<trackingProfile></span></span>  
<span data-ttu-id="12963-109">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="12963-109">\<workflow></span></span>  
<span data-ttu-id="12963-110">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="12963-110">\<cancelRequestedQueries></span></span>  
<span data-ttu-id="12963-111">\<cancelRequestedQuery ></span><span class="sxs-lookup"><span data-stu-id="12963-111">\<cancelRequestedQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="12963-112">構文</span><span class="sxs-lookup"><span data-stu-id="12963-112">Syntax</span></span>  
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="12963-113">属性および要素</span><span class="sxs-lookup"><span data-stu-id="12963-113">Attributes and Elements</span></span>  
 <span data-ttu-id="12963-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="12963-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="12963-115">属性</span><span class="sxs-lookup"><span data-stu-id="12963-115">Attributes</span></span>  
  
|<span data-ttu-id="12963-116">属性</span><span class="sxs-lookup"><span data-stu-id="12963-116">Attribute</span></span>|<span data-ttu-id="12963-117">説明</span><span class="sxs-lookup"><span data-stu-id="12963-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="12963-118">activityName</span><span class="sxs-lookup"><span data-stu-id="12963-118">activityName</span></span>|<span data-ttu-id="12963-119">キャンセルを要求しているアクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="12963-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|<span data-ttu-id="12963-120">childActivityName</span><span class="sxs-lookup"><span data-stu-id="12963-120">childActivityName</span></span>|<span data-ttu-id="12963-121">キャンセルが要求された子アクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="12963-121">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="12963-122">子要素</span><span class="sxs-lookup"><span data-stu-id="12963-122">Child Elements</span></span>  
 <span data-ttu-id="12963-123">なし。</span><span class="sxs-lookup"><span data-stu-id="12963-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="12963-124">親要素</span><span class="sxs-lookup"><span data-stu-id="12963-124">Parent Elements</span></span>  
  
|<span data-ttu-id="12963-125">要素</span><span class="sxs-lookup"><span data-stu-id="12963-125">Element</span></span>|<span data-ttu-id="12963-126">説明</span><span class="sxs-lookup"><span data-stu-id="12963-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="12963-127">\<faultPropagationQuery ></span><span class="sxs-lookup"><span data-stu-id="12963-127">\<faultPropagationQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationquery.md)|<span data-ttu-id="12963-128">親アクティビティが子アクティビティを取り消すための要求を追跡するのに使用する構成要素の一覧を表します。</span><span class="sxs-lookup"><span data-stu-id="12963-128">Represents a list of configuration elements that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="12963-129">追跡参加要素がキャンセル要求レコード オブジェクトを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="12963-129">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="12963-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="12963-130">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.CancelRequestedQueryElement?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.CancelRequestedQuery?displayProperty=nameWithType>     
 [<span data-ttu-id="12963-131">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="12963-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="12963-132">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="12963-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
