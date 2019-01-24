---
title: '&lt;AttributeImplies&gt; 要素 (.NET ネイティブ)'
ms.date: 03/30/2017
ms.assetid: 82db7193-a860-418b-84fc-fff2fdf2e025
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7f4e12f690d685f58b69483631aa0e93c9902636
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54696816"
---
# <a name="ltattributeimpliesgt-element-net-native"></a><span data-ttu-id="629eb-102">&lt;AttributeImplies&gt; 要素 (.NET ネイティブ)</span><span class="sxs-lookup"><span data-stu-id="629eb-102">&lt;AttributeImplies&gt; Element (.NET Native)</span></span>
<span data-ttu-id="629eb-103">それを含む属性が適用されるコード要素のポリシーを定義します。</span><span class="sxs-lookup"><span data-stu-id="629eb-103">Defines policy for code elements the containing attribute is applied to.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="629eb-104">構文</span><span class="sxs-lookup"><span data-stu-id="629eb-104">Syntax</span></span>  
  
```xml  
<AttributeImplies Activate="policy_type"  
                  Browse="policy_type"  
                  Dynamic="policy_type"  
                  Serialize="policy_type"   
                  DataContractSerializer="policy_setting"  
                  DataContractJsonSerializer="policy_setting"  
                  XmlSerializer="policy_setting"  
                  MarshalObject="policy_setting"  
                  MarshalDelegate="policy_setting"  
                  MarshalStructure="policy_setting" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="629eb-105">属性および要素</span><span class="sxs-lookup"><span data-stu-id="629eb-105">Attributes and Elements</span></span>  
 <span data-ttu-id="629eb-106">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="629eb-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="629eb-107">属性</span><span class="sxs-lookup"><span data-stu-id="629eb-107">Attributes</span></span>  
  
|<span data-ttu-id="629eb-108">属性</span><span class="sxs-lookup"><span data-stu-id="629eb-108">Attribute</span></span>|<span data-ttu-id="629eb-109">属性の型</span><span class="sxs-lookup"><span data-stu-id="629eb-109">Attribute type</span></span>|<span data-ttu-id="629eb-110">説明</span><span class="sxs-lookup"><span data-stu-id="629eb-110">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Activate`|<span data-ttu-id="629eb-111">リフレクション</span><span class="sxs-lookup"><span data-stu-id="629eb-111">Reflection</span></span>|<span data-ttu-id="629eb-112">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="629eb-112">Optional attribute.</span></span> <span data-ttu-id="629eb-113">コンストラクターへの実行時アクセスを制御して、インスタンスのアクティブ化を有効にします。</span><span class="sxs-lookup"><span data-stu-id="629eb-113">Controls runtime access to constructors to enable activation of instances.</span></span>|  
|`Browse`|<span data-ttu-id="629eb-114">リフレクション</span><span class="sxs-lookup"><span data-stu-id="629eb-114">Reflection</span></span>|<span data-ttu-id="629eb-115">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="629eb-115">Optional attribute.</span></span> <span data-ttu-id="629eb-116">プログラム要素に関する情報の照会を制御しますが、実行時アクセスは有効にしません。</span><span class="sxs-lookup"><span data-stu-id="629eb-116">Controls querying for information about program elements, but does not enable any runtime access.</span></span>|  
|`Dynamic`|<span data-ttu-id="629eb-117">リフレクション</span><span class="sxs-lookup"><span data-stu-id="629eb-117">Reflection</span></span>|<span data-ttu-id="629eb-118">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="629eb-118">Optional attribute.</span></span> <span data-ttu-id="629eb-119">コンストラクター、メソッド、フィールド、プロパティ、およびイベントを含むすべての型のメンバーへの実行時アクセスを制御して、動的プログラミングを有効にします。</span><span class="sxs-lookup"><span data-stu-id="629eb-119">Controls runtime access to all type members, including constructors, methods, fields, properties, and events, to enable dynamic programming.</span></span>|  
|`Serialize`|<span data-ttu-id="629eb-120">シリアル化</span><span class="sxs-lookup"><span data-stu-id="629eb-120">Serialization</span></span>|<span data-ttu-id="629eb-121">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="629eb-121">Optional attribute.</span></span> <span data-ttu-id="629eb-122">コンストラクター、フィールド、およびプロパティへの実行時アクセスを制御し、Newtonsoft の JSON シリアライザーなどのライブラリによって型インスタンスをシリアル化および逆シリアル化できるようにします。</span><span class="sxs-lookup"><span data-stu-id="629eb-122">Controls runtime access to constructors, fields, and properties, to enable type instances to be serialized and deserialized by libraries such as the Newtonsoft JSON serializer.</span></span>|  
|`DataContractSerializer`|<span data-ttu-id="629eb-123">シリアル化</span><span class="sxs-lookup"><span data-stu-id="629eb-123">Serialization</span></span>|<span data-ttu-id="629eb-124">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="629eb-124">Optional attribute.</span></span> <span data-ttu-id="629eb-125"><xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> クラスを使用するシリアル化のポリシーを制御します。</span><span class="sxs-lookup"><span data-stu-id="629eb-125">Controls policy for serialization that uses the <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> class.</span></span>|  
|`DataContractJsonSerializer`|<span data-ttu-id="629eb-126">シリアル化</span><span class="sxs-lookup"><span data-stu-id="629eb-126">Serialization</span></span>|<span data-ttu-id="629eb-127">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="629eb-127">Optional attribute.</span></span> <span data-ttu-id="629eb-128"><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> クラスを使用する JSON シリアル化のポリシーを制御します。</span><span class="sxs-lookup"><span data-stu-id="629eb-128">Controls policy for JSON serialization that uses the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> class.</span></span>|  
|`XmlSerializer`|<span data-ttu-id="629eb-129">シリアル化</span><span class="sxs-lookup"><span data-stu-id="629eb-129">Serialization</span></span>|<span data-ttu-id="629eb-130">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="629eb-130">Optional attribute.</span></span> <span data-ttu-id="629eb-131"><xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> クラスを使用する XML シリアル化のポリシーを制御します。</span><span class="sxs-lookup"><span data-stu-id="629eb-131">Controls policy for XML serialization that uses the <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> class.</span></span>|  
|`MarshalObject`|<span data-ttu-id="629eb-132">Interop</span><span class="sxs-lookup"><span data-stu-id="629eb-132">Interop</span></span>|<span data-ttu-id="629eb-133">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="629eb-133">Optional attribute.</span></span> <span data-ttu-id="629eb-134">Windows ランタイムと COM に参照型をマーシャリングするためのポリシーを制御します。</span><span class="sxs-lookup"><span data-stu-id="629eb-134">Controls policy for marshaling reference types to Windows Runtime and COM.</span></span>|  
|`MarshalDelegate`|<span data-ttu-id="629eb-135">Interop</span><span class="sxs-lookup"><span data-stu-id="629eb-135">Interop</span></span>|<span data-ttu-id="629eb-136">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="629eb-136">Optional attribute.</span></span> <span data-ttu-id="629eb-137">ネイティブ コードへの関数ポインターとしてデリゲート型をマーシャリングするためのポリシーを制御します。</span><span class="sxs-lookup"><span data-stu-id="629eb-137">Controls policy for marshaling delegate types as function pointers to native code.</span></span>|  
|`MarshalStructure`|<span data-ttu-id="629eb-138">Interop</span><span class="sxs-lookup"><span data-stu-id="629eb-138">Interop</span></span>|<span data-ttu-id="629eb-139">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="629eb-139">Optional attribute.</span></span> <span data-ttu-id="629eb-140">値型をネイティブ コードにマーシャリングするためのポリシーを制御します。</span><span class="sxs-lookup"><span data-stu-id="629eb-140">Controls policy for marshaling value types to native code.</span></span>|  
  
