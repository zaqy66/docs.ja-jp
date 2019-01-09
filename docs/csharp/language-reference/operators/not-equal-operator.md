---
title: '!= 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 12/14/2018
f1_keywords:
- '!=_CSharpKeyword'
helpviewer_keywords:
- inequality operator (!=) [C#]
- not equals operator (!=) [C#]
- '!= operator [C#]'
ms.assetid: eeff7a4e-ad6f-462d-9f8d-49e9b91c6c97
ms.openlocfilehash: 939b5664dba4345e62a43fb2f8d4d5379659d6aa
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2018
ms.locfileid: "53610178"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="b69f9-102">!= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="b69f9-102">!= Operator (C# Reference)</span></span>

<span data-ttu-id="b69f9-103">非等値演算子 `!=` は、そのオペランドが等しくない場合には `true` を返し、それ以外の場合は `false` を返します。</span><span class="sxs-lookup"><span data-stu-id="b69f9-103">The inequality operator `!=` returns `true` if its operands are not equal, `false` otherwise.</span></span> <span data-ttu-id="b69f9-104">[組み込み型](../keywords/built-in-types-table.md)のオペランドの場合、式 `x != y` と式 `!(x == y)` では同じ結果が生成されます。</span><span class="sxs-lookup"><span data-stu-id="b69f9-104">For the operands of the [built-in types](../keywords/built-in-types-table.md), the expression `x != y` produces the same result as the expression `!(x == y)`.</span></span> <span data-ttu-id="b69f9-105">詳細については、「[== 演算子](equality-comparison-operator.md)」の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b69f9-105">For more information, see the [== Operator](equality-comparison-operator.md) article.</span></span>

<span data-ttu-id="b69f9-106">`!=` 演算子の使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b69f9-106">The following example demonstrates the usage of the `!=` operator:</span></span>

[!code-csharp-interactive[non-equality examples](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#NonEquality)]

## <a name="operator-overloadability"></a><span data-ttu-id="b69f9-107">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="b69f9-107">Operator overloadability</span></span>

<span data-ttu-id="b69f9-108">ユーザー定義型は `!=` 演算子を[オーバーロード](../keywords/operator.md)できます。</span><span class="sxs-lookup"><span data-stu-id="b69f9-108">User-defined types can [overload](../keywords/operator.md) the `!=` operator.</span></span> <span data-ttu-id="b69f9-109">型が非等値演算子 `!=` をオーバーロードしている場合、[等値演算子](equality-comparison-operator.md) `==` もオーバーロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b69f9-109">If a type overloads the inequality operator `!=`, it must also overload the [equality operator](equality-comparison-operator.md) `==`.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="b69f9-110">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="b69f9-110">C# language specification</span></span>

<span data-ttu-id="b69f9-111">詳細については、[C# 言語仕様](../language-specification/index.md)に関するページの「[関係演算子と型検査演算子](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators)」のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b69f9-111">For more information, see the [Relational and type-testing operators](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b69f9-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="b69f9-112">See also</span></span>

- [<span data-ttu-id="b69f9-113">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="b69f9-113">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="b69f9-114">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="b69f9-114">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="b69f9-115">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="b69f9-115">C# Operators</span></span>](index.md)
- [<span data-ttu-id="b69f9-116">等価比較</span><span class="sxs-lookup"><span data-stu-id="b69f9-116">Equality comparisons</span></span>](../../programming-guide/statements-expressions-operators/equality-comparisons.md)
