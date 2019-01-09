---
title: WCF の &lt;faultPropagationQuery&gt;
ms.date: 03/30/2017
ms.assetid: fabafbc8-3e45-4feb-8321-0725e9f4079c
ms.openlocfilehash: cf582fce4e899e62daa4f34f193a0232ec19a135
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149034"
---
# <a name="ltfaultpropagationquerygt-of-wcf"></a><span data-ttu-id="6c62c-102">WCF の &lt;faultPropagationQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="6c62c-102">&lt;faultPropagationQuery&gt; of WCF</span></span>

<span data-ttu-id="6c62c-103">1 つのアクティビティ内で発生するエラーの処理を追跡するために使用するクエリを表します。</span><span class="sxs-lookup"><span data-stu-id="6c62c-103">Represents a query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="6c62c-104">このイベントは、FaultHandler がエラーを処理するたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="6c62c-104">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="6c62c-105">1 つのアクティビティ内で発生したエラーの処理は、このようなクエリを使用して追跡する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c62c-105">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="6c62c-106">追跡参加要素がエラー伝達レコードを定期受信するには、このクエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="6c62c-106">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
<span data-ttu-id="6c62c-107">追跡プロファイルのクエリの詳細については、次を参照してください。[追跡プロファイル](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)します。</span><span class="sxs-lookup"><span data-stu-id="6c62c-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="6c62c-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="6c62c-108">\<system.serviceModel></span></span>  
<span data-ttu-id="6c62c-109">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="6c62c-109">\<tracking></span></span>  
<span data-ttu-id="6c62c-110">\<プロファイル ></span><span class="sxs-lookup"><span data-stu-id="6c62c-110">\<profiles></span></span>  
<span data-ttu-id="6c62c-111">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="6c62c-111">\<trackingProfile></span></span>  
<span data-ttu-id="6c62c-112">\<ワークフロー ></span><span class="sxs-lookup"><span data-stu-id="6c62c-112">\<workflow></span></span>  
<span data-ttu-id="6c62c-113">\<faultPropagationQueries ></span><span class="sxs-lookup"><span data-stu-id="6c62c-113">\<faultPropagationQueries></span></span>  
<span data-ttu-id="6c62c-114">\<faultPropagationQuery ></span><span class="sxs-lookup"><span data-stu-id="6c62c-114">\<faultPropagationQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c62c-115">構文</span><span class="sxs-lookup"><span data-stu-id="6c62c-115">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <faultPropagationQueries>
          <faultPropagationQuery faultSourceActivityName="String"
                                 faultHandlerActivityName="String" />
        </faultPropagationQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6c62c-116">属性と要素</span><span class="sxs-lookup"><span data-stu-id="6c62c-116">Attributes and elements</span></span>

<span data-ttu-id="6c62c-117">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="6c62c-117">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="6c62c-118">属性</span><span class="sxs-lookup"><span data-stu-id="6c62c-118">Attributes</span></span>  
  
|<span data-ttu-id="6c62c-119">属性</span><span class="sxs-lookup"><span data-stu-id="6c62c-119">Attribute</span></span>|<span data-ttu-id="6c62c-120">説明</span><span class="sxs-lookup"><span data-stu-id="6c62c-120">Description</span></span>|  
|---------------|-----------------|  
|`faultSourceActivityName`|<span data-ttu-id="6c62c-121">エラーを伝達したエラー ハンドラー アクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="6c62c-121">A string that specifies the name of the fault hander activity that propagated the fault.</span></span> <span data-ttu-id="6c62c-122">既定値は\*、すべてのアクティビティについてエラー伝達レコードが返されることを示します。</span><span class="sxs-lookup"><span data-stu-id="6c62c-122">The default is \*, which indicates that fault propagation records are returned for all activities.</span></span>|  
|`faultHandlerActivityName`|<span data-ttu-id="6c62c-123">エラーの原因となったアクティビティの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="6c62c-123">A string that specifies the name of the activity that was the source of the fault.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6c62c-124">子要素</span><span class="sxs-lookup"><span data-stu-id="6c62c-124">Child elements</span></span>

<span data-ttu-id="6c62c-125">なし。</span><span class="sxs-lookup"><span data-stu-id="6c62c-125">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6c62c-126">親要素</span><span class="sxs-lookup"><span data-stu-id="6c62c-126">Parent elements</span></span>  
  
|<span data-ttu-id="6c62c-127">要素</span><span class="sxs-lookup"><span data-stu-id="6c62c-127">Element</span></span>|<span data-ttu-id="6c62c-128">説明</span><span class="sxs-lookup"><span data-stu-id="6c62c-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6c62c-129">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="6c62c-129">\<faultPropagationQueries></span></span>](faultpropagationqueries-of-wcf.md)|<span data-ttu-id="6c62c-130">1 つのアクティビティ内で発生するエラーの処理を追跡するために使用する、構成要素の一覧を表します。</span><span class="sxs-lookup"><span data-stu-id="6c62c-130">Represents a list of configuration elements that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="6c62c-131">このイベントは、FaultHandler がエラーを処理するたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="6c62c-131">This event occurs each time a FaultHandler processes a fault.</span></span>|
  
## <a name="see-also"></a><span data-ttu-id="6c62c-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="6c62c-132">See also</span></span>  
 
- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="6c62c-133">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="6c62c-133">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="6c62c-134">追跡プロファイル</span><span class="sxs-lookup"><span data-stu-id="6c62c-134">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
