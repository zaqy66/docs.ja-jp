---
title: 列挙型 (F#)
description: F# のリテラルの代わりに列挙体を使用して、読みやすく、保守しやすいコードを作成する方法について説明します。
ms.date: 05/16/2016
ms.openlocfilehash: b51df53caf2e193496cb3694c913cbae08f7eaf5
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/27/2018
ms.locfileid: "43003100"
---
# <a name="enumerations"></a><span data-ttu-id="af752-103">列挙</span><span class="sxs-lookup"><span data-stu-id="af752-103">Enumerations</span></span>

<span data-ttu-id="af752-104">*列挙体*とも呼ばれます*列挙型*、および整数型は、ラベルが割り当てられ、値のサブセットにします。</span><span class="sxs-lookup"><span data-stu-id="af752-104">*Enumerations*, also known as *enums*, , are integral types where labels are assigned to a subset of the values.</span></span> <span data-ttu-id="af752-105">リテラルの代わりに使用すると、コードの読み取りおよび保守が容易になります。</span><span class="sxs-lookup"><span data-stu-id="af752-105">You can use them in place of literals to make code more readable and maintainable.</span></span>


## <a name="syntax"></a><span data-ttu-id="af752-106">構文</span><span class="sxs-lookup"><span data-stu-id="af752-106">Syntax</span></span>

```fsharp
type enum-name =
| value1 = integer-literal1
| value2 = integer-literal2
...
```

## <a name="remarks"></a><span data-ttu-id="af752-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="af752-107">Remarks</span></span>
<span data-ttu-id="af752-108">値を指定する点を除いてを単純な値を持つ判別共用体と同様、列挙型を検索します。</span><span class="sxs-lookup"><span data-stu-id="af752-108">An enumeration looks much like a discriminated union that has simple values, except that the values can be specified.</span></span> <span data-ttu-id="af752-109">通常、値は、0 または 1 から始まる整数またはビット位置を表す整数です。</span><span class="sxs-lookup"><span data-stu-id="af752-109">The values are typically integers that start at 0 or 1, or integers that represent bit positions.</span></span> <span data-ttu-id="af752-110">またを使用する必要がある列挙体のビット位置を表す場合は、[フラグ](xref:System.FlagsAttribute)属性。</span><span class="sxs-lookup"><span data-stu-id="af752-110">If an enumeration is intended to represent bit positions, you should also use the [Flags](xref:System.FlagsAttribute) attribute.</span></span>

<span data-ttu-id="af752-111">、たとえば、を使用できるようにリテラル、サフィックスを持つように、使用されるリテラルから列挙体の基になる型が決定されます`1u`、 `2u`、で、符号なし整数 (`uint32`) 型。</span><span class="sxs-lookup"><span data-stu-id="af752-111">The underlying type of the enumeration is determined from the literal that is used, so that, for example, you can use literals with a suffix, such as `1u`, `2u`, and so on, for an unsigned integer (`uint32`) type.</span></span>

<span data-ttu-id="af752-112">名前付きの値を参照するときにする必要がありますとして使用する列挙型自体の名前、修飾子は、`enum-name.value1`だけでなく、`value1`します。</span><span class="sxs-lookup"><span data-stu-id="af752-112">When you refer to the named values, you must use the name of the enumeration type itself as a qualifier, that is, `enum-name.value1`, not just `value1`.</span></span> <span data-ttu-id="af752-113">この動作は、判別共用体の動作とは異なります。</span><span class="sxs-lookup"><span data-stu-id="af752-113">This behavior differs from that of discriminated unions.</span></span> <span data-ttu-id="af752-114">これは、列挙型が常にあるため、 [RequireQualifiedAccess](https://msdn.microsoft.com/library/8b9b6ade-0471-4413-ac5d-638cd0de5f15)属性。</span><span class="sxs-lookup"><span data-stu-id="af752-114">This is because enumerations always have the [RequireQualifiedAccess](https://msdn.microsoft.com/library/8b9b6ade-0471-4413-ac5d-638cd0de5f15) attribute.</span></span>

<span data-ttu-id="af752-115">次のコードでは、宣言と列挙型の使用を示します。</span><span class="sxs-lookup"><span data-stu-id="af752-115">The following code shows the declaration and use of an enumeration.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2101.fs)]

