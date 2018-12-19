---
title: '&amp;= 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 10/29/2018
f1_keywords:
- '&=_CSharpKeyword'
helpviewer_keywords:
- AND assignment operator (&=) [C#]
- '&= operator [C#]'
ms.assetid: e8d58f3f-72dd-4b5a-b995-452fcce7e6bb
ms.openlocfilehash: 223d2f30ee77457e1f9d5304ec299517932499d0
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237026"
---
# <a name="amp-operator-c-reference"></a><span data-ttu-id="916e6-102">&amp;= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="916e6-102">&amp;= Operator (C# Reference)</span></span>

<span data-ttu-id="916e6-103">AND 代入演算子です。</span><span class="sxs-lookup"><span data-stu-id="916e6-103">The AND assignment operator.</span></span>

<span data-ttu-id="916e6-104">次のような `&=` 演算子を使用する式があるとします</span><span class="sxs-lookup"><span data-stu-id="916e6-104">An expression using the `&=` operator, such as</span></span>

```csharp
x &= y
```

<span data-ttu-id="916e6-105">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="916e6-105">is equivalent to</span></span>

```csharp
x = x & y
```

<span data-ttu-id="916e6-106">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="916e6-106">except that `x` is only evaluated once.</span></span>

<span data-ttu-id="916e6-107">整数オペランドの場合、[`&` 演算子](and-operator.md)はそのオペランドのビット演算論理 AND を計算しますが、[bool](../keywords/bool.md) オペランドの場合は、そのオペランドの論理 AND を計算します。</span><span class="sxs-lookup"><span data-stu-id="916e6-107">For integer operands, the [`&` operator](and-operator.md) computes the bitwise logical AND of its operands; for [bool](../keywords/bool.md) operands, it computes the logical AND of its operands.</span></span>

<span data-ttu-id="916e6-108">`&=` 演算子の使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="916e6-108">The following example demonstrates the usage of the `&=` operator:</span></span>

[!code-csharp-interactive[AND assignment example](~/samples/snippets/csharp/language-reference/operators/AndOperatorExamples.cs#AndAssignmentExample)]

## <a name="operator-overloadability"></a><span data-ttu-id="916e6-109">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="916e6-109">Operator overloadability</span></span>

<span data-ttu-id="916e6-110">ユーザー定義型により、[`&` 演算子](and-operator.md)が[オーバーロード](../keywords/operator.md)される場合、AND 代入演算子 `&=` が暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="916e6-110">If a user-defined type [overloads](../keywords/operator.md) the [`&` operator](and-operator.md), the AND assignment operator `&=` is implicitly overloaded.</span></span> <span data-ttu-id="916e6-111">ユーザー定義型は、AND 代入演算子を明示的にオーバー ロードできません。</span><span class="sxs-lookup"><span data-stu-id="916e6-111">A user-defined type cannot explicitly overload the AND assignment operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="916e6-112">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="916e6-112">C# language specification</span></span>

<span data-ttu-id="916e6-113">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[複合代入](~/_csharplang/spec/expressions.md#compound-assignment)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="916e6-113">For more information, see the [Compound assignment](~/_csharplang/spec/expressions.md#compound-assignment) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="916e6-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="916e6-114">See also</span></span>

- [<span data-ttu-id="916e6-115">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="916e6-115">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="916e6-116">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="916e6-116">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="916e6-117">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="916e6-117">C# Operators</span></span>](index.md)
