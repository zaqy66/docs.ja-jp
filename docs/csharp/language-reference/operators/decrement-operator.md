---
title: -- 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 11/26/2018
f1_keywords:
- --_CSharpKeyword
helpviewer_keywords:
- -- operator [C#]
- decrement operator (--) [C#]
ms.assetid: 6b9cfe86-63c7-421f-9379-c9690fea8720
ms.openlocfilehash: 4fba014e8dabc13cd874e17f23515dc29d93f24b
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236928"
---
# <a name="---operator-c-reference"></a><span data-ttu-id="d0a71-102">-- 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="d0a71-102">-- Operator (C# Reference)</span></span>

<span data-ttu-id="d0a71-103">単項デクリメント演算子 `--` は、オペランドを 1 ずつデクリメントします。</span><span class="sxs-lookup"><span data-stu-id="d0a71-103">The unary decrement operator `--` decrements its operand by 1.</span></span> <span data-ttu-id="d0a71-104">それは、後置デクリメント演算子である `x--` と、前置デクリメント演算子である`--x` という 2 つの形式でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d0a71-104">It's supported in two forms: the postfix decrement operator, `x--`, and the prefix decrement operator, `--x`.</span></span>

## <a name="postfix-decrement-operator"></a><span data-ttu-id="d0a71-105">後置デクリメント演算子</span><span class="sxs-lookup"><span data-stu-id="d0a71-105">Postfix decrement operator</span></span>

<span data-ttu-id="d0a71-106">次の例に示すように、`x--` の結果は、演算子の "*前の*" `x` 値です。</span><span class="sxs-lookup"><span data-stu-id="d0a71-106">The result of `x--` is the value of `x` *before* the operation, as the following example shows:</span></span>

[!code-csharp-interactive[postfix decrement](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PostfixDecrement)]

## <a name="prefix-decrement-operator"></a><span data-ttu-id="d0a71-107">前置デクリメント演算子</span><span class="sxs-lookup"><span data-stu-id="d0a71-107">Prefix decrement operator</span></span>

<span data-ttu-id="d0a71-108">次の例に示すように、`--x` の結果は、演算子の "*後ろの*" `x` 値です。</span><span class="sxs-lookup"><span data-stu-id="d0a71-108">The result of `--x` is the value of `x` *after* the operation, as the following example shows:</span></span>

[!code-csharp-interactive[prefix decrement](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PrefixDecrement)]

## <a name="remarks"></a><span data-ttu-id="d0a71-109">コメント</span><span class="sxs-lookup"><span data-stu-id="d0a71-109">Remarks</span></span>

<span data-ttu-id="d0a71-110">デクリメント演算子は、すべての[整数型](../keywords/integral-types-table.md) ([文字](../keywords/char.md) 型を含みます)、[浮動小数点型](../keywords/floating-point-types-table.md)、および任意の[列挙](../keywords/enum.md)型に対して、事前に定義されています。</span><span class="sxs-lookup"><span data-stu-id="d0a71-110">The decrement operator is predefined for all [integral types](../keywords/integral-types-table.md) (including the [char](../keywords/char.md) type), [floating-point types](../keywords/floating-point-types-table.md), and any [enum](../keywords/enum.md) type.</span></span>

<span data-ttu-id="d0a71-111">デクリメント演算子のオペランドは、変数、[プロパティ](../../programming-guide/classes-and-structs/properties.md)のアクセス、または[インデクサー](../../../csharp/programming-guide/indexers/index.md)のアクセスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0a71-111">An operand of the decrement operator must be a variable, a [property](../../programming-guide/classes-and-structs/properties.md) access, or an [indexer](../../../csharp/programming-guide/indexers/index.md) access.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="d0a71-112">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="d0a71-112">Operator overloadability</span></span>

<span data-ttu-id="d0a71-113">ユーザー定義型は `--` 演算子を[オーバーロード](../keywords/operator.md)できます。</span><span class="sxs-lookup"><span data-stu-id="d0a71-113">User-defined types can [overload](../keywords/operator.md) the `--` operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="d0a71-114">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="d0a71-114">C# language specification</span></span>

<span data-ttu-id="d0a71-115">詳細については、「[C# 言語仕様](../language-specification/index.md)」の「[後置インクリメント演算子と後置デクリメント演算子](~/_csharplang/spec/expressions.md#postfix-increment-and-decrement-operators)と「[前置インクリメント演算子と前置デクリメント演算子](~/_csharplang/spec/expressions.md#prefix-increment-and-decrement-operators)」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0a71-115">For more information, see the [Postfix increment and decrement operators](~/_csharplang/spec/expressions.md#postfix-increment-and-decrement-operators) and [Prefix increment and decrement operators](~/_csharplang/spec/expressions.md#prefix-increment-and-decrement-operators) sections of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d0a71-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="d0a71-116">See also</span></span>

- [<span data-ttu-id="d0a71-117">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="d0a71-117">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="d0a71-118">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="d0a71-118">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="d0a71-119">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="d0a71-119">C# Operators</span></span>](index.md)
- [<span data-ttu-id="d0a71-120">++ 演算子</span><span class="sxs-lookup"><span data-stu-id="d0a71-120">++ Operator</span></span>](increment-operator.md)
- [<span data-ttu-id="d0a71-121">方法: ポインターのインクリメントとデクリメント</span><span class="sxs-lookup"><span data-stu-id="d0a71-121">How to: increment and decrement pointers</span></span>](../../programming-guide/unsafe-code-pointers/how-to-increment-and-decrement-pointers.md)
