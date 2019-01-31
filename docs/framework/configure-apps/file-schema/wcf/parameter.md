---
title: <parameter>
ms.date: 03/30/2017
ms.assetid: 0fb41e2d-64f7-44ab-993e-05892eac6d82
ms.openlocfilehash: 8b14dc1908ef3a06549154f70efb2d4e5cb10076
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55289434"
---
# <a name="parameter"></a><span data-ttu-id="77a75-101">\<パラメーター ></span><span class="sxs-lookup"><span data-stu-id="77a75-101">\<parameter></span></span>
<span data-ttu-id="77a75-102">宣言された型がジェネリック型である場合、ジェネリック パラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="77a75-102">Specifies the generic parameter when a declared type is a generic type.</span></span>  
  
 <span data-ttu-id="77a75-103">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="77a75-103">\<system.runtime.serialization></span></span>  
<span data-ttu-id="77a75-104">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="77a75-104">\<dataContractSerializer></span></span>  
<span data-ttu-id="77a75-105">\<declaredTypes > 要素</span><span class="sxs-lookup"><span data-stu-id="77a75-105">\<declaredTypes> Element</span></span>  
<span data-ttu-id="77a75-106">\<追加 > 要素の\<declaredTypes ></span><span class="sxs-lookup"><span data-stu-id="77a75-106">\<add> element for \<declaredTypes></span></span>  
<span data-ttu-id="77a75-107">\<knownType > 要素</span><span class="sxs-lookup"><span data-stu-id="77a75-107">\<knownType> Element</span></span>  
<span data-ttu-id="77a75-108">\<パラメーター > 要素</span><span class="sxs-lookup"><span data-stu-id="77a75-108">\<parameter> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77a75-109">構文</span><span class="sxs-lookup"><span data-stu-id="77a75-109">Syntax</span></span>  
  
