---
title: <remove> の <configSections> 要素
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/configSections/remove
helpviewer_keywords:
- remove Element
- <remove> Element
ms.assetid: ae4d82e0-e8fe-468c-81ab-46d63c4d66a8
author: guardrex
ms.author: mairaw
ms.openlocfilehash: 9ceffd3194c7df41f12ac6cd6b589602965b4920
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55279098"
---
# <a name="remove-element-for-configsections"></a><span data-ttu-id="fa020-102">\<削除 > 要素の\<configSections ></span><span class="sxs-lookup"><span data-stu-id="fa020-102">\<remove> element for \<configSections></span></span>

<span data-ttu-id="fa020-103">定義済みのセクションまたはセクション グループを削除します。</span><span class="sxs-lookup"><span data-stu-id="fa020-103">Removes a predefined section or section group.</span></span>

<span data-ttu-id="fa020-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="fa020-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="fa020-105">&nbsp;&nbsp;[**\<configSections>**](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="fa020-105">&nbsp;&nbsp;[**\<configSections>**](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) </span></span>  
<span data-ttu-id="fa020-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**</span><span class="sxs-lookup"><span data-stu-id="fa020-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**</span></span>

## <a name="syntax"></a><span data-ttu-id="fa020-107">構文</span><span class="sxs-lookup"><span data-stu-id="fa020-107">Syntax</span></span>

```xml
<remove name="section name or section group name" />
```

## <a name="attribute"></a><span data-ttu-id="fa020-108">属性</span><span class="sxs-lookup"><span data-stu-id="fa020-108">Attribute</span></span>

|           | <span data-ttu-id="fa020-109">説明</span><span class="sxs-lookup"><span data-stu-id="fa020-109">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="fa020-110">**name**</span><span class="sxs-lookup"><span data-stu-id="fa020-110">**name**</span></span>  | <span data-ttu-id="fa020-111">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="fa020-111">Required attribute.</span></span><br><br><span data-ttu-id="fa020-112">セクションまたは削除するセクション グループの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="fa020-112">Specifies the name of the section or section group to remove.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="fa020-113">親要素</span><span class="sxs-lookup"><span data-stu-id="fa020-113">Parent element</span></span>

|     | <span data-ttu-id="fa020-114">説明</span><span class="sxs-lookup"><span data-stu-id="fa020-114">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="fa020-115">**\<configSections >** 要素</span><span class="sxs-lookup"><span data-stu-id="fa020-115">**\<configSections>** Element</span></span>](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) | <span data-ttu-id="fa020-116">構成セクションと名前空間宣言が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fa020-116">Contains configuration section and namespace declarations.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="fa020-117">子要素</span><span class="sxs-lookup"><span data-stu-id="fa020-117">Child elements</span></span>

<span data-ttu-id="fa020-118">なし</span><span class="sxs-lookup"><span data-stu-id="fa020-118">None</span></span>

## <a name="remarks"></a><span data-ttu-id="fa020-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="fa020-119">Remarks</span></span>

<span data-ttu-id="fa020-120">使用することができます、 **\<削除 >** セクションおよびセクション グループを構成ファイル階層内の上位レベルで定義されているアプリケーションから削除する要素。</span><span class="sxs-lookup"><span data-stu-id="fa020-120">You can use the **\<remove>** element to remove sections and section groups from your application that were defined at a higher level in the configuration file hierarchy.</span></span>

## <a name="example"></a><span data-ttu-id="fa020-121">例</span><span class="sxs-lookup"><span data-stu-id="fa020-121">Example</span></span>

<span data-ttu-id="fa020-122">次の例は、使用する方法を示します、 **\<削除 >** マシン構成ファイルで定義したセクションを削除するアプリケーション構成ファイル内の要素。</span><span class="sxs-lookup"><span data-stu-id="fa020-122">The following example shows how to use the **\<remove>** element in an application configuration file to remove a section previously defined in the machine configuration file.</span></span>

<span data-ttu-id="fa020-123">マシン構成ファイルのコードは、次のセクションを宣言します **\<sampleSection >**:</span><span class="sxs-lookup"><span data-stu-id="fa020-123">The following machine configuration file code declares the section **\<sampleSection>**:</span></span>

```xml
<!-- Machine.config file -->
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

<span data-ttu-id="fa020-124">アプリケーション構成ファイルのコードは、次の削除、  **\<sampleSection >** セクション。</span><span class="sxs-lookup"><span data-stu-id="fa020-124">The following application configuration file code removes the **\<sampleSection>** section.</span></span> <span data-ttu-id="fa020-125">削除した後、アプリケーションが設定を取得できません **\<sampleSection >** します。</span><span class="sxs-lookup"><span data-stu-id="fa020-125">After removal, the application cannot retrieve the settings in **\<sampleSection>**.</span></span>

```xml
<!-- Application configuration file -->
<configuration>
  <configSections>
    <remove name="sampleSection"/>
  </configSections>
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="fa020-126">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="fa020-126">Configuration file</span></span>

<span data-ttu-id="fa020-127">この要素は、アプリケーション構成ファイル、マシン構成ファイルで使用できます (*Machine.config*)、および*Web.config*アプリケーション ディレクトリ レベルではないファイル。</span><span class="sxs-lookup"><span data-stu-id="fa020-127">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa020-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa020-128">See also</span></span>

- [<span data-ttu-id="fa020-129">.NET Framework の構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="fa020-129">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
