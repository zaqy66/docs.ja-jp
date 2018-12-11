---
title: '&lt;supportedRuntime&gt;要素'
ms.date: 04/10/2018
ms.custom: updateeachrelease
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#supportedRuntime
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/startup/supportedRuntime
helpviewer_keywords:
- supportedRuntime element
- <supportedRuntime> element
ms.assetid: 1ae16e23-afbe-4de4-b413-bc457f37b69f
author: mcleblanc
ms.author: markl
ms.openlocfilehash: b6303f765d1cc4a17fe19261c7326d8961ac1080
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53129248"
---
# <a name="ltsupportedruntimegt-element"></a><span data-ttu-id="d5e05-102">&lt;supportedRuntime&gt;要素</span><span class="sxs-lookup"><span data-stu-id="d5e05-102">&lt;supportedRuntime&gt; Element</span></span>

<span data-ttu-id="d5e05-103">アプリケーションでサポートされる共通言語ランタイムのバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="d5e05-103">Specifies which versions of the common language runtime the application supports.</span></span> <span data-ttu-id="d5e05-104">バージョン 1.1 以降の .NET Framework で構築されたすべてのアプリケーションでは、この要素を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5e05-104">This element should be used by all applications built with version 1.1 or later of the .NET Framework.</span></span>  
  
[<span data-ttu-id="d5e05-105">\<configuration></span><span class="sxs-lookup"><span data-stu-id="d5e05-105">\<configuration></span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)  
<span data-ttu-id="d5e05-106">&nbsp;&nbsp;[\<startup>](../../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md)</span><span class="sxs-lookup"><span data-stu-id="d5e05-106">&nbsp;&nbsp;[\<startup>](../../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md)</span></span>  
<span data-ttu-id="d5e05-107">&nbsp;&nbsp;&nbsp;&nbsp;**\<supportedRuntime>**</span><span class="sxs-lookup"><span data-stu-id="d5e05-107">&nbsp;&nbsp;&nbsp;&nbsp;**\<supportedRuntime>**</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d5e05-108">構文</span><span class="sxs-lookup"><span data-stu-id="d5e05-108">Syntax</span></span>
  
```xml  
<supportedRuntime version="runtime version" sku="sku id"/>  
```  
  
## <a name="attributes"></a><span data-ttu-id="d5e05-109">属性</span><span class="sxs-lookup"><span data-stu-id="d5e05-109">Attributes</span></span>
  
