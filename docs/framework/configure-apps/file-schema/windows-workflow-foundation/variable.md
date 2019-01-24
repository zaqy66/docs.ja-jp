---
title: '&lt;variable&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 46cc8cbc-10ec-4625-8813-3f5cd6c6afde
ms.openlocfilehash: 185e7e7196f6679ec3d1fae8a2a256b934022ca9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54647882"
---
# <a name="ltvariablegt"></a><span data-ttu-id="55472-102">&lt;variable&gt;</span><span class="sxs-lookup"><span data-stu-id="55472-102">&lt;variable&gt;</span></span>
<span data-ttu-id="55472-103">このアクティビティ クエリに関連付けられている変数のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="55472-103">Represents a collection of variables associated with this activity query.</span></span>  
  
 <span data-ttu-id="55472-104">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="55472-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="55472-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="55472-105">\<system.serviceModel></span></span>  
<span data-ttu-id="55472-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="55472-106">\<tracking></span></span>  
<span data-ttu-id="55472-107">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="55472-107">\<profiles></span></span>  
<span data-ttu-id="55472-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="55472-108">\<trackingProfile></span></span>  
<span data-ttu-id="55472-109">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="55472-109">\<workflow></span></span>  
<span data-ttu-id="55472-110">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="55472-110">\<activityStateQueries></span></span>  
<span data-ttu-id="55472-111">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="55472-111">\<activityStateQuery></span></span>  
<span data-ttu-id="55472-112">\<variables></span><span class="sxs-lookup"><span data-stu-id="55472-112">\<variables></span></span>  
<span data-ttu-id="55472-113">\<変数 ></span><span class="sxs-lookup"><span data-stu-id="55472-113">\<variable></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="55472-114">構文</span><span class="sxs-lookup"><span data-stu-id="55472-114">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="55472-115">属性および要素</span><span class="sxs-lookup"><span data-stu-id="55472-115">Attributes and Elements</span></span>  
 <span data-ttu-id="55472-116">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="55472-116">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="55472-117">属性</span><span class="sxs-lookup"><span data-stu-id="55472-117">Attributes</span></span>  
  
|<span data-ttu-id="55472-118">属性</span><span class="sxs-lookup"><span data-stu-id="55472-118">Attribute</span></span>|<span data-ttu-id="55472-119">説明</span><span class="sxs-lookup"><span data-stu-id="55472-119">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="55472-120">name</span><span class="sxs-lookup"><span data-stu-id="55472-120">name</span></span>|<span data-ttu-id="55472-121">変数の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="55472-121">A string that specifies the name of the variable.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="55472-122">子要素</span><span class="sxs-lookup"><span data-stu-id="55472-122">Child Elements</span></span>  
 <span data-ttu-id="55472-123">なし。</span><span class="sxs-lookup"><span data-stu-id="55472-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="55472-124">親要素</span><span class="sxs-lookup"><span data-stu-id="55472-124">Parent Elements</span></span>  
  
|<span data-ttu-id="55472-125">要素</span><span class="sxs-lookup"><span data-stu-id="55472-125">Element</span></span>|<span data-ttu-id="55472-126">説明</span><span class="sxs-lookup"><span data-stu-id="55472-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="55472-127">\<variable></span><span class="sxs-lookup"><span data-stu-id="55472-127">\<variable></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/variable.md)|<span data-ttu-id="55472-128">アクティビティ状態クエリに関連付けられている変数。</span><span class="sxs-lookup"><span data-stu-id="55472-128">A variable associated with an activity state query.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="55472-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="55472-129">Remarks</span></span>  
 <span data-ttu-id="55472-130">ActivityStateQuery の固有の機能の 1 つは、ワークフローの実行を追跡するときにデータを抽出する機能です。</span><span class="sxs-lookup"><span data-stu-id="55472-130">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="55472-131">これにより、実行後に追跡レコードにアクセスするときにコンテキストが追加されます。</span><span class="sxs-lookup"><span data-stu-id="55472-131">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="55472-132">使用することができます、 [\<引数 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md)、 [\<状態 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)と[\<状態 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)任意の変数または引数を抽出する要素ワークフロー内の任意のアクティビティから</span><span class="sxs-lookup"><span data-stu-id="55472-132">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="55472-133">次の例は、アクティビティの `Closed` 追跡レコードが生成されたときに変数と引数を抽出するアクティビティ状態クエリを示しています。</span><span class="sxs-lookup"><span data-stu-id="55472-133">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="55472-134">ActivityStateRecord でのみ抽出できるし、追跡のため購読中の変数と引数を使用してプロファイル[ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)します。</span><span class="sxs-lookup"><span data-stu-id="55472-134">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="55472-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="55472-135">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.VariableElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="55472-136">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="55472-136">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="55472-137">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="55472-137">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
