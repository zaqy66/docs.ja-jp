---
title: '&lt;knownType&gt;'
ms.date: 03/30/2017
ms.assetid: ee2b7be3-7148-4a3a-b861-48e7330615e5
ms.openlocfilehash: cb36a0d1d1ceb13a6db902904783ee15b14e673b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54541067"
---
# <a name="ltknowntypegt"></a><span data-ttu-id="c1184-102">&lt;knownType&gt;</span><span class="sxs-lookup"><span data-stu-id="c1184-102">&lt;knownType&gt;</span></span>
<span data-ttu-id="c1184-103">逆シリアル化中に <xref:System.Runtime.Serialization.DataContractSerializer> によって使用される型を指定します。</span><span class="sxs-lookup"><span data-stu-id="c1184-103">Specifies a type to be used by <xref:System.Runtime.Serialization.DataContractSerializer> during deserialization.</span></span> <span data-ttu-id="c1184-104">この要素には、"宣言型" のフィールドまたはプロパティによって返される "既知の型" を指定します。</span><span class="sxs-lookup"><span data-stu-id="c1184-104">The element specifies a "known type" that is returned by a field or property of a "declared type."</span></span> <span data-ttu-id="c1184-105">詳細については、次を参照してください。 [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)します。</span><span class="sxs-lookup"><span data-stu-id="c1184-105">For more information, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>  
  
 <span data-ttu-id="c1184-106">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="c1184-106">\<system.runtime.serialization></span></span>  
<span data-ttu-id="c1184-107">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="c1184-107">\<dataContractSerializer></span></span>  
<span data-ttu-id="c1184-108">\<declaredTypes > 要素</span><span class="sxs-lookup"><span data-stu-id="c1184-108">\<declaredTypes> Element</span></span>  
<span data-ttu-id="c1184-109">\<add> of \<declaredTypes></span><span class="sxs-lookup"><span data-stu-id="c1184-109">\<add> of \<declaredTypes></span></span>  
<span data-ttu-id="c1184-110">\<knownType > 要素</span><span class="sxs-lookup"><span data-stu-id="c1184-110">\<knownType> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c1184-111">構文</span><span class="sxs-lookup"><span data-stu-id="c1184-111">Syntax</span></span>  
  
```xml  
<knownType type="String">
  <parameter index="Integer"
             type="String" />
</knownType>
```  
  
## <a name="type"></a><span data-ttu-id="c1184-112">型</span><span class="sxs-lookup"><span data-stu-id="c1184-112">Type</span></span>  
 `string`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c1184-113">属性および要素</span><span class="sxs-lookup"><span data-stu-id="c1184-113">Attributes and Elements</span></span>  
 <span data-ttu-id="c1184-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="c1184-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c1184-115">属性</span><span class="sxs-lookup"><span data-stu-id="c1184-115">Attributes</span></span>  
  
|<span data-ttu-id="c1184-116">属性</span><span class="sxs-lookup"><span data-stu-id="c1184-116">Attribute</span></span>|<span data-ttu-id="c1184-117">説明</span><span class="sxs-lookup"><span data-stu-id="c1184-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c1184-118">型</span><span class="sxs-lookup"><span data-stu-id="c1184-118">type</span></span>|<span data-ttu-id="c1184-119">型 (名前空間を含む)、アセンブリ名、バージョン、カルチャ、および公開キー トークンを指定します。</span><span class="sxs-lookup"><span data-stu-id="c1184-119">Specifies the type (including namespace), assembly name, version, culture, and public key token.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c1184-120">子要素</span><span class="sxs-lookup"><span data-stu-id="c1184-120">Child Elements</span></span>  
  
|<span data-ttu-id="c1184-121">要素</span><span class="sxs-lookup"><span data-stu-id="c1184-121">Element</span></span>|<span data-ttu-id="c1184-122">説明</span><span class="sxs-lookup"><span data-stu-id="c1184-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c1184-123">\<パラメーター ></span><span class="sxs-lookup"><span data-stu-id="c1184-123">\<parameter></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/parameter.md)|<span data-ttu-id="c1184-124">宣言型がジェネリック型である場合に、パラメーター インデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="c1184-124">Specifies a parameter index when the declared type is a generic type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c1184-125">親要素</span><span class="sxs-lookup"><span data-stu-id="c1184-125">Parent Elements</span></span>  
  
|<span data-ttu-id="c1184-126">要素</span><span class="sxs-lookup"><span data-stu-id="c1184-126">Element</span></span>|<span data-ttu-id="c1184-127">説明</span><span class="sxs-lookup"><span data-stu-id="c1184-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c1184-128">\<add></span><span class="sxs-lookup"><span data-stu-id="c1184-128">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)|<span data-ttu-id="c1184-129">宣言されたタイプのコレクションに、宣言されたタイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="c1184-129">Adds a declared type to the collection of declared types.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c1184-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="c1184-130">Remarks</span></span>  
 <span data-ttu-id="c1184-131">既知の型の詳細については、次を参照してください。 [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)と<xref:System.Runtime.Serialization.DataContractSerializer>します。</span><span class="sxs-lookup"><span data-stu-id="c1184-131">For more information about known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="c1184-132">参照してください、 [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)この要素の使用例についてはします。</span><span class="sxs-lookup"><span data-stu-id="c1184-132">See the [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) for an example of using this element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c1184-133">例</span><span class="sxs-lookup"><span data-stu-id="c1184-133">Example</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="c1184-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1184-134">See also</span></span>
- <xref:System.Runtime.Serialization.DataContractSerializer>
- [<span data-ttu-id="c1184-135">既知のデータ コントラクト型</span><span class="sxs-lookup"><span data-stu-id="c1184-135">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [<span data-ttu-id="c1184-136">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="c1184-136">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)
- [<span data-ttu-id="c1184-137">\<add></span><span class="sxs-lookup"><span data-stu-id="c1184-137">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
