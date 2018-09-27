---
title: '&lt;リスナー&gt;要素&lt;ソース&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sources/source/listeners
helpviewer_keywords:
- listeners element for <source>
- <listeners> element for <source>
ms.assetid: a2991f43-b4d3-4614-a8e7-da392de9697f
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 86b85779f4eff72e8ab910a5ccd32fd369270509
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2018
ms.locfileid: "47399009"
---
# <a name="ltlistenersgt-element-for-ltsourcegt"></a><span data-ttu-id="6843a-102">&lt;リスナー&gt;要素&lt;ソース&gt;</span><span class="sxs-lookup"><span data-stu-id="6843a-102">&lt;listeners&gt; Element for &lt;source&gt;</span></span>
<span data-ttu-id="6843a-103">追加または内のリスナーを削除します、<xref:System.Diagnostics.TraceSource.Listeners%2A>のコレクションを<xref:System.Diagnostics.TraceSource>します。</span><span class="sxs-lookup"><span data-stu-id="6843a-103">Adds or removes listeners in the <xref:System.Diagnostics.TraceSource.Listeners%2A> collection for a <xref:System.Diagnostics.TraceSource>.</span></span> <span data-ttu-id="6843a-104">ログ、ウィンドウ、またはテキスト ファイルなど、適切なターゲットへのトレース出力をリスナーに指示します。</span><span class="sxs-lookup"><span data-stu-id="6843a-104">A listener directs the tracing output to an appropriate target, such as a log, window, or text file.</span></span>  
  
 <span data-ttu-id="6843a-105">\<configuration></span><span class="sxs-lookup"><span data-stu-id="6843a-105">\<configuration></span></span>  
<span data-ttu-id="6843a-106">\<system.diagnostics ></span><span class="sxs-lookup"><span data-stu-id="6843a-106">\<system.diagnostics></span></span>  
<span data-ttu-id="6843a-107">\<ソース ></span><span class="sxs-lookup"><span data-stu-id="6843a-107">\<sources></span></span>  
<span data-ttu-id="6843a-108">\<ソース ></span><span class="sxs-lookup"><span data-stu-id="6843a-108">\<source></span></span>  
<span data-ttu-id="6843a-109">\<リスナー > 要素</span><span class="sxs-lookup"><span data-stu-id="6843a-109">\<listeners> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6843a-110">構文</span><span class="sxs-lookup"><span data-stu-id="6843a-110">Syntax</span></span>  
  
```xml  
<listeners>   
  <add>...</add>  
  <remove ... />  
  <clear/>  
</listeners>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6843a-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="6843a-111">Attributes and Elements</span></span>  
 <span data-ttu-id="6843a-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="6843a-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6843a-113">属性</span><span class="sxs-lookup"><span data-stu-id="6843a-113">Attributes</span></span>  
 <span data-ttu-id="6843a-114">なし。</span><span class="sxs-lookup"><span data-stu-id="6843a-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="6843a-115">子要素</span><span class="sxs-lookup"><span data-stu-id="6843a-115">Child Elements</span></span>  
  
|<span data-ttu-id="6843a-116">要素</span><span class="sxs-lookup"><span data-stu-id="6843a-116">Element</span></span>|<span data-ttu-id="6843a-117">説明</span><span class="sxs-lookup"><span data-stu-id="6843a-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6843a-118">\<add></span><span class="sxs-lookup"><span data-stu-id="6843a-118">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/add-element-for-listeners-for-source.md)|<span data-ttu-id="6843a-119">`Listeners` コレクションにリスナーを追加します。</span><span class="sxs-lookup"><span data-stu-id="6843a-119">Adds a listener to the `Listeners` collection.</span></span>|  
|[<span data-ttu-id="6843a-120">\<remove></span><span class="sxs-lookup"><span data-stu-id="6843a-120">\<remove></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/remove-element-for-listeners-for-source.md)|<span data-ttu-id="6843a-121">リスナーを削除、`Listeners`コレクション。</span><span class="sxs-lookup"><span data-stu-id="6843a-121">Removes a listener from the `Listeners` collection.</span></span>|  
|[<span data-ttu-id="6843a-122">\<clear></span><span class="sxs-lookup"><span data-stu-id="6843a-122">\<clear></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/clear-element-for-listeners-for-source.md)|<span data-ttu-id="6843a-123">トレース ソースの `Listeners` コレクションを消去します。</span><span class="sxs-lookup"><span data-stu-id="6843a-123">Clears the `Listeners` collection for a trace source.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6843a-124">親要素</span><span class="sxs-lookup"><span data-stu-id="6843a-124">Parent Elements</span></span>  
  
|<span data-ttu-id="6843a-125">要素</span><span class="sxs-lookup"><span data-stu-id="6843a-125">Element</span></span>|<span data-ttu-id="6843a-126">説明</span><span class="sxs-lookup"><span data-stu-id="6843a-126">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="6843a-127">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="6843a-127">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="6843a-128">メッセージを収集、格納、およびルーティングするトレース リスナーとトレース スイッチを設定するレベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="6843a-128">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sources`|<span data-ttu-id="6843a-129">トレース メッセージを開始するトレース ソースを保持します。</span><span class="sxs-lookup"><span data-stu-id="6843a-129">Contains trace sources that initiate tracing messages.</span></span>|  
|`source`|<span data-ttu-id="6843a-130">トレース メッセージを開始するトレース ソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="6843a-130">Specifies a trace source that initiates tracing messages.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6843a-131">Remarks</span><span class="sxs-lookup"><span data-stu-id="6843a-131">Remarks</span></span>  
  
## <a name="configuration-file"></a><span data-ttu-id="6843a-132">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="6843a-132">Configuration File</span></span>  
 <span data-ttu-id="6843a-133">この要素は、マシン構成ファイル (Machine.config) と、アプリケーション構成ファイルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="6843a-133">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6843a-134">例</span><span class="sxs-lookup"><span data-stu-id="6843a-134">Example</span></span>  
 <span data-ttu-id="6843a-135">次の例は、使用する方法を示します、`<listeners>`コンソール トレース リスナーを追加する要素、`mySource`ソースおよび既定のトレース リスナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="6843a-135">The following example shows how to use the `<listeners>` element to add a console trace listener to the `mySource` source and to remove the default trace listener.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="mySource" switchName="sourceSwitch"   
        switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <add name="console"   
            type="System.Diagnostics.ConsoleTraceListener">  
            <filter type="System.Diagnostics.EventTypeFilter"   
              initializeData="Error"/>  
          </add>  
          <remove name="Default"/>  
        </listeners>  
      </source>  
    </sources>  
    <switches>  
      <add name="sourceSwitch" value="Warning"/>  
    </switches>  
  </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6843a-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="6843a-136">See Also</span></span>  
 <xref:System.Diagnostics.TraceListener>  
 [<span data-ttu-id="6843a-137">トレースおよびデバッグ設定のスキーマ</span><span class="sxs-lookup"><span data-stu-id="6843a-137">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)  
 [<span data-ttu-id="6843a-138">トレース リスナー</span><span class="sxs-lookup"><span data-stu-id="6843a-138">Trace Listeners</span></span>](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
