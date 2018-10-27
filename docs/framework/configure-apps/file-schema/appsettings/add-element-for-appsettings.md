---
title: '&lt;追加&gt;要素&lt;appSettings&gt;'
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/appSettings/add
helpviewer_keywords:
- add Element
- <add> Element
ms.assetid: 8734efdc-00f6-4a65-bba6-084c5bc65246
author: guardrex
ms.author: mairaw
ms.openlocfilehash: e74f0956dd5acebccee87fd6ad8c09b299badffd
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2018
ms.locfileid: "50036386"
---
# <a name="add-element-for-appsettings"></a><span data-ttu-id="132c2-102">\<追加 > 要素の\<appSettings ></span><span class="sxs-lookup"><span data-stu-id="132c2-102">\<add> element for \<appSettings></span></span>

<span data-ttu-id="132c2-103">カスタム アプリケーション設定を追加します。</span><span class="sxs-lookup"><span data-stu-id="132c2-103">Adds a custom application setting.</span></span>

<span data-ttu-id="132c2-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="132c2-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="132c2-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="132c2-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span></span>  
<span data-ttu-id="132c2-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<追加 >**</span><span class="sxs-lookup"><span data-stu-id="132c2-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**</span></span>

## <a name="syntax"></a><span data-ttu-id="132c2-107">構文</span><span class="sxs-lookup"><span data-stu-id="132c2-107">Syntax</span></span>

```xml
<appSettings>
  <add key="Key of custom setting" value="Value of custom setting" />
</appSettings>
```

## <a name="attributes"></a><span data-ttu-id="132c2-108">属性</span><span class="sxs-lookup"><span data-stu-id="132c2-108">Attributes</span></span>

|           | <span data-ttu-id="132c2-109">説明</span><span class="sxs-lookup"><span data-stu-id="132c2-109">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="132c2-110">**key**</span><span class="sxs-lookup"><span data-stu-id="132c2-110">**key**</span></span>   | <span data-ttu-id="132c2-111">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="132c2-111">Required attribute.</span></span><br><br><span data-ttu-id="132c2-112">追加するキーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="132c2-112">Specifies the name of the key to add.</span></span> |
| <span data-ttu-id="132c2-113">**値**</span><span class="sxs-lookup"><span data-stu-id="132c2-113">**value**</span></span> | <span data-ttu-id="132c2-114">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="132c2-114">Required attribute.</span></span><br><br><span data-ttu-id="132c2-115">追加するキーの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="132c2-115">Specifies the value of the key to add.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="132c2-116">親要素</span><span class="sxs-lookup"><span data-stu-id="132c2-116">Parent element</span></span>

|     | <span data-ttu-id="132c2-117">説明</span><span class="sxs-lookup"><span data-stu-id="132c2-117">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="132c2-118">**\<appSettings>**</span><span class="sxs-lookup"><span data-stu-id="132c2-118">**\<appSettings>**</span></span>](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) | <span data-ttu-id="132c2-119">ファイル パス、XML Web サービス URL、またはアプリケーションのその他のカスタム構成情報など、カスタム アプリケーションの設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="132c2-119">Contains custom application settings, such as file paths, XML Web service URLs, or any other custom configuration information for an application.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="132c2-120">子要素</span><span class="sxs-lookup"><span data-stu-id="132c2-120">Child elements</span></span>

<span data-ttu-id="132c2-121">なし</span><span class="sxs-lookup"><span data-stu-id="132c2-121">None</span></span>

## <a name="example"></a><span data-ttu-id="132c2-122">例</span><span class="sxs-lookup"><span data-stu-id="132c2-122">Example</span></span>

<span data-ttu-id="132c2-123">次の例では、アプリケーションの名前のカスタム構成設定を追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="132c2-123">The following example shows how to add a custom configuration setting for the application's name:</span></span>

```xml
<appSettings>
  <add key="ApplicationName" value="MyApplication" />
</appSettings>
```

<span data-ttu-id="132c2-124">次の例では、 `<add>` ASP.NET アプリケーションで 2 つの互換性設定を定義する要素。</span><span class="sxs-lookup"><span data-stu-id="132c2-124">The following example uses the `<add>` element to define two compatibility settings in an ASP.NET application:</span></span>

```xml
<appSettings>
  <add key="AppContext.SetSwitch:Switch.System.Globalization.NoAsyncCurrentCulture" value="true" />
  <add key="AppContext.SetSwitch:Switch.System.Uri.DontEnableStrictRFC3986ReservedCharacterSets" value="true" />
</appSettings>
```

## <a name="see-also"></a><span data-ttu-id="132c2-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="132c2-125">See also</span></span>

- [<span data-ttu-id="132c2-126">.NET Framework の構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="132c2-126">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
