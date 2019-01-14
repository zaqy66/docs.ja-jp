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
ms.openlocfilehash: 82ee7b163efcefae0f2a169b74d29ea4c9f5398a
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/11/2019
ms.locfileid: "54222741"
---
# <a name="ltstartupgt-element"></a><span data-ttu-id="21956-102">&lt;スタートアップ&gt;要素</span><span class="sxs-lookup"><span data-stu-id="21956-102">&lt;startup&gt; element</span></span>

<span data-ttu-id="21956-103">共通言語ランタイムのスタートアップの情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="21956-103">Specifies common language runtime startup information.</span></span>

 <span data-ttu-id="21956-104">\<configuration >\<スタートアップ ></span><span class="sxs-lookup"><span data-stu-id="21956-104">\<configuration> \<startup></span></span>

## <a name="syntax"></a><span data-ttu-id="21956-105">構文</span><span class="sxs-lookup"><span data-stu-id="21956-105">Syntax</span></span>

```xml
<startup useLegacyV2RuntimeActivationPolicy="true|false" > 
</startup>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="21956-106">属性と要素</span><span class="sxs-lookup"><span data-stu-id="21956-106">Attributes and elements</span></span>

 <span data-ttu-id="21956-107">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="21956-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="21956-108">属性</span><span class="sxs-lookup"><span data-stu-id="21956-108">Attributes</span></span>

|<span data-ttu-id="21956-109">属性</span><span class="sxs-lookup"><span data-stu-id="21956-109">Attribute</span></span>|<span data-ttu-id="21956-110">説明</span><span class="sxs-lookup"><span data-stu-id="21956-110">Description</span></span>|
|---------------|-----------------|
|`useLegacyV2RuntimeActivationPolicy`|<span data-ttu-id="21956-111">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="21956-111">Optional attribute.</span></span><br /><br /> <span data-ttu-id="21956-112">有効にするかどうかを指定します、[!INCLUDE[dnprdnext](../../../../../includes/dnprdnext-md.md)]ランタイムのアクティブ化ポリシーを使用するか、[!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)]アクティブ化ポリシー。</span><span class="sxs-lookup"><span data-stu-id="21956-112">Specifies whether to enable the [!INCLUDE[dnprdnext](../../../../../includes/dnprdnext-md.md)] runtime activation policy or to use the [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)] activation policy.</span></span>|

## <a name="uselegacyv2runtimeactivationpolicy-attribute"></a><span data-ttu-id="21956-113">useLegacyV2RuntimeActivationPolicy 属性</span><span class="sxs-lookup"><span data-stu-id="21956-113">useLegacyV2RuntimeActivationPolicy attribute</span></span>

|<span data-ttu-id="21956-114">[値]</span><span class="sxs-lookup"><span data-stu-id="21956-114">Value</span></span>|<span data-ttu-id="21956-115">説明</span><span class="sxs-lookup"><span data-stu-id="21956-115">Description</span></span>|
|-----------|-----------------|
|`true`|<span data-ttu-id="21956-116">有効にする[!INCLUDE[dnprdnext](../../../../../includes/dnprdnext-md.md)]ランタイムのアクティブ化ポリシーは、レガシ ランタイムのアクティブ化の手法をバインドする、選択したランタイムの (など、 [CorBindToRuntimeEx 関数](../../../unmanaged-api/hosting/corbindtoruntimeex-function.md))、ランタイムの代わりに、構成ファイルから選択するにはCLR バージョン 2.0 では、それらを上限します。</span><span class="sxs-lookup"><span data-stu-id="21956-116">Enable [!INCLUDE[dnprdnext](../../../../../includes/dnprdnext-md.md)] runtime activation policy for the chosen runtime, which is to bind legacy runtime activation techniques (such as the [CorBindToRuntimeEx function](../../../unmanaged-api/hosting/corbindtoruntimeex-function.md)) to the runtime chosen from the configuration file instead of capping them at CLR version 2.0.</span></span> <span data-ttu-id="21956-117">したがって、CLR バージョン 4 以降を構成ファイルから選択した場合、.NET Framework の以前のバージョンで作成された混合モードのアセンブリは、選択した CLR バージョンで読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="21956-117">Thus, if CLR version 4 or later is chosen from the configuration file, mixed-mode assemblies created with earlier versions of the .NET Framework are loaded with the chosen CLR version.</span></span> <span data-ttu-id="21956-118">この値の設定も、実質的にインプロセスでサイド バイ サイドでの機能を無効にする、同じプロセスに読み込みの CLR バージョン 1.1 または CLR バージョン 2.0 はできません。</span><span class="sxs-lookup"><span data-stu-id="21956-118">Setting this value prevents CLR version 1.1 or CLR version 2.0 from loading into the same process, effectively disabling the in-process side-by-side feature.</span></span>|
|`false`|<span data-ttu-id="21956-119">既定のアクティブ化ポリシーを使用して、[!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)]レガシ ランタイムをプロセスに CLR 1.1 または 2.0 バージョンを読み込む手法をアクティブ化を許可するが、後で対象とします。</span><span class="sxs-lookup"><span data-stu-id="21956-119">Use the default activation policy for the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] and later, which is to allow legacy runtime activation techniques to load CLR version 1.1 or 2.0 into the process.</span></span> <span data-ttu-id="21956-120">この値を設定すると、混合モードのアセンブリから、またはそれ以降、.NET Framework 4 でビルドされた場合を除きに、.NET Framework 4 またはそれ以降の読み込みができません。</span><span class="sxs-lookup"><span data-stu-id="21956-120">Setting this value prevents mixed-mode assemblies from loading into the .NET Framework 4 or later unless they were built with the .NET Framework 4 or later.</span></span> <span data-ttu-id="21956-121">この値が既定値です。</span><span class="sxs-lookup"><span data-stu-id="21956-121">This value is the default.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="21956-122">子要素</span><span class="sxs-lookup"><span data-stu-id="21956-122">Child elements</span></span>

|<span data-ttu-id="21956-123">要素</span><span class="sxs-lookup"><span data-stu-id="21956-123">Element</span></span>|<span data-ttu-id="21956-124">説明</span><span class="sxs-lookup"><span data-stu-id="21956-124">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="21956-125">\<requiredRuntime></span><span class="sxs-lookup"><span data-stu-id="21956-125">\<requiredRuntime></span></span>](requiredruntime-element.md)|<span data-ttu-id="21956-126">バージョン 1.0 の共通言語ランタイムのみがアプリケーションでサポートされることを指定します。</span><span class="sxs-lookup"><span data-stu-id="21956-126">Specifies that the application supports only version 1.0 of the common language runtime.</span></span> <span data-ttu-id="21956-127">ランタイム バージョン 1.1 以降でビルドされたアプリケーションを使用する必要があります、  **\<supportedRuntime >** 要素。</span><span class="sxs-lookup"><span data-stu-id="21956-127">Applications built with runtime version 1.1 or later should use the **\<supportedRuntime>** element.</span></span>|
|[<span data-ttu-id="21956-128">\<supportedRuntime></span><span class="sxs-lookup"><span data-stu-id="21956-128">\<supportedRuntime></span></span>](supportedruntime-element.md)|<span data-ttu-id="21956-129">アプリケーションでサポートされる共通言語ランタイムのバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="21956-129">Specifies which versions of the common language runtime the application supports.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="21956-130">親要素</span><span class="sxs-lookup"><span data-stu-id="21956-130">Parent elements</span></span>

|<span data-ttu-id="21956-131">要素</span><span class="sxs-lookup"><span data-stu-id="21956-131">Element</span></span>|<span data-ttu-id="21956-132">説明</span><span class="sxs-lookup"><span data-stu-id="21956-132">Description</span></span>|
|-------------|-----------------|
|`configuration`|<span data-ttu-id="21956-133">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="21956-133">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|

## <a name="remarks"></a><span data-ttu-id="21956-134">Remarks</span><span class="sxs-lookup"><span data-stu-id="21956-134">Remarks</span></span>

 <span data-ttu-id="21956-135"> *\*\<SupportedRuntime >** 1.1 以降、ランタイムのバージョンを使用して構築されたすべてのアプリケーションで要素を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21956-135">The **\<supportedRuntime>** element should be used by all applications built using version 1.1 or later of the runtime.</span></span> <span data-ttu-id="21956-136">ランタイムのバージョン 1.0 をサポートするために構築されたアプリケーションを使用する必要があります、  **\<requiredRuntime >** 要素。</span><span class="sxs-lookup"><span data-stu-id="21956-136">Applications built to support only version 1.0 of the runtime must use the **\<requiredRuntime>** element.</span></span>

 <span data-ttu-id="21956-137">Microsoft Internet Explorer でホストされるアプリケーションのスタートアップ コードは無視されます、 **\<スタートアップ >** 要素とその子要素。</span><span class="sxs-lookup"><span data-stu-id="21956-137">The startup code for an application hosted in Microsoft Internet Explorer ignores the **\<startup>** element and its child elements.</span></span>

## <a name="the-uselegacyv2runtimeactivationpolicy-attribute"></a><span data-ttu-id="21956-138">UseLegacyV2RuntimeActivationPolicy 属性</span><span class="sxs-lookup"><span data-stu-id="21956-138">The useLegacyV2RuntimeActivationPolicy attribute</span></span>

 <span data-ttu-id="21956-139">この属性は、アプリケーションなどに、レガシ アクティブ化パスを使用する場合に便利ですが、 [CorBindToRuntimeEx 関数](../../../unmanaged-api/hosting/corbindtoruntimeex-function.md)、それらのパスを以前のバージョンではなく、CLR の version 4 をアクティブ化して、アプリケーションがある場合、または構築された、[!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)]が以前のバージョンの .NET Framework でビルドされた混合モードのアセンブリに依存しています。</span><span class="sxs-lookup"><span data-stu-id="21956-139">This attribute is useful if your application uses legacy activation paths, such as the [CorBindToRuntimeEx function](../../../unmanaged-api/hosting/corbindtoruntimeex-function.md), and you want those paths to activate version 4 of the CLR instead of an earlier version, or if your application is built with the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] but has a dependency on a mixed-mode assembly built with an earlier version of the .NET Framework.</span></span> <span data-ttu-id="21956-140">そのようなシナリオで、属性を設定して`true`します。</span><span class="sxs-lookup"><span data-stu-id="21956-140">In those scenarios, set the attribute to `true`.</span></span>

> [!NOTE]
> <span data-ttu-id="21956-141">属性を設定`true`CLR version 1.1 または CLR バージョン 2.0 が実質的にインプロセスでサイド バイ サイドでの機能を無効にする、同じプロセスに読み込まれなくなります (を参照してください[COM 相互運用機能のサイド バイ サイドで実行](https://msdn.microsoft.com/library/4302318c-3586-49bf-8620-b9a39cdf4a32))。</span><span class="sxs-lookup"><span data-stu-id="21956-141">Setting the attribute to `true` prevents CLR version 1.1 or CLR version 2.0 from loading into the same process, effectively disabling the in-process side-by-side feature (see [Side-by-Side Execution for COM Interop](https://msdn.microsoft.com/library/4302318c-3586-49bf-8620-b9a39cdf4a32)).</span></span>

## <a name="example"></a><span data-ttu-id="21956-142">例</span><span class="sxs-lookup"><span data-stu-id="21956-142">Example</span></span>

 <span data-ttu-id="21956-143">次の例では、構成ファイルでランタイムのバージョンを指定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="21956-143">The following example shows how to specify the runtime version in a configuration file.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="21956-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="21956-144">See also</span></span>

- [<span data-ttu-id="21956-145">スタートアップ設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="21956-145">Startup Settings Schema</span></span>](index.md)
- [<span data-ttu-id="21956-146">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="21956-146">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="21956-147">方法: .NET Framework 4 またはそれ以降のバージョンをサポートするアプリを構成します。</span><span class="sxs-lookup"><span data-stu-id="21956-147">How to: Configure an app to support .NET Framework 4 or later versions</span></span>](../../../migration-guide/how-to-configure-an-app-to-support-net-framework-4-or-4-5.md)
- [<span data-ttu-id="21956-148">COM 相互運用機能のサイド バイ サイドで実行</span><span class="sxs-lookup"><span data-stu-id="21956-148">Side-by-Side Execution for COM Interop</span></span>](https://msdn.microsoft.com/library/4302318c-3586-49bf-8620-b9a39cdf4a32)
- [<span data-ttu-id="21956-149">インプロセスの side-by-side 実行</span><span class="sxs-lookup"><span data-stu-id="21956-149">In-Process Side-by-Side Execution</span></span>](../../../deployment/in-process-side-by-side-execution.md)