|<span data-ttu-id="d5e05-110">属性</span><span class="sxs-lookup"><span data-stu-id="d5e05-110">Attribute</span></span>|<span data-ttu-id="d5e05-111">説明</span><span class="sxs-lookup"><span data-stu-id="d5e05-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="d5e05-112">**version**</span><span class="sxs-lookup"><span data-stu-id="d5e05-112">**version**</span></span>|<span data-ttu-id="d5e05-113">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="d5e05-113">Optional attribute.</span></span><br /><br /> <span data-ttu-id="d5e05-114">このアプリケーションがサポートする共通言語ランタイム (CLR: Common Language Runtime) のバージョンを指定する文字列値。</span><span class="sxs-lookup"><span data-stu-id="d5e05-114">A string value that specifies the version of the common language runtime (CLR) that this application supports.</span></span> <span data-ttu-id="d5e05-115">有効な値について、`version`属性を参照してください、 [「ランタイム バージョン」の値](#version)セクション。</span><span class="sxs-lookup"><span data-stu-id="d5e05-115">For valid values of the `version` attribute, see the ["runtime version" values](#version) section.</span></span> <span data-ttu-id="d5e05-116">**注:** を通じて、.NET Framework 3.5、"*ランタイム バージョン*"値には、フォーム*メジャー*.*マイナー*.*ビルド*します。</span><span class="sxs-lookup"><span data-stu-id="d5e05-116">**Note:**  Through the .NET Framework 3.5, the "*runtime version*" value takes the form *major*.*minor*.*build*.</span></span> <span data-ttu-id="d5e05-117">[!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)] 以降では、必要となるのはメジャー バージョン番号とマイナー バージョン番号のみです (つまり、"v4.0.30319" ではなく "v4.0")。</span><span class="sxs-lookup"><span data-stu-id="d5e05-117">Beginning with the [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)], only the major and minor version numbers are required (that is, "v4.0" instead of "v4.0.30319").</span></span> <span data-ttu-id="d5e05-118">短い文字列を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d5e05-118">The shorter string is recommended.</span></span>|  
|<span data-ttu-id="d5e05-119">**sku**</span><span class="sxs-lookup"><span data-stu-id="d5e05-119">**sku**</span></span>|<span data-ttu-id="d5e05-120">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="d5e05-120">Optional attribute.</span></span><br /><br /> <span data-ttu-id="d5e05-121">在庫管理単位 (SKU) を指定する文字列の値。SKU はこのアプリケーションがサポートする .NET Framework リリースを指定します。</span><span class="sxs-lookup"><span data-stu-id="d5e05-121">A string value that specifies the stock-keeping unit (SKU), which in turn specifies which .NET Framework release this application supports.</span></span><br /><br /> <span data-ttu-id="d5e05-122">.NET Framework 4.0 以降では、`sku` 属性の使用が推奨されます。</span><span class="sxs-lookup"><span data-stu-id="d5e05-122">Starting with the .NET Framework 4.0, the use of the `sku` attribute is recommended.</span></span>  <span data-ttu-id="d5e05-123">この属性が指定される場合は、アプリケーションが対象とする .NET Framework のバージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="d5e05-123">When present, it indicates the version of the .NET Framework that the app targets.</span></span><br /><br /> <span data-ttu-id="d5e05-124">Sku 属性の有効な値は、次を参照してください。、 ["sku id"値](#sku)セクション。</span><span class="sxs-lookup"><span data-stu-id="d5e05-124">For valid values of the sku attribute, see the ["sku id" values](#sku) section.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d5e05-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="d5e05-125">Remarks</span></span>

<span data-ttu-id="d5e05-126">場合、  **\<supportedRuntime >** 要素が、アプリケーション構成ファイルに存在しない、アプリケーションをビルドするために使用するランタイムのバージョンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d5e05-126">If the **\<supportedRuntime>** element is not present in the application configuration file, the version of the runtime used to build the application is used.</span></span>  

<span data-ttu-id="d5e05-127">**\<SupportedRuntime >** 1.1 以降、ランタイムのバージョンを使用して構築されたすべてのアプリケーションで要素を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5e05-127">The **\<supportedRuntime>** element should be used by all applications built using version 1.1 or later of the runtime.</span></span> <span data-ttu-id="d5e05-128">ランタイムのバージョン 1.0 をサポートするために構築されたアプリケーションを使用する必要があります、 [ \<requiredRuntime >](../../../../../docs/framework/configure-apps/file-schema/startup/requiredruntime-element.md)要素。</span><span class="sxs-lookup"><span data-stu-id="d5e05-128">Applications built to support only version 1.0 of the runtime must use the [\<requiredRuntime>](../../../../../docs/framework/configure-apps/file-schema/startup/requiredruntime-element.md) element.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d5e05-129">使用する場合、 [CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md)構成ファイルを指定する関数を使用する必要があります、`<requiredRuntime>`ランタイムのすべてのバージョンの要素。</span><span class="sxs-lookup"><span data-stu-id="d5e05-129">If you use the [CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md) function to specify the configuration file, you must use the `<requiredRuntime>` element for all versions of the runtime.</span></span> <span data-ttu-id="d5e05-130">`<supportedRuntime>`を使用する場合、要素は無視されます[CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md)します。</span><span class="sxs-lookup"><span data-stu-id="d5e05-130">The `<supportedRuntime>` element is ignored when you use [CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md).</span></span>  
  
<span data-ttu-id="d5e05-131">NET Framework 1.1 から 3.5 までのランタイムの複数のバージョンをサポートするアプリケーションでは、ランタイムの複数のバージョンをサポートする場合は、最初の要素で最も優先度の高いバージョンを指定し、最後の要素で最も優先度の低いバージョンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5e05-131">For apps that support versions of the runtime from the .NET Framework 1.1 through 3.5, when multiple versions of the runtime are supported, the first element should specify the most preferred version of the runtime, and the last element should specify the least preferred version.</span></span> <span data-ttu-id="d5e05-132">.NET Framework 4.0 以降のバージョンをサポートするアプリケーションでは、`version` 属性は .NET Framework 4 以降のバージョンで共通の CLR バージョンを示します。`sku` 属性は、アプリケーションが対象とする単一の .NET Framework バージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="d5e05-132">For apps that support the .NET Framework 4.0 or later versions, the `version` attribute indicates the CLR version, which is common to the .NET Framework 4 and later versions, and the `sku` attribute indicates single .NET Framework version that the app targets.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d5e05-133">アプリケーションがなど、レガシ アクティブ化パスを使用するかどうか、 [CorBindToRuntimeEx 関数](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md)、それらのパスを以前のバージョンではなく、CLR の version 4 をアクティブ化して、アプリケーションが、でビルドされた場合または[!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)]依存していますが、以前のバージョンの .NET Framework でビルドされた混合モードのアセンブリでないを指定するための十分な[!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)]でサポートされているランタイムの一覧。</span><span class="sxs-lookup"><span data-stu-id="d5e05-133">If your application uses legacy activation paths, such as the [CorBindToRuntimeEx function](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md), and you want those paths to activate version 4 of the CLR instead of an earlier version, or if your application is built with the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] but has a dependency on a mixed-mode assembly built with an earlier version of the .NET Framework, it is not sufficient to specify the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] in the list of supported runtimes.</span></span> <span data-ttu-id="d5e05-134">さらに、 [ \<startup > 要素](../../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md)、構成ファイルで設定する必要があります、`useLegacyV2RuntimeActivationPolicy`属性を`true`します。</span><span class="sxs-lookup"><span data-stu-id="d5e05-134">In addition, in the [\<startup> element](../../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md) in your configuration file, you must set the `useLegacyV2RuntimeActivationPolicy` attribute to `true`.</span></span> <span data-ttu-id="d5e05-135">ただし、この属性を `true` に設定することは、以前のバージョンの .NET Framework でビルドされたすべてのコンポーネントが、それらのビルドに使用されたランタイムではなく、[!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] を使用して実行されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="d5e05-135">However, setting this attribute to `true` means that all components built with earlier versions of the .NET Framework are run using the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] instead of the runtimes they were built with.</span></span>  
  
