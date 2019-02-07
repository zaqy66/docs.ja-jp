---
title: <= 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 12/18/2018
f1_keywords:
- <=_CSharpKeyword
helpviewer_keywords:
- less than or equal to operator (<=) [C#]
- <= operator [C#]
ms.assetid: bb0caec9-d253-4105-b8bc-5252233251e4
ms.openlocfilehash: cb11a746d36cc22ab2341e28a7efba3c0b3510eb
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55257006"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="3d215-102">\<= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="3d215-102">\<= Operator (C# Reference)</span></span>

<span data-ttu-id="3d215-103">"次の値より小さいか等しい" 関係演算子 `<=` は、最初のオペランドが 2 番目のオペランドより小さいか等しい場合に `true` を返し、それ以外の場合は `false` を返します。</span><span class="sxs-lookup"><span data-stu-id="3d215-103">The "less than or equal" relational operator `<=` returns `true` if its first operand is less than or equal to its second operand, `false` otherwise.</span></span> <span data-ttu-id="3d215-104">すべての数値型と列挙型が `<=` 演算子をサポートします。</span><span class="sxs-lookup"><span data-stu-id="3d215-104">All numeric and enumeration types support the `<=` operator.</span></span> <span data-ttu-id="3d215-105">同じ[列挙](../keywords/enum.md)型のオペランドで、基になる整数型の対応する値が比較されます。</span><span class="sxs-lookup"><span data-stu-id="3d215-105">For operands of the same [enum](../keywords/enum.md) type, the corresponding values of the underlying integral type are compared.</span></span>

> [!NOTE]
> <span data-ttu-id="3d215-106">関係演算子 `==`、`>`、`<`、`>=`、および `<=` で、いずれかのオペランドが数字 (<xref:System.Double.NaN?displayProperty=nameWithType> または <xref:System.Single.NaN?displayProperty=nameWithType>) ではない場合、演算の結果は `false` になります。</span><span class="sxs-lookup"><span data-stu-id="3d215-106">For relational operators `==`, `>`, `<`, `>=`, and `<=`, if any of the operands is not a number (<xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType>) the result of operation is `false`.</span></span> <span data-ttu-id="3d215-107">つまり、`NaN` の値はそれ以外のどの `double` (または `float`) の値を上回ることも、下回ることも、等しいこともありません。</span><span class="sxs-lookup"><span data-stu-id="3d215-107">That means that the `NaN` value is neither greater than, less than, nor equal to any other `double` (or `float`) value.</span></span> <span data-ttu-id="3d215-108">詳細およびサンプルについては、<xref:System.Double.NaN?displayProperty=nameWithType> または <xref:System.Single.NaN?displayProperty=nameWithType> の参照記事をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="3d215-108">For more information and examples, see the <xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType> reference article.</span></span>

<span data-ttu-id="3d215-109">`<=` 演算子の使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3d215-109">The following example demonstrates the usage of the `<=` operator:</span></span>

[!code-csharp-interactive[less than or equal example](~/samples/snippets/csharp/language-reference/operators/GreaterAndLessOperatorsExamples.cs#LessOrEqual)]

## <a name="operator-overloadability"></a><span data-ttu-id="3d215-110">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="3d215-110">Operator overloadability</span></span>

<span data-ttu-id="3d215-111">ユーザー定義型は `<=` 演算子を[オーバーロード](../keywords/operator.md)できます。</span><span class="sxs-lookup"><span data-stu-id="3d215-111">User-defined types can [overload](../keywords/operator.md) the `<=` operator.</span></span> <span data-ttu-id="3d215-112">型が "次の値より小さいか等しい" 演算子 `<=` をオーバーロードする場合、["次の値より大きいか等しい" 演算子](greater-than-equal-operator.md) `>=` もオーバーロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d215-112">If a type overloads the "less than or equal" operator `<=`, it must also overload the ["greater than or equal" operator](greater-than-equal-operator.md) `>=`.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="3d215-113">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="3d215-113">C# language specification</span></span>

<span data-ttu-id="3d215-114">詳細については、[C# 言語仕様](../language-specification/index.md)に関するページの「[関係演算子と型検査演算子](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators)」のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d215-114">For more information, see the [Relational and type-testing operators](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3d215-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d215-115">See also</span></span>

- [<span data-ttu-id="3d215-116">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="3d215-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="3d215-117">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="3d215-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="3d215-118">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="3d215-118">C# Operators</span></span>](index.md)
- [<span data-ttu-id="3d215-119">< 演算子</span><span class="sxs-lookup"><span data-stu-id="3d215-119">< Operator</span></span>](less-than-operator.md)
- [<span data-ttu-id="3d215-120">== 演算子</span><span class="sxs-lookup"><span data-stu-id="3d215-120">== Operator</span></span>](equality-comparison-operator.md)
- <xref:System.IComparable%601?displayProperty=nameWithType>
