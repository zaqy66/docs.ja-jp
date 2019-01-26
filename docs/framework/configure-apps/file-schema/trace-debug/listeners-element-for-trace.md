---
title: '&lt;リスナー&gt;要素&lt;トレース&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/trace/listeners
helpviewer_keywords:
- <listeners> element
- listeners element
ms.assetid: 1394c2c3-6304-46db-87c1-8e8b16f5ad5b
ms.openlocfilehash: d98c286a49aa6439b6b82b5982a2ea4690c98b43
ms.sourcegitcommit: b351b0781a035616c90c68ccae6dd60aae66a953
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/26/2019
ms.locfileid: "55083822"
---
# <a name="ltlistenersgt-element-for-lttracegt"></a><span data-ttu-id="6daf4-102">&lt;リスナー&gt;要素&lt;トレース&gt;</span><span class="sxs-lookup"><span data-stu-id="6daf4-102">&lt;listeners&gt; Element for &lt;trace&gt;</span></span>
<span data-ttu-id="6daf4-103">収集、するリスナーをストアを指定し、メッセージをルーティングします。</span><span class="sxs-lookup"><span data-stu-id="6daf4-103">Specifies a listener that collects, stores, and routes messages.</span></span> <span data-ttu-id="6daf4-104">リスナーでは、適切なターゲットのトレースを出力します。</span><span class="sxs-lookup"><span data-stu-id="6daf4-104">Listeners direct the tracing output to an appropriate target.</span></span>  
  
 <span data-ttu-id="6daf4-105">\<configuration > 要素</span><span class="sxs-lookup"><span data-stu-id="6daf4-105">\<configuration> Element</span></span>  
<span data-ttu-id="6daf4-106">\<system.diagnostics > 要素</span><span class="sxs-lookup"><span data-stu-id="6daf4-106">\<system.diagnostics> Element</span></span>  
<span data-ttu-id="6daf4-107">\<トレース > 要素</span><span class="sxs-lookup"><span data-stu-id="6daf4-107">\<trace> Element</span></span>  
<span data-ttu-id="6daf4-108">\<リスナー > 要素の\<トレース ></span><span class="sxs-lookup"><span data-stu-id="6daf4-108">\<listeners> Element for \<trace></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6daf4-109">構文</span><span class="sxs-lookup"><span data-stu-id="6daf4-109">Syntax</span></span>  
  
