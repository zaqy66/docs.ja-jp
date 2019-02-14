---
title: <add>appSettings&gt;の<appSettings>add&gt;要素
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/appSettings/add
helpviewer_keywords:
- add Element
- <add> Element
ms.assetid: 8734efdc-00f6-4a65-bba6-084c5bc65246
author: guardrex
ms.author: mairaw
ms.openlocfilehash: dde773dc722cf75da9d922ccf28af4bf4a09636c
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55277473"
---
# <a name="add-element-for-appsettings"></a><span data-ttu-id="41c16-102">\<appSettings>の\<add>要素</span><span class="sxs-lookup"><span data-stu-id="41c16-102">\<add> element for \<appSettings></span></span>

<span data-ttu-id="41c16-103">カスタム アプリケーション設定を追加します。</span><span class="sxs-lookup"><span data-stu-id="41c16-103">Adds a custom application setting.</span></span>

<span data-ttu-id="41c16-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="41c16-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="41c16-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="41c16-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span></span>  
<span data-ttu-id="41c16-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**</span><span class="sxs-lookup"><span data-stu-id="41c16-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**</span></span>

## <a name="syntax"></a><span data-ttu-id="41c16-107">構文</span><span class="sxs-lookup"><span data-stu-id="41c16-107">Syntax</span></span>

```xml
<appSettings>
  <add key="Key of custom setting" value="Value of custom setting" />
</appSettings>
```

## <a name="attributes"></a><span data-ttu-id="41c16-108">属性</span><span class="sxs-lookup"><span data-stu-id="41c16-108">Attributes</span></span>

|           | <span data-ttu-id="41c16-109">説明</span><span class="sxs-lookup"><span data-stu-id="41c16-109">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="41c16-110">**key**</span><span class="sxs-lookup"><span data-stu-id="41c16-110">**key**</span></span>   | <span data-ttu-id="41c16-111">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="41c16-111">Required attribute.</span></span><br><br><span data-ttu-id="41c16-112">追加するキーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="41c16-112">Specifies the name of the key to add.</span></span> |
| <span data-ttu-id="41c16-113">**value**</span><span class="sxs-lookup"><span data-stu-id="41c16-113">**value**</span></span> | <span data-ttu-id="41c16-114">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="41c16-114">Required attribute.</span></span><br><br><span data-ttu-id="41c16-115">追加するキーの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="41c16-115">Specifies the value of the key to add.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="41c16-116">親要素</span><span class="sxs-lookup"><span data-stu-id="41c16-116">Parent element</span></span>

|     | <span data-ttu-id="41c16-117">説明</span><span class="sxs-lookup"><span data-stu-id="41c16-117">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="41c16-118">**\<appSettings>**</span><span class="sxs-lookup"><span data-stu-id="41c16-118">**\<appSettings>**</span></span>](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) | <span data-ttu-id="41c16-119">ファイル パス、XML Web サービス URL、またはアプリケーションのその他のカスタム構成情報など、カスタム アプリケーションの設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="41c16-119">Contains custom application settings, such as file paths, XML Web service URLs, or any other custom configuration information for an application.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="41c16-120">子要素</span><span class="sxs-lookup"><span data-stu-id="41c16-120">Child elements</span></span>

<span data-ttu-id="41c16-121">なし</span><span class="sxs-lookup"><span data-stu-id="41c16-121">None</span></span>

## <a name="example"></a><span data-ttu-id="41c16-122">例</span><span class="sxs-lookup"><span data-stu-id="41c16-122">Example</span></span>

<span data-ttu-id="41c16-123">次の例では、アプリケーションの名前のカスタム構成設定を追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="41c16-123">The following example shows how to add a custom configuration setting for the application's name:</span></span>

```xml
<appSettings>
  <add key="ApplicationName" value="MyApplication" />
</appSettings>
```

<span data-ttu-id="41c16-124">次の例では、 `<add>` ASP.NET アプリケーションで 2 つの互換性設定を定義する要素。</span><span class="sxs-lookup"><span data-stu-id="41c16-124">The following example uses the `<add>` element to define two compatibility settings in an ASP.NET application:</span></span>

```xml
<appSettings>
  <add key="AppContext.SetSwitch:Switch.System.Globalization.NoAsyncCurrentCulture" value="true" />
  <add key="AppContext.SetSwitch:Switch.System.Uri.DontEnableStrictRFC3986ReservedCharacterSets" value="true" />
</appSettings>
```

## <a name="see-also"></a><span data-ttu-id="41c16-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="41c16-125">See also</span></span>

- [<span data-ttu-id="41c16-126">.NET Framework の構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="41c16-126">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
