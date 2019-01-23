---
title: WCF の &lt;workflow&gt;
ms.date: 03/30/2017
ms.assetid: c0443eba-d3b4-4fae-886e-9878daf77691
ms.openlocfilehash: 6c6efe9ee1ad582e25fc2bc578a15d6182eee2a9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54639956"
---
# <a name="ltworkflowgt-of-wcf"></a><span data-ttu-id="dcf34-102">WCF の &lt;workflow&gt;</span><span class="sxs-lookup"><span data-stu-id="dcf34-102">&lt;workflow&gt; of WCF</span></span>
<span data-ttu-id="dcf34-103">ランタイムから直接出力される追跡レコードをリッスンし、追跡レコードの構成方法に従って処理を行う追跡参加要素を構成します。</span><span class="sxs-lookup"><span data-stu-id="dcf34-103">Configure a tracking participant that listens to the tracking records being emitted from the runtime directly and process them in whatever way it was configured.</span></span> <span data-ttu-id="dcf34-104">これには、特定の出力 (ファイル、コンソール、ETW など) への書き込み、レコードの処理や集計、またはその他の必要な組み合わせが含まれます。</span><span class="sxs-lookup"><span data-stu-id="dcf34-104">This includes writing to a specific output (e.g., file, Console, ETW), processing/aggregating the records, or any other combination that might be required.</span></span>  
  
 <span data-ttu-id="dcf34-105">ワークフロー追跡と追跡参加要素の詳細については、次を参照してください。[ワークフロー追跡とトレース](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)と[追跡参加要素](../../../../../docs/framework/windows-workflow-foundation/tracking-participants.md)します。</span><span class="sxs-lookup"><span data-stu-id="dcf34-105">For more information in workflow tracking and tracking participants, see [Workflow Tracking and Tracing](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md) and [Tracking Participants](../../../../../docs/framework/windows-workflow-foundation/tracking-participants.md).</span></span>  
  
 <span data-ttu-id="dcf34-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="dcf34-106">\<system.serviceModel></span></span>  
<span data-ttu-id="dcf34-107">\<追跡 ></span><span class="sxs-lookup"><span data-stu-id="dcf34-107">\<tracking></span></span>  
<span data-ttu-id="dcf34-108">\<参加者 ></span><span class="sxs-lookup"><span data-stu-id="dcf34-108">\<participants></span></span>  
<span data-ttu-id="dcf34-109">\<add></span><span class="sxs-lookup"><span data-stu-id="dcf34-109">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dcf34-110">構文</span><span class="sxs-lookup"><span data-stu-id="dcf34-110">Syntax</span></span>  
  
