---
title: '&amp;&amp; 演算子 (C# リファレンス)'
ms.date: 11/06/2018
f1_keywords:
- '&&_CSharpKeyword'
helpviewer_keywords:
- '&& operator [C#]'
- logical AND operator [C#]
ms.assetid: 2e4f0a1c-92a3-40f8-8e3b-17b607f20c31
ms.openlocfilehash: d0e6d9a5aedc7dc87393e3dea070bf442b3268dc
ms.sourcegitcommit: b5cd9d5d3b75a5537fc9ad8a3f085f0bb1845ee0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "43529236"
---
# <a name="ampamp-operator-c-reference"></a><span data-ttu-id="316ae-102">&amp;&amp; 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="316ae-102">&amp;&amp; Operator (C# Reference)</span></span>

<span data-ttu-id="316ae-103">条件論理 AND 演算子 `&&` は、"短絡" 論理 AND 演算子とも呼ばれ、その [bool](../keywords/bool.md) オペランドの論理 AND を計算します。</span><span class="sxs-lookup"><span data-stu-id="316ae-103">The conditional logical AND operator `&&`, also known as the "short-circuiting" logical AND operator, computes the logical AND of its [bool](../keywords/bool.md) operands.</span></span> <span data-ttu-id="316ae-104">`x` と `y` の両方が `true` と評価されれば、`x && y` の結果は `true` です。</span><span class="sxs-lookup"><span data-stu-id="316ae-104">The result of `x && y` is `true` if both `x` and `y` evaluate to `true`.</span></span> <span data-ttu-id="316ae-105">それ以外の場合、結果は `false` です。</span><span class="sxs-lookup"><span data-stu-id="316ae-105">Otherwise, the result is `false`.</span></span> <span data-ttu-id="316ae-106">最初のオペランドが `false` と評価されると、2 番目のオペランドは評価されず、演算の結果は `false` になります。</span><span class="sxs-lookup"><span data-stu-id="316ae-106">If the first operand evaluates to `false`, the second operand is not evaluated and the result of operation is `false`.</span></span> <span data-ttu-id="316ae-107">次の例は、その動作を示します。</span><span class="sxs-lookup"><span data-stu-id="316ae-107">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[conditional logical AND](~/samples/snippets/csharp/language-reference/operators/ConditionalLogicalOperatorsExamples.cs#And)]

<span data-ttu-id="316ae-108">[論理 AND 演算子](and-operator.md) `&` もその `bool` オペランドの論理 AND を計算しますが、常に両方のオペランドを評価します。</span><span class="sxs-lookup"><span data-stu-id="316ae-108">The [logical AND operator](and-operator.md) `&` also computes the logical AND of its `bool` operands, but always evaluates both operands.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="316ae-109">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="316ae-109">Operator overloadability</span></span>

<span data-ttu-id="316ae-110">ユーザー定義型は条件論理 AND 演算子をオーバーロードできません。</span><span class="sxs-lookup"><span data-stu-id="316ae-110">A user-defined type cannot overload the conditional logical AND operator.</span></span> <span data-ttu-id="316ae-111">ただし、ユーザー定義型が[論理 AND](and-operator.md)、[true](../keywords/true-operator.md)、および [false](../keywords/false-operator.md) 演算子を特定の方法でオーバーロードする場合、`&&` 演算はその型のオペランドに対して評価を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="316ae-111">However, if a user-defined type overloads the [logical AND](and-operator.md), [true](../keywords/true-operator.md), and [false](../keywords/false-operator.md) operators in a certain way, the `&&` operation can be evaluated for the operands of that type.</span></span> <span data-ttu-id="316ae-112">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[ユーザー定義型条件論理演算子](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="316ae-112">For more information, see the [User-defined conditional logical operators](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="316ae-113">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="316ae-113">C# language specification</span></span>

<span data-ttu-id="316ae-114">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[条件論理演算子](~/_csharplang/spec/expressions.md#conditional-logical-operators)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="316ae-114">For more information, see the [Conditional logical operators](~/_csharplang/spec/expressions.md#conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="316ae-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="316ae-115">See also</span></span>

- [<span data-ttu-id="316ae-116">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="316ae-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="316ae-117">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="316ae-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="316ae-118">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="316ae-118">C# Operators</span></span>](index.md)
- [<span data-ttu-id="316ae-119">|| 演算子</span><span class="sxs-lookup"><span data-stu-id="316ae-119">|| operator</span></span>](conditional-or-operator.md)
- [! 演算子]<span data-ttu-id="316ae-120">(logical-negation-operator.md)</span><span class="sxs-lookup"><span data-stu-id="316ae-120">(logical-negation-operator.md)</span></span>
- [<span data-ttu-id="316ae-121">& 演算子</span><span class="sxs-lookup"><span data-stu-id="316ae-121">& operator</span></span>](and-operator.md)
