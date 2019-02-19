---
title: '>> 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- '>>_CSharpKeyword'
helpviewer_keywords:
- '>> operator [C#]'
- right shift operator (>>) [C#]
ms.assetid: a07f8679-d318-4ef8-b38b-65903efb8056
ms.openlocfilehash: 809cd2cab29d3378892ea224cf846e9d0909b073
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219725"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="777fa-102">>> 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="777fa-102">>> operator (C# Reference)</span></span>

<span data-ttu-id="777fa-103">右シフト演算子 `>>` では、最初のオペランドが 2 番目のオペランドで定義されたビット数だけ右にシフトされます。</span><span class="sxs-lookup"><span data-stu-id="777fa-103">The right-shift operator `>>` shifts its first operand right by the number of bits defined by its second operand.</span></span> <span data-ttu-id="777fa-104">すべての整数型で `>>` 演算子がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="777fa-104">All integer types support the `>>` operator.</span></span> <span data-ttu-id="777fa-105">ただし、2 番目のオペランドの型は、[int](../keywords/int.md) または[事前に定義された `int` への暗黙的な数値変換](../keywords/implicit-numeric-conversions-table.md)を持つ型にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="777fa-105">However, the type of the second operand must be [int](../keywords/int.md) or a type that has a [predefined implicit numeric conversion](../keywords/implicit-numeric-conversions-table.md) to `int`.</span></span>

<span data-ttu-id="777fa-106">右シフト演算では、下位ビットが破棄されます。</span><span class="sxs-lookup"><span data-stu-id="777fa-106">The right-shift operation discards the low-order bits.</span></span> <span data-ttu-id="777fa-107">空の上位ビット位置は、最初のオペランドの型に基づいて次のように設定されます。</span><span class="sxs-lookup"><span data-stu-id="777fa-107">The high-order empty bit positions are set based on the type of the first operand as follows:</span></span>

- <span data-ttu-id="777fa-108">最初のオペランドの型が [int](../keywords/int.md) または [long](../keywords/long.md) である場合、右シフト演算子では、**算術**シフトが実行されます: 最初のオペランドの最上位ビット (符号ビット) の値が空の上位ビット位置に反映されます。</span><span class="sxs-lookup"><span data-stu-id="777fa-108">If the first operand is of type [int](../keywords/int.md) or [long](../keywords/long.md), the right-shift operator performs an **arithmetic** shift: the value of the most significant bit (the sign bit) of the first operand is propagated to the high-order empty bit positions.</span></span> <span data-ttu-id="777fa-109">つまり、最初のオペランドが負でない場合は空の上位ビット位置が 0 に設定され、負の場合は 1 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="777fa-109">That is, the high-order empty bit positions are set to zero if the first operand is non-negative and set to one if it's negative.</span></span>

- <span data-ttu-id="777fa-110">最初のオペランドの型が [uint](../keywords/uint.md) または [ulong](../keywords/ulong.md) である場合、右シフト演算子では、**論理**シフトが実行されます: 空の上位ビット位置は常に 0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="777fa-110">If the first operand is of type [uint](../keywords/uint.md) or [ulong](../keywords/ulong.md), the right-shift operator performs a **logical** shift: the high-order empty bit positions are always set to zero.</span></span>

<span data-ttu-id="777fa-111">次の例は、その動作を示します。</span><span class="sxs-lookup"><span data-stu-id="777fa-111">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[right shift example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShift)]

## <a name="shift-count"></a><span data-ttu-id="777fa-112">シフト数</span><span class="sxs-lookup"><span data-stu-id="777fa-112">Shift count</span></span>

<span data-ttu-id="777fa-113">式 `x >> count` では、実際のシフト数は次のように `x` の型によって異なります。</span><span class="sxs-lookup"><span data-stu-id="777fa-113">For the expression `x >> count`, the actual shift count depends on the type of `x` as follows:</span></span>