<span data-ttu-id="d5e05-136">アプリケーションは、そのアプリケーションを実行できる .NET Framework のすべてのバージョンでテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d5e05-136">We recommend that you test applications with all the .NET Framework versions that they can run on.</span></span>  
  
<a name="version"></a>   
## <a name="runtime-version-values"></a><span data-ttu-id="d5e05-137">"ランタイム バージョン" の値</span><span class="sxs-lookup"><span data-stu-id="d5e05-137">"runtime version" values</span></span>  
<span data-ttu-id="d5e05-138">`runtime`属性が特定のアプリケーションに必要な共通言語ランタイム (CLR) バージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="d5e05-138">The `runtime` attribute specifies the Common Language Runtime (CLR) version that is required for a given application.</span></span> <span data-ttu-id="d5e05-139">すべてのバージョンの .NET Framework v4.x の指定、 `v4.0` CLR。</span><span class="sxs-lookup"><span data-stu-id="d5e05-139">Note that all .NET Framework v4.x versions specify the `v4.0` CLR.</span></span> <span data-ttu-id="d5e05-140">次の表に、有効な値、*ランタイム バージョン*の値、`version`属性。</span><span class="sxs-lookup"><span data-stu-id="d5e05-140">The following table lists valid values for the *runtime version* value of the `version` attribute.</span></span>  