## <a name="all-attributes"></a><span data-ttu-id="629eb-141">すべての属性</span><span class="sxs-lookup"><span data-stu-id="629eb-141">All attributes</span></span>  
  
|<span data-ttu-id="629eb-142">値</span><span class="sxs-lookup"><span data-stu-id="629eb-142">Value</span></span>|<span data-ttu-id="629eb-143">説明</span><span class="sxs-lookup"><span data-stu-id="629eb-143">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="629eb-144">*policy_setting*</span><span class="sxs-lookup"><span data-stu-id="629eb-144">*policy_setting*</span></span>|<span data-ttu-id="629eb-145">このポリシーの種類に適用する設定です。</span><span class="sxs-lookup"><span data-stu-id="629eb-145">The setting to apply to this policy type.</span></span> <span data-ttu-id="629eb-146">指定できる値は、`All`、`Auto`、`Excluded`、`Public`、`PublicAndInternal`、`Required Public`、`Required PublicAndInternal`、および `Required All` です。</span><span class="sxs-lookup"><span data-stu-id="629eb-146">Possible values are `All`, `Auto`, `Excluded`, `Public`, `PublicAndInternal`, `Required Public`, `Required PublicAndInternal`, and `Required All`.</span></span> <span data-ttu-id="629eb-147">詳細については、「[ランタイム ディレクティブのポリシー設定](../../../docs/framework/net-native/runtime-directive-policy-settings.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="629eb-147">For more information, see [Runtime Directive Policy Settings](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="629eb-148">子要素</span><span class="sxs-lookup"><span data-stu-id="629eb-148">Child Elements</span></span>  
 <span data-ttu-id="629eb-149">なし。</span><span class="sxs-lookup"><span data-stu-id="629eb-149">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="629eb-150">親要素</span><span class="sxs-lookup"><span data-stu-id="629eb-150">Parent Elements</span></span>  
  
|<span data-ttu-id="629eb-151">要素</span><span class="sxs-lookup"><span data-stu-id="629eb-151">Element</span></span>|<span data-ttu-id="629eb-152">説明</span><span class="sxs-lookup"><span data-stu-id="629eb-152">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="629eb-153">\<Type></span><span class="sxs-lookup"><span data-stu-id="629eb-153">\<Type></span></span>](../../../docs/framework/net-native/type-element-net-native.md)|<span data-ttu-id="629eb-154">型とそのすべてのメンバーにリフレクション ポリシーを適用します。</span><span class="sxs-lookup"><span data-stu-id="629eb-154">Applies reflection policy to a type and all its members.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="629eb-155">Remarks</span><span class="sxs-lookup"><span data-stu-id="629eb-155">Remarks</span></span>  
 <span data-ttu-id="629eb-156">`<AttributeImplies>` 要素は、それを含む型が属性 (つまり、<xref:System.Attribute?displayProperty=nameWithType> から継承されるクラス) である場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="629eb-156">The `<AttributeImplies>` element is used if its containing type is an attribute (that is, a class derived from <xref:System.Attribute?displayProperty=nameWithType>).</span></span> <span data-ttu-id="629eb-157">特定のプログラム要素に属性が適用される場合、`<AttributeImplies>` 要素によって定義されるポリシーがそのプログラム要素に適用されます。</span><span class="sxs-lookup"><span data-stu-id="629eb-157">If the attribute is applied to a particular program element, the policy defined by the `<AttributeImplies>` element applies to that program element.</span></span>  
  
 <span data-ttu-id="629eb-158">リフレクション、シリアル化、および相互運用属性はいずれも省略可能ですが、そのうち少なくとも 1 つが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="629eb-158">The reflection, serialization, and interop attributes are all optional, although at least one should be present.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="629eb-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="629eb-159">See also</span></span>
- [<span data-ttu-id="629eb-160">\<型 > 要素</span><span class="sxs-lookup"><span data-stu-id="629eb-160">\<Type> Element</span></span>](../../../docs/framework/net-native/type-element-net-native.md)
- [<span data-ttu-id="629eb-161">ランタイム ディレクティブ (rd.xml) 構成ファイル リファレンス</span><span class="sxs-lookup"><span data-stu-id="629eb-161">Runtime Directives (rd.xml) Configuration File Reference</span></span>](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="629eb-162">ランタイム ディレクティブ要素</span><span class="sxs-lookup"><span data-stu-id="629eb-162">Runtime Directive Elements</span></span>](../../../docs/framework/net-native/runtime-directive-elements.md)
- [<span data-ttu-id="629eb-163">ランタイム ディレクティブ ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="629eb-163">Runtime Directive Policy Settings</span></span>](../../../docs/framework/net-native/runtime-directive-policy-settings.md)
