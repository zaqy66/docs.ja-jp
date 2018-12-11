---
title: '&lt;argument&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: a7144d53-8023-4e90-971f-895e016fd58a
ms.openlocfilehash: 8172093f36bd09ea33b1a447ee61dc36afb1b358
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53154230"
---
# <a name="ltargumentgt"></a><span data-ttu-id="bd797-102">&lt;argument&gt;</span><span class="sxs-lookup"><span data-stu-id="bd797-102">&lt;argument&gt;</span></span>
<span data-ttu-id="bd797-103">アクティビティ状態クエリに関連付けられている引数を表す構成要素。</span><span class="sxs-lookup"><span data-stu-id="bd797-103">A configuration element that represents an argument associated with an activity state query.</span></span>  
  
 <span data-ttu-id="bd797-104">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="bd797-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="bd797-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="bd797-105">\<system.serviceModel></span></span>  
<span data-ttu-id="bd797-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="bd797-106">\<tracking></span></span>  
<span data-ttu-id="bd797-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="bd797-107">\<trackingProfile></span></span>  
<span data-ttu-id="bd797-108">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="bd797-108">\<workflow></span></span>  
<span data-ttu-id="bd797-109">\<activityStateQueries ></span><span class="sxs-lookup"><span data-stu-id="bd797-109">\<activityStateQueries></span></span>  
<span data-ttu-id="bd797-110">\<activityStateQuery ></span><span class="sxs-lookup"><span data-stu-id="bd797-110">\<activityStateQuery></span></span>  
<span data-ttu-id="bd797-111">\<引数 ></span><span class="sxs-lookup"><span data-stu-id="bd797-111">\<arguments></span></span>  
<span data-ttu-id="bd797-112">\<引数 ></span><span class="sxs-lookup"><span data-stu-id="bd797-112">\<argument></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bd797-113">構文</span><span class="sxs-lookup"><span data-stu-id="bd797-113">Syntax</span></span>  
  
```xml
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <arguments>
          <argument name="String"/>
        </arguments>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bd797-114">属性および要素</span><span class="sxs-lookup"><span data-stu-id="bd797-114">Attributes and Elements</span></span>  
 <span data-ttu-id="bd797-115">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="bd797-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bd797-116">属性</span><span class="sxs-lookup"><span data-stu-id="bd797-116">Attributes</span></span>  
  
|<span data-ttu-id="bd797-117">属性</span><span class="sxs-lookup"><span data-stu-id="bd797-117">Attribute</span></span>|<span data-ttu-id="bd797-118">説明</span><span class="sxs-lookup"><span data-stu-id="bd797-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="bd797-119">name</span><span class="sxs-lookup"><span data-stu-id="bd797-119">name</span></span>|<span data-ttu-id="bd797-120">この引数の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="bd797-120">A string that specifies the name of the argument.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bd797-121">子要素</span><span class="sxs-lookup"><span data-stu-id="bd797-121">Child Elements</span></span>  
 <span data-ttu-id="bd797-122">なし。</span><span class="sxs-lookup"><span data-stu-id="bd797-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="bd797-123">親要素</span><span class="sxs-lookup"><span data-stu-id="bd797-123">Parent Elements</span></span>  
  
|<span data-ttu-id="bd797-124">要素</span><span class="sxs-lookup"><span data-stu-id="bd797-124">Element</span></span>|<span data-ttu-id="bd797-125">説明</span><span class="sxs-lookup"><span data-stu-id="bd797-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bd797-126">\<引数 ></span><span class="sxs-lookup"><span data-stu-id="bd797-126">\<arguments></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md)|<span data-ttu-id="bd797-127">このアクティビティ クエリに関連付けられている引数のコレクション。</span><span class="sxs-lookup"><span data-stu-id="bd797-127">A collection of arguments associated with this activity query.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bd797-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="bd797-128">Remarks</span></span>  
 <span data-ttu-id="bd797-129">ActivityStateQuery の固有の機能の 1 つは、ワークフローの実行を追跡するときにデータを抽出する機能です。</span><span class="sxs-lookup"><span data-stu-id="bd797-129">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="bd797-130">これにより、実行後に追跡レコードにアクセスするときにコンテキストが追加されます。</span><span class="sxs-lookup"><span data-stu-id="bd797-130">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="bd797-131">使用することができます、 [\<引数 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md)、 [\<状態 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)と[\<状態 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)任意の変数または引数を抽出する要素ワークフロー内の任意のアクティビティから</span><span class="sxs-lookup"><span data-stu-id="bd797-131">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="bd797-132">次の例は、アクティビティの `Closed` 追跡レコードが生成されたときに変数と引数を抽出するアクティビティ状態クエリを示しています。</span><span class="sxs-lookup"><span data-stu-id="bd797-132">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="bd797-133">ActivityStateRecord でのみ抽出できるし、追跡のため購読中の変数と引数を使用してプロファイル[ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)します。</span><span class="sxs-lookup"><span data-stu-id="bd797-133">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="bd797-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd797-134">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.ArgumentElement?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="bd797-135">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="bd797-135">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="bd797-136">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="bd797-136">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
