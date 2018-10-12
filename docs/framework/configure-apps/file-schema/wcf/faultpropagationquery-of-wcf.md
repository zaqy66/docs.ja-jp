---
title: WCF の &lt;faultPropagationQuery&gt;
ms.date: 03/30/2017
ms.assetid: fabafbc8-3e45-4feb-8321-0725e9f4079c
ms.openlocfilehash: c3853c470a9243835e071d35008dfff5b885591d
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2018
ms.locfileid: "49123320"
---
# <a name="ltfaultpropagationquerygt-of-wcf"></a><span data-ttu-id="266ab-102">WCF の &lt;faultPropagationQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="266ab-102">&lt;faultPropagationQuery&gt; of WCF</span></span>

<span data-ttu-id="266ab-103">1 つのアクティビティ内で発生するエラーの処理を追跡するために使用するクエリを表します。</span><span class="sxs-lookup"><span data-stu-id="266ab-103">Represents a query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="266ab-104">このイベントは、FaultHandler がエラーを処理するたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="266ab-104">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="266ab-105">1 つのアクティビティ内で発生したエラーの処理は、このようなクエリを使用して追跡する必要があります。</span><span class="sxs-lookup"><span data-stu-id="266ab-105">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="266ab-106">追跡参加要素がエラー伝達レコードを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="266ab-106">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
<span data-ttu-id="266ab-107">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="266ab-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="266ab-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="266ab-108">\<system.serviceModel></span></span>  
<span data-ttu-id="266ab-109">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="266ab-109">\<tracking></span></span>  
<span data-ttu-id="266ab-110">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="266ab-110">\<profiles></span></span>  
<span data-ttu-id="266ab-111">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="266ab-111">\<trackingProfile></span></span>  
<span data-ttu-id="266ab-112">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="266ab-112">\<workflow></span></span>  
<span data-ttu-id="266ab-113">\<faultPropagationQueries ></span><span class="sxs-lookup"><span data-stu-id="266ab-113">\<faultPropagationQueries></span></span>  
<span data-ttu-id="266ab-114">\<faultPropagationQuery ></span><span class="sxs-lookup"><span data-stu-id="266ab-114">\<faultPropagationQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="266ab-115">構文</span><span class="sxs-lookup"><span data-stu-id="266ab-115">Syntax</span></span>  
  
```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <faultPropagationQueries>
          <faultPropagationQuery faultSourceActivityName="String"
                                 faultHandlerActivityName="String"/>
        </faultPropagationQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```
  
## <a name="attributes-and-elements"></a><span data-ttu-id="266ab-116">属性と要素</span><span class="sxs-lookup"><span data-stu-id="266ab-116">Attributes and elements</span></span>

<span data-ttu-id="266ab-117">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="266ab-117">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="266ab-118">属性</span><span class="sxs-lookup"><span data-stu-id="266ab-118">Attributes</span></span>  
  
|<span data-ttu-id="266ab-119">属性</span><span class="sxs-lookup"><span data-stu-id="266ab-119">Attribute</span></span>|<span data-ttu-id="266ab-120">説明</span><span class="sxs-lookup"><span data-stu-id="266ab-120">Description</span></span>|  
|---------------|-----------------|  
|`faultSourceActivityName`|<span data-ttu-id="266ab-121">エラーを伝達したエラー ハンドラー アクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="266ab-121">A string that specifies the name of the fault hander activity that propagated the fault.</span></span> <span data-ttu-id="266ab-122">既定値は\*、すべてのアクティビティについてエラー伝達レコードが返されることを示します。</span><span class="sxs-lookup"><span data-stu-id="266ab-122">The default is \*, which indicates that fault propagation records are returned for all activities.</span></span>|  
|`faultHandlerActivityName`|<span data-ttu-id="266ab-123">エラーの原因となったアクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="266ab-123">A string that specifies the name of the activity that was the source of the fault.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="266ab-124">子要素</span><span class="sxs-lookup"><span data-stu-id="266ab-124">Child elements</span></span>

<span data-ttu-id="266ab-125">なし。</span><span class="sxs-lookup"><span data-stu-id="266ab-125">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="266ab-126">親要素</span><span class="sxs-lookup"><span data-stu-id="266ab-126">Parent elements</span></span>  
  
|<span data-ttu-id="266ab-127">要素</span><span class="sxs-lookup"><span data-stu-id="266ab-127">Element</span></span>|<span data-ttu-id="266ab-128">説明</span><span class="sxs-lookup"><span data-stu-id="266ab-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="266ab-129">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="266ab-129">\<faultPropagationQueries></span></span>](faultpropagationqueries-of-wcf.md)|<span data-ttu-id="266ab-130">1 つのアクティビティ内で発生するエラーの処理を追跡するために使用する、構成要素の一覧を表します。</span><span class="sxs-lookup"><span data-stu-id="266ab-130">Represents a list of configuration elements that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="266ab-131">このイベントは、FaultHandler がエラーを処理するたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="266ab-131">This event occurs each time a FaultHandler processes a fault.</span></span>|
  
## <a name="see-also"></a><span data-ttu-id="266ab-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="266ab-132">See also</span></span>  
 
- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="266ab-133">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="266ab-133">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="266ab-134">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="266ab-134">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
