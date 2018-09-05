---
title: '&lt;スタートアップ&gt;要素'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/startup
- http://schemas.microsoft.com/.NetConfiguration/v2.0#startup
helpviewer_keywords:
- container tags, <startup> element
- <startup> element
- startup element
ms.assetid: 536acfd8-f827-452f-838a-e14fa3b87621
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 4d39dc28082fbed932a60228ac216f2f700c2e9f
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43734708"
---
# <a name="ltstartupgt-element"></a><span data-ttu-id="a6938-102">&lt;スタートアップ&gt;要素</span><span class="sxs-lookup"><span data-stu-id="a6938-102">&lt;startup&gt; Element</span></span>
<span data-ttu-id="a6938-103">共通言語ランタイムのスタートアップの情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="a6938-103">Specifies common language runtime startup information.</span></span>  
  
 <span data-ttu-id="a6938-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="a6938-104">\<configuration></span></span>  
<span data-ttu-id="a6938-105">\<startup></span><span class="sxs-lookup"><span data-stu-id="a6938-105">\<startup></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a6938-106">構文</span><span class="sxs-lookup"><span data-stu-id="a6938-106">Syntax</span></span>  
  
```xml  
<startup useLegacyV2RuntimeActivationPolicy="true|false" >   
</startup>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a6938-107">属性および要素</span><span class="sxs-lookup"><span data-stu-id="a6938-107">Attributes and Elements</span></span>  
 <span data-ttu-id="a6938-108">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="a6938-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a6938-109">属性</span><span class="sxs-lookup"><span data-stu-id="a6938-109">Attributes</span></span>  
  
|<span data-ttu-id="a6938-110">属性</span><span class="sxs-lookup"><span data-stu-id="a6938-110">Attribute</span></span>|<span data-ttu-id="a6938-111">説明</span><span class="sxs-lookup"><span data-stu-id="a6938-111">Description</span></span>|  
|---------------|-----------------|  
|`useLegacyV2RuntimeActivationPolicy`|<span data-ttu-id="a6938-112">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="a6938-112">Optional attribute.</span></span><br /><br /> <span data-ttu-id="a6938-113">有効にするかどうかを指定します、[!INCLUDE[dnprdnext](../../../../../includes/dnprdnext-md.md)]ランタイムのアクティブ化ポリシーを使用するか、[!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)]アクティブ化ポリシー。</span><span class="sxs-lookup"><span data-stu-id="a6938-113">Specifies whether to enable the [!INCLUDE[dnprdnext](../../../../../includes/dnprdnext-md.md)] runtime activation policy or to use the [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)] activation policy.</span></span>|  
  
## <a name="uselegacyv2runtimeactivationpolicy-attribute"></a><span data-ttu-id="a6938-114">useLegacyV2RuntimeActivationPolicy 属性</span><span class="sxs-lookup"><span data-stu-id="a6938-114">useLegacyV2RuntimeActivationPolicy Attribute</span></span>  
  
|<span data-ttu-id="a6938-115">[値]</span><span class="sxs-lookup"><span data-stu-id="a6938-115">Value</span></span>|<span data-ttu-id="a6938-116">説明</span><span class="sxs-lookup"><span data-stu-id="a6938-116">Description</span></span>|  
|-----------|-----------------|  
|`true`|<span data-ttu-id="a6938-117">有効にする[!INCLUDE[dnprdnext](../../../../../includes/dnprdnext-md.md)]ランタイムのアクティブ化ポリシーは、レガシ ランタイムのアクティブ化の手法をバインドする、選択したランタイムの (など、 [CorBindToRuntimeEx 関数](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md))、ランタイムの代わりに、構成ファイルから選択するにはCLR バージョン 2.0 では、それらを上限します。</span><span class="sxs-lookup"><span data-stu-id="a6938-117">Enable [!INCLUDE[dnprdnext](../../../../../includes/dnprdnext-md.md)] runtime activation policy for the chosen runtime, which is to bind legacy runtime activation techniques (such as the [CorBindToRuntimeEx function](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md)) to the runtime chosen from the configuration file instead of capping them at CLR version 2.0.</span></span> <span data-ttu-id="a6938-118">したがって、CLR バージョン 4 以降を構成ファイルから選択した場合、.NET Framework の以前のバージョンで作成された混合モードのアセンブリは、選択した CLR バージョンで読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="a6938-118">Thus, if CLR version 4 or later is chosen from the configuration file, mixed-mode assemblies created with earlier versions of the .NET Framework are loaded with the chosen CLR version.</span></span> <span data-ttu-id="a6938-119">この値の設定も、実質的にインプロセスでサイド バイ サイドでの機能を無効にする、同じプロセスに読み込みの CLR バージョン 1.1 または CLR バージョン 2.0 はできません。</span><span class="sxs-lookup"><span data-stu-id="a6938-119">Setting this value prevents CLR version 1.1 or CLR version 2.0 from loading into the same process, effectively disabling the in-process side-by-side feature.</span></span>|  
|`false`|<span data-ttu-id="a6938-120">既定のアクティブ化ポリシーを使用して、[!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)]レガシ ランタイムをプロセスに CLR 1.1 または 2.0 バージョンを読み込む手法をアクティブ化を許可するが、後で対象とします。</span><span class="sxs-lookup"><span data-stu-id="a6938-120">Use the default activation policy for the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] and later, which is to allow legacy runtime activation techniques to load CLR version 1.1 or 2.0 into the process.</span></span> <span data-ttu-id="a6938-121">この値を設定すると、混合モードのアセンブリから、またはそれ以降、.NET Framework 4 でビルドされた場合を除きに、.NET Framework 4 またはそれ以降の読み込みができません。</span><span class="sxs-lookup"><span data-stu-id="a6938-121">Setting this value prevents mixed-mode assemblies from loading into the .NET Framework 4 or later unless they were built with the .NET Framework 4 or later.</span></span> <span data-ttu-id="a6938-122">この値が既定値です。</span><span class="sxs-lookup"><span data-stu-id="a6938-122">This value is the default.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a6938-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a6938-123">Child Elements</span></span>  
  
|<span data-ttu-id="a6938-124">要素</span><span class="sxs-lookup"><span data-stu-id="a6938-124">Element</span></span>|<span data-ttu-id="a6938-125">説明</span><span class="sxs-lookup"><span data-stu-id="a6938-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a6938-126">\<requiredRuntime></span><span class="sxs-lookup"><span data-stu-id="a6938-126">\<requiredRuntime></span></span>](../../../../../docs/framework/configure-apps/file-schema/startup/requiredruntime-element.md)|<span data-ttu-id="a6938-127">バージョン 1.0 の共通言語ランタイムのみがアプリケーションでサポートされることを指定します。</span><span class="sxs-lookup"><span data-stu-id="a6938-127">Specifies that the application supports only version 1.0 of the common language runtime.</span></span> <span data-ttu-id="a6938-128">ランタイム バージョン 1.1 以降でビルドされたアプリケーションを使用する必要があります、  **\<supportedRuntime >** 要素。</span><span class="sxs-lookup"><span data-stu-id="a6938-128">Applications built with runtime version 1.1 or later should use the **\<supportedRuntime>** element.</span></span>|  
|[<span data-ttu-id="a6938-129">\<supportedRuntime></span><span class="sxs-lookup"><span data-stu-id="a6938-129">\<supportedRuntime></span></span>](../../../../../docs/framework/configure-apps/file-schema/startup/supportedruntime-element.md)|<span data-ttu-id="a6938-130">アプリケーションでサポートされる共通言語ランタイムのバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="a6938-130">Specifies which versions of the common language runtime the application supports.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a6938-131">親要素</span><span class="sxs-lookup"><span data-stu-id="a6938-131">Parent Elements</span></span>  
  
|<span data-ttu-id="a6938-132">要素</span><span class="sxs-lookup"><span data-stu-id="a6938-132">Element</span></span>|<span data-ttu-id="a6938-133">説明</span><span class="sxs-lookup"><span data-stu-id="a6938-133">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="a6938-134">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="a6938-134">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a6938-135">Remarks</span><span class="sxs-lookup"><span data-stu-id="a6938-135">Remarks</span></span>  
 <span data-ttu-id="a6938-136">**\<SupportedRuntime >** 1.1 以降、ランタイムのバージョンを使用して構築されたすべてのアプリケーションで要素を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6938-136">The **\<supportedRuntime>** element should be used by all applications built using version 1.1 or later of the runtime.</span></span> <span data-ttu-id="a6938-137">ランタイムのバージョン 1.0 をサポートするために構築されたアプリケーションを使用する必要があります、  **\<requiredRuntime >** 要素。</span><span class="sxs-lookup"><span data-stu-id="a6938-137">Applications built to support only version 1.0 of the runtime must use the **\<requiredRuntime>** element.</span></span>  
  
 <span data-ttu-id="a6938-138">Microsoft Internet Explorer でホストされるアプリケーションのスタートアップ コードは無視されます、 **\<スタートアップ >** 要素とその子要素。</span><span class="sxs-lookup"><span data-stu-id="a6938-138">The startup code for an application hosted in Microsoft Internet Explorer ignores the **\<startup>** element and its child elements.</span></span>  
  
## <a name="the-uselegacyv2runtimeactivationpolicy-attribute"></a><span data-ttu-id="a6938-139">UseLegacyV2RuntimeActivationPolicy 属性</span><span class="sxs-lookup"><span data-stu-id="a6938-139">The useLegacyV2RuntimeActivationPolicy Attribute</span></span>  
 <span data-ttu-id="a6938-140">この属性は、アプリケーションなどに、レガシ アクティブ化パスを使用する場合に便利ですが、 [CorBindToRuntimeEx 関数](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md)、それらのパスを以前のバージョンではなく、CLR の version 4 をアクティブ化して、アプリケーションがある場合、または構築された、[!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)]が以前のバージョンの .NET Framework でビルドされた混合モードのアセンブリに依存しています。</span><span class="sxs-lookup"><span data-stu-id="a6938-140">This attribute is useful if your application uses legacy activation paths, such as the [CorBindToRuntimeEx function](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md), and you want those paths to activate version 4 of the CLR instead of an earlier version, or if your application is built with the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] but has a dependency on a mixed-mode assembly built with an earlier version of the .NET Framework.</span></span> <span data-ttu-id="a6938-141">そのようなシナリオで、属性を設定して`true`します。</span><span class="sxs-lookup"><span data-stu-id="a6938-141">In those scenarios, set the attribute to `true`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a6938-142">属性を設定`true`CLR version 1.1 または CLR バージョン 2.0 が実質的にインプロセスでサイド バイ サイドでの機能を無効にする、同じプロセスに読み込まれなくなります (を参照してください[COM 相互運用機能のサイド バイ サイドで実行](https://msdn.microsoft.com/library/4302318c-3586-49bf-8620-b9a39cdf4a32))。</span><span class="sxs-lookup"><span data-stu-id="a6938-142">Setting the attribute to `true` prevents CLR version 1.1 or CLR version 2.0 from loading into the same process, effectively disabling the in-process side-by-side feature (see [Side-by-Side Execution for COM Interop](https://msdn.microsoft.com/library/4302318c-3586-49bf-8620-b9a39cdf4a32)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="a6938-143">例</span><span class="sxs-lookup"><span data-stu-id="a6938-143">Example</span></span>  
 <span data-ttu-id="a6938-144">次の例では、構成ファイルでランタイムのバージョンを指定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a6938-144">The following example shows how to specify the runtime version in a configuration file.</span></span>  
  
```xml  
<!-- When used with version 1.0 of the .NET Framework runtime -->  
<configuration>  
   <startup>  
      <requiredRuntime version="v1.0.3705" safemode="true"/>  
   </startup>  
