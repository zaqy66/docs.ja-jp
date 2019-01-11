---
title: '&lt;requiredRuntime&gt;要素'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#requiredRuntime
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/startup/requiredRuntime
helpviewer_keywords:
- requiredRuntime element
- <requiredRuntime> element
- container tags, <requiredRuntime> element
ms.assetid: 9fa1639e-beb8-43be-b7a4-12f7b229c34b
ms.openlocfilehash: 66de3e30ce862cd317e80ea267bf22ce728aca82
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/11/2019
ms.locfileid: "54222130"
---
# <a name="ltrequiredruntimegt-element"></a><span data-ttu-id="e6b1f-102">&lt;requiredRuntime&gt;要素</span><span class="sxs-lookup"><span data-stu-id="e6b1f-102">&lt;requiredRuntime&gt; element</span></span>

<span data-ttu-id="e6b1f-103">バージョン 1.0 の共通言語ランタイムのみがアプリケーションでサポートされることを指定します。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-103">Specifies that the application supports only version 1.0 of the common language runtime.</span></span> <span data-ttu-id="e6b1f-104">この要素は非推奨し、使用できなくする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-104">This element is deprecated and should no longer be used.</span></span> <span data-ttu-id="e6b1f-105">[ `supportedRuntime` ](supportedruntime-element.md)要素を代わりに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-105">The [`supportedRuntime`](supportedruntime-element.md) element should be used instead.</span></span>

<span data-ttu-id="e6b1f-106">\<configuration >\<スタートアップ > \<requiredRuntime ></span><span class="sxs-lookup"><span data-stu-id="e6b1f-106">\<configuration> \<startup> \<requiredRuntime></span></span>

## <a name="syntax"></a><span data-ttu-id="e6b1f-107">構文</span><span class="sxs-lookup"><span data-stu-id="e6b1f-107">Syntax</span></span>

