---
title: '&lt;variables&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: da0fd144-dda9-4613-b650-fe6325076513
ms.openlocfilehash: 4dc7ab2dd15beb9707807147917c344e989be7f1
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53154126"
---
# <a name="ltvariablesgt"></a><span data-ttu-id="218d6-102">&lt;variables&gt;</span><span class="sxs-lookup"><span data-stu-id="218d6-102">&lt;variables&gt;</span></span>
<span data-ttu-id="218d6-103">このアクティビティ クエリに関連付けられている変数のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="218d6-103">Represents a collection of variables associated with this activity query.</span></span>  
  
 <span data-ttu-id="218d6-104">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="218d6-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="218d6-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="218d6-105">\<system.serviceModel></span></span>  
<span data-ttu-id="218d6-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="218d6-106">\<tracking></span></span>  
<span data-ttu-id="218d6-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="218d6-107">\<trackingProfile></span></span>  
<span data-ttu-id="218d6-108">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="218d6-108">\<workflow></span></span>  
<span data-ttu-id="218d6-109">\<activityStateQueries ></span><span class="sxs-lookup"><span data-stu-id="218d6-109">\<activityStateQueries></span></span>  
<span data-ttu-id="218d6-110">\<activityStateQuery ></span><span class="sxs-lookup"><span data-stu-id="218d6-110">\<activityStateQuery></span></span>  
<span data-ttu-id="218d6-111">\<変数 ></span><span class="sxs-lookup"><span data-stu-id="218d6-111">\<variables></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="218d6-112">構文</span><span class="sxs-lookup"><span data-stu-id="218d6-112">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <variables>
          <variable name="String" />
        </variables>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="218d6-113">属性および要素</span><span class="sxs-lookup"><span data-stu-id="218d6-113">Attributes and Elements</span></span>  
 <span data-ttu-id="218d6-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="218d6-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="218d6-115">属性</span><span class="sxs-lookup"><span data-stu-id="218d6-115">Attributes</span></span>  
 <span data-ttu-id="218d6-116">なし。</span><span class="sxs-lookup"><span data-stu-id="218d6-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="218d6-117">子要素</span><span class="sxs-lookup"><span data-stu-id="218d6-117">Child Elements</span></span>  
  
|<span data-ttu-id="218d6-118">要素</span><span class="sxs-lookup"><span data-stu-id="218d6-118">Element</span></span>|<span data-ttu-id="218d6-119">説明</span><span class="sxs-lookup"><span data-stu-id="218d6-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="218d6-120">\<変数 ></span><span class="sxs-lookup"><span data-stu-id="218d6-120">\<variable></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/variable.md)|<span data-ttu-id="218d6-121">アクティビティ状態クエリに関連付けられている変数。</span><span class="sxs-lookup"><span data-stu-id="218d6-121">A variable associated with an activity state query.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="218d6-122">親要素</span><span class="sxs-lookup"><span data-stu-id="218d6-122">Parent Elements</span></span>  
  
|<span data-ttu-id="218d6-123">要素</span><span class="sxs-lookup"><span data-stu-id="218d6-123">Element</span></span>|<span data-ttu-id="218d6-124">説明</span><span class="sxs-lookup"><span data-stu-id="218d6-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="218d6-125">\<activityStateQuery ></span><span class="sxs-lookup"><span data-stu-id="218d6-125">\<activityStateQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)|<span data-ttu-id="218d6-126">親アクティビティが子アクティビティを取り消すための要求を追跡するのに使用する構成要素を表します。</span><span class="sxs-lookup"><span data-stu-id="218d6-126">Represents a configuration element that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="218d6-127">追跡参加要素がキャンセル要求レコード オブジェクトを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="218d6-127">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="218d6-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="218d6-128">Remarks</span></span>  
 <span data-ttu-id="218d6-129">ActivityStateQuery の固有の機能の 1 つは、ワークフローの実行を追跡するときにデータを抽出する機能です。</span><span class="sxs-lookup"><span data-stu-id="218d6-129">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="218d6-130">これにより、実行後に追跡レコードにアクセスするときにコンテキストが追加されます。</span><span class="sxs-lookup"><span data-stu-id="218d6-130">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="218d6-131">使用することができます、 [\<引数 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md)、 [\<状態 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)と[\<状態 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)任意の変数または引数を抽出する要素ワークフロー内の任意のアクティビティから</span><span class="sxs-lookup"><span data-stu-id="218d6-131">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="218d6-132">次の例は、アクティビティの `Closed` 追跡レコードが生成されたときに変数と引数を抽出するアクティビティ状態クエリを示しています。</span><span class="sxs-lookup"><span data-stu-id="218d6-132">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="218d6-133">ActivityStateRecord でのみ抽出できるし、追跡のため購読中の変数と引数を使用してプロファイル[ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)します。</span><span class="sxs-lookup"><span data-stu-id="218d6-133">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="218d6-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="218d6-134">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.VariableElementCollection?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="218d6-135">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="218d6-135">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="218d6-136">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="218d6-136">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
