---
title: == 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 12/14/2018
f1_keywords:
- ==_CSharpKeyword
helpviewer_keywords:
- == operator [C#]
- equality operator [C#]
ms.assetid: 34c6b597-caa2-4855-a7cd-38ecdd11bd07
ms.openlocfilehash: 6d86348eefc87e847267f262141ff49e5d51faae
ms.sourcegitcommit: 3d0c29b878f00caec288dfecb3a5c959de5aa629
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2018
ms.locfileid: "53655960"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="b9ccb-102">== 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="b9ccb-102">== Operator (C# Reference)</span></span>

<span data-ttu-id="b9ccb-103">等値演算子 `==` は、そのオペランドが等しい場合には `true` を返し、それ以外の場合は `false` を返します。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-103">The equality operator `==` returns `true` if its operands are equal, `false` otherwise.</span></span>

## <a name="value-types-equality"></a><span data-ttu-id="b9ccb-104">値の型の等価性</span><span class="sxs-lookup"><span data-stu-id="b9ccb-104">Value types equality</span></span>

<span data-ttu-id="b9ccb-105">[組み込みの値の型](../keywords/value-types-table.md)のオペランドは、その値が等しい場合は等しくなります。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-105">Operands of the [built-in value types](../keywords/value-types-table.md) are equal if their values are equal:</span></span>

[!code-csharp-interactive[value types equality](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#ValueTypesEquality)]

> [!NOTE]
> <span data-ttu-id="b9ccb-106">関係演算子 `==`、`>`、`<`、`>=`、および `<=` で、いずれかのオペランドが数字 (<xref:System.Double.NaN?displayProperty=nameWithType> または <xref:System.Single.NaN?displayProperty=nameWithType>) ではない場合、演算の結果は `false` になります。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-106">For relational operators `==`, `>`, `<`, `>=`, and `<=`, if any of the operands is not a number (<xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType>) the result of operation is `false`.</span></span> <span data-ttu-id="b9ccb-107">つまり、`NaN` の値はそれ以外のどの `double` (または `float`) の値を上回ることも、下回ることも、等しいこともありません。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-107">That means that the `NaN` value is neither greater than, less than, nor equal to any other `double` (or `float`) value.</span></span> <span data-ttu-id="b9ccb-108">詳細およびサンプルについては、<xref:System.Double.NaN?displayProperty=nameWithType> または <xref:System.Single.NaN?displayProperty=nameWithType> の参照記事をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-108">For more information and examples, see the <xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType> reference article.</span></span>

<span data-ttu-id="b9ccb-109">同じ[列挙](../keywords/enum.md)型の 2 つのオペランドは、基になる整数型の対応する値が等しい場合は等しくなります。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-109">Two operands of the same [enum](../keywords/enum.md) type are equal if the corresponding values of the underlying integral type are equal.</span></span>

<span data-ttu-id="b9ccb-110">既定では、`==` 演算子はユーザー定義の[構造体](../keywords/struct.md)型には定義されていません。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-110">By default, the `==` operator is not defined for a user-defined [struct](../keywords/struct.md) type.</span></span> <span data-ttu-id="b9ccb-111">ユーザー定義型は `==` 演算子を[オーバーロード](#operator-overloadability)できます。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-111">A user-defined type can [overload](#operator-overloadability) the `==` operator.</span></span>

<span data-ttu-id="b9ccb-112">C# 7.3 より、`==` および [`!=`](not-equal-operator.md) 演算子は C# の[タプル](../../tuples.md)によってサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-112">Beginning with C# 7.3, the `==` and [`!=`](not-equal-operator.md) operators are supported by C# [tuples](../../tuples.md).</span></span> <span data-ttu-id="b9ccb-113">詳細については、「[C# のタプル型](../../tuples.md)」の記事の「[等値とタプル](../../tuples.md#equality-and-tuples)」のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-113">For more information, see the [Equality and tuples](../../tuples.md#equality-and-tuples) section of the [C# tuple types](../../tuples.md) article.</span></span>

## <a name="string-equality"></a><span data-ttu-id="b9ccb-114">文字列の等価性</span><span class="sxs-lookup"><span data-stu-id="b9ccb-114">String equality</span></span>

<span data-ttu-id="b9ccb-115">2 つの [string](../keywords/string.md) オペランドは、その両方が `null` であるか、両方の文字列インスタンスの長さが同じで、それぞれの文字列の位置に同じ文字が含まれている場合に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-115">Two [string](../keywords/string.md) operands are equal when both of them are `null` or both string instances are of the same length and have identical characters in each character position:</span></span>

[!code-csharp-interactive[string equality](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#StringEquality)]

<span data-ttu-id="b9ccb-116">序数の比較では大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-116">That is case-sensitive ordinal comparison.</span></span> <span data-ttu-id="b9ccb-117">文字列を比較する方法の詳細については、「[C# で文字列を比較する方法](../../how-to/compare-strings.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-117">For more information about how to compare strings, see [How to compare strings in C#](../../how-to/compare-strings.md).</span></span>

## <a name="reference-types-equality"></a><span data-ttu-id="b9ccb-118">参照型の等価性</span><span class="sxs-lookup"><span data-stu-id="b9ccb-118">Reference types equality</span></span>

<span data-ttu-id="b9ccb-119">`string` 参照型オペランド以外の 2 つは、同じオブジェクトを参照しているときに等しくなります。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-119">Two other than `string` reference type operands are equal when they refer to the same object:</span></span>

[!code-csharp-interactive[reference type equality](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#ReferenceTypesEquality)]

<span data-ttu-id="b9ccb-120">次の例は、`==` 演算子がユーザー定義の参照型でサポートされていることを示しています。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-120">The example shows that the `==` operator is supported by user-defined reference types.</span></span> <span data-ttu-id="b9ccb-121">ただし、ユーザー定義の参照型は `==` 演算子をオーバーロードできます。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-121">However, a user-defined reference type can overload the `==` operator.</span></span> <span data-ttu-id="b9ccb-122">参照型が `==` 演算子をオーバーロードする場合、その型の 2 つの参照が同じオブジェクトを参照しているかどうかを調べるには <xref:System.Object.ReferenceEquals%2A?displayProperty=nameWithType> メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-122">If a reference type overloads the `==` operator, use the <xref:System.Object.ReferenceEquals%2A?displayProperty=nameWithType> method to check if two references of that type refer to the same object.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="b9ccb-123">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="b9ccb-123">Operator overloadability</span></span>

<span data-ttu-id="b9ccb-124">ユーザー定義型は `==` 演算子を[オーバーロード](../keywords/operator.md)できます。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-124">User-defined types can [overload](../keywords/operator.md) the `==` operator.</span></span> <span data-ttu-id="b9ccb-125">型が等値演算子 `==` をオーバーロードしている場合、[非等値演算子](not-equal-operator.md) `!=` もオーバーロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-125">If a type overloads the equality operator `==`, it must also overload the [inequality operator](not-equal-operator.md) `!=`.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="b9ccb-126">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="b9ccb-126">C# language specification</span></span>

<span data-ttu-id="b9ccb-127">詳細については、[C# 言語仕様](../language-specification/index.md)に関するページの「[関係演算子と型検査演算子](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators)」のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9ccb-127">For more information, see the [Relational and type-testing operators](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b9ccb-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="b9ccb-128">See also</span></span>

- [<span data-ttu-id="b9ccb-129">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="b9ccb-129">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="b9ccb-130">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="b9ccb-130">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="b9ccb-131">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="b9ccb-131">C# Operators</span></span>](index.md)
- [<span data-ttu-id="b9ccb-132">等価比較</span><span class="sxs-lookup"><span data-stu-id="b9ccb-132">Equality comparisons</span></span>](../../programming-guide/statements-expressions-operators/equality-comparisons.md)
