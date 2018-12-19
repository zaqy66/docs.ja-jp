---
title: /= 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 12/13/2018
f1_keywords:
- /=_CSharpKeyword
helpviewer_keywords:
- division assignment operator (/=) [C#]
- /= (division assignment operator) [C#]
ms.assetid: 50fc02b0-ee9c-4c3e-b58d-d591282caf1c
ms.openlocfilehash: ed4dd6c0c944b77543aae4de8d51534b4df4f4ef
ms.sourcegitcommit: d6e419f9d9cd7e8f21ebf5acde6d016c16332579
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/12/2018
ms.locfileid: "53286521"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="26b94-102">/= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="26b94-102">/= Operator (C# Reference)</span></span>

<span data-ttu-id="26b94-103">除算代入演算子です。</span><span class="sxs-lookup"><span data-stu-id="26b94-103">The division assignment operator.</span></span>

<span data-ttu-id="26b94-104">次のような `/=` 演算子を使用する式があるとします</span><span class="sxs-lookup"><span data-stu-id="26b94-104">An expression using the `/=` operator, such as</span></span>

```csharp
x /= y
```

<span data-ttu-id="26b94-105">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="26b94-105">is equivalent to</span></span>

```csharp
x = x / y
```

<span data-ttu-id="26b94-106">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="26b94-106">except that `x` is only evaluated once.</span></span>

<span data-ttu-id="26b94-107">[除算演算子](division-operator.md) `/` は、1 つ目のオペランドを 2 つ目のオペランドで除算します。</span><span class="sxs-lookup"><span data-stu-id="26b94-107">The [division operator](division-operator.md) `/` divides its first operand by its second operand.</span></span> <span data-ttu-id="26b94-108">すべての数値型でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="26b94-108">It's supported by all numeric types.</span></span>

<span data-ttu-id="26b94-109">`/=` 演算子の使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="26b94-109">The following example demonstrates the usage of the `/=` operator:</span></span>

[!code-csharp-interactive[divide and assign](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#DivisionAssignment)]

## <a name="operator-overloadability"></a><span data-ttu-id="26b94-110">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="26b94-110">Operator overloadability</span></span>

<span data-ttu-id="26b94-111">ユーザー定義型により[除算演算子](division-operator.md) `/` が[オーバーロード](../keywords/operator.md)される場合、除算代入演算子 `/=` が暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="26b94-111">If a user-defined type [overloads](../keywords/operator.md) the [division operator](division-operator.md) `/`, the division assignment operator `/=` is implicitly overloaded.</span></span> <span data-ttu-id="26b94-112">ユーザー定義型は、除算代入演算子を明示的にオーバー ロードできません。</span><span class="sxs-lookup"><span data-stu-id="26b94-112">A user-defined type cannot explicitly overload the division assignment operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="26b94-113">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="26b94-113">C# language specification</span></span>

<span data-ttu-id="26b94-114">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[複合代入](~/_csharplang/spec/expressions.md#compound-assignment)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="26b94-114">For more information, see the [Compound assignment](~/_csharplang/spec/expressions.md#compound-assignment) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="26b94-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="26b94-115">See also</span></span>

- [<span data-ttu-id="26b94-116">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="26b94-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="26b94-117">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="26b94-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="26b94-118">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="26b94-118">C# Operators</span></span>](index.md)
