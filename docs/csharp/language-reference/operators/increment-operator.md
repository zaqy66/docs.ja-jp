---
title: ++ 演算子 (C# リファレンス)
ms.date: 11/26/2018
f1_keywords:
- ++_CSharpKeyword
helpviewer_keywords:
- increment operator (++) [C#]
- ++ operator [C#]
ms.assetid: e9dec353-070b-44fb-98ed-eb8fdf753feb
ms.openlocfilehash: b29f4f1ab00c0f8026f118cb72b090e3b728bfc5
ms.sourcegitcommit: 6ae7cdd0437a32884556dd4826ca90e957b7a4e3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2018
ms.locfileid: "48030471"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="01f22-102">++ 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="01f22-102">++ Operator (C# Reference)</span></span>

<span data-ttu-id="01f22-103">単項インクリメント演算子 `++` は、オペランドを 1 ずつインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="01f22-103">The unary increment operator `++` increments its operand by 1.</span></span> <span data-ttu-id="01f22-104">それは、後置インクリメント演算子である `x++` と、前置インクリメント演算子である`++x` という 2 つの形式でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="01f22-104">It's supported in two forms: the postfix increment operator, `x++`, and the prefix increment operator, `++x`.</span></span>

## <a name="postfix-increment-operator"></a><span data-ttu-id="01f22-105">後置インクリメント演算子</span><span class="sxs-lookup"><span data-stu-id="01f22-105">Postfix increment operator</span></span>

<span data-ttu-id="01f22-106">次の例に示すように、`x++` の結果は、演算子の`x` "*前の*" 値です。</span><span class="sxs-lookup"><span data-stu-id="01f22-106">The result of `x++` is the value of `x` *before* the operation, as the following example shows:</span></span>

[!code-csharp-interactive[postfix increment](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PostfixIncrement)]

## <a name="prefix-increment-operator"></a><span data-ttu-id="01f22-107">前置インクリメント演算子</span><span class="sxs-lookup"><span data-stu-id="01f22-107">Prefix increment operator</span></span>

<span data-ttu-id="01f22-108">次の例に示すように、`++x` の結果は、演算子の`x` "*後ろの*" 値です。</span><span class="sxs-lookup"><span data-stu-id="01f22-108">The result of `++x` is the value of `x` *after* the operation, as the following example shows:</span></span>

[!code-csharp-interactive[prefix increment](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PrefixIncrement)]

## <a name="remarks"></a><span data-ttu-id="01f22-109">コメント</span><span class="sxs-lookup"><span data-stu-id="01f22-109">Remarks</span></span>

<span data-ttu-id="01f22-110">インクリメント演算子は、すべての[整数型](../keywords/integral-types-table.md) ([文字](../keywords/char.md) 型を含みます)、[浮動小数点型](../keywords/floating-point-types-table.md)、および任意の[列挙](../keywords/enum.md)型に対して、事前に定義されています。</span><span class="sxs-lookup"><span data-stu-id="01f22-110">The increment operator is predefined for all [integral types](../keywords/integral-types-table.md) (including the [char](../keywords/char.md) type), [floating-point types](../keywords/floating-point-types-table.md), and any [enum](../keywords/enum.md) type.</span></span>

<span data-ttu-id="01f22-111">インクリメント演算子のオペランドは、変数、[プロパティ](../../programming-guide/classes-and-structs/properties.md)のアクセス、または [インデクサー](../../../csharp/programming-guide/indexers/index.md)のアクセスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f22-111">An operand of the increment operator must be a variable, a [property](../../programming-guide/classes-and-structs/properties.md) access, or an [indexer](../../../csharp/programming-guide/indexers/index.md) access.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="01f22-112">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="01f22-112">Operator overloadability</span></span>

<span data-ttu-id="01f22-113">ユーザー定義型は `++` 演算子を[オーバーロード](../keywords/operator.md)できます。</span><span class="sxs-lookup"><span data-stu-id="01f22-113">User-defined types can [overload](../keywords/operator.md) the `++` operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="01f22-114">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="01f22-114">C# language specification</span></span>

<span data-ttu-id="01f22-115">詳細については、「[C# 言語仕様](../language-specification/index.md)」の「[後置インクリメント演算子と後置デクリメント演算子](~/_csharplang/spec/expressions.md#postfix-increment-and-decrement-operators)と「[前置インクリメント演算子と前置デクリメント演算子](~/_csharplang/spec/expressions.md#prefix-increment-and-decrement-operators)」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="01f22-115">For more information, see the [Postfix increment and decrement operators](~/_csharplang/spec/expressions.md#postfix-increment-and-decrement-operators) and [Prefix increment and decrement operators](~/_csharplang/spec/expressions.md#prefix-increment-and-decrement-operators) sections of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="01f22-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="01f22-116">See also</span></span>

- [<span data-ttu-id="01f22-117">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="01f22-117">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="01f22-118">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="01f22-118">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="01f22-119">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="01f22-119">C# Operators</span></span>](index.md)
- [<span data-ttu-id="01f22-120">-- 演算子</span><span class="sxs-lookup"><span data-stu-id="01f22-120">-- Operator</span></span>](decrement-operator.md)
- [<span data-ttu-id="01f22-121">方法: ポインターのインクリメントとデクリメント</span><span class="sxs-lookup"><span data-stu-id="01f22-121">How to: increment and decrement pointers</span></span>](../../programming-guide/unsafe-code-pointers/how-to-increment-and-decrement-pointers.md)
