---
title: '&lt;ソース&gt;要素'
ms.date: 09/29/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sources/source
- http://schemas.microsoft.com/.NetConfiguration/v2.0#source
helpviewer_keywords:
- <source> element
- source element
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 818324077322fffb40a192c9197efde6e8ff7591
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47088946"
---
# <a name="ltsourcegt-element"></a><span data-ttu-id="28320-102">&lt;ソース&gt;要素</span><span class="sxs-lookup"><span data-stu-id="28320-102">&lt;source&gt; Element</span></span>
<span data-ttu-id="28320-103">トレース メッセージを開始するトレース ソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="28320-103">Specifies a trace source that initiates tracing messages.</span></span>  
  
 <span data-ttu-id="28320-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="28320-104">\<configuration></span></span>  
<span data-ttu-id="28320-105">\<system.diagnostics ></span><span class="sxs-lookup"><span data-stu-id="28320-105">\<system.diagnostics></span></span>  
<span data-ttu-id="28320-106">\<ソース ></span><span class="sxs-lookup"><span data-stu-id="28320-106">\<sources></span></span>  
<span data-ttu-id="28320-107">\<ソース ></span><span class="sxs-lookup"><span data-stu-id="28320-107">\<source></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="28320-108">構文</span><span class="sxs-lookup"><span data-stu-id="28320-108">Syntax</span></span>  
  
```xml  
<source>   
  <listeners>...</listeners>  
</source>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="28320-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="28320-109">Attributes and Elements</span></span>  
 <span data-ttu-id="28320-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="28320-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="28320-111">属性</span><span class="sxs-lookup"><span data-stu-id="28320-111">Attributes</span></span>  
  
|<span data-ttu-id="28320-112">属性</span><span class="sxs-lookup"><span data-stu-id="28320-112">Attribute</span></span>|<span data-ttu-id="28320-113">説明</span><span class="sxs-lookup"><span data-stu-id="28320-113">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="28320-114">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="28320-114">Optional attribute.</span></span><br /><br /> <span data-ttu-id="28320-115">トレース ソースの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="28320-115">Specifies the name of the trace source.</span></span>|  
|`switchName`|<span data-ttu-id="28320-116">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="28320-116">Optional attribute.</span></span><br /><br /> <span data-ttu-id="28320-117">アプリケーションでは、トレース スイッチのインスタンスの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="28320-117">Specifies the name of a trace switch instance in the application.</span></span> <span data-ttu-id="28320-118">スイッチで指定されていない場合、`<switches>`要素の値が、スイッチのレベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="28320-118">If the switch is not identified in a `<switches>` element, the value specifies the level for the switch.</span></span>|  
|`switchType`|<span data-ttu-id="28320-119">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="28320-119">Optional attribute.</span></span><br /><br /> <span data-ttu-id="28320-120">トレース スイッチの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="28320-120">Specifies the type of the trace switch.</span></span> <span data-ttu-id="28320-121">存在する場合、型はクラス名として有効にする必要があり、空の文字列にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="28320-121">If present, the type must be a valid class name and cannot be an empty string.</span></span>|  
|`extraAttribute`|<span data-ttu-id="28320-122">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="28320-122">Optional attribute.</span></span><br /><br /> <span data-ttu-id="28320-123">識別されるトレース ソースに固有の属性の値を指定します、<xref:System.Diagnostics.TraceSource.GetSupportedAttributes%2A>トレース ソースのためのメソッド。</span><span class="sxs-lookup"><span data-stu-id="28320-123">Specifies the value for a trace source-specific attribute identified by the <xref:System.Diagnostics.TraceSource.GetSupportedAttributes%2A> method for that trace source.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="28320-124">子要素</span><span class="sxs-lookup"><span data-stu-id="28320-124">Child Elements</span></span>  
  
|<span data-ttu-id="28320-125">要素</span><span class="sxs-lookup"><span data-stu-id="28320-125">Element</span></span>|<span data-ttu-id="28320-126">説明</span><span class="sxs-lookup"><span data-stu-id="28320-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="28320-127">\<listeners></span><span class="sxs-lookup"><span data-stu-id="28320-127">\<listeners></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/listeners-element-for-source.md)|<span data-ttu-id="28320-128">収集、格納、およびメッセージをルーティングするリスナーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="28320-128">Contains listeners that collect, store, and route messages.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="28320-129">親要素</span><span class="sxs-lookup"><span data-stu-id="28320-129">Parent Elements</span></span>  
  
|<span data-ttu-id="28320-130">要素</span><span class="sxs-lookup"><span data-stu-id="28320-130">Element</span></span>|<span data-ttu-id="28320-131">説明</span><span class="sxs-lookup"><span data-stu-id="28320-131">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="28320-132">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="28320-132">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="28320-133">メッセージを収集、格納、およびルーティングするトレース リスナーとトレース スイッチを設定するレベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="28320-133">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sources`|<span data-ttu-id="28320-134">トレース メッセージを開始するトレース ソースを保持します。</span><span class="sxs-lookup"><span data-stu-id="28320-134">Contains trace sources that initiate tracing messages.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="28320-135">Remarks</span><span class="sxs-lookup"><span data-stu-id="28320-135">Remarks</span></span>  
 <span data-ttu-id="28320-136">この要素は、マシン構成ファイル (Machine.config) と、アプリケーション構成ファイルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="28320-136">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="28320-137">例</span><span class="sxs-lookup"><span data-stu-id="28320-137">Example</span></span>  
 <span data-ttu-id="28320-138">次の例は、使用する方法を示します、`<source>`トレース ソースを追加する要素`mySource`という名前のソース スイッチのレベルを設定して`sourceSwitch`します。</span><span class="sxs-lookup"><span data-stu-id="28320-138">The following example shows how to use the `<source>` element to add the trace source `mySource` and to set the level for the source switch named `sourceSwitch`.</span></span> <span data-ttu-id="28320-139">トレース情報をコンソールに出力する、コンソール トレース リスナーが追加されます。</span><span class="sxs-lookup"><span data-stu-id="28320-139">A console trace listener is added that writes trace information to the console.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="mySource" switchName="sourceSwitch" switchType="System.Diagnostics.SourceSwitch"  >  
        <listeners>  
          <add name="console" type="System.Diagnostics.ConsoleTraceListener" >  
            <filter type="System.Diagnostics.EventTypeFilter" initializeData="Error" />  
          </add>  
          <remove name="Default" />  
        </listeners>  
      </source>  
    </sources>  
        <switches>  
           <add name="sourceSwitch" value="Warning" />  
        </switches>    
  </system.diagnostics>   
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="28320-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="28320-140">See Also</span></span>  
 [<span data-ttu-id="28320-141">トレースおよびデバッグ設定のスキーマ</span><span class="sxs-lookup"><span data-stu-id="28320-141">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)  
 [<span data-ttu-id="28320-142">トレース スイッチ</span><span class="sxs-lookup"><span data-stu-id="28320-142">Trace Switches</span></span>](../../../../../docs/framework/debug-trace-profile/trace-switches.md)
