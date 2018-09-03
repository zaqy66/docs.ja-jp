---
title: '&lt;schemaImporterExtensions&gt; 要素'
ms.date: 03/30/2017
helpviewer_keywords:
- XML serialization, configuration
- schemaImporterExtensions element
- <schemaImporterExtensions> element
ms.assetid: 465ef2a0-f909-4ac1-9a56-0ead5c849698
ms.openlocfilehash: 8bcd8abb138c645f61bf833b49cda2631d1778dd
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43478014"
---
# <a name="ltschemaimporterextensionsgt-element"></a><span data-ttu-id="73d94-102">&lt;schemaImporterExtensions&gt; 要素</span><span class="sxs-lookup"><span data-stu-id="73d94-102">&lt;schemaImporterExtensions&gt; Element</span></span>
<span data-ttu-id="73d94-103">XSD の型を .NET Framework の型にマッピングするために <xref:System.Xml.Serialization.XmlSchemaImporter> によって使用される型を含みます。</span><span class="sxs-lookup"><span data-stu-id="73d94-103">Contains types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> for mapping of XSD types to .NET Framework types.</span></span> <span data-ttu-id="73d94-104">構成ファイルの詳細については、「[構成ファイル スキーマ](../../../docs/framework/configure-apps/file-schema/index.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73d94-104">For more information about configuration files, see [Configuration File Schema](../../../docs/framework/configure-apps/file-schema/index.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="73d94-105">構文</span><span class="sxs-lookup"><span data-stu-id="73d94-105">Syntax</span></span>  
  
```xml  
<schemaImporterExtensions>  
    <!-- Add types -->  
</schemaImporterExtensions>  
```  
  
## <a name="child-elements"></a><span data-ttu-id="73d94-106">子要素</span><span class="sxs-lookup"><span data-stu-id="73d94-106">Child Elements</span></span>  
  
|<span data-ttu-id="73d94-107">要素</span><span class="sxs-lookup"><span data-stu-id="73d94-107">Element</span></span>|<span data-ttu-id="73d94-108">説明</span><span class="sxs-lookup"><span data-stu-id="73d94-108">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="73d94-109">\<追加 > 要素の\<schemaImporterExtensions ></span><span class="sxs-lookup"><span data-stu-id="73d94-109">\<add> Element for \<schemaImporterExtensions></span></span>](../../../docs/standard/serialization/add-element-for-schemaimporterextensions.md)|<span data-ttu-id="73d94-110">マッピングを作成するために <xref:System.Xml.Serialization.XmlSchemaImporter> によって使用される型を追加します。</span><span class="sxs-lookup"><span data-stu-id="73d94-110">Adds types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> to create mappings.</span></span>|  
  
## <a name="parent-elements"></a><span data-ttu-id="73d94-111">親要素</span><span class="sxs-lookup"><span data-stu-id="73d94-111">Parent Elements</span></span>  
  
|<span data-ttu-id="73d94-112">要素</span><span class="sxs-lookup"><span data-stu-id="73d94-112">Element</span></span>|<span data-ttu-id="73d94-113">説明</span><span class="sxs-lookup"><span data-stu-id="73d94-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="73d94-114">\<system.xml.serialization> 要素</span><span class="sxs-lookup"><span data-stu-id="73d94-114">\<system.xml.serialization> Element</span></span>](../../../docs/standard/serialization/system-xml-serialization-element.md)|<span data-ttu-id="73d94-115">XML シリアル化を制御する最上位の要素です。</span><span class="sxs-lookup"><span data-stu-id="73d94-115">The top-level element for controlling XML serialization.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="73d94-116">例</span><span class="sxs-lookup"><span data-stu-id="73d94-116">Example</span></span>  
 <span data-ttu-id="73d94-117">XSD の型を .NET Framework の型にマッピングする際に <xref:System.Xml.Serialization.XmlSchemaImporter> によって使用される型を追加する方法を次のコード例に示します。</span><span class="sxs-lookup"><span data-stu-id="73d94-117">The following code example illustrates how to add types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> when mapping XSD types to .NET Framework types.</span></span>  
  
```xml  
<system.xml.serialization>  
    <schemaImporterExtensions>  
        <add name = "MobileCapabilities" type =   
        "System.Web.Mobile.MobileCapabilities,   
        System.Web.Mobile, Version - 2.0.0.0, Culture = neutral,   
        PublicKeyToken = b03f5f6f11d40a3a" />  
    </schemaImporterExtensions>  
</system.xml.serialization>  
```  
  
## <a name="see-also"></a><span data-ttu-id="73d94-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="73d94-118">See Also</span></span>  
 <xref:System.Xml.Serialization.XmlSchemaImporter>  
 <xref:System.Xml.Serialization.Configuration.DateTimeSerializationSection.DateTimeSerializationMode>  
 [<span data-ttu-id="73d94-119">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="73d94-119">Configuration File Schema</span></span>](../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="73d94-120">\<dateTimeSerialization> 要素</span><span class="sxs-lookup"><span data-stu-id="73d94-120">\<dateTimeSerialization> Element</span></span>](../../../docs/standard/serialization/datetimeserialization-element.md)  
 [<span data-ttu-id="73d94-121">\<追加 > 要素の\<schemaImporterExtensions ></span><span class="sxs-lookup"><span data-stu-id="73d94-121">\<add> Element for \<schemaImporterExtensions></span></span>](../../../docs/standard/serialization/add-element-for-schemaimporterextensions.md)  
 [<span data-ttu-id="73d94-122">\<system.xml.serialization> 要素</span><span class="sxs-lookup"><span data-stu-id="73d94-122">\<system.xml.serialization> Element</span></span>](../../../docs/standard/serialization/system-xml-serialization-element.md)
