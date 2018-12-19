---
title: '&amp;&amp; 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 11/06/2018
f1_keywords:
- '&&_CSharpKeyword'
helpviewer_keywords:
- '&& operator [C#]'
- logical AND operator [C#]
ms.assetid: 2e4f0a1c-92a3-40f8-8e3b-17b607f20c31
ms.openlocfilehash: 82442f50275f21e0a0748951dc50628a8d7e11bb
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243593"
---
# <a name="ampamp-operator-c-reference"></a><span data-ttu-id="102ab-102">&amp;&amp; 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="102ab-102">&amp;&amp; Operator (C# Reference)</span></span>

<span data-ttu-id="102ab-103">条件論理 AND 演算子 `&&` は、"短絡" 論理 AND 演算子とも呼ばれ、その [bool](../keywords/bool.md) オペランドの論理 AND を計算します。</span><span class="sxs-lookup"><span data-stu-id="102ab-103">The conditional logical AND operator `&&`, also known as the "short-circuiting" logical AND operator, computes the logical AND of its [bool](../keywords/bool.md) operands.</span></span> <span data-ttu-id="102ab-104">`x` と `y` の両方が `true` と評価されれば、`x && y` の結果は `true` です。</span><span class="sxs-lookup"><span data-stu-id="102ab-104">The result of `x && y` is `true` if both `x` and `y` evaluate to `true`.</span></span> <span data-ttu-id="102ab-105">それ以外の場合、結果は `false` です。</span><span class="sxs-lookup"><span data-stu-id="102ab-105">Otherwise, the result is `false`.</span></span> <span data-ttu-id="102ab-106">最初のオペランドが `false` と評価されると、2 番目のオペランドは評価されず、演算の結果は `false` になります。</span><span class="sxs-lookup"><span data-stu-id="102ab-106">If the first operand evaluates to `false`, the second operand is not evaluated and the result of operation is `false`.</span></span> <span data-ttu-id="102ab-107">次の例は、その動作を示します。</span><span class="sxs-lookup"><span data-stu-id="102ab-107">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[conditional logical AND](~/samples/snippets/csharp/language-reference/operators/ConditionalLogicalOperatorsExamples.cs#And)]

<span data-ttu-id="102ab-108">[論理 AND 演算子](and-operator.md) `&` もその `bool` オペランドの論理 AND を計算しますが、常に両方のオペランドを評価します。</span><span class="sxs-lookup"><span data-stu-id="102ab-108">The [logical AND operator](and-operator.md) `&` also computes the logical AND of its `bool` operands, but always evaluates both operands.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="102ab-109">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="102ab-109">Operator overloadability</span></span>

<span data-ttu-id="102ab-110">ユーザー定義型は条件論理 AND 演算子をオーバーロードできません。</span><span class="sxs-lookup"><span data-stu-id="102ab-110">A user-defined type cannot overload the conditional logical AND operator.</span></span> <span data-ttu-id="102ab-111">ただし、ユーザー定義型が[論理 AND](and-operator.md) と [true および false 演算子](../keywords/true-false-operators.md)を特定の方法でオーバーロードしている場合は、その型のオペランドに対する `&&` 演算の評価が可能になります。</span><span class="sxs-lookup"><span data-stu-id="102ab-111">However, if a user-defined type overloads the [logical AND](and-operator.md) and [true and false operators](../keywords/true-false-operators.md) in a certain way, the `&&` operation can be evaluated for the operands of that type.</span></span> <span data-ttu-id="102ab-112">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[ユーザー定義型条件論理演算子](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="102ab-112">For more information, see the [User-defined conditional logical operators](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="102ab-113">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="102ab-113">C# language specification</span></span>

<span data-ttu-id="102ab-114">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[条件論理演算子](~/_csharplang/spec/expressions.md#conditional-logical-operators)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="102ab-114">For more information, see the [Conditional logical operators](~/_csharplang/spec/expressions.md#conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="102ab-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="102ab-115">See also</span></span>

- [<span data-ttu-id="102ab-116">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="102ab-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="102ab-117">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="102ab-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="102ab-118">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="102ab-118">C# Operators</span></span>](index.md)
- [<span data-ttu-id="102ab-119">|| 演算子</span><span class="sxs-lookup"><span data-stu-id="102ab-119">|| operator</span></span>](conditional-or-operator.md)
- [<span data-ttu-id="102ab-120">\! 演算子</span><span class="sxs-lookup"><span data-stu-id="102ab-120">! operator</span></span>](logical-negation-operator.md)
- [<span data-ttu-id="102ab-121">& 演算子</span><span class="sxs-lookup"><span data-stu-id="102ab-121">& operator</span></span>](and-operator.md)
