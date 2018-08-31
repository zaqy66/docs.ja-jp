---
title: '&lt;schemaImporterExtensions&gt; 要素'
ms.date: 03/30/2017
helpviewer_keywords:
- XML serialization, configuration
- schemaImporterExtensions element
- <schemaImporterExtensions> element
ms.assetid: 465ef2a0-f909-4ac1-9a56-0ead5c849698
ms.openlocfilehash: 8bcd8abb138c645f61bf833b49cda2631d1778dd
ms.sourcegitcommit: fe02afbc39e78afd78cc6050e4a9c12a75f579f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/30/2018
ms.locfileid: "43255630"
---
# <a name="ltschemaimporterextensionsgt-element"></a><span data-ttu-id="d368b-102">&lt;schemaImporterExtensions&gt; 要素</span><span class="sxs-lookup"><span data-stu-id="d368b-102">&lt;schemaImporterExtensions&gt; Element</span></span>
<span data-ttu-id="d368b-103">XSD の型を .NET Framework の型にマッピングするために <xref:System.Xml.Serialization.XmlSchemaImporter> によって使用される型を含みます。</span><span class="sxs-lookup"><span data-stu-id="d368b-103">Contains types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> for mapping of XSD types to .NET Framework types.</span></span> <span data-ttu-id="d368b-104">構成ファイルの詳細については、「[構成ファイル スキーマ](../../../docs/framework/configure-apps/file-schema/index.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d368b-104">For more information about configuration files, see [Configuration File Schema](../../../docs/framework/configure-apps/file-schema/index.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d368b-105">構文</span><span class="sxs-lookup"><span data-stu-id="d368b-105">Syntax</span></span>  
  
```xml  
<schemaImporterExtensions>  
    <!-- Add types -->  
</schemaImporterExtensions>  
```  
  
## <a name="child-elements"></a><span data-ttu-id="d368b-106">子要素</span><span class="sxs-lookup"><span data-stu-id="d368b-106">Child Elements</span></span>  
  
|<span data-ttu-id="d368b-107">要素</span><span class="sxs-lookup"><span data-stu-id="d368b-107">Element</span></span>|<span data-ttu-id="d368b-108">説明</span><span class="sxs-lookup"><span data-stu-id="d368b-108">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d368b-109">\<追加 > 要素の\<schemaImporterExtensions ></span><span class="sxs-lookup"><span data-stu-id="d368b-109">\<add> Element for \<schemaImporterExtensions></span></span>](../../../docs/standard/serialization/add-element-for-schemaimporterextensions.md)|<span data-ttu-id="d368b-110">マッピングを作成するために <xref:System.Xml.Serialization.XmlSchemaImporter> によって使用される型を追加します。</span><span class="sxs-lookup"><span data-stu-id="d368b-110">Adds types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> to create mappings.</span></span>|  
  
## <a name="parent-elements"></a><span data-ttu-id="d368b-111">親要素</span><span class="sxs-lookup"><span data-stu-id="d368b-111">Parent Elements</span></span>  
  
|<span data-ttu-id="d368b-112">要素</span><span class="sxs-lookup"><span data-stu-id="d368b-112">Element</span></span>|<span data-ttu-id="d368b-113">説明</span><span class="sxs-lookup"><span data-stu-id="d368b-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d368b-114">\<system.xml.serialization> 要素</span><span class="sxs-lookup"><span data-stu-id="d368b-114">\<system.xml.serialization> Element</span></span>](../../../docs/standard/serialization/system-xml-serialization-element.md)|<span data-ttu-id="d368b-115">XML シリアル化を制御する最上位の要素です。</span><span class="sxs-lookup"><span data-stu-id="d368b-115">The top-level element for controlling XML serialization.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="d368b-116">例</span><span class="sxs-lookup"><span data-stu-id="d368b-116">Example</span></span>  
 <span data-ttu-id="d368b-117">XSD の型を .NET Framework の型にマッピングする際に <xref:System.Xml.Serialization.XmlSchemaImporter> によって使用される型を追加する方法を次のコード例に示します。</span><span class="sxs-lookup"><span data-stu-id="d368b-117">The following code example illustrates how to add types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> when mapping XSD types to .NET Framework types.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="d368b-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="d368b-118">See Also</span></span>  
 <xref:System.Xml.Serialization.XmlSchemaImporter>  
 <xref:System.Xml.Serialization.Configuration.DateTimeSerializationSection.DateTimeSerializationMode>  
 [<span data-ttu-id="d368b-119">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="d368b-119">Configuration File Schema</span></span>](../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="d368b-120">\<dateTimeSerialization> 要素</span><span class="sxs-lookup"><span data-stu-id="d368b-120">\<dateTimeSerialization> Element</span></span>](../../../docs/standard/serialization/datetimeserialization-element.md)  
 [<span data-ttu-id="d368b-121">\<追加 > 要素の\<schemaImporterExtensions ></span><span class="sxs-lookup"><span data-stu-id="d368b-121">\<add> Element for \<schemaImporterExtensions></span></span>](../../../docs/standard/serialization/add-element-for-schemaimporterextensions.md)  
 [<span data-ttu-id="d368b-122">\<system.xml.serialization> 要素</span><span class="sxs-lookup"><span data-stu-id="d368b-122">\<system.xml.serialization> Element</span></span>](../../../docs/standard/serialization/system-xml-serialization-element.md)
