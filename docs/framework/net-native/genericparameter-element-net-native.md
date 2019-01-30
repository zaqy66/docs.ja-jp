---
title: <GenericParameter> 要素 (.NET ネイティブ)
ms.date: 03/30/2017
ms.assetid: cbd49732-3615-49a5-a900-f96947cdc3e6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: db9876727244d528ec3b7f1c3c9875bb5ca645b5
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55257773"
---
# <a name="genericparameter-element-net-native"></a><span data-ttu-id="4cb91-102">\<GenericParameter > 要素 (.NET ネイティブ)</span><span class="sxs-lookup"><span data-stu-id="4cb91-102">\<GenericParameter> Element (.NET Native)</span></span>
<span data-ttu-id="4cb91-103">ジェネリック型またはメソッドのパラメーターの型にポリシーを適用します。</span><span class="sxs-lookup"><span data-stu-id="4cb91-103">Applies policy to the parameter type of a generic type or method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4cb91-104">構文</span><span class="sxs-lookup"><span data-stu-id="4cb91-104">Syntax</span></span>  
  
```xml  
<GenericParameter Name="generic_parameter_name"  
                  Activate="policy_type"  
                  Browse="policy_type"  
                  Dynamic="policy_type"  
                  Serialize="policy_type"  
                  DataContractSerializer="policy_type"  
                  DataContractJsonSerializer="policy_type"  
                  XmlSerializer="policy_type"  
                  MarshalObject="policy_type"  
                  MarshalDelegate="policy_type"  
                  MarshalStructure="policy_type"  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4cb91-105">属性および要素</span><span class="sxs-lookup"><span data-stu-id="4cb91-105">Attributes and Elements</span></span>  
 <span data-ttu-id="4cb91-106">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="4cb91-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4cb91-107">属性</span><span class="sxs-lookup"><span data-stu-id="4cb91-107">Attributes</span></span>  
  
|<span data-ttu-id="4cb91-108">属性</span><span class="sxs-lookup"><span data-stu-id="4cb91-108">Attribute</span></span>|<span data-ttu-id="4cb91-109">属性の型</span><span class="sxs-lookup"><span data-stu-id="4cb91-109">Attribute type</span></span>|<span data-ttu-id="4cb91-110">説明</span><span class="sxs-lookup"><span data-stu-id="4cb91-110">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="4cb91-111">全般</span><span class="sxs-lookup"><span data-stu-id="4cb91-111">General</span></span>|<span data-ttu-id="4cb91-112">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="4cb91-112">Required attribute.</span></span> <span data-ttu-id="4cb91-113">ジェネリック パラメーターの名前。</span><span class="sxs-lookup"><span data-stu-id="4cb91-113">The name of the generic parameter.</span></span> <span data-ttu-id="4cb91-114">たとえば、ジェネリック デリゲート <xref:System.Func%603> の場合、デリゲートの戻り値に実行時ポリシーを適用するための `Name` 属性の値は "TResult" です。</span><span class="sxs-lookup"><span data-stu-id="4cb91-114">For example, for the generic delegate <xref:System.Func%603>, the value of the `Name` attribute is "TResult" to apply runtime policy to the delegate's return value.</span></span>|  
|`Activate`|<span data-ttu-id="4cb91-115">リフレクション</span><span class="sxs-lookup"><span data-stu-id="4cb91-115">Reflection</span></span>|<span data-ttu-id="4cb91-116">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="4cb91-116">Optional attribute.</span></span> <span data-ttu-id="4cb91-117">コンストラクターへの実行時アクセスを制御して、インスタンスのアクティブ化を有効にします。</span><span class="sxs-lookup"><span data-stu-id="4cb91-117">Controls runtime access to constructors to enable activation of instances.</span></span>|  
|`Browse`|<span data-ttu-id="4cb91-118">リフレクション</span><span class="sxs-lookup"><span data-stu-id="4cb91-118">Reflection</span></span>|<span data-ttu-id="4cb91-119">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="4cb91-119">Optional attribute.</span></span> <span data-ttu-id="4cb91-120">プログラム要素に関する情報の照会を制御しますが、実行時アクセスは有効にしません。</span><span class="sxs-lookup"><span data-stu-id="4cb91-120">Controls querying for information about program elements, but does not enable any runtime access.</span></span>|  
|`Dynamic`|<span data-ttu-id="4cb91-121">リフレクション</span><span class="sxs-lookup"><span data-stu-id="4cb91-121">Reflection</span></span>|<span data-ttu-id="4cb91-122">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="4cb91-122">Optional attribute.</span></span> <span data-ttu-id="4cb91-123">コンストラクター、メソッド、フィールド、プロパティ、およびイベントを含むすべての型のメンバーへの実行時アクセスを制御して、動的プログラミングを有効にします。</span><span class="sxs-lookup"><span data-stu-id="4cb91-123">Controls runtime access to all type members, including constructors, methods, fields, properties, and events, to enable dynamic programming.</span></span>|  
|`Serialize`|<span data-ttu-id="4cb91-124">シリアル化</span><span class="sxs-lookup"><span data-stu-id="4cb91-124">Serialization</span></span>|<span data-ttu-id="4cb91-125">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="4cb91-125">Optional attribute.</span></span> <span data-ttu-id="4cb91-126">コンストラクター、フィールド、およびプロパティへの実行時アクセスを制御し、Newtonsoft の JSON シリアライザーなどのライブラリによって型インスタンスをシリアル化および逆シリアル化できるようにします。</span><span class="sxs-lookup"><span data-stu-id="4cb91-126">Controls runtime access to constructors, fields, and properties, to enable type instances to be serialized and deserialized by libraries such as the Newtonsoft JSON serializer.</span></span>|  
|`DataContractSerializer`|<span data-ttu-id="4cb91-127">シリアル化</span><span class="sxs-lookup"><span data-stu-id="4cb91-127">Serialization</span></span>|<span data-ttu-id="4cb91-128">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="4cb91-128">Optional attribute.</span></span> <span data-ttu-id="4cb91-129"><xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> クラスを使用するシリアル化のポリシーを制御します。</span><span class="sxs-lookup"><span data-stu-id="4cb91-129">Controls policy for serialization that uses the <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> class.</span></span>|  
|`DataContractJsonSerializer`|<span data-ttu-id="4cb91-130">シリアル化</span><span class="sxs-lookup"><span data-stu-id="4cb91-130">Serialization</span></span>|<span data-ttu-id="4cb91-131">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="4cb91-131">Optional attribute.</span></span> <span data-ttu-id="4cb91-132"><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> クラスを使用する JSON シリアル化のポリシーを制御します。</span><span class="sxs-lookup"><span data-stu-id="4cb91-132">Controls policy for JSON serialization that uses the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> class.</span></span>|  
|`XmlSerializer`|<span data-ttu-id="4cb91-133">シリアル化</span><span class="sxs-lookup"><span data-stu-id="4cb91-133">Serialization</span></span>|<span data-ttu-id="4cb91-134">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="4cb91-134">Optional attribute.</span></span> <span data-ttu-id="4cb91-135"><xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> クラスを使用する XML シリアル化のポリシーを制御します。</span><span class="sxs-lookup"><span data-stu-id="4cb91-135">Controls policy for XML serialization that uses the <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> class.</span></span>|  
|`MarshalObject`|<span data-ttu-id="4cb91-136">Interop</span><span class="sxs-lookup"><span data-stu-id="4cb91-136">Interop</span></span>|<span data-ttu-id="4cb91-137">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="4cb91-137">Optional attribute.</span></span> <span data-ttu-id="4cb91-138">Windows ランタイムと COM に参照型をマーシャリングするためのポリシーを制御します。</span><span class="sxs-lookup"><span data-stu-id="4cb91-138">Controls policy for marshaling reference types to Windows Runtime and COM.</span></span>|  
|`MarshalDelegate`|<span data-ttu-id="4cb91-139">Interop</span><span class="sxs-lookup"><span data-stu-id="4cb91-139">Interop</span></span>|<span data-ttu-id="4cb91-140">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="4cb91-140">Optional attribute.</span></span> <span data-ttu-id="4cb91-141">ネイティブ コードへの関数ポインターとしてデリゲート型をマーシャリングするためのポリシーを制御します。</span><span class="sxs-lookup"><span data-stu-id="4cb91-141">Controls policy for marshaling delegate types as function pointers to native code.</span></span>|  
|`MarshalStructure`|<span data-ttu-id="4cb91-142">Interop</span><span class="sxs-lookup"><span data-stu-id="4cb91-142">Interop</span></span>|<span data-ttu-id="4cb91-143">省略可能な属性です。</span><span class="sxs-lookup"><span data-stu-id="4cb91-143">Optional attribute.</span></span> <span data-ttu-id="4cb91-144">値型をネイティブ コードにマーシャリングするためのポリシーを制御します。</span><span class="sxs-lookup"><span data-stu-id="4cb91-144">Controls policy for marshaling value types to native code.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="4cb91-145">Name 属性</span><span class="sxs-lookup"><span data-stu-id="4cb91-145">Name attribute</span></span>  
  
|<span data-ttu-id="4cb91-146">値</span><span class="sxs-lookup"><span data-stu-id="4cb91-146">Value</span></span>|<span data-ttu-id="4cb91-147">説明</span><span class="sxs-lookup"><span data-stu-id="4cb91-147">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="4cb91-148">*generic_parameter_name*</span><span class="sxs-lookup"><span data-stu-id="4cb91-148">*generic_parameter_name*</span></span>|<span data-ttu-id="4cb91-149">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="4cb91-149">Required attribute.</span></span> <span data-ttu-id="4cb91-150">ジェネリック型パラメーターの名前。</span><span class="sxs-lookup"><span data-stu-id="4cb91-150">The name of the generic type parameter.</span></span> <span data-ttu-id="4cb91-151">たとえば、ジェネリック デリゲート <xref:System.Func%603> の場合、*generic_parameter_name* の値 "TResult" によって、デリゲートの戻り値に実行時ポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="4cb91-151">For example, for the generic delegate <xref:System.Func%603>, a *generic_parameter_name* value of "TResult" applies runtime policy to the delegate's return value.</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="4cb91-152">その他すべての属性</span><span class="sxs-lookup"><span data-stu-id="4cb91-152">All other attributes</span></span>  
  
|<span data-ttu-id="4cb91-153">値</span><span class="sxs-lookup"><span data-stu-id="4cb91-153">Value</span></span>|<span data-ttu-id="4cb91-154">説明</span><span class="sxs-lookup"><span data-stu-id="4cb91-154">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="4cb91-155">*policy_setting*</span><span class="sxs-lookup"><span data-stu-id="4cb91-155">*policy_setting*</span></span>|<span data-ttu-id="4cb91-156">このポリシーの種類に適用する設定です。</span><span class="sxs-lookup"><span data-stu-id="4cb91-156">The setting to apply to this policy type.</span></span> <span data-ttu-id="4cb91-157">指定できる値は、`All`、`Public`、`PublicAndInternal`、`Required Public`、`Required PublicAndInternal`、および `Required All` です。</span><span class="sxs-lookup"><span data-stu-id="4cb91-157">Possible values are `All`, `Public`, `PublicAndInternal`, `Required Public`, `Required PublicAndInternal`, and `Required All`.</span></span> <span data-ttu-id="4cb91-158">詳細については、「[ランタイム ディレクティブのポリシー設定](../../../docs/framework/net-native/runtime-directive-policy-settings.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cb91-158">For more information, see [Runtime Directive Policy Settings](../../../docs/framework/net-native/runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4cb91-159">子要素</span><span class="sxs-lookup"><span data-stu-id="4cb91-159">Child Elements</span></span>  
 <span data-ttu-id="4cb91-160">なし。</span><span class="sxs-lookup"><span data-stu-id="4cb91-160">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4cb91-161">親要素</span><span class="sxs-lookup"><span data-stu-id="4cb91-161">Parent Elements</span></span>  
  
|<span data-ttu-id="4cb91-162">要素</span><span class="sxs-lookup"><span data-stu-id="4cb91-162">Element</span></span>|<span data-ttu-id="4cb91-163">説明</span><span class="sxs-lookup"><span data-stu-id="4cb91-163">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4cb91-164">\<Method></span><span class="sxs-lookup"><span data-stu-id="4cb91-164">\<Method></span></span>](../../../docs/framework/net-native/method-element-net-native.md)|<span data-ttu-id="4cb91-165">コンストラクターまたはメソッドにランタイム リフレクション ポリシーを適用します。</span><span class="sxs-lookup"><span data-stu-id="4cb91-165">Applies runtime reflection policy to a constructor or method.</span></span>|  
|[<span data-ttu-id="4cb91-166">\<Type></span><span class="sxs-lookup"><span data-stu-id="4cb91-166">\<Type></span></span>](../../../docs/framework/net-native/type-element-net-native.md)|<span data-ttu-id="4cb91-167">クラスや構造体など、特定の型にランタイム リフレクション ポリシーを適用します。</span><span class="sxs-lookup"><span data-stu-id="4cb91-167">Applies runtime reflection policy to a particular type, such as a class or structure.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4cb91-168">Remarks</span><span class="sxs-lookup"><span data-stu-id="4cb91-168">Remarks</span></span>  
 <span data-ttu-id="4cb91-169">`<GenericParameter>` 要素は [\<Method>](../../../docs/framework/net-native/method-element-net-native.md) 要素または [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) 要素のいずれかの子で、ジェネリック型またはメソッド シグネチャでの名前によって指定される、特定のジェネリック型パラメーターにポリシーを適用するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4cb91-169">The `<GenericParameter>` element is a child of either the [\<Method>](../../../docs/framework/net-native/method-element-net-native.md) or [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) element and is used to apply policy to a particular generic type parameter, which is specified by its name in the generic type or method signature.</span></span>  
  
 <span data-ttu-id="4cb91-170">`<GenericParameter>` 要素は、シリアライザーで使用する場合に最も役立ちます。</span><span class="sxs-lookup"><span data-stu-id="4cb91-170">The `<GenericParameter>` element is most useful when used with serializers.</span></span> <span data-ttu-id="4cb91-171">次の例では、`<GenericParameter>` 要素を使用して、NewtonSoft の JSON シリアライザーの [JsonConvert.DeserializeObject\<T>(String)](https://www.newtonsoft.com/json/help/html/M_Newtonsoft_Json_JsonConvert_DeserializeObject__1.htm) メソッド オーバーロードの呼び出しで、`T` 型にポリシーを適用します。</span><span class="sxs-lookup"><span data-stu-id="4cb91-171">The following example uses the `<GenericParameter>` element to apply policy to the type `T` in calls to the NewtonSoft JSON serializer's [JsonConvert.DeserializeObject\<T>(String)](https://www.newtonsoft.com/json/help/html/M_Newtonsoft_Json_JsonConvert_DeserializeObject__1.htm) method overloads.</span></span>  
  
```xml  
<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">  
   <Type Name="Newtonsoft.Json.JsonConvert" >  
      <Method Name="DeserializeObject{T}">  
         <GenericParameter Name="T" Serialize="Required All" />  
      </Method>  
   </Type>  
