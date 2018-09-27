---
title: '&lt;スイッチ&gt;要素'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/switches
- http://schemas.microsoft.com/.NetConfiguration/v2.0#switches
helpviewer_keywords:
- <switches> element
- switches element
- trace switches, <switches> element
ms.assetid: 4cf36786-b89a-40e2-a0f1-86bb9b783343
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 7ca375935c1dfcdb406257ece1a9dfd18851dddf
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47232631"
---
# <a name="ltswitchesgt-element"></a><span data-ttu-id="5328a-102">&lt;スイッチ&gt;要素</span><span class="sxs-lookup"><span data-stu-id="5328a-102">&lt;switches&gt; Element</span></span>
<span data-ttu-id="5328a-103">トレース スイッチと、トレース スイッチを設定するレベルを保持します。</span><span class="sxs-lookup"><span data-stu-id="5328a-103">Contains trace switches and the level where the trace switches are set.</span></span>  
  
 <span data-ttu-id="5328a-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="5328a-104">\<configuration></span></span>  
<span data-ttu-id="5328a-105">\<system.diagnostics ></span><span class="sxs-lookup"><span data-stu-id="5328a-105">\<system.diagnostics></span></span>  
<span data-ttu-id="5328a-106">\<スイッチ ></span><span class="sxs-lookup"><span data-stu-id="5328a-106">\<switches></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5328a-107">構文</span><span class="sxs-lookup"><span data-stu-id="5328a-107">Syntax</span></span>  
  
```xml  
      <switches>   
</switches>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5328a-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="5328a-108">Attributes and Elements</span></span>  
 <span data-ttu-id="5328a-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="5328a-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5328a-110">属性</span><span class="sxs-lookup"><span data-stu-id="5328a-110">Attributes</span></span>  
 <span data-ttu-id="5328a-111">なし。</span><span class="sxs-lookup"><span data-stu-id="5328a-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="5328a-112">子要素</span><span class="sxs-lookup"><span data-stu-id="5328a-112">Child Elements</span></span>  
  
|<span data-ttu-id="5328a-113">要素</span><span class="sxs-lookup"><span data-stu-id="5328a-113">Element</span></span>|<span data-ttu-id="5328a-114">説明</span><span class="sxs-lookup"><span data-stu-id="5328a-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5328a-115">\<add></span><span class="sxs-lookup"><span data-stu-id="5328a-115">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/add-element-for-switches.md)|<span data-ttu-id="5328a-116">トレース スイッチを設定するレベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="5328a-116">Specifies the level where a trace switch is set.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5328a-117">親要素</span><span class="sxs-lookup"><span data-stu-id="5328a-117">Parent Elements</span></span>  
  
|<span data-ttu-id="5328a-118">要素</span><span class="sxs-lookup"><span data-stu-id="5328a-118">Element</span></span>|<span data-ttu-id="5328a-119">説明</span><span class="sxs-lookup"><span data-stu-id="5328a-119">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="5328a-120">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="5328a-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`System.diagnostics`|<span data-ttu-id="5328a-121">メッセージを収集、格納、およびルーティングするトレース リスナーとトレース スイッチを設定するレベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="5328a-121">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5328a-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="5328a-122">Remarks</span></span>  
 <span data-ttu-id="5328a-123">構成ファイル内に配置して、トレース スイッチのレベルを変更できます。</span><span class="sxs-lookup"><span data-stu-id="5328a-123">You can change the level of a trace switch by putting it in a configuration file.</span></span> <span data-ttu-id="5328a-124">スイッチの場合、 <xref:System.Diagnostics.BooleanSwitch>、オンとオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="5328a-124">If the switch is a <xref:System.Diagnostics.BooleanSwitch>, you can turn it on and off.</span></span> <span data-ttu-id="5328a-125">スイッチの場合、<xref:System.Diagnostics.TraceSwitch>デバッグ メッセージをアプリケーションの出力やトレースの種類を指定するためにさまざまなレベルを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="5328a-125">If the switch is a <xref:System.Diagnostics.TraceSwitch>, you can assign different levels to it to specify the types of trace or debug messages the application outputs.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5328a-126">例</span><span class="sxs-lookup"><span data-stu-id="5328a-126">Example</span></span>  
 <span data-ttu-id="5328a-127">次の例は、使用する方法を示します、 **\<切り替える >** を設定する要素、`General`トレース スイッチを<xref:System.Diagnostics.TraceLevel>レベル、および有効にする、`Data`ブール トレース スイッチ。</span><span class="sxs-lookup"><span data-stu-id="5328a-127">The following example shows how to use the **\<switch>** element to set the `General` trace switch to the <xref:System.Diagnostics.TraceLevel> level, and enable the `Data` Boolean trace switch.</span></span>  
  
```xml  
<configuration>  
   <system.diagnostics>  
      <switches>  
         <add name="General" value="4" />  
         <add name="Data" value="1" />  
      </switches>  
   </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="5328a-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="5328a-128">See Also</span></span>  
 <xref:System.Diagnostics.Switch>  
 <xref:System.Diagnostics.TraceSwitch>  
 <xref:System.Diagnostics.BooleanSwitch>  
 [<span data-ttu-id="5328a-129">トレースおよびデバッグ設定のスキーマ</span><span class="sxs-lookup"><span data-stu-id="5328a-129">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
