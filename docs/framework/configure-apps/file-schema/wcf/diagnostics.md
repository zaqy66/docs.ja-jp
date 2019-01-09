---
title: '&lt;診断&gt;'
ms.date: 03/30/2017
ms.assetid: 0c2f95c4-cc12-4fb5-a70c-7fc6fa95db58
ms.openlocfilehash: 3ee611d3903ba36748837d2743cd03d54670befd
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149346"
---
# <a name="ltdiagnosticsgt"></a><span data-ttu-id="cbac0-102">&lt;診断&gt;</span><span class="sxs-lookup"><span data-stu-id="cbac0-102">&lt;diagnostics&gt;</span></span>
<span data-ttu-id="cbac0-103">`diagnostics` 要素は、ランタイムの検査と管理を行う管理者が使用できる設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="cbac0-103">The `diagnostics` element defines settings that can be used by an administrator for run-time inspection and control.</span></span>  
  
 <span data-ttu-id="cbac0-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="cbac0-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="cbac0-105">\<診断 ></span><span class="sxs-lookup"><span data-stu-id="cbac0-105">\<diagnostics></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cbac0-106">構文</span><span class="sxs-lookup"><span data-stu-id="cbac0-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <diagnostics etwProviderId="String"
               performanceCounters="Off/ServiceOnly/All/Default"
               wmiProviderEnabled="Boolean">
    <endToEndTracing activityTracing="Boolean"
                     messageFlowTracing="Boolean"
                     propagateActivity="Boolean" />
    <messageLogging logEntireMessage="Boolean"
                    logMalformedMessages="Boolean"
                    logMessagesAtServiceLevel="Boolean"
                    logMessagesAtTransportLevel="Boolean"
                    maxMessagesToLog="Integer"
                    maxSizeOfMessageToLog="Integer">
      <filters>
        <clear />
      </filters>
    </messageLogging>
  </diagnostics>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cbac0-107">属性および要素</span><span class="sxs-lookup"><span data-stu-id="cbac0-107">Attributes and Elements</span></span>  
 <span data-ttu-id="cbac0-108">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="cbac0-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cbac0-109">属性</span><span class="sxs-lookup"><span data-stu-id="cbac0-109">Attributes</span></span>  
  
|<span data-ttu-id="cbac0-110">属性</span><span class="sxs-lookup"><span data-stu-id="cbac0-110">Attribute</span></span>|<span data-ttu-id="cbac0-111">説明</span><span class="sxs-lookup"><span data-stu-id="cbac0-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="cbac0-112">etwProviderId</span><span class="sxs-lookup"><span data-stu-id="cbac0-112">etwProviderId</span></span>|<span data-ttu-id="cbac0-113">イベントを ETW セッションに書き込むイベント追跡プロバイダーの識別子を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="cbac0-113">A string that specifies the identifier for the Event-Tracing provider, which writes events to ETW sessions.</span></span>|  
|<span data-ttu-id="cbac0-114">performanceCounters</span><span class="sxs-lookup"><span data-stu-id="cbac0-114">performanceCounters</span></span>|<span data-ttu-id="cbac0-115">アセンブリのパフォーマンス カウンターが有効であるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="cbac0-115">Specifies whether performance counters for the assembly are enabled.</span></span> <span data-ttu-id="cbac0-116">有効な値は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cbac0-116">Valid values are</span></span><br /><br /> <span data-ttu-id="cbac0-117">オフ。パフォーマンス カウンターは無効です。</span><span class="sxs-lookup"><span data-stu-id="cbac0-117">-   Off: Performance counters are disabled.</span></span><br /><span data-ttu-id="cbac0-118">-ServiceOnly:このサービスに関連するパフォーマンス カウンターだけが有効です。</span><span class="sxs-lookup"><span data-stu-id="cbac0-118">-   ServiceOnly: Only performance counters relevant to this service is enabled.</span></span><br /><span data-ttu-id="cbac0-119">-All:パフォーマンス カウンターは実行時に表示できます。</span><span class="sxs-lookup"><span data-stu-id="cbac0-119">-   All: Performance counters can be viewed at runtime.</span></span><br /><span data-ttu-id="cbac0-120">-既定値:単一のパフォーマンス カウンター インスタンス _WCF_Admin が作成されます。</span><span class="sxs-lookup"><span data-stu-id="cbac0-120">-   Default: A single performance counter instance _WCF_Admin is created.</span></span> <span data-ttu-id="cbac0-121">このインスタンスは、インフラストラクチャで使用される SQM データのコレクションを有効にするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cbac0-121">This instance is used to enable the collection of SQM data for used by the infrastructure.</span></span> <span data-ttu-id="cbac0-122">このインスタンスのカウンター値は更新されず、0 のままになります。</span><span class="sxs-lookup"><span data-stu-id="cbac0-122">None of the counter values for this instance are updated and therefore will remain at zero.</span></span> <span data-ttu-id="cbac0-123">WCF の構成が存在しない場合は、これが既定値になります。</span><span class="sxs-lookup"><span data-stu-id="cbac0-123">This is the default value if no configuration is present for WCF.</span></span>|  
|<span data-ttu-id="cbac0-124">wmiProviderEnabled</span><span class="sxs-lookup"><span data-stu-id="cbac0-124">wmiProviderEnabled</span></span>|<span data-ttu-id="cbac0-125">アセンブリの WMI プロバイダーが有効であるかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="cbac0-125">A Boolean value that specifies whether the WMI provider for the assembly is enabled.</span></span> <span data-ttu-id="cbac0-126">ユーザーが Windows Communication Foundation (WCF) の検査および制御機能に対する実行時アクセス権を取得するには、WMI プロバイダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="cbac0-126">The WMI provider is required for user to gain run-time access to the inspection and control features of Windows Communication Foundation (WCF).</span></span> <span data-ttu-id="cbac0-127">既定値は `false` です。</span><span class="sxs-lookup"><span data-stu-id="cbac0-127">The default is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cbac0-128">子要素</span><span class="sxs-lookup"><span data-stu-id="cbac0-128">Child Elements</span></span>  
  