|<span data-ttu-id="d5e05-141">.NET Framework のバージョン</span><span class="sxs-lookup"><span data-stu-id="d5e05-141">.NET Framework version</span></span>|<span data-ttu-id="d5e05-142">`version` 属性</span><span class="sxs-lookup"><span data-stu-id="d5e05-142">`version` attribute</span></span>|  
|----------------------------|-------------------------|  
|<span data-ttu-id="d5e05-143">1</span><span class="sxs-lookup"><span data-stu-id="d5e05-143">1.0</span></span>|<span data-ttu-id="d5e05-144">"v1.0.3705"</span><span class="sxs-lookup"><span data-stu-id="d5e05-144">"v1.0.3705"</span></span>|  
|<span data-ttu-id="d5e05-145">1.1</span><span class="sxs-lookup"><span data-stu-id="d5e05-145">1.1</span></span>|<span data-ttu-id="d5e05-146">"v1.1.4322"</span><span class="sxs-lookup"><span data-stu-id="d5e05-146">"v1.1.4322"</span></span>|  
|<span data-ttu-id="d5e05-147">2.0</span><span class="sxs-lookup"><span data-stu-id="d5e05-147">2.0</span></span>|<span data-ttu-id="d5e05-148">"v2.0.50727"</span><span class="sxs-lookup"><span data-stu-id="d5e05-148">"v2.0.50727"</span></span>|  
|<span data-ttu-id="d5e05-149">3.0</span><span class="sxs-lookup"><span data-stu-id="d5e05-149">3.0</span></span>|<span data-ttu-id="d5e05-150">"v2.0.50727"</span><span class="sxs-lookup"><span data-stu-id="d5e05-150">"v2.0.50727"</span></span>|  
|<span data-ttu-id="d5e05-151">3.5</span><span class="sxs-lookup"><span data-stu-id="d5e05-151">3.5</span></span>|<span data-ttu-id="d5e05-152">"v2.0.50727"</span><span class="sxs-lookup"><span data-stu-id="d5e05-152">"v2.0.50727"</span></span>|  
|<span data-ttu-id="d5e05-153">4.0 4.7.2</span><span class="sxs-lookup"><span data-stu-id="d5e05-153">4.0-4.7.2</span></span>|<span data-ttu-id="d5e05-154">"v4.0"</span><span class="sxs-lookup"><span data-stu-id="d5e05-154">"v4.0"</span></span>|  

<a name="sku"></a>   
## <a name="sku-id-values"></a><span data-ttu-id="d5e05-155">"sku id" の値</span><span class="sxs-lookup"><span data-stu-id="d5e05-155">"sku id" values</span></span>

<span data-ttu-id="d5e05-156">`sku`属性では、ターゲット フレームワーク モニカー (TFM) を使用して、アプリが対象とし、実行に必要とする .NET Framework のバージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="d5e05-156">The `sku` attribute uses a target framework moniker (TFM) to indicate the version of the .NET Framework that the app targets and requires to run.</span></span> <span data-ttu-id="d5e05-157">次の表に、有効な値でサポートされている、`sku`属性、.NET Framework 4 以降します。</span><span class="sxs-lookup"><span data-stu-id="d5e05-157">The following table lists valid values that are supported by the `sku` attribute, starting with the .NET Framework 4.</span></span>
  
