---
title: <state> の <states>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: ab483c7f-a091-4933-ba6b-708d96846d38
ms.openlocfilehash: 657814eb120878cdc71cd7603d0499ff65ca50e8
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271435"
---
# <a name="state-of-states"></a><span data-ttu-id="f1433-102">\<状態 > の\<状態 ></span><span class="sxs-lookup"><span data-stu-id="f1433-102">\<state> of \<states></span></span>
<span data-ttu-id="f1433-103">追跡レコードを生成する必要がある定期受信済みアクティビティの状態を含む構成要素。</span><span class="sxs-lookup"><span data-stu-id="f1433-103">A configuration element that contains the state of the subscribed activity for which a tracking record should be emitted.</span></span>  
  
 <span data-ttu-id="f1433-104">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="f1433-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="f1433-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="f1433-105">\<system.serviceModel></span></span>  
<span data-ttu-id="f1433-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="f1433-106">\<tracking></span></span>  
<span data-ttu-id="f1433-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="f1433-107">\<trackingProfile></span></span>  
<span data-ttu-id="f1433-108">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="f1433-108">\<workflow></span></span>  
<span data-ttu-id="f1433-109">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="f1433-109">\<activityStateQueries></span></span>  
<span data-ttu-id="f1433-110">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="f1433-110">\<activityStateQuery></span></span>  
<span data-ttu-id="f1433-111">\<states></span><span class="sxs-lookup"><span data-stu-id="f1433-111">\<states></span></span>  
<span data-ttu-id="f1433-112">\<state></span><span class="sxs-lookup"><span data-stu-id="f1433-112">\<state></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f1433-113">構文</span><span class="sxs-lookup"><span data-stu-id="f1433-113">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <states>
          <state name="String" />
        </states>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f1433-114">属性および要素</span><span class="sxs-lookup"><span data-stu-id="f1433-114">Attributes and Elements</span></span>  
 <span data-ttu-id="f1433-115">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="f1433-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f1433-116">属性</span><span class="sxs-lookup"><span data-stu-id="f1433-116">Attributes</span></span>  
  
|<span data-ttu-id="f1433-117">属性</span><span class="sxs-lookup"><span data-stu-id="f1433-117">Attribute</span></span>|<span data-ttu-id="f1433-118">説明</span><span class="sxs-lookup"><span data-stu-id="f1433-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f1433-119">name</span><span class="sxs-lookup"><span data-stu-id="f1433-119">name</span></span>|<span data-ttu-id="f1433-120">追跡レコードを生成する必要がある定期受信済みアクティビティの状態を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="f1433-120">A string that specifies the state of the subscribed activity for which a tracking record should be emitted.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f1433-121">子要素</span><span class="sxs-lookup"><span data-stu-id="f1433-121">Child Elements</span></span>  
 <span data-ttu-id="f1433-122">なし。</span><span class="sxs-lookup"><span data-stu-id="f1433-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f1433-123">親要素</span><span class="sxs-lookup"><span data-stu-id="f1433-123">Parent Elements</span></span>  
  
|<span data-ttu-id="f1433-124">要素</span><span class="sxs-lookup"><span data-stu-id="f1433-124">Element</span></span>|<span data-ttu-id="f1433-125">説明</span><span class="sxs-lookup"><span data-stu-id="f1433-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f1433-126">\<states></span><span class="sxs-lookup"><span data-stu-id="f1433-126">\<states></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states-of-activitystatequery.md)|<span data-ttu-id="f1433-127">追跡レコードを生成する必要がある定期受信済みアクティビティの状態を含む構成要素のコレクション。</span><span class="sxs-lookup"><span data-stu-id="f1433-127">A collection of configuration elements that contain the states of the subscribed activity for which a tracking record should be emitted.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f1433-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="f1433-128">Remarks</span></span>  
 <span data-ttu-id="f1433-129">ActivityStateQuery の固有の機能の 1 つは、ワークフローの実行を追跡するときにデータを抽出する機能です。</span><span class="sxs-lookup"><span data-stu-id="f1433-129">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="f1433-130">これにより、実行後に追跡レコードにアクセスするときにコンテキストが追加されます。</span><span class="sxs-lookup"><span data-stu-id="f1433-130">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="f1433-131">使用することができます、 [\<引数 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md)、 [\<状態 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)と[\<状態 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)任意の変数または引数を抽出する要素ワークフロー内の任意のアクティビティから</span><span class="sxs-lookup"><span data-stu-id="f1433-131">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="f1433-132">次の例は、アクティビティの `Closed` 追跡レコードが生成されたときに変数と引数を抽出するアクティビティ状態クエリを示しています。</span><span class="sxs-lookup"><span data-stu-id="f1433-132">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="f1433-133">ActivityStateRecord でのみ抽出できるし、追跡のため購読中の変数と引数を使用してプロファイル[ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)します。</span><span class="sxs-lookup"><span data-stu-id="f1433-133">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
```xml  
<activityStateQuery activityName="SendEmailActivity">  
  <states>  
    <state name="Closed"/>  
  </states>  
  <variables>  
    <variable name="FromAddress"/>  
  </variables>  
  <arguments>  
    <argument name="Result"/>  
  </arguments>  
</activityStateQuery>  
```  
  
## <a name="see-also"></a><span data-ttu-id="f1433-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1433-134">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="f1433-135">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="f1433-135">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="f1433-136">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="f1433-136">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