</configuration>  
<!-- When used with version 1.1 (or later) of the runtime -->  
<configuration>  
   <startup>  
      <supportedRuntime version="v1.1.4322"/>  
      <supportedRuntime version="v1.0.3705"/>  
   </startup>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="a6938-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6938-145">See Also</span></span>  
 [<span data-ttu-id="a6938-146">スタートアップ設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="a6938-146">Startup Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/startup/index.md)  
 [<span data-ttu-id="a6938-147">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="a6938-147">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="a6938-148">\<PaveOver> 使用するランタイム バージョンの指定</span><span class="sxs-lookup"><span data-stu-id="a6938-148">\<PaveOver> Specifying Which Runtime Version to Use</span></span>](https://msdn.microsoft.com/library/c376208d-980d-42b4-865b-fbe0d9cc97c2)  
 [<span data-ttu-id="a6938-149">COM 相互運用機能のサイド バイ サイドで実行</span><span class="sxs-lookup"><span data-stu-id="a6938-149">Side-by-Side Execution for COM Interop</span></span>](https://msdn.microsoft.com/library/4302318c-3586-49bf-8620-b9a39cdf4a32)  
 [<span data-ttu-id="a6938-150">インプロセスの side-by-side 実行</span><span class="sxs-lookup"><span data-stu-id="a6938-150">In-Process Side-by-Side Execution</span></span>](../../../../../docs/framework/deployment/in-process-side-by-side-execution.md)