```xml  
<parameter index="Integer"
           type="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="77a75-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="77a75-110">Attributes and Elements</span></span>  
 <span data-ttu-id="77a75-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="77a75-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="77a75-112">属性</span><span class="sxs-lookup"><span data-stu-id="77a75-112">Attributes</span></span>  
  
|<span data-ttu-id="77a75-113">属性</span><span class="sxs-lookup"><span data-stu-id="77a75-113">Attribute</span></span>|<span data-ttu-id="77a75-114">説明</span><span class="sxs-lookup"><span data-stu-id="77a75-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="77a75-115">インデックス</span><span class="sxs-lookup"><span data-stu-id="77a75-115">index</span></span>|<span data-ttu-id="77a75-116">宣言された型がジェネリック型である場合、既知の型を返すジェネリック パラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="77a75-116">When the declared type is a generic type, specifies the generic parameter that will return the known type.</span></span>|  
|<span data-ttu-id="77a75-117">型</span><span class="sxs-lookup"><span data-stu-id="77a75-117">type</span></span>|<span data-ttu-id="77a75-118">シリアル化と逆シリアル化で使用される既知の型を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="77a75-118">A string that describes the known type used for serialization and deserialization.</span></span>|  
  
## <a name="index-attribute"></a><span data-ttu-id="77a75-119">index 属性</span><span class="sxs-lookup"><span data-stu-id="77a75-119">index Attribute</span></span>  
  
|<span data-ttu-id="77a75-120">値</span><span class="sxs-lookup"><span data-stu-id="77a75-120">Value</span></span>|<span data-ttu-id="77a75-121">説明</span><span class="sxs-lookup"><span data-stu-id="77a75-121">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="77a75-122">"0"</span><span class="sxs-lookup"><span data-stu-id="77a75-122">"0"</span></span>|<span data-ttu-id="77a75-123">ジェネリック型の最初のパラメーター。</span><span class="sxs-lookup"><span data-stu-id="77a75-123">The first parameter in the generic type.</span></span> <span data-ttu-id="77a75-124">たとえば、<xref:System.Collections.Generic.List%601> にはパラメーターが 1 つだけあります。</span><span class="sxs-lookup"><span data-stu-id="77a75-124">For example, a <xref:System.Collections.Generic.List%601> has only one parameter.</span></span> <span data-ttu-id="77a75-125">宣言型として使用される場合、index は "0" に設定されます。</span><span class="sxs-lookup"><span data-stu-id="77a75-125">If it is used as the declared type, the index would be set to "0".</span></span>|  
|<span data-ttu-id="77a75-126">"1"</span><span class="sxs-lookup"><span data-stu-id="77a75-126">"1"</span></span>|<span data-ttu-id="77a75-127">ジェネリック型の 2 番目のパラメーター。</span><span class="sxs-lookup"><span data-stu-id="77a75-127">The second parameter in a generic type.</span></span> <span data-ttu-id="77a75-128">たとえば、<xref:System.Collections.Generic.Dictionary%602> には 2 つのパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="77a75-128">For example, a <xref:System.Collections.Generic.Dictionary%602> has two parameters.</span></span> <span data-ttu-id="77a75-129">2 番目のパラメーターによって既知の型が返される場合は、index 属性を "1" に設定します。</span><span class="sxs-lookup"><span data-stu-id="77a75-129">If the known type is returned by the second parameter, set the index attribute to "1".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="77a75-130">子要素</span><span class="sxs-lookup"><span data-stu-id="77a75-130">Child Elements</span></span>  
 <span data-ttu-id="77a75-131">なし。</span><span class="sxs-lookup"><span data-stu-id="77a75-131">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="77a75-132">親要素</span><span class="sxs-lookup"><span data-stu-id="77a75-132">Parent Elements</span></span>  
  
|<span data-ttu-id="77a75-133">要素</span><span class="sxs-lookup"><span data-stu-id="77a75-133">Element</span></span>|<span data-ttu-id="77a75-134">説明</span><span class="sxs-lookup"><span data-stu-id="77a75-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="77a75-135">\<knownType></span><span class="sxs-lookup"><span data-stu-id="77a75-135">\<knownType></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/knowntype.md)|<span data-ttu-id="77a75-136">宣言型のフィールドまたはプロパティによって返される既知の型を指定します。</span><span class="sxs-lookup"><span data-stu-id="77a75-136">Specifies a known type that can be returned by a field or property of the declared type.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="77a75-137">Remarks</span><span class="sxs-lookup"><span data-stu-id="77a75-137">Remarks</span></span>  
 <span data-ttu-id="77a75-138">既知の型の詳細については、次を参照してください。 [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)と<xref:System.Runtime.Serialization.DataContractSerializer>します。</span><span class="sxs-lookup"><span data-stu-id="77a75-138">For more information about known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="77a75-139">参照してください、 [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)この要素の使用例についてはします。</span><span class="sxs-lookup"><span data-stu-id="77a75-139">See the [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) for an example of using this element.</span></span>  
  
 <span data-ttu-id="77a75-140">この構成要素に、両方の属性を同時に設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="77a75-140">This configuration element cannot have both attributes at the same time.</span></span> <span data-ttu-id="77a75-141">両方の属性が設定された場合、<xref:System.Configuration.ConfigurationErrorsException> が発生します。</span><span class="sxs-lookup"><span data-stu-id="77a75-141">If both attributes are set, a <xref:System.Configuration.ConfigurationErrorsException> occurs.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77a75-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="77a75-142">See also</span></span>
- <xref:System.Runtime.Serialization.DataContractSerializer>
- [<span data-ttu-id="77a75-143">既知のデータ コントラクト型</span><span class="sxs-lookup"><span data-stu-id="77a75-143">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [<span data-ttu-id="77a75-144">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="77a75-144">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)
- [<span data-ttu-id="77a75-145">\<add></span><span class="sxs-lookup"><span data-stu-id="77a75-145">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
