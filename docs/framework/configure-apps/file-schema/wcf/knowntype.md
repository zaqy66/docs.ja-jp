---
title: <knownType>
ms.date: 03/30/2017
ms.assetid: ee2b7be3-7148-4a3a-b861-48e7330615e5
ms.openlocfilehash: 1224a410d030669e340bd328c9158c85cdfeaeee
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55266456"
---
# <a name="knowntype"></a><span data-ttu-id="ddc0f-101">\<knownType ></span><span class="sxs-lookup"><span data-stu-id="ddc0f-101">\<knownType></span></span>
<span data-ttu-id="ddc0f-102">逆シリアル化中に <xref:System.Runtime.Serialization.DataContractSerializer> によって使用される型を指定します。</span><span class="sxs-lookup"><span data-stu-id="ddc0f-102">Specifies a type to be used by <xref:System.Runtime.Serialization.DataContractSerializer> during deserialization.</span></span> <span data-ttu-id="ddc0f-103">この要素には、"宣言型" のフィールドまたはプロパティによって返される "既知の型" を指定します。</span><span class="sxs-lookup"><span data-stu-id="ddc0f-103">The element specifies a "known type" that is returned by a field or property of a "declared type."</span></span> <span data-ttu-id="ddc0f-104">詳細については、次を参照してください。 [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)します。</span><span class="sxs-lookup"><span data-stu-id="ddc0f-104">For more information, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>  
  
 <span data-ttu-id="ddc0f-105">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="ddc0f-105">\<system.runtime.serialization></span></span>  
<span data-ttu-id="ddc0f-106">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="ddc0f-106">\<dataContractSerializer></span></span>  
<span data-ttu-id="ddc0f-107">\<declaredTypes > 要素</span><span class="sxs-lookup"><span data-stu-id="ddc0f-107">\<declaredTypes> Element</span></span>  
<span data-ttu-id="ddc0f-108">\<add> of \<declaredTypes></span><span class="sxs-lookup"><span data-stu-id="ddc0f-108">\<add> of \<declaredTypes></span></span>  
<span data-ttu-id="ddc0f-109">\<knownType > 要素</span><span class="sxs-lookup"><span data-stu-id="ddc0f-109">\<knownType> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ddc0f-110">構文</span><span class="sxs-lookup"><span data-stu-id="ddc0f-110">Syntax</span></span>  
  
```xml  
<knownType type="String">
  <parameter index="Integer"
             type="String" />
</knownType>
```  
  
## <a name="type"></a><span data-ttu-id="ddc0f-111">型</span><span class="sxs-lookup"><span data-stu-id="ddc0f-111">Type</span></span>  
 `string`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ddc0f-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="ddc0f-112">Attributes and Elements</span></span>  
 <span data-ttu-id="ddc0f-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="ddc0f-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ddc0f-114">属性</span><span class="sxs-lookup"><span data-stu-id="ddc0f-114">Attributes</span></span>  
  
|<span data-ttu-id="ddc0f-115">属性</span><span class="sxs-lookup"><span data-stu-id="ddc0f-115">Attribute</span></span>|<span data-ttu-id="ddc0f-116">説明</span><span class="sxs-lookup"><span data-stu-id="ddc0f-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ddc0f-117">型</span><span class="sxs-lookup"><span data-stu-id="ddc0f-117">type</span></span>|<span data-ttu-id="ddc0f-118">型 (名前空間を含む)、アセンブリ名、バージョン、カルチャ、および公開キー トークンを指定します。</span><span class="sxs-lookup"><span data-stu-id="ddc0f-118">Specifies the type (including namespace), assembly name, version, culture, and public key token.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ddc0f-119">子要素</span><span class="sxs-lookup"><span data-stu-id="ddc0f-119">Child Elements</span></span>  
  
|<span data-ttu-id="ddc0f-120">要素</span><span class="sxs-lookup"><span data-stu-id="ddc0f-120">Element</span></span>|<span data-ttu-id="ddc0f-121">説明</span><span class="sxs-lookup"><span data-stu-id="ddc0f-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ddc0f-122">\<パラメーター ></span><span class="sxs-lookup"><span data-stu-id="ddc0f-122">\<parameter></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/parameter.md)|<span data-ttu-id="ddc0f-123">宣言型がジェネリック型である場合に、パラメーター インデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="ddc0f-123">Specifies a parameter index when the declared type is a generic type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ddc0f-124">親要素</span><span class="sxs-lookup"><span data-stu-id="ddc0f-124">Parent Elements</span></span>  
  
|<span data-ttu-id="ddc0f-125">要素</span><span class="sxs-lookup"><span data-stu-id="ddc0f-125">Element</span></span>|<span data-ttu-id="ddc0f-126">説明</span><span class="sxs-lookup"><span data-stu-id="ddc0f-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ddc0f-127">\<add></span><span class="sxs-lookup"><span data-stu-id="ddc0f-127">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)|<span data-ttu-id="ddc0f-128">宣言されたタイプのコレクションに、宣言されたタイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="ddc0f-128">Adds a declared type to the collection of declared types.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ddc0f-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="ddc0f-129">Remarks</span></span>  
 <span data-ttu-id="ddc0f-130">既知の型の詳細については、次を参照してください。 [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)と<xref:System.Runtime.Serialization.DataContractSerializer>します。</span><span class="sxs-lookup"><span data-stu-id="ddc0f-130">For more information about known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="ddc0f-131">参照してください、 [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)この要素の使用例についてはします。</span><span class="sxs-lookup"><span data-stu-id="ddc0f-131">See the [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) for an example of using this element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ddc0f-132">例</span><span class="sxs-lookup"><span data-stu-id="ddc0f-132">Example</span></span>  
  
```xml  
<add type="MyCompany.Library.Shape,
           MyAssembly, Version=2.0.0.0, Culture=neutral,
           PublicKeyToken=XXXXXX, processorArchitecture=MSIL">
  <knownType type="MyCompany.Library.Circle,
                   MyAssembly, Version=2.0.0.0, Culture=neutral,
                   PublicKeyToken=XXXXXX,
                   processorArchitecture=MSIL"/>
</add>
```  
  
## <a name="see-also"></a><span data-ttu-id="ddc0f-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="ddc0f-133">See also</span></span>
- <xref:System.Runtime.Serialization.DataContractSerializer>
- [<span data-ttu-id="ddc0f-134">既知のデータ コントラクト型</span><span class="sxs-lookup"><span data-stu-id="ddc0f-134">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [<span data-ttu-id="ddc0f-135">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="ddc0f-135">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)
- [<span data-ttu-id="ddc0f-136">\<add></span><span class="sxs-lookup"><span data-stu-id="ddc0f-136">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
