---
title: '&lt;argument&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: a7144d53-8023-4e90-971f-895e016fd58a
ms.openlocfilehash: 3744781f844d4a1728ba1e9846b2b8c56c0ad8fd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54554605"
---
# <a name="ltargumentgt"></a><span data-ttu-id="2948e-102">&lt;argument&gt;</span><span class="sxs-lookup"><span data-stu-id="2948e-102">&lt;argument&gt;</span></span>
<span data-ttu-id="2948e-103">アクティビティ状態クエリに関連付けられている引数を表す構成要素。</span><span class="sxs-lookup"><span data-stu-id="2948e-103">A configuration element that represents an argument associated with an activity state query.</span></span>  
  
 <span data-ttu-id="2948e-104">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="2948e-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="2948e-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="2948e-105">\<system.serviceModel></span></span>  
<span data-ttu-id="2948e-106">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="2948e-106">\<tracking></span></span>  
<span data-ttu-id="2948e-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="2948e-107">\<trackingProfile></span></span>  
<span data-ttu-id="2948e-108">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="2948e-108">\<workflow></span></span>  
<span data-ttu-id="2948e-109">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="2948e-109">\<activityStateQueries></span></span>  
<span data-ttu-id="2948e-110">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="2948e-110">\<activityStateQuery></span></span>  
<span data-ttu-id="2948e-111">\<arguments></span><span class="sxs-lookup"><span data-stu-id="2948e-111">\<arguments></span></span>  
<span data-ttu-id="2948e-112">\<argument></span><span class="sxs-lookup"><span data-stu-id="2948e-112">\<argument></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2948e-113">構文</span><span class="sxs-lookup"><span data-stu-id="2948e-113">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2948e-114">属性および要素</span><span class="sxs-lookup"><span data-stu-id="2948e-114">Attributes and Elements</span></span>  
 <span data-ttu-id="2948e-115">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="2948e-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2948e-116">属性</span><span class="sxs-lookup"><span data-stu-id="2948e-116">Attributes</span></span>  
  
|<span data-ttu-id="2948e-117">属性</span><span class="sxs-lookup"><span data-stu-id="2948e-117">Attribute</span></span>|<span data-ttu-id="2948e-118">説明</span><span class="sxs-lookup"><span data-stu-id="2948e-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="2948e-119">name</span><span class="sxs-lookup"><span data-stu-id="2948e-119">name</span></span>|<span data-ttu-id="2948e-120">この引数の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="2948e-120">A string that specifies the name of the argument.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2948e-121">子要素</span><span class="sxs-lookup"><span data-stu-id="2948e-121">Child Elements</span></span>  
 <span data-ttu-id="2948e-122">なし。</span><span class="sxs-lookup"><span data-stu-id="2948e-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2948e-123">親要素</span><span class="sxs-lookup"><span data-stu-id="2948e-123">Parent Elements</span></span>  
  
|<span data-ttu-id="2948e-124">要素</span><span class="sxs-lookup"><span data-stu-id="2948e-124">Element</span></span>|<span data-ttu-id="2948e-125">説明</span><span class="sxs-lookup"><span data-stu-id="2948e-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2948e-126">\<arguments></span><span class="sxs-lookup"><span data-stu-id="2948e-126">\<arguments></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md)|<span data-ttu-id="2948e-127">このアクティビティ クエリに関連付けられている引数のコレクション。</span><span class="sxs-lookup"><span data-stu-id="2948e-127">A collection of arguments associated with this activity query.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2948e-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="2948e-128">Remarks</span></span>  
 <span data-ttu-id="2948e-129">ActivityStateQuery の固有の機能の 1 つは、ワークフローの実行を追跡するときにデータを抽出する機能です。</span><span class="sxs-lookup"><span data-stu-id="2948e-129">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="2948e-130">これにより、実行後に追跡レコードにアクセスするときにコンテキストが追加されます。</span><span class="sxs-lookup"><span data-stu-id="2948e-130">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="2948e-131">使用することができます、 [\<引数 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md)、 [\<状態 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)と[\<状態 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)任意の変数または引数を抽出する要素ワークフロー内の任意のアクティビティから</span><span class="sxs-lookup"><span data-stu-id="2948e-131">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="2948e-132">次の例は、アクティビティの `Closed` 追跡レコードが生成されたときに変数と引数を抽出するアクティビティ状態クエリを示しています。</span><span class="sxs-lookup"><span data-stu-id="2948e-132">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="2948e-133">ActivityStateRecord でのみ抽出できるし、追跡のため購読中の変数と引数を使用してプロファイル[ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)します。</span><span class="sxs-lookup"><span data-stu-id="2948e-133">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="2948e-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="2948e-134">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.ArgumentElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="2948e-135">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="2948e-135">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="2948e-136">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="2948e-136">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
