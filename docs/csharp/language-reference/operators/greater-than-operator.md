---
title: '&gt; 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 12/18/2018
f1_keywords:
- '>_CSharpKeyword'
helpviewer_keywords:
- '> operator [C#]'
- greater than operator (>) [C#]
ms.assetid: 26d3cb69-9c0b-4cc5-858b-5be1abd6659d
ms.openlocfilehash: 0c9d414d159b5e2f1faa24e9bd5f073d1ca874a4
ms.sourcegitcommit: 3d0c29b878f00caec288dfecb3a5c959de5aa629
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2018
ms.locfileid: "53655973"
---
# <a name="gt-operator-c-reference"></a><span data-ttu-id="3eb95-102">&gt; 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="3eb95-102">&gt; Operator (C# Reference)</span></span>

<span data-ttu-id="3eb95-103">"次の値より大きい" 関係演算子 `>` は、最初のオペランドが 2 番目のオペランドより大きい場合に `true` を返し、それ以外の場合は `false` を返します。</span><span class="sxs-lookup"><span data-stu-id="3eb95-103">The "greater than" relational operator `>` returns `true` if its first operand is greater than its second operand, `false` otherwise.</span></span> <span data-ttu-id="3eb95-104">すべての数値型と列挙型が `>` 演算子をサポートします。</span><span class="sxs-lookup"><span data-stu-id="3eb95-104">All numeric and enumeration types support the `>` operator.</span></span> <span data-ttu-id="3eb95-105">同じ[列挙](../keywords/enum.md)型のオペランドで、基になる整数型の対応する値が比較されます。</span><span class="sxs-lookup"><span data-stu-id="3eb95-105">For operands of the same [enum](../keywords/enum.md) type, the corresponding values of the underlying integral type are compared.</span></span>

> [!NOTE]
> <span data-ttu-id="3eb95-106">関係演算子 `==`、`>`、`<`、`>=`、および `<=` で、いずれかのオペランドが数字 (<xref:System.Double.NaN?displayProperty=nameWithType> または <xref:System.Single.NaN?displayProperty=nameWithType>) ではない場合、演算の結果は `false` になります。</span><span class="sxs-lookup"><span data-stu-id="3eb95-106">For relational operators `==`, `>`, `<`, `>=`, and `<=`, if any of the operands is not a number (<xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType>) the result of operation is `false`.</span></span> <span data-ttu-id="3eb95-107">つまり、`NaN` の値はそれ以外のどの `double` (または `float`) の値を上回ることも、下回ることも、等しいこともありません。</span><span class="sxs-lookup"><span data-stu-id="3eb95-107">That means that the `NaN` value is neither greater than, less than, nor equal to any other `double` (or `float`) value.</span></span> <span data-ttu-id="3eb95-108">詳細およびサンプルについては、<xref:System.Double.NaN?displayProperty=nameWithType> または <xref:System.Single.NaN?displayProperty=nameWithType> の参照記事をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="3eb95-108">For more information and examples, see the <xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType> reference article.</span></span>

<span data-ttu-id="3eb95-109">`>` 演算子の使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3eb95-109">The following example demonstrates the usage of the `>` operator:</span></span>

[!code-csharp-interactive[greater than example](~/samples/snippets/csharp/language-reference/operators/GreaterAndLessOperatorsExamples.cs#Greater)]

## <a name="operator-overloadability"></a><span data-ttu-id="3eb95-110">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="3eb95-110">Operator overloadability</span></span>

<span data-ttu-id="3eb95-111">ユーザー定義型は `>` 演算子を[オーバーロード](../keywords/operator.md)できます。</span><span class="sxs-lookup"><span data-stu-id="3eb95-111">User-defined types can [overload](../keywords/operator.md) the `>` operator.</span></span> <span data-ttu-id="3eb95-112">型が "次の値より大きい" 演算子 `>` をオーバーロードする場合、["次の値より小さい" 演算子](less-than-operator.md) `<` もオーバーロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3eb95-112">If a type overloads the "greater than" operator `>`, it must also overload the ["less than" operator](less-than-operator.md) `<`.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="3eb95-113">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="3eb95-113">C# language specification</span></span>

<span data-ttu-id="3eb95-114">詳細については、[C# 言語仕様](../language-specification/index.md)に関するページの「[関係演算子と型検査演算子](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators)」のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3eb95-114">For more information, see the [Relational and type-testing operators](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3eb95-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="3eb95-115">See also</span></span>

- [<span data-ttu-id="3eb95-116">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="3eb95-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="3eb95-117">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="3eb95-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="3eb95-118">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="3eb95-118">C# Operators</span></span>](index.md)
- [<span data-ttu-id="3eb95-119">>= 演算子</span><span class="sxs-lookup"><span data-stu-id="3eb95-119">>= Operator</span></span>](greater-than-equal-operator.md)
- <xref:System.IComparable%601?displayProperty=nameWithType>