|<span data-ttu-id="cbac0-129">要素</span><span class="sxs-lookup"><span data-stu-id="cbac0-129">Element</span></span>|<span data-ttu-id="cbac0-130">説明</span><span class="sxs-lookup"><span data-stu-id="cbac0-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cbac0-131">\<endToEndTracing ></span><span class="sxs-lookup"><span data-stu-id="cbac0-131">\<endToEndTracing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/endtoendtracing.md)|<span data-ttu-id="cbac0-132">サービス アプリケーションの実行中にエンドツーエンドのトレースのさまざまな側面を有効または無効にするための構成要素。</span><span class="sxs-lookup"><span data-stu-id="cbac0-132">A configuration element that allows you to enable and disable different aspects of end-to-end tracing during the running of a service application.</span></span>|  
|[<span data-ttu-id="cbac0-133">\<messageLogging ></span><span class="sxs-lookup"><span data-stu-id="cbac0-133">\<messageLogging></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/messagelogging.md)|<span data-ttu-id="cbac0-134">WCF メッセージ ログの設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="cbac0-134">Describes the settings for WCF message logging.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="cbac0-135">親要素</span><span class="sxs-lookup"><span data-stu-id="cbac0-135">Parent Elements</span></span>  
  
|<span data-ttu-id="cbac0-136">要素</span><span class="sxs-lookup"><span data-stu-id="cbac0-136">Element</span></span>|<span data-ttu-id="cbac0-137">説明</span><span class="sxs-lookup"><span data-stu-id="cbac0-137">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="cbac0-138">serviceModel</span><span class="sxs-lookup"><span data-stu-id="cbac0-138">serviceModel</span></span>|<span data-ttu-id="cbac0-139">すべての WCF 構成要素のルート要素です。</span><span class="sxs-lookup"><span data-stu-id="cbac0-139">The root element of all WCF configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cbac0-140">Remarks</span><span class="sxs-lookup"><span data-stu-id="cbac0-140">Remarks</span></span>  
 <span data-ttu-id="cbac0-141">`diagnostics` セクションは、アセンブリに配置されるすべてのサービスの診断設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="cbac0-141">The `diagnostics` section defines the diagnostics settings for all services located in an assembly.</span></span> <span data-ttu-id="cbac0-142">アセンブリ内のサービスが 1 つでない限り、サービス レベル別に診断設定を定義することはできません。</span><span class="sxs-lookup"><span data-stu-id="cbac0-142">It is not possible to define separate diagnostics settings at the service level unless there is only one service in the assembly.</span></span> <span data-ttu-id="cbac0-143">属性は、セクションの要件に応じて設定されます。</span><span class="sxs-lookup"><span data-stu-id="cbac0-143">Attributes are set according to the requirements of the section.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cbac0-144">例</span><span class="sxs-lookup"><span data-stu-id="cbac0-144">Example</span></span>  
  
```xml  
<diagnostics wmiProviderEnabled="false"
             performanceCounters="all">
  <messageLogging logEntireMessage="true"
                  logMalformedMessages="true"
                  logMessagesAtServiceLevel="true"
                  logMessagesAtTransportLevel="true"
                  maxMessagesToLog="42"
                  maxSizeOfMessageToLog="42">
    <filters>
      <clear />
    </filters>
  </messageLogging>
</diagnostics>
```  
  
## <a name="see-also"></a><span data-ttu-id="cbac0-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="cbac0-145">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.DiagnosticSection>  
 <xref:System.ServiceModel.Diagnostics>