```xml  
<tracking>
  <participants>
    <add name="String"
         profileName="String"
         type="String" />
  </participants>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dcf34-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="dcf34-111">Attributes and Elements</span></span>  
 <span data-ttu-id="dcf34-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="dcf34-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dcf34-113">属性</span><span class="sxs-lookup"><span data-stu-id="dcf34-113">Attributes</span></span>  
  
|<span data-ttu-id="dcf34-114">要素</span><span class="sxs-lookup"><span data-stu-id="dcf34-114">Element</span></span>|<span data-ttu-id="dcf34-115">説明</span><span class="sxs-lookup"><span data-stu-id="dcf34-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="dcf34-116">name</span><span class="sxs-lookup"><span data-stu-id="dcf34-116">name</span></span>|<span data-ttu-id="dcf34-117">追跡参加要素の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="dcf34-117">A string that specifies the name of a tracking participant.</span></span>|  
|<span data-ttu-id="dcf34-118">profileName</span><span class="sxs-lookup"><span data-stu-id="dcf34-118">profileName</span></span>|<span data-ttu-id="dcf34-119">追跡参加要素が定期受信した追跡レコードを定義する、追跡プロファイルの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="dcf34-119">A string that specifies the name of the tracking profile which defines the tracking records the tracking participant has subscribed to.</span></span>|  
|<span data-ttu-id="dcf34-120">型</span><span class="sxs-lookup"><span data-stu-id="dcf34-120">type</span></span>|<span data-ttu-id="dcf34-121">追跡参加要素の型を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="dcf34-121">A string that specifies the type of a tracking participant.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="dcf34-122">子要素</span><span class="sxs-lookup"><span data-stu-id="dcf34-122">Child Elements</span></span>  
 <span data-ttu-id="dcf34-123">なし。</span><span class="sxs-lookup"><span data-stu-id="dcf34-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="dcf34-124">親要素</span><span class="sxs-lookup"><span data-stu-id="dcf34-124">Parent Elements</span></span>  
  
|<span data-ttu-id="dcf34-125">要素</span><span class="sxs-lookup"><span data-stu-id="dcf34-125">Element</span></span>|<span data-ttu-id="dcf34-126">説明</span><span class="sxs-lookup"><span data-stu-id="dcf34-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="dcf34-127">\<participants></span><span class="sxs-lookup"><span data-stu-id="dcf34-127">\<participants></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/participants.md)|<span data-ttu-id="dcf34-128">追跡参加要素の一覧</span><span class="sxs-lookup"><span data-stu-id="dcf34-128">A list of tracking participants</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dcf34-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="dcf34-129">Remarks</span></span>  
 <span data-ttu-id="dcf34-130">追跡参加要素は、ワークフローから生成される追跡データを取得し、それを別のメディアに保存するために使用します。</span><span class="sxs-lookup"><span data-stu-id="dcf34-130">Tracking participants are used to get the tracking data emitted from the workflow and store it into different mediums.</span></span> <span data-ttu-id="dcf34-131">同様に、追跡レコードの後処理はすべて、追跡参加要素内でも実行できます。</span><span class="sxs-lookup"><span data-stu-id="dcf34-131">Likewise, any post processing on the tracking Records can also be done within the tracking participant.</span></span>  
  
 <span data-ttu-id="dcf34-132">複数の追跡参加要素が追跡イベントを同時に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="dcf34-132">Multiple tracking participants can consume the tracking events simultaneously.</span></span> <span data-ttu-id="dcf34-133">各追跡参加要素は、それぞれ別の追跡プロファイルと関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="dcf34-133">Each tracking participant can be associated with a different tracking profile.</span></span>  
  
 <span data-ttu-id="dcf34-134">追跡レコードを ETW セッションに書き込む、標準の追跡参加要素が用意されています。</span><span class="sxs-lookup"><span data-stu-id="dcf34-134">A standard tracking participant is provided which writes the tracking records to an ETW session.</span></span> <span data-ttu-id="dcf34-135">参加要素は、追跡固有の動作を構成ファイルに追加することによって、ワークフロー サービスで構成されます。</span><span class="sxs-lookup"><span data-stu-id="dcf34-135">The participant is configured on a workflow service by adding a tracking-specific behavior in a configuration file.</span></span> <span data-ttu-id="dcf34-136">ETW 追跡参加要素を有効にすると、追跡レコードをイベント ビューアーで表示できます。</span><span class="sxs-lookup"><span data-stu-id="dcf34-136">Enabling an ETW tracking participant allows tracking records to be viewed in the event viewer.</span></span> <span data-ttu-id="dcf34-137">これで要件が満たされない場合は、カスタムの追跡参加要素を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="dcf34-137">If that does not meet your requirements, you can also write a custom tracking participant.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dcf34-138">例</span><span class="sxs-lookup"><span data-stu-id="dcf34-138">Example</span></span>  
 <span data-ttu-id="dcf34-139">次の構成例は、Web.config ファイルで構成されている標準の ETW 追跡参加要素を示します。</span><span class="sxs-lookup"><span data-stu-id="dcf34-139">The following configuration example shows the standard ETW tracking participant being configured in the Web.config file.</span></span>  
  
 <span data-ttu-id="dcf34-140">ETW 追跡参加要素が追跡レコードを ETW に書き込むために使用するプロバイダー ID は、`<diagnostics>` セクションで定義されます。</span><span class="sxs-lookup"><span data-stu-id="dcf34-140">The Provider Id that the ETW Tracking Participant uses for writing the Tracking Records to ETW is defined in the `<diagnostics>` section.</span></span> <span data-ttu-id="dcf34-141">追跡参加要素には、その要素が定期受信した追跡レコードを指定するためのプロファイルが関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="dcf34-141">The tracking participant has a profile associated with it to specify the tracking records it has subscribed to.</span></span> <span data-ttu-id="dcf34-142">これは、`profileName` 要素の `<add>` 属性で定義されます。</span><span class="sxs-lookup"><span data-stu-id="dcf34-142">This is defined by the `profileName` attribute of the `<add>` element.</span></span> <span data-ttu-id="dcf34-143">これらが定義されると、追跡参加要素は `<etwTracking>` サービス動作に追加されます。</span><span class="sxs-lookup"><span data-stu-id="dcf34-143">Once these are defined, the Tracking Participant is added to the `<etwTracking>` service behavior.</span></span> <span data-ttu-id="dcf34-144">これにより、選択した追跡参加要素がワークフロー インスタンスの拡張機能に追加され、追跡レコードの受信が開始されます。</span><span class="sxs-lookup"><span data-stu-id="dcf34-144">This will add the selected Tracking Participants to the Workflow instance’s extensions, so that they begin to receive the Tracking Records.</span></span>  
  
```xml  
<configuration>
  <system.web>
    <compilation targetFrameworkMoniker=".NETFramework,Version=v4.0" />
  </system.web>
  <system.serviceModel>
    <diagnostics etwProviderId="52A3165D-4AD9-405C-B1E8-7D9A257EAC9F" />
    <tracking>
      <participants>
        <add name="EtwTrackingParticipant"
             type="System.Activities.Tracking.EtwTrackingParticipant, System.Activities, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"
             profileName="HealthMonitoring_Tracking_Profile" />
      </participants>
    </tracking>
    <behaviors>
      <serviceBehaviors>
        <behavior>
          <etwTracking profileName="Sample Tracking Profile" />
        </behavior>
      </serviceBehaviors>
    </behaviors>
  </system.serviceModel>
</configuration>
```  
  
## <a name="see-also"></a><span data-ttu-id="dcf34-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="dcf34-145">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.TrackingSection>
- <xref:System.ServiceModel.Activities.Description.EtwTrackingBehavior>
- <xref:System.ServiceModel.Activities.Configuration.EtwTrackingBehaviorElement>
- [<span data-ttu-id="dcf34-146">ワークフローの追跡とトレース</span><span class="sxs-lookup"><span data-stu-id="dcf34-146">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="dcf34-147">追跡参加要素</span><span class="sxs-lookup"><span data-stu-id="dcf34-147">Tracking Participants</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-participants.md)