- <span data-ttu-id="777fa-114">`x` の型が [int](../keywords/int.md) または [uint](../keywords/uint.md) である場合、シフト数は、2 番目のオペランドの下位 *5* ビットで指定されます。</span><span class="sxs-lookup"><span data-stu-id="777fa-114">If the type of `x` is [int](../keywords/int.md) or [uint](../keywords/uint.md), the shift count is given by the low-order *five* bits of the second operand.</span></span> <span data-ttu-id="777fa-115">つまり、シフト数は `count & 0x1F` (または `count & 0b_1_1111`) から計算されます。</span><span class="sxs-lookup"><span data-stu-id="777fa-115">That is, the shift count is computed from `count & 0x1F` (or `count & 0b_1_1111`).</span></span>

- <span data-ttu-id="777fa-116">`x` の型が [long](../keywords/long.md) または [ulong](../keywords/ulong.md) である場合、シフト数は、2 番目のオペランドの下位 *6* ビットで指定されます。</span><span class="sxs-lookup"><span data-stu-id="777fa-116">If the type of `x` is [long](../keywords/long.md) or [ulong](../keywords/ulong.md), the shift count is given by the low-order *six* bits of the second operand.</span></span> <span data-ttu-id="777fa-117">つまり、シフト数は `count & 0x3F` (または `count & 0b_11_1111`) から計算されます。</span><span class="sxs-lookup"><span data-stu-id="777fa-117">That is, the shift count is computed from `count & 0x3F` (or `count & 0b_11_1111`).</span></span>

<span data-ttu-id="777fa-118">次の例は、その動作を示します。</span><span class="sxs-lookup"><span data-stu-id="777fa-118">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[shift count example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShiftByLargeCount)]

## <a name="remarks"></a><span data-ttu-id="777fa-119">解説</span><span class="sxs-lookup"><span data-stu-id="777fa-119">Remarks</span></span>

<span data-ttu-id="777fa-120">シフト演算が原因でオーバーフローが発生することはなく、[checked と unchecked](../keywords/checked-and-unchecked.md) のコンテキストで同じ結果が生成されることはありません。</span><span class="sxs-lookup"><span data-stu-id="777fa-120">Shift operations never cause overflows and produce the same results in [checked and unchecked](../keywords/checked-and-unchecked.md) contexts.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="777fa-121">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="777fa-121">Operator overloadability</span></span>

<span data-ttu-id="777fa-122">ユーザー定義型は `>>` 演算子を[オーバーロード](../keywords/operator.md)できます。</span><span class="sxs-lookup"><span data-stu-id="777fa-122">User-defined types can [overload](../keywords/operator.md) the `>>` operator.</span></span> <span data-ttu-id="777fa-123">ユーザー定義型 `T` では、`>>` 演算子がオーバーロードされます。最初のオペランドの型は `T` である必要があり、2 番目のオペランドの型は `int` である必要があります。</span><span class="sxs-lookup"><span data-stu-id="777fa-123">If a user-defined type `T` overloads the `>>` operator, the type of the first operand must be `T` and the type of the second operand must be `int`.</span></span> <span data-ttu-id="777fa-124">`>>` 演算子がオーバーロードされると、[右シフト代入演算子](right-shift-assignment-operator.md) `>>=` も暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="777fa-124">When the `>>` operator is overloaded, the [right-shift assignment operator](right-shift-assignment-operator.md) `>>=` is also implicitly overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="777fa-125">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="777fa-125">C# language specification</span></span>

<span data-ttu-id="777fa-126">詳細については、[C# 言語仕様](../language-specification/index.md)に関するページの「[シフト演算子](~/_csharplang/spec/expressions.md#shift-operators)」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="777fa-126">For more information, see the [Shift operators](~/_csharplang/spec/expressions.md#shift-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="777fa-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="777fa-127">See also</span></span>

- [<span data-ttu-id="777fa-128">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="777fa-128">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="777fa-129">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="777fa-129">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="777fa-130">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="777fa-130">C# operators</span></span>](index.md)
- [<span data-ttu-id="777fa-131"><< 演算子</span><span class="sxs-lookup"><span data-stu-id="777fa-131"><< operator</span></span>](left-shift-operator.md)