```xml
   <requiredRuntime  
version="runtime version"
safemode="true|false"/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="e6b1f-108">属性と要素</span><span class="sxs-lookup"><span data-stu-id="e6b1f-108">Attributes and elements</span></span>

<span data-ttu-id="e6b1f-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-109">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="e6b1f-110">属性</span><span class="sxs-lookup"><span data-stu-id="e6b1f-110">Attributes</span></span>

|<span data-ttu-id="e6b1f-111">属性</span><span class="sxs-lookup"><span data-stu-id="e6b1f-111">Attribute</span></span>|<span data-ttu-id="e6b1f-112">説明</span><span class="sxs-lookup"><span data-stu-id="e6b1f-112">Description</span></span>|
|---------------|-----------------|
|`version`|<span data-ttu-id="e6b1f-113">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-113">Optional attribute.</span></span><br /><br /> <span data-ttu-id="e6b1f-114">このアプリケーションがサポートする .NET Framework のバージョンを指定する文字列値。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-114">A string value that specifies the version of the .NET Framework that this application supports.</span></span> <span data-ttu-id="e6b1f-115">文字列値は、.NET Framework のインストールのルート下にあるディレクトリ名と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-115">The string value must match the directory name found under the .NET Framework installation root.</span></span> <span data-ttu-id="e6b1f-116">文字列値の内容は解析されません。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-116">The contents of the string value are not parsed.</span></span>|
|`safemode`|<span data-ttu-id="e6b1f-117">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-117">Optional attribute.</span></span><br /><br /> <span data-ttu-id="e6b1f-118">ランタイム スタートアップ コードがランタイム バージョンを確認するレジストリを検索するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-118">Specifies whether the runtime startup code searches the registry to determine the runtime version.</span></span>|

## <a name="safemode-attribute"></a><span data-ttu-id="e6b1f-119">セーフ モード属性</span><span class="sxs-lookup"><span data-stu-id="e6b1f-119">safemode attribute</span></span>

|<span data-ttu-id="e6b1f-120">[値]</span><span class="sxs-lookup"><span data-stu-id="e6b1f-120">Value</span></span>|<span data-ttu-id="e6b1f-121">説明</span><span class="sxs-lookup"><span data-stu-id="e6b1f-121">Description</span></span>|
|-----------|-----------------|
|`false`|<span data-ttu-id="e6b1f-122">ランタイム スタートアップ コードは、レジストリを検索します。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-122">The runtime startup code looks in the registry.</span></span> <span data-ttu-id="e6b1f-123">これが既定値です。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-123">This is the default value.</span></span>|
|`true`|<span data-ttu-id="e6b1f-124">ランタイム スタートアップ コードは、レジストリでは検索しません。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-124">The runtime startup code does not look in the registry.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="e6b1f-125">子要素</span><span class="sxs-lookup"><span data-stu-id="e6b1f-125">Child elements</span></span>

<span data-ttu-id="e6b1f-126">なし。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-126">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="e6b1f-127">親要素</span><span class="sxs-lookup"><span data-stu-id="e6b1f-127">Parent elements</span></span>

|<span data-ttu-id="e6b1f-128">要素</span><span class="sxs-lookup"><span data-stu-id="e6b1f-128">Element</span></span>|<span data-ttu-id="e6b1f-129">説明</span><span class="sxs-lookup"><span data-stu-id="e6b1f-129">Description</span></span>|
|-------------|-----------------|
|`configuration`|<span data-ttu-id="e6b1f-130">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-130">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|
|`startup`|<span data-ttu-id="e6b1f-131">`<requiredRuntime>`要素を含んでいます。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-131">Contains the `<requiredRuntime>` element.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e6b1f-132">Remarks</span><span class="sxs-lookup"><span data-stu-id="e6b1f-132">Remarks</span></span>
 <span data-ttu-id="e6b1f-133">ランタイムのバージョン 1.0 をサポートするために構築されたアプリケーションを使用する必要があります、`<requiredRuntime>`要素。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-133">Applications built to support only version 1.0 of the runtime must use the `<requiredRuntime>` element.</span></span> <span data-ttu-id="e6b1f-134">1.1 以降、ランタイムのバージョンを使用して構築されたアプリケーションを使用する必要があります、`<supportedRuntime>`要素。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-134">Applications built using version 1.1 or later of the runtime must use the `<supportedRuntime>` element.</span></span>

> [!NOTE]
> <span data-ttu-id="e6b1f-135">使用する場合、 [CorBindToRuntimeByCfg](../../../unmanaged-api/hosting/corbindtoruntimebycfg-function.md)構成ファイルを指定する関数を使用する必要があります、`<requiredRuntime>`ランタイムのすべてのバージョンの要素。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-135">If you use the [CorBindToRuntimeByCfg](../../../unmanaged-api/hosting/corbindtoruntimebycfg-function.md) function to specify the configuration file, you must use the `<requiredRuntime>` element for all versions of the runtime.</span></span> <span data-ttu-id="e6b1f-136">`<supportedRuntime>`を使用する場合、要素は無視されます[CorBindToRuntimeByCfg](../../../unmanaged-api/hosting/corbindtoruntimebycfg-function.md)します。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-136">The `<supportedRuntime>` element is ignored when you use [CorBindToRuntimeByCfg](../../../unmanaged-api/hosting/corbindtoruntimebycfg-function.md).</span></span>

 <span data-ttu-id="e6b1f-137">`version`属性文字列は指定されたバージョンの .NET Framework のインストール フォルダーの名前と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-137">The `version` attribute string must match the installation folder name for the specified version of the .NET Framework.</span></span> <span data-ttu-id="e6b1f-138">この文字列は解釈されません。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-138">This string is not interpreted.</span></span> <span data-ttu-id="e6b1f-139">ランタイム スタートアップ コードが一致するフォルダーを見つけられない場合、ランタイムが読み込まれていません。スタートアップ コードでは、エラー メッセージが表示され、終了します。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-139">If the runtime startup code does not find a matching folder, the runtime is not loaded; the startup code shows an error message and quits.</span></span>

> [!NOTE]
> <span data-ttu-id="e6b1f-140">Microsoft Internet Explorer でホストされているアプリケーションのスタートアップ コードは無視されます、`<requiredRuntime>`要素。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-140">The startup code for an application that is hosted in Microsoft Internet Explorer ignores the `<requiredRuntime>` element.</span></span>

## <a name="example"></a><span data-ttu-id="e6b1f-141">例</span><span class="sxs-lookup"><span data-stu-id="e6b1f-141">Example</span></span>

<span data-ttu-id="e6b1f-142">次の例では、構成ファイルでランタイムのバージョンを指定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-142">The following example shows how to specify the runtime version in a configuration file.</span></span>

```xml
<configuration>
   <startup>
      <requiredRuntime version="v1.0.3705" safemode="true"/>
   </startup>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="e6b1f-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="e6b1f-143">See also</span></span>

- [<span data-ttu-id="e6b1f-144">スタートアップ設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="e6b1f-144">Startup Settings Schema</span></span>](index.md)
- [<span data-ttu-id="e6b1f-145">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="e6b1f-145">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="e6b1f-146">方法: .NET Framework 4 またはそれ以降のバージョンをサポートするアプリを構成します。</span><span class="sxs-lookup"><span data-stu-id="e6b1f-146">How to: Configure an app to support .NET Framework 4 or later versions</span></span>](../../../migration-guide/how-to-configure-an-app-to-support-net-framework-4-or-4-5.md)