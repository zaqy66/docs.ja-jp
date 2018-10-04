---
title: '&lt;追加&gt;要素&lt;リスナー&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sharedListeners/add
helpviewer_keywords:
- initializeData attribute
- <add> element for <sharedListeners>
- add element for <sharedListeners>
ms.assetid: 1595e1bc-2492-421f-8384-7f382eb8eb57
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 93fdb548882422634e1d2456b4d37f434b278f8d
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "48777829"
---
# <a name="ltaddgt-element-for-ltsharedlistenersgt"></a><span data-ttu-id="f27e5-102">&lt;追加&gt;要素&lt;リスナー&gt;</span><span class="sxs-lookup"><span data-stu-id="f27e5-102">&lt;add&gt; Element for &lt;sharedListeners&gt;</span></span>
<span data-ttu-id="f27e5-103">`sharedListeners` コレクションにリスナーを追加します。</span><span class="sxs-lookup"><span data-stu-id="f27e5-103">Adds a listener to the `sharedListeners` collection.</span></span> <span data-ttu-id="f27e5-104">`sharedListeners` リスナーのコレクションは、 [\<ソース >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/source-element.md)または[\<トレース >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/trace-element.md)を参照できます。</span><span class="sxs-lookup"><span data-stu-id="f27e5-104">`sharedListeners` is a collection of listeners that any [\<source>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/source-element.md) or [\<trace>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/trace-element.md) can reference.</span></span>  <span data-ttu-id="f27e5-105">既定でリスナーに、`sharedListeners`でコレクションが配置されていない、`Listeners`コレクション。</span><span class="sxs-lookup"><span data-stu-id="f27e5-105">By default, listeners in the `sharedListeners` collection are not placed in a `Listeners` collection.</span></span> <span data-ttu-id="f27e5-106">名前で追加する必要があります、 [\<ソース >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/source-element.md)または[\<トレース >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/trace-element.md)します。</span><span class="sxs-lookup"><span data-stu-id="f27e5-106">They must be added by name to the [\<source>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/source-element.md) or [\<trace>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/trace-element.md).</span></span> <span data-ttu-id="f27e5-107">リスナーを取得することはできません、`sharedListeners`実行時にコード内のコレクション。</span><span class="sxs-lookup"><span data-stu-id="f27e5-107">It is not possible to get the listeners in the `sharedListeners` collection in code at run time.</span></span>  
  
 <span data-ttu-id="f27e5-108">\<configuration></span><span class="sxs-lookup"><span data-stu-id="f27e5-108">\<configuration></span></span>  
<span data-ttu-id="f27e5-109">\<system.diagnostics ></span><span class="sxs-lookup"><span data-stu-id="f27e5-109">\<system.diagnostics></span></span>  
<span data-ttu-id="f27e5-110">\<上の sharedListeners > 要素</span><span class="sxs-lookup"><span data-stu-id="f27e5-110">\<sharedListeners> Element</span></span>  
<span data-ttu-id="f27e5-111">\<add></span><span class="sxs-lookup"><span data-stu-id="f27e5-111">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f27e5-112">構文</span><span class="sxs-lookup"><span data-stu-id="f27e5-112">Syntax</span></span>  
  
