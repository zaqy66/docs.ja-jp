---
title: '&lt;オフ&gt;要素&lt;リスナー&gt;の&lt;トレース&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/trace/listeners/clear
helpviewer_keywords:
- clear element for <listeners> for <trace>
- <clear> element for <listeners> for <trace>
ms.assetid: b44732a8-271f-4a06-ba9e-fe3298d6f192
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 91b4b4f132138fa6752c1da9b28e7a3ab7fad006
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47082891"
---
# <a name="ltcleargt-element-for-ltlistenersgt-for-lttracegt"></a><span data-ttu-id="43484-102">&lt;オフ&gt;要素&lt;リスナー&gt;の&lt;トレース&gt;</span><span class="sxs-lookup"><span data-stu-id="43484-102">&lt;clear&gt; Element for &lt;listeners&gt; for &lt;trace&gt;</span></span>
<span data-ttu-id="43484-103">トレースの `Listeners` コレクションを削除します。</span><span class="sxs-lookup"><span data-stu-id="43484-103">Clears the `Listeners` collection for trace.</span></span>  
  
 <span data-ttu-id="43484-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="43484-104">\<configuration></span></span>  
<span data-ttu-id="43484-105">\<system.diagnostics ></span><span class="sxs-lookup"><span data-stu-id="43484-105">\<system.diagnostics></span></span>  
<span data-ttu-id="43484-106">\<トレース ></span><span class="sxs-lookup"><span data-stu-id="43484-106">\<trace></span></span>  
<span data-ttu-id="43484-107">\<リスナー ></span><span class="sxs-lookup"><span data-stu-id="43484-107">\<listeners></span></span>  
<span data-ttu-id="43484-108">\<クリア ></span><span class="sxs-lookup"><span data-stu-id="43484-108">\<clear></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="43484-109">構文</span><span class="sxs-lookup"><span data-stu-id="43484-109">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="43484-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="43484-110">Attributes and Elements</span></span>  
 <span data-ttu-id="43484-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="43484-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="43484-112">属性</span><span class="sxs-lookup"><span data-stu-id="43484-112">Attributes</span></span>  
 <span data-ttu-id="43484-113">なし。</span><span class="sxs-lookup"><span data-stu-id="43484-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="43484-114">子要素</span><span class="sxs-lookup"><span data-stu-id="43484-114">Child Elements</span></span>  
 <span data-ttu-id="43484-115">なし。</span><span class="sxs-lookup"><span data-stu-id="43484-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="43484-116">親要素</span><span class="sxs-lookup"><span data-stu-id="43484-116">Parent Elements</span></span>  
  