```xml  
<listeners>   
  <add>...</add>  
  <clear/>  
  <remove ... />  
</listeners>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6daf4-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="6daf4-110">Attributes and Elements</span></span>  
 <span data-ttu-id="6daf4-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="6daf4-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6daf4-112">属性</span><span class="sxs-lookup"><span data-stu-id="6daf4-112">Attributes</span></span>  
 <span data-ttu-id="6daf4-113">なし。</span><span class="sxs-lookup"><span data-stu-id="6daf4-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="6daf4-114">子要素</span><span class="sxs-lookup"><span data-stu-id="6daf4-114">Child Elements</span></span>  
  
|<span data-ttu-id="6daf4-115">要素</span><span class="sxs-lookup"><span data-stu-id="6daf4-115">Element</span></span>|<span data-ttu-id="6daf4-116">説明</span><span class="sxs-lookup"><span data-stu-id="6daf4-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6daf4-117">\<add></span><span class="sxs-lookup"><span data-stu-id="6daf4-117">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/add-element-for-listeners-for-trace.md)|<span data-ttu-id="6daf4-118">`Listeners` コレクションにリスナーを追加します。</span><span class="sxs-lookup"><span data-stu-id="6daf4-118">Adds a listener to the `Listeners` collection.</span></span>|  
|[<span data-ttu-id="6daf4-119">\<clear></span><span class="sxs-lookup"><span data-stu-id="6daf4-119">\<clear></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/clear-element-for-listeners-for-trace.md)|<span data-ttu-id="6daf4-120">トレースの `Listeners` コレクションを削除します。</span><span class="sxs-lookup"><span data-stu-id="6daf4-120">Clears the `Listeners` collection for trace.</span></span>|  
|[<span data-ttu-id="6daf4-121">\<remove></span><span class="sxs-lookup"><span data-stu-id="6daf4-121">\<remove></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/remove-element-for-listeners-for-trace.md)|<span data-ttu-id="6daf4-122">リスナーを削除、`Listeners`コレクション。</span><span class="sxs-lookup"><span data-stu-id="6daf4-122">Removes a listener from the `Listeners` collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6daf4-123">親要素</span><span class="sxs-lookup"><span data-stu-id="6daf4-123">Parent Elements</span></span>  
  
|<span data-ttu-id="6daf4-124">要素</span><span class="sxs-lookup"><span data-stu-id="6daf4-124">Element</span></span>|<span data-ttu-id="6daf4-125">説明</span><span class="sxs-lookup"><span data-stu-id="6daf4-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="6daf4-126">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="6daf4-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="6daf4-127">ASP.NET 構成セクションのルート要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="6daf4-127">Specifies the root element for the ASP.NET configuration section.</span></span>|  
|`trace`|<span data-ttu-id="6daf4-128">トレース メッセージを収集、格納、およびルーティングするリスナーを保持します。</span><span class="sxs-lookup"><span data-stu-id="6daf4-128">Contains listeners that collect, store, and route tracing messages.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6daf4-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="6daf4-129">Remarks</span></span>  
 <span data-ttu-id="6daf4-130"><xref:System.Diagnostics.Debug>と<xref:System.Diagnostics.Trace>クラスが同じ共有**リスナー**コレクション。</span><span class="sxs-lookup"><span data-stu-id="6daf4-130">The <xref:System.Diagnostics.Debug> and <xref:System.Diagnostics.Trace> classes share the same **Listeners** collection.</span></span> <span data-ttu-id="6daf4-131">これらのクラスのいずれかで、コレクションにリスナー オブジェクトを追加する場合、その他のクラスは、同一のリスナーを使用します。</span><span class="sxs-lookup"><span data-stu-id="6daf4-131">If you add a listener object to the collection in one of these classes, the other class uses the same listener.</span></span> <span data-ttu-id="6daf4-132">.NET Framework に付属するリスナー クラスから派生、<xref:System.Diagnostics.TraceListener>クラス。</span><span class="sxs-lookup"><span data-stu-id="6daf4-132">The listener classes shipped with the .NET Framework derive from the <xref:System.Diagnostics.TraceListener> class.</span></span>  
  
## <a name="configuration-file"></a><span data-ttu-id="6daf4-133">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="6daf4-133">Configuration File</span></span>  
 <span data-ttu-id="6daf4-134">この要素は、マシン構成ファイル (Machine.config) と、アプリケーション構成ファイルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="6daf4-134">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6daf4-135">例</span><span class="sxs-lookup"><span data-stu-id="6daf4-135">Example</span></span>  
 <span data-ttu-id="6daf4-136">次の例は、使用する方法を示します、 **\<リスナー >** リスナーを追加する要素`MyListener`と`MyEventListener`を**リスナー**コレクション。</span><span class="sxs-lookup"><span data-stu-id="6daf4-136">The following example shows how to use the **\<listeners>** element to add the listeners `MyListener` and `MyEventListener` to the **Listeners** collection.</span></span> <span data-ttu-id="6daf4-137">`MyListener` という名前のファイルを作成します。`MyListener.log`し、ファイルに出力を書き込みます。</span><span class="sxs-lookup"><span data-stu-id="6daf4-137">`MyListener` creates a file called `MyListener.log` and writes the output to the file.</span></span> <span data-ttu-id="6daf4-138">`MyEventListener` イベント ログにエントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="6daf4-138">`MyEventListener` creates an entry in the event log.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <trace autoflush="true" indentsize="0">  
      <listeners>  
        <add name="myListener"   
          type="System.Diagnostics.TextWriterTraceListener,   
            system, version=1.0.3300.0, Culture=neutral,   
            PublicKeyToken=b77a5c561934e089"   
          initializeData="c:\myListener.log" />  
        <add name="MyEventListener"  
          type="System.Diagnostics.EventLogTraceListener,   
            system, version=1.0.3300.0, Culture=neutral,   
            PublicKeyToken=b77a5c561934e089"  
          initializeData="MyConfigEventLog"/>  
      </listeners>  
    </trace>  
  </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6daf4-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="6daf4-139">See also</span></span>
- <xref:System.Diagnostics.TraceListener>
- [<span data-ttu-id="6daf4-140">トレースおよびデバッグ設定のスキーマ</span><span class="sxs-lookup"><span data-stu-id="6daf4-140">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