```xml  
<add name="name"   
  type="TraceListenerClassName, Version, Culture, PublicKeyToken"  
  initializeData="data"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f27e5-113">属性および要素</span><span class="sxs-lookup"><span data-stu-id="f27e5-113">Attributes and Elements</span></span>  
 <span data-ttu-id="f27e5-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="f27e5-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f27e5-115">属性</span><span class="sxs-lookup"><span data-stu-id="f27e5-115">Attributes</span></span>  
  
|<span data-ttu-id="f27e5-116">属性</span><span class="sxs-lookup"><span data-stu-id="f27e5-116">Attribute</span></span>|<span data-ttu-id="f27e5-117">説明</span><span class="sxs-lookup"><span data-stu-id="f27e5-117">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="f27e5-118">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="f27e5-118">Required attribute.</span></span><br /><br /> <span data-ttu-id="f27e5-119">共有リスナーを追加するために使用するリスナーの名前を指定します、`Listeners`コレクション。</span><span class="sxs-lookup"><span data-stu-id="f27e5-119">Specifies the name of the listener that is used to add the shared listener to a `Listeners` collection.</span></span>|  
|`type`|<span data-ttu-id="f27e5-120">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="f27e5-120">Required attribute.</span></span><br /><br /> <span data-ttu-id="f27e5-121">リスナーの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="f27e5-121">Specifies the type of the listener.</span></span> <span data-ttu-id="f27e5-122">指定された条件に一致する文字列を使用する必要があります[完全修飾型名の指定](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md)します。</span><span class="sxs-lookup"><span data-stu-id="f27e5-122">You must use a string that meets the requirements specified in [Specifying Fully Qualified Type Names](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span></span>|  
|`initializeData`|<span data-ttu-id="f27e5-123">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="f27e5-123">Optional attribute.</span></span><br /><br /> <span data-ttu-id="f27e5-124">指定したクラスのコンス トラクターに渡された文字列。</span><span class="sxs-lookup"><span data-stu-id="f27e5-124">The string passed to the constructor for the specified class.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f27e5-125">子要素</span><span class="sxs-lookup"><span data-stu-id="f27e5-125">Child Elements</span></span>  
  
|<span data-ttu-id="f27e5-126">要素</span><span class="sxs-lookup"><span data-stu-id="f27e5-126">Element</span></span>|<span data-ttu-id="f27e5-127">説明</span><span class="sxs-lookup"><span data-stu-id="f27e5-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f27e5-128">\<filter></span><span class="sxs-lookup"><span data-stu-id="f27e5-128">\<filter></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/filter-element-for-add-for-sharedlisteners.md)|<span data-ttu-id="f27e5-129">`sharedListeners` コレクションのリスナーにフィルターを追加します。</span><span class="sxs-lookup"><span data-stu-id="f27e5-129">Adds a filter to a listener in the `sharedListeners` collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f27e5-130">親要素</span><span class="sxs-lookup"><span data-stu-id="f27e5-130">Parent Elements</span></span>  
  
|<span data-ttu-id="f27e5-131">要素</span><span class="sxs-lookup"><span data-stu-id="f27e5-131">Element</span></span>|<span data-ttu-id="f27e5-132">説明</span><span class="sxs-lookup"><span data-stu-id="f27e5-132">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="f27e5-133">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="f27e5-133">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="f27e5-134">メッセージを収集、格納、およびルーティングするトレース リスナーとトレース スイッチを設定するレベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="f27e5-134">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sharedListeners`|<span data-ttu-id="f27e5-135">任意のソースまたは trace 要素を参照できるリスナーのコレクション。</span><span class="sxs-lookup"><span data-stu-id="f27e5-135">A collection of listeners that any source or trace element can reference.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f27e5-136">Remarks</span><span class="sxs-lookup"><span data-stu-id="f27e5-136">Remarks</span></span>  
 <span data-ttu-id="f27e5-137">.NET Framework に付属するリスナー クラスから派生、<xref:System.Diagnostics.TraceListener>クラス。</span><span class="sxs-lookup"><span data-stu-id="f27e5-137">The listener classes shipped with the .NET Framework derive from the <xref:System.Diagnostics.TraceListener> class.</span></span> <span data-ttu-id="f27e5-138">値、`name`属性を使用する共有リスナーを追加して、`Listeners`トレースまたはトレース ソースのいずれかのコレクション。</span><span class="sxs-lookup"><span data-stu-id="f27e5-138">The value for the `name` attribute is used to add the shared listener to a `Listeners` collection for either a trace or a trace source.</span></span> <span data-ttu-id="f27e5-139">値、`initializeData`属性を作成するリスナーの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="f27e5-139">The value for the `initializeData` attribute depends on the type of listener you create.</span></span> <span data-ttu-id="f27e5-140">指定する必要はないすべてのトレース リスナー`initializeData`します。</span><span class="sxs-lookup"><span data-stu-id="f27e5-140">Not all trace listeners require that you specify `initializeData`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f27e5-141">使用すると、`initializeData`属性、コンパイラの警告「、'initializeData' 属性は宣言されていません」. を取得する可能性があります</span><span class="sxs-lookup"><span data-stu-id="f27e5-141">When you use the `initializeData` attribute, you may get the compiler warning "The 'initializeData' attribute is not declared."</span></span> <span data-ttu-id="f27e5-142">この警告は、構成設定は、抽象基本クラスに対しても検証するために発生します。 <xref:System.Diagnostics.TraceListener>、これを認識しません、`initializeData`属性。</span><span class="sxs-lookup"><span data-stu-id="f27e5-142">This warning occurs because the configuration settings are validated against the abstract base class <xref:System.Diagnostics.TraceListener>, which does not recognize the `initializeData` attribute.</span></span> <span data-ttu-id="f27e5-143">通常、パラメーターを受け取るコンス トラクターを持つトレース リスナーの実装のためには、この警告を無視できます。</span><span class="sxs-lookup"><span data-stu-id="f27e5-143">Typically, you can ignore this warning for trace listener implementations that have a constructor that takes a parameter.</span></span>  
  
 <span data-ttu-id="f27e5-144">次の表は、.NET Framework に含まれているトレース リスナーの表示し、の値を記述、`initializeData`属性。</span><span class="sxs-lookup"><span data-stu-id="f27e5-144">The following table shows the trace listeners that are included with the .NET Framework and describes the value of their `initializeData` attributes.</span></span>  
  
