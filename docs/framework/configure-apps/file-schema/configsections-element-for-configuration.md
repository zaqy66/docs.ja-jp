---
title: '&lt;configSections&gt;要素&lt;構成&gt;'
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/configSections
helpviewer_keywords:
- configSections Element
- <configSections> Element
ms.assetid: 9f963c1b-dc3f-4220-a8b6-2dd7a5a8e039
author: guardrex
ms.author: mairaw
ms.openlocfilehash: f46c84a1674a3e9352d0a4ccda23d44e650a70ed
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629489"
---
# <a name="configsections-element-for-configuration"></a><span data-ttu-id="537ad-102">\<configSections > 要素の\<構成 ></span><span class="sxs-lookup"><span data-stu-id="537ad-102">\<configSections> element for \<configuration></span></span>

<span data-ttu-id="537ad-103">構成セクションと名前空間宣言が含まれています。</span><span class="sxs-lookup"><span data-stu-id="537ad-103">Contains configuration section and namespace declarations.</span></span>

<span data-ttu-id="537ad-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="537ad-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="537ad-105">&nbsp;&nbsp;**\<configSections>**</span><span class="sxs-lookup"><span data-stu-id="537ad-105">&nbsp;&nbsp;**\<configSections>**</span></span>

## <a name="attributes"></a><span data-ttu-id="537ad-106">属性</span><span class="sxs-lookup"><span data-stu-id="537ad-106">Attributes</span></span>

<span data-ttu-id="537ad-107">なし</span><span class="sxs-lookup"><span data-stu-id="537ad-107">None</span></span>

## <a name="parent-element"></a><span data-ttu-id="537ad-108">親要素</span><span class="sxs-lookup"><span data-stu-id="537ad-108">Parent element</span></span>

|     | <span data-ttu-id="537ad-109">説明</span><span class="sxs-lookup"><span data-stu-id="537ad-109">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="537ad-110">**\<configuration>**</span><span class="sxs-lookup"><span data-stu-id="537ad-110">**\<configuration>**</span></span>](~/docs/framework/configure-apps/file-schema/configuration-element.md) | <span data-ttu-id="537ad-111">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="537ad-111">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="537ad-112">子要素</span><span class="sxs-lookup"><span data-stu-id="537ad-112">Child elements</span></span>

|     | <span data-ttu-id="537ad-113">説明</span><span class="sxs-lookup"><span data-stu-id="537ad-113">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="537ad-114">**\<section>**</span><span class="sxs-lookup"><span data-stu-id="537ad-114">**\<section>**</span></span>](~/docs/framework/configure-apps/file-schema/section-element.md) | <span data-ttu-id="537ad-115">構成セクションの宣言が含まれています。</span><span class="sxs-lookup"><span data-stu-id="537ad-115">Contains a configuration section declaration.</span></span> |
| [<span data-ttu-id="537ad-116">**\<sectionGroup>**</span><span class="sxs-lookup"><span data-stu-id="537ad-116">**\<sectionGroup>**</span></span>](~/docs/framework/configure-apps/file-schema/sectiongroup-element-for-configsections.md) | <span data-ttu-id="537ad-117">構成セクションの名前空間を定義します。</span><span class="sxs-lookup"><span data-stu-id="537ad-117">Defines a namespace for configuration sections.</span></span> |
| [<span data-ttu-id="537ad-118">**\<remove>**</span><span class="sxs-lookup"><span data-stu-id="537ad-118">**\<remove>**</span></span>](~/docs/framework/configure-apps/file-schema/remove-element-for-configsections.md) | <span data-ttu-id="537ad-119">定義済みのセクションまたはセクション グループを削除します。</span><span class="sxs-lookup"><span data-stu-id="537ad-119">Removes a predefined section or section group.</span></span> |
| [<span data-ttu-id="537ad-120">**\<clear>**</span><span class="sxs-lookup"><span data-stu-id="537ad-120">**\<clear>**</span></span>](~/docs/framework/configure-apps/file-schema/clear-element-for-configsections.md) | <span data-ttu-id="537ad-121">以前に定義されたセクションおよびセクション グループのすべてをクリアします。</span><span class="sxs-lookup"><span data-stu-id="537ad-121">Clears all previously defined sections and section groups.</span></span> |

## <a name="remarks"></a><span data-ttu-id="537ad-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="537ad-122">Remarks</span></span>

<span data-ttu-id="537ad-123">この要素は、構成ファイルでは場合の最初の子要素があります、 **\<構成 >** 要素。</span><span class="sxs-lookup"><span data-stu-id="537ad-123">If this element is in a configuration file, it must be the first child element of the **\<configuration>** element.</span></span>

## <a name="example"></a><span data-ttu-id="537ad-124">例</span><span class="sxs-lookup"><span data-stu-id="537ad-124">Example</span></span>

<span data-ttu-id="537ad-125">次の例では、構成セクションを定義し、そのセクションの設定を定義する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="537ad-125">The following example shows how to define a configuration section and define settings for that section:</span></span>

```xml
<configuration>
  <configSections>
    <section name="sampleSection"
             type="System.Configuration.SingleTagSectionHandler" />
  </configSections>
  <sampleSection setting1="Value1" 
                 setting2="value two" 
                 setting3="third value" />
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="537ad-126">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="537ad-126">Configuration file</span></span>

<span data-ttu-id="537ad-127">この要素は、アプリケーション構成ファイル、マシン構成ファイルで使用できます (*Machine.config*)、および*Web.config*アプリケーション ディレクトリ レベルではないファイル。</span><span class="sxs-lookup"><span data-stu-id="537ad-127">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="537ad-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="537ad-128">See also</span></span>

- [<span data-ttu-id="537ad-129">.NET Framework の構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="537ad-129">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