|<span data-ttu-id="43484-117">要素</span><span class="sxs-lookup"><span data-stu-id="43484-117">Element</span></span>|<span data-ttu-id="43484-118">説明</span><span class="sxs-lookup"><span data-stu-id="43484-118">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="43484-119">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="43484-119">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="43484-120">メッセージを収集、格納、およびルーティングするトレース リスナーとトレース スイッチを設定するレベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="43484-120">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`trace`|<span data-ttu-id="43484-121">トレース メッセージを収集、格納、およびルーティングするリスナーを保持します。</span><span class="sxs-lookup"><span data-stu-id="43484-121">Contains listeners that collect, store, and route tracing messages.</span></span>|  
|`listeners`|<span data-ttu-id="43484-122">収集、格納、およびメッセージをルーティングするリスナーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="43484-122">Contains listeners that collect, store, and route messages.</span></span> <span data-ttu-id="43484-123">リスナーでは、適切なターゲットのトレースを出力します。</span><span class="sxs-lookup"><span data-stu-id="43484-123">Listeners direct the tracing output to an appropriate target.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="43484-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="43484-124">Remarks</span></span>  
 <span data-ttu-id="43484-125">`<clear>`要素からすべてのリスナーを削除して、`Listeners`トレースのコレクション。</span><span class="sxs-lookup"><span data-stu-id="43484-125">The `<clear>` element removes all listeners from the `Listeners` collection for trace.</span></span> <span data-ttu-id="43484-126">使用することができます、`<clear>`要素を使用する前に、`<add>`要素をコレクション内の他のアクティブなリスナーが存在しないことを特定します。</span><span class="sxs-lookup"><span data-stu-id="43484-126">You can use the `<clear>` element before using the `<add>` element to be certain there are no other active listeners in the collection.</span></span>  
  
 <span data-ttu-id="43484-127">オフにすることができます、`Listeners`呼び出すことによってプログラムでのコレクション、<xref:System.Diagnostics.TraceListenerCollection.Clear%2A>メソッドを<xref:System.Diagnostics.Trace.Listeners%2A?displayProperty=nameWithType>プロパティ (`System.Diagnostics.Trace.Listeners.Clear()`)。</span><span class="sxs-lookup"><span data-stu-id="43484-127">You can clear the `Listeners` collection programmatically by calling the <xref:System.Diagnostics.TraceListenerCollection.Clear%2A> method on the <xref:System.Diagnostics.Trace.Listeners%2A?displayProperty=nameWithType> property (`System.Diagnostics.Trace.Listeners.Clear()`).</span></span>  
  
 <span data-ttu-id="43484-128">この要素は、マシン構成ファイル (Machine.config) と、アプリケーション構成ファイルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="43484-128">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="43484-129">`<clear>`要素は、削除、<xref:System.Diagnostics.DefaultTraceListener>から、`Listeners`の動作を変更するコレクション、 <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType>、 <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=nameWithType>、 <xref:System.Diagnostics.Debug.Fail%2A?displayProperty=nameWithType>、および<xref:System.Diagnostics.Trace.Fail%2A?displayProperty=nameWithType>メソッド。</span><span class="sxs-lookup"><span data-stu-id="43484-129">The `<clear>` element removes the <xref:System.Diagnostics.DefaultTraceListener> from the `Listeners` collection, altering the behavior of the <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Debug.Fail%2A?displayProperty=nameWithType>, and <xref:System.Diagnostics.Trace.Fail%2A?displayProperty=nameWithType> methods.</span></span> <span data-ttu-id="43484-130">呼び出す、`Assert`または`Fail`メソッドは、通常、メッセージ ボックスの表示になります。</span><span class="sxs-lookup"><span data-stu-id="43484-130">Calling an `Assert` or `Fail` method normally results in the display of a message box.</span></span> <span data-ttu-id="43484-131">場合、メッセージ ボックスが表示されません、<xref:System.Diagnostics.DefaultTraceListener>内にない、`Listeners`コレクション。</span><span class="sxs-lookup"><span data-stu-id="43484-131">However, the message box is not displayed if the <xref:System.Diagnostics.DefaultTraceListener> is not in the `Listeners` collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="43484-132">例</span><span class="sxs-lookup"><span data-stu-id="43484-132">Example</span></span>  
 <span data-ttu-id="43484-133">次の例は、使用する方法を示します、`<clear>`要素を使用する前に、`<add>`リスナーを追加する要素`console`を`Listeners`トレースのコレクション。</span><span class="sxs-lookup"><span data-stu-id="43484-133">The following example shows how to use the `<clear>` element before using the `<add>` element to add the listener `console` to the `Listeners` collection for trace.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <trace autoflush="false" indentsize="4">  
      <listeners>  
        <clear/>  
        <add name="console"   
          type="System.Diagnostics.ConsoleTraceListener" >  
          <filter type="System.Diagnostics.EventTypeFilter"   
            initializeData="Error" />  
        </add>  
      </listeners>  
    </trace>  
  </system.diagnostics>  
</configuration>   
```  
  
## <a name="see-also"></a><span data-ttu-id="43484-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="43484-134">See Also</span></span>  
 <xref:System.Diagnostics.Trace.Listeners%2A>  
 <xref:System.Diagnostics.Trace>  
 <xref:System.Diagnostics.Debug>  
 <xref:System.Diagnostics.TraceSource>  
 [<span data-ttu-id="43484-135">トレースおよびデバッグ設定のスキーマ</span><span class="sxs-lookup"><span data-stu-id="43484-135">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)  
 [<span data-ttu-id="43484-136">\<remove></span><span class="sxs-lookup"><span data-stu-id="43484-136">\<remove></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/remove-element-for-listeners-for-trace.md)  
 [<span data-ttu-id="43484-137">トレース リスナー</span><span class="sxs-lookup"><span data-stu-id="43484-137">Trace Listeners</span></span>](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
