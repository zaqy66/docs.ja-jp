---
title: '|| 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 11/06/2018
f1_keywords:
- '||_CSharpKeyword'
helpviewer_keywords:
- logical OR operator [C#]
- conditional-OR operator (||) [C#]
- '|| operator [C#]'
ms.assetid: 7d442d8e-400d-421f-b4d2-034bf82bcbdc
ms.openlocfilehash: 079c021eb68ece097c7f644416f1e9469a82dcea
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54415430"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="5802d-102">|| 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="5802d-102">|| Operator (C# Reference)</span></span>

<span data-ttu-id="5802d-103">条件論理 OR 演算子 `||` は、"短絡" 論理 OR 演算子とも呼ばれ、その [bool](../keywords/bool.md) オペランドの論理 OR を計算します。</span><span class="sxs-lookup"><span data-stu-id="5802d-103">The conditional logical OR operator `||`, also known as the "short-circuiting" logical OR operator, computes the logical OR of its [bool](../keywords/bool.md) operands.</span></span> <span data-ttu-id="5802d-104">`x` または `y` のどちらかが `true` と評価された場合、`x || y` の結果は `true` になります。</span><span class="sxs-lookup"><span data-stu-id="5802d-104">The result of `x || y` is `true` if either `x` or `y` evaluates to `true`.</span></span> <span data-ttu-id="5802d-105">それ以外の場合、結果は `false` です。</span><span class="sxs-lookup"><span data-stu-id="5802d-105">Otherwise, the result is `false`.</span></span> <span data-ttu-id="5802d-106">最初のオペランドが `true` と評価されると、2 番目のオペランドは評価されず、演算の結果は `true` になります。</span><span class="sxs-lookup"><span data-stu-id="5802d-106">If the first operand evaluates to `true`, the second operand is not evaluated and the result of operation is `true`.</span></span> <span data-ttu-id="5802d-107">次の例は、その動作を示します。</span><span class="sxs-lookup"><span data-stu-id="5802d-107">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[conditional logical OR](~/samples/snippets/csharp/language-reference/operators/ConditionalLogicalOperatorsExamples.cs#Or)]

<span data-ttu-id="5802d-108">[論理 OR 演算子](or-operator.md) `|` もその `bool` オペランドの論理 OR を計算しますが、常に両方のオペランドを評価します。</span><span class="sxs-lookup"><span data-stu-id="5802d-108">The [logical OR operator](or-operator.md) `|` also computes the logical OR of its `bool` operands, but always evaluates both operands.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="5802d-109">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="5802d-109">Operator overloadability</span></span>

<span data-ttu-id="5802d-110">ユーザー定義型は条件論理 OR 演算子をオーバーロードできません。</span><span class="sxs-lookup"><span data-stu-id="5802d-110">A user-defined type cannot overload the conditional logical OR operator.</span></span> <span data-ttu-id="5802d-111">ただし、ユーザー定義型が[論理 OR](or-operator.md) と [true および false 演算子](../keywords/true-false-operators.md)を特定の方法でオーバーロードしている場合は、その型のオペランドに対する `||` 演算の評価が可能になります。</span><span class="sxs-lookup"><span data-stu-id="5802d-111">However, if a user-defined type overloads the [logical OR](or-operator.md) and [true and false operators](../keywords/true-false-operators.md) in a certain way, the `||` operation can be evaluated for the operands of that type.</span></span> <span data-ttu-id="5802d-112">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[ユーザー定義型条件論理演算子](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5802d-112">For more information, see the [User-defined conditional logical operators](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="5802d-113">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="5802d-113">C# language specification</span></span>

<span data-ttu-id="5802d-114">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[条件論理演算子](~/_csharplang/spec/expressions.md#conditional-logical-operators)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5802d-114">For more information, see the [Conditional logical operators](~/_csharplang/spec/expressions.md#conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5802d-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="5802d-115">See also</span></span>

- [<span data-ttu-id="5802d-116">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="5802d-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="5802d-117">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="5802d-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="5802d-118">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="5802d-118">C# Operators</span></span>](index.md)
- [<span data-ttu-id="5802d-119">&& 演算子</span><span class="sxs-lookup"><span data-stu-id="5802d-119">&& operator</span></span>](conditional-and-operator.md)
- [<span data-ttu-id="5802d-120">\! 演算子</span><span class="sxs-lookup"><span data-stu-id="5802d-120">\! operator</span></span>](logical-negation-operator.md)
- [<span data-ttu-id="5802d-121">| 演算子</span><span class="sxs-lookup"><span data-stu-id="5802d-121">| operator</span></span>](or-operator.md)
