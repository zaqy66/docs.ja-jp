---
title: WCF の &lt;activityStateQueries&gt;
ms.date: 10/08/2018
ms.assetid: 9e45db49-ed85-4fdf-bd65-0d5477e31823
ms.openlocfilehash: 081dc297912ed5735dd51111936b85b61f463d2d
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2018
ms.locfileid: "49123242"
---
# <a name="ltactivitystatequeriesgt-of-wcf"></a><span data-ttu-id="41969-102">WCF の &lt;activityStateQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="41969-102">&lt;activityStateQueries&gt; of WCF</span></span>

<span data-ttu-id="41969-103">ワークフロー インスタンスを構成するアクティビティのライフサイクルの変化を追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="41969-103">Represents a collection of queries that are used to track life cycle changes of the activities that make up a workflow instance.</span></span> <span data-ttu-id="41969-104">たとえば、ワークフロー インスタンス内で、「電子メールの送信」アクティビティが完了するたびの追跡する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="41969-104">For example, you may want to keep track of every time the "Send E-Mail" activity completes within a workflow instance.</span></span> <span data-ttu-id="41969-105">追跡参加要素がアクティビティ状態レコード オブジェクトを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="41969-105">This query is necessary for a tracking participant to subscribe to activity state record objects.</span></span> <span data-ttu-id="41969-106">定期受信可能な状態は ActivityStates で指定します。</span><span class="sxs-lookup"><span data-stu-id="41969-106">The available states to subscribe to are specified in ActivityStates.</span></span>

<span data-ttu-id="41969-107">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="41969-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>

<span data-ttu-id="41969-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="41969-108">\<system.serviceModel></span></span>  
<span data-ttu-id="41969-109">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="41969-109">\<tracking></span></span>  
<span data-ttu-id="41969-110">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="41969-110">\<profiles></span></span>  
<span data-ttu-id="41969-111">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="41969-111">\<trackingProfile></span></span>  
<span data-ttu-id="41969-112">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="41969-112">\<workflow></span></span>  
<span data-ttu-id="41969-113">\<activityStateQueries ></span><span class="sxs-lookup"><span data-stu-id="41969-113">\<activityStateQueries></span></span>  

## <a name="syntax"></a><span data-ttu-id="41969-114">構文</span><span class="sxs-lookup"><span data-stu-id="41969-114">Syntax</span></span>  
  
```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <activityStateQueries>
          <activityStateQuery activityName="String">
            <arguments>
              <argument name="String"/>
            </arguments>
            <states>
              <state name="String"/>
            </states>
            <variables>
              <variable name="String"/>
            </variables>
          </activityStateQuery>
        </activityStateQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  

## <a name="attributes-and-elements"></a><span data-ttu-id="41969-115">属性と要素</span><span class="sxs-lookup"><span data-stu-id="41969-115">Attributes and elements</span></span>

<span data-ttu-id="41969-116">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="41969-116">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41969-117">属性</span><span class="sxs-lookup"><span data-stu-id="41969-117">Attributes</span></span>  

<span data-ttu-id="41969-118">なし。</span><span class="sxs-lookup"><span data-stu-id="41969-118">None.</span></span>  

### <a name="child-elements"></a><span data-ttu-id="41969-119">子要素</span><span class="sxs-lookup"><span data-stu-id="41969-119">Child elements</span></span>

|<span data-ttu-id="41969-120">要素</span><span class="sxs-lookup"><span data-stu-id="41969-120">Element</span></span>|<span data-ttu-id="41969-121">説明</span><span class="sxs-lookup"><span data-stu-id="41969-121">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="41969-122">\<activityStateQuery ></span><span class="sxs-lookup"><span data-stu-id="41969-122">\<activityStateQuery></span></span>](activitystatequery-of-wcf.md)|<span data-ttu-id="41969-123">1 つのアクティビティ内で発生するエラーの処理を追跡するために使用するクエリ。</span><span class="sxs-lookup"><span data-stu-id="41969-123">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="41969-124">このイベントは、FaultHandler がエラーを処理するたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="41969-124">This event occurs each time a FaultHandler processes a fault.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="41969-125">親要素</span><span class="sxs-lookup"><span data-stu-id="41969-125">Parent elements</span></span>

|<span data-ttu-id="41969-126">要素</span><span class="sxs-lookup"><span data-stu-id="41969-126">Element</span></span>|<span data-ttu-id="41969-127">説明</span><span class="sxs-lookup"><span data-stu-id="41969-127">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="41969-128">\<workflow></span><span class="sxs-lookup"><span data-stu-id="41969-128">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="41969-129">`activityDefinitionId` プロパティによって識別される特定のワークフローのすべてのクエリを格納する構成要素。</span><span class="sxs-lookup"><span data-stu-id="41969-129">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|

## <a name="see-also"></a><span data-ttu-id="41969-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="41969-130">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityStateQueryElementCollection>    
- <xref:System.Activities.Tracking.ActivityStateQuery>    
- [<span data-ttu-id="41969-131">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="41969-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
- [<span data-ttu-id="41969-132">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="41969-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
