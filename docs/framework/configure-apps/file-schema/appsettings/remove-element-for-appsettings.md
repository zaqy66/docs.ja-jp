---
title: <remove> の <appSettings> 要素
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/appSettings/remove
helpviewer_keywords:
- remove Element
- <remove> Element
ms.assetid: 218c4464-e007-4539-803f-7c8b0a909fd8
author: guardrex
ms.author: mairaw
ms.openlocfilehash: cf9a34e47b70aaff12b29b9c5cf944d5bb15fee9
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55258722"
---
# <a name="remove-element-for-appsettings"></a><span data-ttu-id="e16d3-102">\<削除 > 要素の\<appSettings ></span><span class="sxs-lookup"><span data-stu-id="e16d3-102">\<remove> element for \<appSettings></span></span>

<span data-ttu-id="e16d3-103">カスタム アプリケーションの設定を削除します。</span><span class="sxs-lookup"><span data-stu-id="e16d3-103">Removes custom application settings.</span></span>

<span data-ttu-id="e16d3-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="e16d3-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="e16d3-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="e16d3-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span></span>  
<span data-ttu-id="e16d3-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**</span><span class="sxs-lookup"><span data-stu-id="e16d3-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**</span></span>

## <a name="syntax"></a><span data-ttu-id="e16d3-107">構文</span><span class="sxs-lookup"><span data-stu-id="e16d3-107">Syntax</span></span>

```xml
<appSettings>
  <remove key="Key of custom setting" />
</appSettings>
```

### <a name="attribute"></a><span data-ttu-id="e16d3-108">属性</span><span class="sxs-lookup"><span data-stu-id="e16d3-108">Attribute</span></span>

|         | <span data-ttu-id="e16d3-109">説明</span><span class="sxs-lookup"><span data-stu-id="e16d3-109">Description</span></span> |
| ------- | ----------- |
| <span data-ttu-id="e16d3-110">**key**</span><span class="sxs-lookup"><span data-stu-id="e16d3-110">**key**</span></span> | <span data-ttu-id="e16d3-111">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="e16d3-111">Required attribute.</span></span><br><br><span data-ttu-id="e16d3-112">削除するキーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e16d3-112">Specifies the name of the key to remove.</span></span> |

### <a name="parent-element"></a><span data-ttu-id="e16d3-113">親要素</span><span class="sxs-lookup"><span data-stu-id="e16d3-113">Parent element</span></span>

|     | <span data-ttu-id="e16d3-114">説明</span><span class="sxs-lookup"><span data-stu-id="e16d3-114">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="e16d3-115">**\<appSettings>**</span><span class="sxs-lookup"><span data-stu-id="e16d3-115">**\<appSettings>**</span></span>](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) | <span data-ttu-id="e16d3-116">ファイル パス、XML Web サービス URL、またはアプリケーションのその他のカスタム構成情報など、カスタム アプリケーションの設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e16d3-116">Contains custom application settings, such as file paths, XML Web service URLs, or any other custom configuration information for an application.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="e16d3-117">子要素</span><span class="sxs-lookup"><span data-stu-id="e16d3-117">Child elements</span></span>

<span data-ttu-id="e16d3-118">なし</span><span class="sxs-lookup"><span data-stu-id="e16d3-118">None</span></span>

## <a name="example"></a><span data-ttu-id="e16d3-119">例</span><span class="sxs-lookup"><span data-stu-id="e16d3-119">Example</span></span>

<span data-ttu-id="e16d3-120">次の例のカスタム構成設定を削除する方法を示しています`ApplicationName`:。</span><span class="sxs-lookup"><span data-stu-id="e16d3-120">The following example shows how to remove a custom configuration setting for `ApplicationName`:</span></span>

```xml
<appSettings>
  <remove key="ApplicationName" />
</appSettings>
```

## <a name="see-also"></a><span data-ttu-id="e16d3-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="e16d3-121">See also</span></span>

- [<span data-ttu-id="e16d3-122">.NET Framework の構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="e16d3-122">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
