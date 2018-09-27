---
title: '&lt;上の sharedListeners&gt;要素'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#sharedListeners
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sharedListeners
helpviewer_keywords:
- <sharedListeners> element
- listeners
- shared listeners
- trace listeners, <sharedListeners> element
- sharedListeners element
ms.assetid: de200534-19dd-4156-86cf-c50521802c4c
author: mcleblanc
ms.author: markl
ms.openlocfilehash: b312ea8180c464fb9f955e7d7079cac930c8bf05
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2018
ms.locfileid: "47397112"
---
# <a name="ltsharedlistenersgt-element"></a><span data-ttu-id="15140-102">&lt;上の sharedListeners&gt;要素</span><span class="sxs-lookup"><span data-stu-id="15140-102">&lt;sharedListeners&gt; Element</span></span>
<span data-ttu-id="15140-103">任意の source 要素または trace 要素が参照できるリスナーを含みます。</span><span class="sxs-lookup"><span data-stu-id="15140-103">Contains listeners that any source or trace element can reference.</span></span>  <span data-ttu-id="15140-104">これらのリスナーが既定では、トレースを受信しないと、実行時にこれらのリスナーを取得することはできません。</span><span class="sxs-lookup"><span data-stu-id="15140-104">These listeners do not receive any traces by default, and it is not possible to retrieve these listeners at run time.</span></span> <span data-ttu-id="15140-105">共有リスナーとして識別されたリスナーは、名前によってソースまたはトレースに追加できます。</span><span class="sxs-lookup"><span data-stu-id="15140-105">Listeners identified as shared listeners can be added to sources or traces by name.</span></span>  
  
 <span data-ttu-id="15140-106">\<configuration></span><span class="sxs-lookup"><span data-stu-id="15140-106">\<configuration></span></span>  
<span data-ttu-id="15140-107">\<system.diagnostics ></span><span class="sxs-lookup"><span data-stu-id="15140-107">\<system.diagnostics></span></span>  
<span data-ttu-id="15140-108">\<上の sharedListeners ></span><span class="sxs-lookup"><span data-stu-id="15140-108">\<sharedListeners></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="15140-109">構文</span><span class="sxs-lookup"><span data-stu-id="15140-109">Syntax</span></span>  
  
```xml  
<sharedListeners>   
  <add>...</add>  
</sharedListeners>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="15140-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="15140-110">Attributes and Elements</span></span>  
 <span data-ttu-id="15140-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="15140-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="15140-112">属性</span><span class="sxs-lookup"><span data-stu-id="15140-112">Attributes</span></span>  
 <span data-ttu-id="15140-113">なし。</span><span class="sxs-lookup"><span data-stu-id="15140-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="15140-114">子要素</span><span class="sxs-lookup"><span data-stu-id="15140-114">Child Elements</span></span>  
  
|<span data-ttu-id="15140-115">要素</span><span class="sxs-lookup"><span data-stu-id="15140-115">Element</span></span>|<span data-ttu-id="15140-116">説明</span><span class="sxs-lookup"><span data-stu-id="15140-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="15140-117">\<add></span><span class="sxs-lookup"><span data-stu-id="15140-117">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/add-element-for-listeners-for-trace.md)|<span data-ttu-id="15140-118">`sharedListeners` コレクションにリスナーを追加します。</span><span class="sxs-lookup"><span data-stu-id="15140-118">Adds a listener to the `sharedListeners` collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="15140-119">親要素</span><span class="sxs-lookup"><span data-stu-id="15140-119">Parent Elements</span></span>  
  
|<span data-ttu-id="15140-120">要素</span><span class="sxs-lookup"><span data-stu-id="15140-120">Element</span></span>|<span data-ttu-id="15140-121">説明</span><span class="sxs-lookup"><span data-stu-id="15140-121">Description</span></span>|  
|-------------|-----------------|  
|`Configuration`|<span data-ttu-id="15140-122">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="15140-122">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="15140-123">ASP.NET 構成セクションのルート要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="15140-123">Specifies the root element for the ASP.NET configuration section.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="15140-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="15140-124">Remarks</span></span>  
 <span data-ttu-id="15140-125">共有リスナー コレクションにリスナーを追加することはありませんが、アクティブなリスナー。</span><span class="sxs-lookup"><span data-stu-id="15140-125">Adding a listener to the shared listeners collection does not make it an active listener.</span></span> <span data-ttu-id="15140-126">これは、必要がありますに追加されますトレース ソースまたはトレースに追加することによって、 `Listeners` trace 要素のコレクション。</span><span class="sxs-lookup"><span data-stu-id="15140-126">It must still be added to a trace source or a trace by adding it to the `Listeners` collection for that trace element.</span></span> <span data-ttu-id="15140-127">.NET Framework でリスナー クラスから派生、<xref:System.Diagnostics.TraceListener>クラス。</span><span class="sxs-lookup"><span data-stu-id="15140-127">The listener classes in the .NET Framework derive from the <xref:System.Diagnostics.TraceListener> class.</span></span>  
  
 <span data-ttu-id="15140-128">この要素は、マシン構成ファイル (Machine.config) と、アプリケーション構成ファイルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="15140-128">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="15140-129">例</span><span class="sxs-lookup"><span data-stu-id="15140-129">Example</span></span>  
 <span data-ttu-id="15140-130">次の例は、使用する方法を示します、`<sharedListeners>`リスナーを追加する要素`console`を`Listeners`両方のコレクション、<xref:System.Diagnostics.TraceSource>と<xref:System.Diagnostics.Trace>クラス。</span><span class="sxs-lookup"><span data-stu-id="15140-130">The following example shows how to use the `<sharedListeners>` element to add the listener `console` to the `Listeners` collection for both the <xref:System.Diagnostics.TraceSource> and <xref:System.Diagnostics.Trace> classes.</span></span> <span data-ttu-id="15140-131">コンソール トレース リスナーは、いずれかの呼び出しを通じて、コンソールにトレース情報を書き込みます<xref:System.Diagnostics.TraceSource>または<xref:System.Diagnostics.Trace>します。</span><span class="sxs-lookup"><span data-stu-id="15140-131">The console trace listener writes trace information to the console through calls to either <xref:System.Diagnostics.TraceSource> or <xref:System.Diagnostics.Trace>.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sharedListeners>  
      <add name="console" type="System.Diagnostics.ConsoleTraceListener" >  
        <filter type="System.Diagnostics.EventTypeFilter"  
          initializeData="Warning" />  
      </add>  
    </sharedListeners>  
    <sources>  
      <source name="mySource" switchName="sourceSwitch"  >  
        <listeners>  
          <add name="console" />  
        </listeners>  
      </source>  
    </sources>  
    <switches>  
      <add name="sourceSwitch" value="Verbose"/>  
    </switches>  
    <trace>  
      <listeners>  
        <add name="console" />  
      </listeners>  
    </trace>  
  </system.diagnostics>  
</configuration></system.diagnostics>   
```  
  
## <a name="see-also"></a><span data-ttu-id="15140-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="15140-132">See Also</span></span>  
 <xref:System.Diagnostics.TraceListener>  
 [<span data-ttu-id="15140-133">トレースおよびデバッグ設定のスキーマ</span><span class="sxs-lookup"><span data-stu-id="15140-133">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)  
 [<span data-ttu-id="15140-134">トレース リスナー</span><span class="sxs-lookup"><span data-stu-id="15140-134">Trace Listeners</span></span>](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
