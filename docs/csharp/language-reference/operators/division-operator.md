---
title: / 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 12/13/2018
f1_keywords:
- /_CSharpKeyword
helpviewer_keywords:
- / operator [C#]
- division operator [C#]
ms.assetid: d155e496-678f-4efa-bebe-2bd08da2c5af
ms.openlocfilehash: 45bcd64b60e7d13f389064faefeda815ea1f32c9
ms.sourcegitcommit: d6e419f9d9cd7e8f21ebf5acde6d016c16332579
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/12/2018
ms.locfileid: "53286534"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="4b7b3-102">/ 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="4b7b3-102">/ Operator (C# Reference)</span></span>

<span data-ttu-id="4b7b3-103">除算演算子 `/` は、1 つ目のオペランドを 2 つ目のオペランドで除算します。</span><span class="sxs-lookup"><span data-stu-id="4b7b3-103">The division operator `/` divides its first operand by its second operand.</span></span> <span data-ttu-id="4b7b3-104">数値型はすべて除算演算子に対応しています。</span><span class="sxs-lookup"><span data-stu-id="4b7b3-104">All numeric types support the division operator.</span></span>

## <a name="integer-division"></a><span data-ttu-id="4b7b3-105">整数の除算</span><span class="sxs-lookup"><span data-stu-id="4b7b3-105">Integer division</span></span>

<span data-ttu-id="4b7b3-106">整数型のオペランドに対する `/` 演算子の結果は、整数型で、2 つのオペランドの商を 0 方向に丸めたものと等しくなります。</span><span class="sxs-lookup"><span data-stu-id="4b7b3-106">For the operands of integer types, the result of the `/` operator is of an integer type and equals the quotient of the two operands rounded towards zero:</span></span>

[!code-csharp-interactive[integer division](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#Integer)]

<span data-ttu-id="4b7b3-107">2 つのオペランドの商を浮動小数点数として取得するには、`float`、`double`、または `decimal` 型を使います。</span><span class="sxs-lookup"><span data-stu-id="4b7b3-107">To obtain the quotient of the two operands as a floating-point number, use the `float`, `double`, or `decimal` type:</span></span>

[!code-csharp-interactive[integer as floating-point division](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#IntegerAsFloatingPoint)]

## <a name="floating-point-division"></a><span data-ttu-id="4b7b3-108">浮動小数点の除算</span><span class="sxs-lookup"><span data-stu-id="4b7b3-108">Floating-point division</span></span>

<span data-ttu-id="4b7b3-109">`float`、`double`、`decimal` 型に対する `/` 演算子の結果は、2 つのオペランドの商となります。</span><span class="sxs-lookup"><span data-stu-id="4b7b3-109">For the `float`, `double`, and `decimal` types, the result of the `/` operator is the quotient of the two operands:</span></span>

[!code-csharp-interactive[floating-point division](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#FloatingPoint)]

<span data-ttu-id="4b7b3-110">オペランドの 1 つが `decimal` であった場合、もう 1 つのオペランドを `float` や `double` にすることはできません。`float` と `double` は暗黙的に `decimal` に変換できないためです。</span><span class="sxs-lookup"><span data-stu-id="4b7b3-110">If one of the operands is `decimal`, another operand can be neither `float` nor `double`, because neither `float` nor `double` is implicitly convertible to `decimal`.</span></span> <span data-ttu-id="4b7b3-111">`float` または `double` オペランドは明示的に `decimal` 型に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b7b3-111">You must explicitly convert the `float` or `double` operand to the `decimal` type.</span></span> <span data-ttu-id="4b7b3-112">数値型間の暗黙的な変換について詳しくは、「[暗黙的な数値変換の一覧表](../keywords/implicit-numeric-conversions-table.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4b7b3-112">For more information about implicit conversions between numeric types, see [Implicit numeric conversions table](../keywords/implicit-numeric-conversions-table.md).</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="4b7b3-113">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="4b7b3-113">Operator overloadability</span></span>

<span data-ttu-id="4b7b3-114">ユーザー定義型は `/` 演算子を[オーバーロード](../keywords/operator.md)できます。</span><span class="sxs-lookup"><span data-stu-id="4b7b3-114">User-defined types can [overload](../keywords/operator.md) the `/` operator.</span></span> <span data-ttu-id="4b7b3-115">`/` 演算子をオーバーロードすると、[除算代入演算子](division-assignment-operator.md) `/=` も暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="4b7b3-115">When the `/` operator is overloaded, the [division assignment operator](division-assignment-operator.md) `/=` is also implicitly overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="4b7b3-116">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="4b7b3-116">C# language specification</span></span>

<span data-ttu-id="4b7b3-117">詳細については、「[C# 言語仕様](../language-specification/index.md)」の「[除算演算子](~/_csharplang/spec/expressions.md#division-operator)」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b7b3-117">For more information, see the [Division operator](~/_csharplang/spec/expressions.md#division-operator) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4b7b3-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b7b3-118">See also</span></span>

- [<span data-ttu-id="4b7b3-119">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="4b7b3-119">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="4b7b3-120">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="4b7b3-120">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="4b7b3-121">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="4b7b3-121">C# Operators</span></span>](index.md)
- [<span data-ttu-id="4b7b3-122">% 演算子</span><span class="sxs-lookup"><span data-stu-id="4b7b3-122">% Operator</span></span>](remainder-operator.md)