|<span data-ttu-id="d5e05-158">.NET Framework のバージョン</span><span class="sxs-lookup"><span data-stu-id="d5e05-158">.NET Framework version</span></span>|<span data-ttu-id="d5e05-159">`sku` 属性</span><span class="sxs-lookup"><span data-stu-id="d5e05-159">`sku` attribute</span></span>|  
|----------------------------|---------------------|  
|<span data-ttu-id="d5e05-160">4.0</span><span class="sxs-lookup"><span data-stu-id="d5e05-160">4.0</span></span>|<span data-ttu-id="d5e05-161">".NETFramework,Version=v4.0"</span><span class="sxs-lookup"><span data-stu-id="d5e05-161">".NETFramework,Version=v4.0"</span></span>|  
|<span data-ttu-id="d5e05-162">4.0、Client Profile</span><span class="sxs-lookup"><span data-stu-id="d5e05-162">4.0, Client Profile</span></span>|<span data-ttu-id="d5e05-163">".NETFramework,Version=v4.0,Profile=Client"</span><span class="sxs-lookup"><span data-stu-id="d5e05-163">".NETFramework,Version=v4.0,Profile=Client"</span></span>|  
|<span data-ttu-id="d5e05-164">4.0、プラットフォームの更新プログラム 1</span><span class="sxs-lookup"><span data-stu-id="d5e05-164">4.0, platform update 1</span></span>|<span data-ttu-id="d5e05-165">".NETFramework、バージョン = v4.0.1"</span><span class="sxs-lookup"><span data-stu-id="d5e05-165">".NETFramework,Version=v4.0.1"</span></span>|  
|<span data-ttu-id="d5e05-166">4.0、Client Profile、更新プログラム 1</span><span class="sxs-lookup"><span data-stu-id="d5e05-166">4.0, Client Profile, update 1</span></span>|<span data-ttu-id="d5e05-167">".NETFramework、バージョン v4.0.1、プロファイルの = = クライアント"</span><span class="sxs-lookup"><span data-stu-id="d5e05-167">".NETFramework,Version=v4.0.1,Profile=Client"</span></span>|  
|<span data-ttu-id="d5e05-168">4.0、プラットフォームの更新プログラム 2</span><span class="sxs-lookup"><span data-stu-id="d5e05-168">4.0, platform update 2</span></span>|<span data-ttu-id="d5e05-169">".NETFramework、バージョン = v4.0.2 以降を予定"</span><span class="sxs-lookup"><span data-stu-id="d5e05-169">".NETFramework,Version=v4.0.2"</span></span>|  
|<span data-ttu-id="d5e05-170">4.0、Client Profile、更新プログラム 2</span><span class="sxs-lookup"><span data-stu-id="d5e05-170">4.0, Client Profile, update 2</span></span>|<span data-ttu-id="d5e05-171">".NETFramework、バージョン = v4.0.2 以降を予定プロファイル、クライアントを ="</span><span class="sxs-lookup"><span data-stu-id="d5e05-171">".NETFramework,Version=v4.0.2,Profile=Client"</span></span>|  
|<span data-ttu-id="d5e05-172">4.0、プラットフォームの更新プログラム 3</span><span class="sxs-lookup"><span data-stu-id="d5e05-172">4.0, platform update 3</span></span>|<span data-ttu-id="d5e05-173">".NETFramework、バージョン = v4.0.3"</span><span class="sxs-lookup"><span data-stu-id="d5e05-173">".NETFramework,Version=v4.0.3"</span></span>|  
|<span data-ttu-id="d5e05-174">4.0、Client Profile、更新プログラム 3</span><span class="sxs-lookup"><span data-stu-id="d5e05-174">4.0, Client Profile, update 3</span></span>|<span data-ttu-id="d5e05-175">".NETFramework、バージョン v4.0.3、プロファイルの = = クライアント"</span><span class="sxs-lookup"><span data-stu-id="d5e05-175">".NETFramework,Version=v4.0.3,Profile=Client"</span></span>|  
|<span data-ttu-id="d5e05-176">4.5</span><span class="sxs-lookup"><span data-stu-id="d5e05-176">4.5</span></span>|<span data-ttu-id="d5e05-177">".NETFramework,Version=v4.5"</span><span class="sxs-lookup"><span data-stu-id="d5e05-177">".NETFramework,Version=v4.5"</span></span>|  
|<span data-ttu-id="d5e05-178">4.5.1</span><span class="sxs-lookup"><span data-stu-id="d5e05-178">4.5.1</span></span>|<span data-ttu-id="d5e05-179">".NETFramework,Version=v4.5.1"</span><span class="sxs-lookup"><span data-stu-id="d5e05-179">".NETFramework,Version=v4.5.1"</span></span>|  
|<span data-ttu-id="d5e05-180">4.5.2</span><span class="sxs-lookup"><span data-stu-id="d5e05-180">4.5.2</span></span>|<span data-ttu-id="d5e05-181">".NETFramework,Version=v4.5.2"</span><span class="sxs-lookup"><span data-stu-id="d5e05-181">".NETFramework,Version=v4.5.2"</span></span>|  
|<span data-ttu-id="d5e05-182">4.6</span><span class="sxs-lookup"><span data-stu-id="d5e05-182">4.6</span></span>|<span data-ttu-id="d5e05-183">".NETFramework,Version=v4.6"</span><span class="sxs-lookup"><span data-stu-id="d5e05-183">".NETFramework,Version=v4.6"</span></span>|  
|<span data-ttu-id="d5e05-184">4.6.1</span><span class="sxs-lookup"><span data-stu-id="d5e05-184">4.6.1</span></span>|<span data-ttu-id="d5e05-185">".NETFramework,Version=v4.6.1"</span><span class="sxs-lookup"><span data-stu-id="d5e05-185">".NETFramework,Version=v4.6.1"</span></span>|  
|<span data-ttu-id="d5e05-186">4.6.2</span><span class="sxs-lookup"><span data-stu-id="d5e05-186">4.6.2</span></span>|<span data-ttu-id="d5e05-187">".NETFramework,Version=v4.6.2"</span><span class="sxs-lookup"><span data-stu-id="d5e05-187">".NETFramework,Version=v4.6.2"</span></span>|  
|<span data-ttu-id="d5e05-188">4.7</span><span class="sxs-lookup"><span data-stu-id="d5e05-188">4.7</span></span>|<span data-ttu-id="d5e05-189">".NETFramework,Version=v4.7"</span><span class="sxs-lookup"><span data-stu-id="d5e05-189">".NETFramework,Version=v4.7"</span></span>|
|<span data-ttu-id="d5e05-190">4.7.1</span><span class="sxs-lookup"><span data-stu-id="d5e05-190">4.7.1</span></span>|<span data-ttu-id="d5e05-191">".NETFramework,Version=v4.7.1"</span><span class="sxs-lookup"><span data-stu-id="d5e05-191">".NETFramework,Version=v4.7.1"</span></span>|
|<span data-ttu-id="d5e05-192">4.7.2</span><span class="sxs-lookup"><span data-stu-id="d5e05-192">4.7.2</span></span>|<span data-ttu-id="d5e05-193">".NETFramework、バージョン = v4.7.2"</span><span class="sxs-lookup"><span data-stu-id="d5e05-193">".NETFramework,Version=v4.7.2"</span></span>|

