---
title: '&lt;faultPropagationQueries&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 00ff90ae-ebe0-4c85-a93f-61557288d0a3
ms.openlocfilehash: 546b37279c8ba58f9dd9f07dabacb7af602ff232
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54610059"
---
# <a name="ltfaultpropagationqueriesgt"></a><span data-ttu-id="82513-102">&lt;faultPropagationQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="82513-102">&lt;faultPropagationQueries&gt;</span></span>
<span data-ttu-id="82513-103">1 つのアクティビティ内で発生するエラーの処理を追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="82513-103">Represents a collection of queries that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="82513-104">このイベントは、FaultHandler がエラーを処理するたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="82513-104">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="82513-105">1 つのアクティビティ内で発生したエラーの処理は、このようなクエリを使用して追跡する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82513-105">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="82513-106">追跡参加要素がエラー伝達レコードを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="82513-106">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
 <span data-ttu-id="82513-107">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="82513-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="82513-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="82513-108">\<system.serviceModel></span></span>  
<span data-ttu-id="82513-109">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="82513-109">\<tracking></span></span>  
<span data-ttu-id="82513-110">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="82513-110">\<trackingProfile></span></span>  
<span data-ttu-id="82513-111">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="82513-111">\<workflow></span></span>  
<span data-ttu-id="82513-112">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="82513-112">\<faultPropagationQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="82513-113">構文</span><span class="sxs-lookup"><span data-stu-id="82513-113">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <faultPropagationQueries>
        <faultPropagationQuery activityName="String" 
                               faultHandlerActivityName="String" />
      </faultPropagationQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="82513-114">属性および要素</span><span class="sxs-lookup"><span data-stu-id="82513-114">Attributes and Elements</span></span>  
 <span data-ttu-id="82513-115">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="82513-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="82513-116">属性</span><span class="sxs-lookup"><span data-stu-id="82513-116">Attributes</span></span>  
 <span data-ttu-id="82513-117">なし。</span><span class="sxs-lookup"><span data-stu-id="82513-117">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="82513-118">子要素</span><span class="sxs-lookup"><span data-stu-id="82513-118">Child Elements</span></span>  
  
|<span data-ttu-id="82513-119">要素</span><span class="sxs-lookup"><span data-stu-id="82513-119">Element</span></span>|<span data-ttu-id="82513-120">説明</span><span class="sxs-lookup"><span data-stu-id="82513-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="82513-121">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="82513-121">\<faultPropagationQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationquery.md)|<span data-ttu-id="82513-122">1 つのアクティビティ内で発生するエラーの処理を追跡するために使用するクエリ。</span><span class="sxs-lookup"><span data-stu-id="82513-122">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="82513-123">このイベントは、FaultHandler がエラーを処理するたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="82513-123">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="82513-124">親要素</span><span class="sxs-lookup"><span data-stu-id="82513-124">Parent Elements</span></span>  
  
|<span data-ttu-id="82513-125">要素</span><span class="sxs-lookup"><span data-stu-id="82513-125">Element</span></span>|<span data-ttu-id="82513-126">説明</span><span class="sxs-lookup"><span data-stu-id="82513-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="82513-127">\<workflow></span><span class="sxs-lookup"><span data-stu-id="82513-127">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="82513-128">識別される特定のワークフローのすべてのクエリを格納する構成要素、 **activityDefinitionId**プロパティ。</span><span class="sxs-lookup"><span data-stu-id="82513-128">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="82513-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="82513-129">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="82513-130">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="82513-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="82513-131">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="82513-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
