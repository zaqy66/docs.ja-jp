---
title: <remove> NameValueSectionHandler および DictionarySectionHandler の要素
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/sectionName/remove
helpviewer_keywords:
- remove Element
- <remove> Element
ms.assetid: 8d8af7f5-26c9-4db9-bbe4-b2a4e6949568
author: guardrex
ms.author: mairaw
ms.openlocfilehash: c86d231a4e3e8e15df94017a6ca461b365643ea5
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55267418"
---
# <a name="remove-element-for-namevaluesectionhandler-and-dictionarysectionhandler"></a><span data-ttu-id="c498b-102">\<削除 > NameValueSectionHandler および DictionarySectionHandler の要素</span><span class="sxs-lookup"><span data-stu-id="c498b-102">\<remove> element for NameValueSectionHandler and DictionarySectionHandler</span></span>

<span data-ttu-id="c498b-103">以前に定義された設定を削除します。</span><span class="sxs-lookup"><span data-stu-id="c498b-103">Removes a previously defined setting.</span></span>

<span data-ttu-id="c498b-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="c498b-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="c498b-105">&nbsp;&nbsp;[**\<sectionName>**](~/docs/framework/configure-apps/file-schema/custom-element-2.md) </span><span class="sxs-lookup"><span data-stu-id="c498b-105">&nbsp;&nbsp;[**\<sectionName>**](~/docs/framework/configure-apps/file-schema/custom-element-2.md) </span></span>  
<span data-ttu-id="c498b-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**</span><span class="sxs-lookup"><span data-stu-id="c498b-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**</span></span>

## <a name="syntax"></a><span data-ttu-id="c498b-107">構文</span><span class="sxs-lookup"><span data-stu-id="c498b-107">Syntax</span></span>

```xml
<add remove="key" />
```

## <a name="attribute"></a><span data-ttu-id="c498b-108">属性</span><span class="sxs-lookup"><span data-stu-id="c498b-108">Attribute</span></span>

|           | <span data-ttu-id="c498b-109">説明</span><span class="sxs-lookup"><span data-stu-id="c498b-109">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="c498b-110">**key**</span><span class="sxs-lookup"><span data-stu-id="c498b-110">**key**</span></span>   | <span data-ttu-id="c498b-111">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="c498b-111">Required attribute.</span></span><br><br><span data-ttu-id="c498b-112">削除する設定の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="c498b-112">Specifies the name of the setting to remove.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="c498b-113">親要素</span><span class="sxs-lookup"><span data-stu-id="c498b-113">Parent element</span></span>

| <span data-ttu-id="c498b-114">要素</span><span class="sxs-lookup"><span data-stu-id="c498b-114">Element</span></span> | <span data-ttu-id="c498b-115">説明</span><span class="sxs-lookup"><span data-stu-id="c498b-115">Description</span></span> |
| ------- | ------------|
| [<span data-ttu-id="c498b-116">**\<sectionName >** 要素</span><span class="sxs-lookup"><span data-stu-id="c498b-116">**\<sectionName>** Element</span></span>](~/docs/framework/configure-apps/file-schema/custom-element-2.md) | <span data-ttu-id="c498b-117">使用して、カスタム構成セクションの設定を定義、<xref:System.Configuration.NameValueSectionHandler>と<xref:System.Configuration.DictionarySectionHandler>クラス。</span><span class="sxs-lookup"><span data-stu-id="c498b-117">Defines settings for custom configuration sections that use the <xref:System.Configuration.NameValueSectionHandler> and <xref:System.Configuration.DictionarySectionHandler> classes.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="c498b-118">子要素</span><span class="sxs-lookup"><span data-stu-id="c498b-118">Child elements</span></span>

<span data-ttu-id="c498b-119">なし</span><span class="sxs-lookup"><span data-stu-id="c498b-119">None</span></span>

## <a name="remarks"></a><span data-ttu-id="c498b-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="c498b-120">Remarks</span></span>

<span data-ttu-id="c498b-121">使用することができます、 **\<削除 >** 構成ファイル階層内の上位レベルで定義されているアプリケーションから設定を削除する要素。</span><span class="sxs-lookup"><span data-stu-id="c498b-121">You can use the **\<remove>** element to remove settings from your application that were defined at a higher level in the configuration file hierarchy.</span></span>

## <a name="example"></a><span data-ttu-id="c498b-122">例</span><span class="sxs-lookup"><span data-stu-id="c498b-122">Example</span></span>

<span data-ttu-id="c498b-123">次の例は、使用する方法を示します、 **\<削除 >** マシン構成ファイルで定義した設定を削除するアプリケーション構成ファイル内の要素。</span><span class="sxs-lookup"><span data-stu-id="c498b-123">The following example shows how to use the **\<remove>** element in an application configuration file to remove settings previously defined in the machine configuration file.</span></span>

<span data-ttu-id="c498b-124">マシン構成ファイルのコードは、次のセクションを宣言します **\<mySection >** し、2 つの設定を追加`key1`と`key2`に。</span><span class="sxs-lookup"><span data-stu-id="c498b-124">The following machine configuration file code declares the section **\<mySection>** and adds two settings, `key1` and `key2`, to it:</span></span>

```xml
<!-- Machine.config file -->
<configuration>
  <configSections>
    <section name="mySection" type="System.Configuration.NameValueSectionHandler,System" />
  </configSections>
  <mySection>
    <add key="key1" value="value1" />
    <add key="key2" value="value2" />
  </mySection>
</configuration>
```

<span data-ttu-id="c498b-125">アプリケーション構成ファイルのコードは、次の削除、`key2`設定から **\<mySection >**:</span><span class="sxs-lookup"><span data-stu-id="c498b-125">The following application configuration file code removes the `key2` setting from **\<mySection>**:</span></span>

```xml
<!--Application configuration file -->
<configuration>
  <mySection>
    <remove key="key2" />
  </mySection>
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="c498b-126">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="c498b-126">Configuration file</span></span>

<span data-ttu-id="c498b-127">この要素は、アプリケーション構成ファイル、マシン構成ファイルで使用できます (*Machine.config*)、および*Web.config*アプリケーション ディレクトリ レベルではないファイル。</span><span class="sxs-lookup"><span data-stu-id="c498b-127">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="c498b-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="c498b-128">See also</span></span>

- [<span data-ttu-id="c498b-129">.NET Framework の構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="c498b-129">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