## <a name="example"></a><span data-ttu-id="d5e05-194">例</span><span class="sxs-lookup"><span data-stu-id="d5e05-194">Example</span></span>  
 <span data-ttu-id="d5e05-195">サポートされているランタイムのバージョンを構成ファイルで指定する例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d5e05-195">The following example shows how to specify the supported runtime version in a configuration file.</span></span> <span data-ttu-id="d5e05-196">構成ファイルでは、アプリが .NET Framework 4.7 を対象とすることを示します。</span><span class="sxs-lookup"><span data-stu-id="d5e05-196">The configuration file indicates that the app targets the .NET Framework 4.7.</span></span>  
  
```xml  
<configuration>  
   <startup>  
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.7" />  
   </startup>  
</configuration>  
```  
  
## <a name="configuration-file"></a><span data-ttu-id="d5e05-197">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="d5e05-197">Configuration file</span></span>

<span data-ttu-id="d5e05-198">この要素は、アプリケーション構成ファイルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="d5e05-198">This element can be used in the application configuration file.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5e05-199">関連項目</span><span class="sxs-lookup"><span data-stu-id="d5e05-199">See also</span></span>

 [<span data-ttu-id="d5e05-200">スタートアップ設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="d5e05-200">Startup Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/startup/index.md)  
 [<span data-ttu-id="d5e05-201">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="d5e05-201">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="d5e05-202">インプロセスの side-by-side 実行</span><span class="sxs-lookup"><span data-stu-id="d5e05-202">In-Process Side-by-Side Execution</span></span>](../../../../../docs/framework/deployment/in-process-side-by-side-execution.md)  