<span data-ttu-id="af752-116">適切な演算子を使用して基になる型には、次のコードに示すように、列挙型を変換できます簡単にします。</span><span class="sxs-lookup"><span data-stu-id="af752-116">You can easily convert enumerations to the underlying type by using the appropriate operator, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2102.fs)]

<span data-ttu-id="af752-117">列挙型は、次の基になる型のいずれかを指定できます: `sbyte`、 `byte`、 `int16`、 `uint16`、 `int32`、 `uint32`、 `int64`、 `uint16`、 `uint64`、および`char`します。</span><span class="sxs-lookup"><span data-stu-id="af752-117">Enumerated types can have one of the following underlying types: `sbyte`, `byte`, `int16`, `uint16`, `int32`, `uint32`, `int64`, `uint16`, `uint64`, and `char`.</span></span> <span data-ttu-id="af752-118">列挙型は、.NET Framework でから継承された型として表されます。 `System.Enum`、から継承順番`System.ValueType`します。</span><span class="sxs-lookup"><span data-stu-id="af752-118">Enumeration types are represented in the .NET Framework as types that are inherited from `System.Enum`, which in turn is inherited from `System.ValueType`.</span></span> <span data-ttu-id="af752-119">したがって、スタックまたは親オブジェクトでのインラインに配置されている値型では、基になる型の任意の値が列挙体の有効な値。</span><span class="sxs-lookup"><span data-stu-id="af752-119">Thus, they are value types that are located on the stack or inline in the containing object, and any value of the underlying type is a valid value of the enumeration.</span></span> <span data-ttu-id="af752-120">これは重要な場合、パターン マッチに列挙値の名前のない値をキャッチするパターンを指定する必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="af752-120">This is significant when pattern matching on enumeration values, because you have to provide a pattern that catches the unnamed values.</span></span>

<span data-ttu-id="af752-121">`enum`関数の f# ライブラリで使用できます、定義済みの以外の値も、列挙値を生成する名前付きの値。</span><span class="sxs-lookup"><span data-stu-id="af752-121">The `enum` function in the F# library can be used to generate an enumeration value, even a value other than one of the predefined, named values.</span></span> <span data-ttu-id="af752-122">使用する、`enum`次のように機能します。</span><span class="sxs-lookup"><span data-stu-id="af752-122">You use the `enum` function as follows.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2103.fs)]

<span data-ttu-id="af752-123">既定の`enum`関数は型で機能`int32`します。</span><span class="sxs-lookup"><span data-stu-id="af752-123">The default `enum` function works with type `int32`.</span></span> <span data-ttu-id="af752-124">そのため、基になるその他の型を持つ列挙型で使用できません。</span><span class="sxs-lookup"><span data-stu-id="af752-124">Therefore, it cannot be used with enumeration types that have other underlying types.</span></span> <span data-ttu-id="af752-125">代わりに、次を使用します。</span><span class="sxs-lookup"><span data-stu-id="af752-125">Instead, use the following.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2104.fs)]

<span data-ttu-id="af752-126">さらに、ケースの列挙型として常に出力されます。`public`します。</span><span class="sxs-lookup"><span data-stu-id="af752-126">Additionally, cases for enums are always emitted as `public`.</span></span> <span data-ttu-id="af752-127">これは、c# および .NET プラットフォームの残りの部分に配置します。</span><span class="sxs-lookup"><span data-stu-id="af752-127">This is so that they align with C# and the rest of the .NET platform.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af752-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="af752-128">See Also</span></span>
[<span data-ttu-id="af752-129">F# 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="af752-129">F# Language Reference</span></span>](index.md)

[<span data-ttu-id="af752-130">キャストと変換</span><span class="sxs-lookup"><span data-stu-id="af752-130">Casting and Conversions</span></span>](casting-and-conversions.md)
