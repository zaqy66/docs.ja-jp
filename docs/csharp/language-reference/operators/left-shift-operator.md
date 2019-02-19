---
title: << 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- <<_CSharpKeyword
helpviewer_keywords:
- left shift operator (<<) [C#]
- << operator [C#]
ms.assetid: a654eb56-1ff7-4bf3-9064-b631be0cdccc
ms.openlocfilehash: deea2d0f720ba7f096e65c67378586bc88f24673
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219438"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="f7b5d-102">\<\< 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="f7b5d-102">\<\< operator (C# Reference)</span></span>

<span data-ttu-id="f7b5d-103">左シフト演算子 `<<` では、最初のオペランドが 2 番目のオペランドで定義されたビット数だけ左にシフトされます。</span><span class="sxs-lookup"><span data-stu-id="f7b5d-103">The left-shift operator `<<` shifts its first operand left by the number of bits defined by its second operand.</span></span> <span data-ttu-id="f7b5d-104">すべての整数型で `<<` 演算子がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="f7b5d-104">All integer types support the `<<` operator.</span></span> <span data-ttu-id="f7b5d-105">ただし、2 番目のオペランドの型は、[int](../keywords/int.md) または[事前に定義された `int` への暗黙的な数値変換](../keywords/implicit-numeric-conversions-table.md)を持つ型にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b5d-105">However, the type of the second operand must be [int](../keywords/int.md) or a type that has a [predefined implicit numeric conversion](../keywords/implicit-numeric-conversions-table.md) to `int`.</span></span>

<span data-ttu-id="f7b5d-106">次の例に示すように、結果の型の範囲外にある上位ビットは破棄され、空の下位ビット位置は、ゼロに設定されます。</span><span class="sxs-lookup"><span data-stu-id="f7b5d-106">The high-order bits that are outside the range of the result type are discarded, and the low-order empty bit positions are set to zero, as the following example shows:</span></span>

[!code-csharp-interactive[left shift example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#LeftShift)]

## <a name="shift-count"></a><span data-ttu-id="f7b5d-107">シフト数</span><span class="sxs-lookup"><span data-stu-id="f7b5d-107">Shift count</span></span>

<span data-ttu-id="f7b5d-108">式 `x << count` では、実際のシフト数は次のように `x` の型によって異なります。</span><span class="sxs-lookup"><span data-stu-id="f7b5d-108">For the expression `x << count`, the actual shift count depends on the type of `x` as follows:</span></span>

- <span data-ttu-id="f7b5d-109">`x` の型が [int](../keywords/int.md) または [uint](../keywords/uint.md) である場合、シフト数は、2 番目のオペランドの下位 *5* ビットで指定されます。</span><span class="sxs-lookup"><span data-stu-id="f7b5d-109">If the type of `x` is [int](../keywords/int.md) or [uint](../keywords/uint.md), the shift count is given by the low-order *five* bits of the second operand.</span></span> <span data-ttu-id="f7b5d-110">つまり、シフト数は `count & 0x1F` (または `count & 0b_1_1111`) から計算されます。</span><span class="sxs-lookup"><span data-stu-id="f7b5d-110">That is, the shift count is computed from `count & 0x1F` (or `count & 0b_1_1111`).</span></span>

- <span data-ttu-id="f7b5d-111">`x` の型が [long](../keywords/long.md) または [ulong](../keywords/ulong.md) である場合、シフト数は、2 番目のオペランドの下位 *6* ビットで指定されます。</span><span class="sxs-lookup"><span data-stu-id="f7b5d-111">If the type of `x` is [long](../keywords/long.md) or [ulong](../keywords/ulong.md), the shift count is given by the low-order *six* bits of the second operand.</span></span> <span data-ttu-id="f7b5d-112">つまり、シフト数は `count & 0x3F` (または `count & 0b_11_1111`) から計算されます。</span><span class="sxs-lookup"><span data-stu-id="f7b5d-112">That is, the shift count is computed from `count & 0x3F` (or `count & 0b_11_1111`).</span></span>

<span data-ttu-id="f7b5d-113">次の例は、その動作を示します。</span><span class="sxs-lookup"><span data-stu-id="f7b5d-113">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[shift count example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#LeftShiftByLargeCount)]

## <a name="remarks"></a><span data-ttu-id="f7b5d-114">解説</span><span class="sxs-lookup"><span data-stu-id="f7b5d-114">Remarks</span></span>

<span data-ttu-id="f7b5d-115">シフト演算が原因でオーバーフローが発生することはなく、[checked と unchecked](../keywords/checked-and-unchecked.md) のコンテキストで同じ結果が生成されることはありません。</span><span class="sxs-lookup"><span data-stu-id="f7b5d-115">Shift operations never cause overflows and produce the same results in [checked and unchecked](../keywords/checked-and-unchecked.md) contexts.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="f7b5d-116">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="f7b5d-116">Operator overloadability</span></span>

<span data-ttu-id="f7b5d-117">ユーザー定義型は `<<` 演算子を[オーバーロード](../keywords/operator.md)できます。</span><span class="sxs-lookup"><span data-stu-id="f7b5d-117">User-defined types can [overload](../keywords/operator.md) the `<<` operator.</span></span> <span data-ttu-id="f7b5d-118">ユーザー定義型 `T` では、`<<` 演算子がオーバーロードされます。最初のオペランドの型は `T` である必要があり、2 番目のオペランドの型は `int` である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b5d-118">If a user-defined type `T` overloads the `<<` operator, the type of the first operand must be `T` and the type of the second operand must be `int`.</span></span> <span data-ttu-id="f7b5d-119">`<<` 演算子がオーバーロードされると、[左シフト代入演算子](left-shift-assignment-operator.md) `<<=` も暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="f7b5d-119">When the `<<` operator is overloaded, the [left-shift assignment operator](left-shift-assignment-operator.md) `<<=` is also implicitly overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="f7b5d-120">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="f7b5d-120">C# language specification</span></span>

<span data-ttu-id="f7b5d-121">詳細については、[C# 言語仕様](../language-specification/index.md)に関するページの「[シフト演算子](~/_csharplang/spec/expressions.md#shift-operators)」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7b5d-121">For more information, see the [Shift operators](~/_csharplang/spec/expressions.md#shift-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f7b5d-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="f7b5d-122">See also</span></span>

- [<span data-ttu-id="f7b5d-123">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="f7b5d-123">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="f7b5d-124">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="f7b5d-124">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="f7b5d-125">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="f7b5d-125">C# Operators</span></span>](index.md)
- [<span data-ttu-id="f7b5d-126">>> 演算子</span><span class="sxs-lookup"><span data-stu-id="f7b5d-126">>> operator</span></span>](right-shift-operator.md)