</Directives>  
```  
  
## <a name="see-also"></a><span data-ttu-id="4cb91-172">関連項目</span><span class="sxs-lookup"><span data-stu-id="4cb91-172">See also</span></span>
- [<span data-ttu-id="4cb91-173">\<Method> 要素</span><span class="sxs-lookup"><span data-stu-id="4cb91-173">\<Method> Element</span></span>](../../../docs/framework/net-native/method-element-net-native.md)
- [<span data-ttu-id="4cb91-174">\<型 > 要素</span><span class="sxs-lookup"><span data-stu-id="4cb91-174">\<Type> Element</span></span>](../../../docs/framework/net-native/type-element-net-native.md)
- [<span data-ttu-id="4cb91-175">ランタイム ディレクティブ (rd.xml) 構成ファイル リファレンス</span><span class="sxs-lookup"><span data-stu-id="4cb91-175">Runtime Directives (rd.xml) Configuration File Reference</span></span>](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="4cb91-176">ランタイム ディレクティブ ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="4cb91-176">Runtime Directive Policy Settings</span></span>](../../../docs/framework/net-native/runtime-directive-policy-settings.md)
- [<span data-ttu-id="4cb91-177">ランタイム ディレクティブ要素</span><span class="sxs-lookup"><span data-stu-id="4cb91-177">Runtime Directive Elements</span></span>](../../../docs/framework/net-native/runtime-directive-elements.md)
