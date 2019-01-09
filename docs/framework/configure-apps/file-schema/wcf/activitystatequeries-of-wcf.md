---
title: WCF の &lt;activityStateQueries&gt;
ms.date: 10/08/2018
ms.assetid: 9e45db49-ed85-4fdf-bd65-0d5477e31823
ms.openlocfilehash: 2dabfdd248006de60b5e84e739f78e03f364dde3
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146187"
---
# <a name="ltactivitystatequeriesgt-of-wcf"></a><span data-ttu-id="d75f8-102">WCF の &lt;activityStateQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="d75f8-102">&lt;activityStateQueries&gt; of WCF</span></span>

<span data-ttu-id="d75f8-103">ワークフロー インスタンスを構成するアクティビティのライフサイクルの変化を追跡するために使用する、クエリのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="d75f8-103">Represents a collection of queries that are used to track life cycle changes of the activities that make up a workflow instance.</span></span> <span data-ttu-id="d75f8-104">たとえば、ワークフロー インスタンス内で、「電子メールの送信」アクティビティが完了するたびの追跡する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d75f8-104">For example, you may want to keep track of every time the "Send E-Mail" activity completes within a workflow instance.</span></span> <span data-ttu-id="d75f8-105">追跡参加要素がアクティビティ状態レコード オブジェクトを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="d75f8-105">This query is necessary for a tracking participant to subscribe to activity state record objects.</span></span> <span data-ttu-id="d75f8-106">定期受信可能な状態は ActivityStates で指定します。</span><span class="sxs-lookup"><span data-stu-id="d75f8-106">The available states to subscribe to are specified in ActivityStates.</span></span>

<span data-ttu-id="d75f8-107">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="d75f8-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>

<span data-ttu-id="d75f8-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="d75f8-108">\<system.serviceModel></span></span>  
<span data-ttu-id="d75f8-109">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="d75f8-109">\<tracking></span></span>  
<span data-ttu-id="d75f8-110">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="d75f8-110">\<profiles></span></span>  
<span data-ttu-id="d75f8-111">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="d75f8-111">\<trackingProfile></span></span>  
<span data-ttu-id="d75f8-112">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="d75f8-112">\<workflow></span></span>  
<span data-ttu-id="d75f8-113">\<activityStateQueries ></span><span class="sxs-lookup"><span data-stu-id="d75f8-113">\<activityStateQueries></span></span>  

## <a name="syntax"></a><span data-ttu-id="d75f8-114">構文</span><span class="sxs-lookup"><span data-stu-id="d75f8-114">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <activityStateQueries>
          <activityStateQuery activityName="String">
            <arguments>
              <argument name="String" />
            </arguments>
            <states>
              <state name="String" />
            </states>
            <variables>
              <variable name="String" />
            </variables>
          </activityStateQuery>
        </activityStateQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  

## <a name="attributes-and-elements"></a><span data-ttu-id="d75f8-115">属性と要素</span><span class="sxs-lookup"><span data-stu-id="d75f8-115">Attributes and elements</span></span>

<span data-ttu-id="d75f8-116">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="d75f8-116">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d75f8-117">属性</span><span class="sxs-lookup"><span data-stu-id="d75f8-117">Attributes</span></span>  

<span data-ttu-id="d75f8-118">なし。</span><span class="sxs-lookup"><span data-stu-id="d75f8-118">None.</span></span>  

### <a name="child-elements"></a><span data-ttu-id="d75f8-119">子要素</span><span class="sxs-lookup"><span data-stu-id="d75f8-119">Child elements</span></span>

|<span data-ttu-id="d75f8-120">要素</span><span class="sxs-lookup"><span data-stu-id="d75f8-120">Element</span></span>|<span data-ttu-id="d75f8-121">説明</span><span class="sxs-lookup"><span data-stu-id="d75f8-121">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="d75f8-122">\<activityStateQuery ></span><span class="sxs-lookup"><span data-stu-id="d75f8-122">\<activityStateQuery></span></span>](activitystatequery-of-wcf.md)|<span data-ttu-id="d75f8-123">1 つのアクティビティ内で発生するエラーの処理を追跡するために使用するクエリ。</span><span class="sxs-lookup"><span data-stu-id="d75f8-123">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="d75f8-124">このイベントは、FaultHandler がエラーを処理するたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="d75f8-124">This event occurs each time a FaultHandler processes a fault.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="d75f8-125">親要素</span><span class="sxs-lookup"><span data-stu-id="d75f8-125">Parent elements</span></span>

|<span data-ttu-id="d75f8-126">要素</span><span class="sxs-lookup"><span data-stu-id="d75f8-126">Element</span></span>|<span data-ttu-id="d75f8-127">説明</span><span class="sxs-lookup"><span data-stu-id="d75f8-127">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="d75f8-128">\<workflow></span><span class="sxs-lookup"><span data-stu-id="d75f8-128">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="d75f8-129">`activityDefinitionId` プロパティによって識別される特定のワークフローのすべてのクエリを格納する構成要素。</span><span class="sxs-lookup"><span data-stu-id="d75f8-129">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|

## <a name="see-also"></a><span data-ttu-id="d75f8-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="d75f8-130">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityStateQueryElementCollection>    
- <xref:System.Activities.Tracking.ActivityStateQuery>    
- [<span data-ttu-id="d75f8-131">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="d75f8-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
- [<span data-ttu-id="d75f8-132">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="d75f8-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
