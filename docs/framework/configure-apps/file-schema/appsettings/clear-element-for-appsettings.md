---
title: '&lt;オフ&gt;要素&lt;appSettings&gt;'
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/appSettings/clear
helpviewer_keywords:
- clear Element
- <clear> Element
ms.assetid: 6d18c7be-27db-438b-8fb5-765d396b0b7b
author: guardrex
ms.author: mairaw
ms.openlocfilehash: bc52e3149c213925ea64a8421ee65befeea4161e
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50184219"
---
# <a name="clear-element-for-appsettings"></a><span data-ttu-id="e1645-102">\<クリア > 要素の\<appSettings ></span><span class="sxs-lookup"><span data-stu-id="e1645-102">\<clear> element for \<appSettings></span></span>

<span data-ttu-id="e1645-103">カスタム アプリケーションの設定をクリアします。</span><span class="sxs-lookup"><span data-stu-id="e1645-103">Clears custom application settings.</span></span>

<span data-ttu-id="e1645-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="e1645-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="e1645-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="e1645-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span></span>  
<span data-ttu-id="e1645-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<クリア >**</span><span class="sxs-lookup"><span data-stu-id="e1645-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<clear>**</span></span>

## <a name="syntax"></a><span data-ttu-id="e1645-107">構文</span><span class="sxs-lookup"><span data-stu-id="e1645-107">Syntax</span></span>

```xml
<appSettings>
  <clear />
</appSettings>
```

## <a name="attributes"></a><span data-ttu-id="e1645-108">属性</span><span class="sxs-lookup"><span data-stu-id="e1645-108">Attributes</span></span>

<span data-ttu-id="e1645-109">なし</span><span class="sxs-lookup"><span data-stu-id="e1645-109">None</span></span>

## <a name="parent-element"></a><span data-ttu-id="e1645-110">親要素</span><span class="sxs-lookup"><span data-stu-id="e1645-110">Parent element</span></span>

|     | <span data-ttu-id="e1645-111">説明</span><span class="sxs-lookup"><span data-stu-id="e1645-111">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="e1645-112">**\<appSettings>**</span><span class="sxs-lookup"><span data-stu-id="e1645-112">**\<appSettings>**</span></span>](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) | <span data-ttu-id="e1645-113">ファイル パス、XML Web サービスの Url、またはその他のカスタム アプリケーションの構成情報など、カスタム アプリケーション設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e1645-113">Contains custom application settings, such as file paths, XML Web service URLs, or any other custom application configuration information.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="e1645-114">子要素</span><span class="sxs-lookup"><span data-stu-id="e1645-114">Child elements</span></span>

<span data-ttu-id="e1645-115">なし</span><span class="sxs-lookup"><span data-stu-id="e1645-115">None</span></span>

## <a name="example"></a><span data-ttu-id="e1645-116">例</span><span class="sxs-lookup"><span data-stu-id="e1645-116">Example</span></span>

<span data-ttu-id="e1645-117">次の例では、カスタム構成設定をクリアする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e1645-117">The following example shows how to clear custom configuration settings:</span></span>

```xml
<appSettings>
  <clear />
</appSettings>
```

## <a name="see-also"></a><span data-ttu-id="e1645-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="e1645-118">See also</span></span>

- [<span data-ttu-id="e1645-119">.NET Framework の構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="e1645-119">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