|<span data-ttu-id="f27e5-145">トレース リスナー クラス</span><span class="sxs-lookup"><span data-stu-id="f27e5-145">Trace listener class</span></span>|<span data-ttu-id="f27e5-146">initializeData 属性値</span><span class="sxs-lookup"><span data-stu-id="f27e5-146">initializeData attribute value</span></span>|  
|--------------------------|------------------------------------|  
|<xref:System.Diagnostics.ConsoleTraceListener>|<span data-ttu-id="f27e5-147">`useErrorStream`値、<xref:System.Diagnostics.ConsoleTraceListener.%23ctor%2A>コンス トラクター。</span><span class="sxs-lookup"><span data-stu-id="f27e5-147">The `useErrorStream` value for the <xref:System.Diagnostics.ConsoleTraceListener.%23ctor%2A> constructor.</span></span>  <span data-ttu-id="f27e5-148">設定、`initializeData`属性を"`true`「書き込むトレースとデバッグの出力を標準エラー ストリームに設定」`false`"標準出力ストリームに書き込む。</span><span class="sxs-lookup"><span data-stu-id="f27e5-148">Set the `initializeData` attribute to "`true`" to write trace and debug output to the standard error stream; set it to "`false`" to write to the standard output stream.</span></span>|  
|<xref:System.Diagnostics.DelimitedListTraceListener>|<span data-ttu-id="f27e5-149">ファイルの名前、<xref:System.Diagnostics.DelimitedListTraceListener>に書き込みます。</span><span class="sxs-lookup"><span data-stu-id="f27e5-149">The name of the file the <xref:System.Diagnostics.DelimitedListTraceListener> writes to.</span></span>|  
|<xref:System.Diagnostics.EventLogTraceListener?displayProperty=nameWithType>|<span data-ttu-id="f27e5-150">既存のイベント ログ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="f27e5-150">The name of an existing event log source.</span></span>|  
|<xref:System.Diagnostics.EventSchemaTraceListener?displayProperty=nameWithType>|<span data-ttu-id="f27e5-151">ファイルの名前を<xref:System.Diagnostics.EventSchemaTraceListener>に書き込みます。</span><span class="sxs-lookup"><span data-stu-id="f27e5-151">The name of the file that the <xref:System.Diagnostics.EventSchemaTraceListener> writes to.</span></span>|  
|<xref:System.Diagnostics.TextWriterTraceListener?displayProperty=nameWithType>|<span data-ttu-id="f27e5-152">ファイルの名前を<xref:System.Diagnostics.TextWriterTraceListener>に書き込みます。</span><span class="sxs-lookup"><span data-stu-id="f27e5-152">The name of the file that the <xref:System.Diagnostics.TextWriterTraceListener> writes to.</span></span>|  
|<xref:System.Diagnostics.XmlWriterTraceListener>|<span data-ttu-id="f27e5-153">ファイルの名前を<xref:System.Diagnostics.XmlWriterTraceListener>に書き込みます。</span><span class="sxs-lookup"><span data-stu-id="f27e5-153">The name of the file that the <xref:System.Diagnostics.XmlWriterTraceListener> writes to.</span></span>|  
  
## <a name="configuration-file"></a><span data-ttu-id="f27e5-154">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="f27e5-154">Configuration File</span></span>  
 <span data-ttu-id="f27e5-155">この要素は、マシン構成ファイル (Machine.config) と、アプリケーション構成ファイルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="f27e5-155">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f27e5-156">例</span><span class="sxs-lookup"><span data-stu-id="f27e5-156">Example</span></span>  
 <span data-ttu-id="f27e5-157">次の例は、使用する方法を示します`<add>`要素を追加する、 <xref:System.Diagnostics.TextWriterTraceListener> `textListener`を`sharedListeners`コレクション。</span><span class="sxs-lookup"><span data-stu-id="f27e5-157">The following example shows how to use `<add>` elements to add the <xref:System.Diagnostics.TextWriterTraceListener>`textListener` to the `sharedListeners` collection.</span></span>   <span data-ttu-id="f27e5-158">`textListener` 名前で追加、`Listeners`トレース ソースのコレクション`TraceSourceApp`します。</span><span class="sxs-lookup"><span data-stu-id="f27e5-158">`textListener` is added by name to the `Listeners` collection for the trace source `TraceSourceApp`.</span></span> <span data-ttu-id="f27e5-159">`textListener`ファイル myListener.log にリスナーがトレース出力を書き込みます。</span><span class="sxs-lookup"><span data-stu-id="f27e5-159">The `textListener` listener writes trace output to the file myListener.log.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="TraceSourceApp" switchName="sourceSwitch"   
        switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <add name="console"   
            type="System.Diagnostics.ConsoleTraceListener"/>  
          <add name="textListener"/>  
          <remove name="Default"/>  
        </listeners>  
      </source>  
    </sources>  
    <sharedListeners>  
      <add name="textListener"   
        type="System.Diagnostics.TextWriterTraceListener"   
        initializeData="myListener.log"/>  
    </sharedListeners>  
    <switches>  
      <add name="sourceSwitch" value="Warning"/>  
    </switches>  
  </system.diagnostics>  
</configuration>   
```  
  
## <a name="see-also"></a><span data-ttu-id="f27e5-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="f27e5-160">See Also</span></span>  
 <xref:System.Diagnostics.TraceSource>  
 <xref:System.Diagnostics.TraceListener>  
 [<span data-ttu-id="f27e5-161">トレースおよびデバッグ設定のスキーマ</span><span class="sxs-lookup"><span data-stu-id="f27e5-161">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)  
 [<span data-ttu-id="f27e5-162">トレース リスナー</span><span class="sxs-lookup"><span data-stu-id="f27e5-162">Trace Listeners</span></span>](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
