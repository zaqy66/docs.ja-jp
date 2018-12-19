---
title: += 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 10/29/2018
f1_keywords:
- +=_CSharpKeyword
helpviewer_keywords:
- += operator [C#]
- addition assignment operator (+=) [C#]
- event subscription [C#]
ms.assetid: 9cdf97e6-331d-492b-85e1-3ec3171484e9
ms.openlocfilehash: 5d48f2fe53a9bb6f781f8d35f1e0983bcaa30f88
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53240932"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="63c2f-102">+= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="63c2f-102">+= Operator (C# Reference)</span></span>

<span data-ttu-id="63c2f-103">加算代入演算子です。</span><span class="sxs-lookup"><span data-stu-id="63c2f-103">The addition assignment operator.</span></span>

<span data-ttu-id="63c2f-104">次のような `+=` 演算子を使用する式があるとします</span><span class="sxs-lookup"><span data-stu-id="63c2f-104">An expression using the `+=` operator, such as</span></span>

```csharp
x += y
```

<span data-ttu-id="63c2f-105">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="63c2f-105">is equivalent to</span></span>

```csharp
x = x + y
```

<span data-ttu-id="63c2f-106">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="63c2f-106">except that `x` is only evaluated once.</span></span>
  
<span data-ttu-id="63c2f-107">数値型の場合、[加算演算子](addition-operator.md) `+` によってそのオペランドの合計が計算されます。</span><span class="sxs-lookup"><span data-stu-id="63c2f-107">For numeric types, the [addition operator](addition-operator.md) `+` computes the sum of its operands.</span></span> <span data-ttu-id="63c2f-108">一方または両方のオペランドが[文字列型](../keywords/string.md)である場合、そのオペランドの文字列表現を連結します。</span><span class="sxs-lookup"><span data-stu-id="63c2f-108">If one or both operands is of type [string](../keywords/string.md), it concatenates the string representations of its operands.</span></span> <span data-ttu-id="63c2f-109">デリゲート型の場合、`+` 演算子によって、そのオペランドの組み合わせである新しいデリゲート インスタンスが返されます。</span><span class="sxs-lookup"><span data-stu-id="63c2f-109">For delegate types, the `+` operator returns a new delegate instance that is combination of its operands.</span></span>

<span data-ttu-id="63c2f-110">[イベント](../keywords/event.md)をサブスクライブするとき、`+=` 演算子を使用してイベント ハンドラー メソッドを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="63c2f-110">You also use the `+=` operator to specify an event handler method when you subscribe to an [event](../keywords/event.md).</span></span> <span data-ttu-id="63c2f-111">詳細については、「[方法 :イベント サブスクリプションとサブスクリプションの解除](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63c2f-111">For more information, see [How to: Subscribe to and Unsubscribe from Events](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).</span></span>

<span data-ttu-id="63c2f-112">`+=` 演算子の使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="63c2f-112">The following example demonstrates the usage of the `+=` operator:</span></span>

[!code-csharp-interactive[+= examples](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddAndAssign)]

## <a name="operator-overloadability"></a><span data-ttu-id="63c2f-113">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="63c2f-113">Operator overloadability</span></span>

<span data-ttu-id="63c2f-114">ユーザー定義型により[加算演算子](addition-operator.md) `+` が[オーバーロード](../keywords/operator.md)される場合、加算代入演算子 `+=` が暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="63c2f-114">If a user-defined type [overloads](../keywords/operator.md) the [addition operator](addition-operator.md) `+`, the addition assignment operator `+=` is implicitly overloaded.</span></span> <span data-ttu-id="63c2f-115">ユーザー定義型は、加算代入演算子を明示的にオーバー ロードできません。</span><span class="sxs-lookup"><span data-stu-id="63c2f-115">A user-defined type cannot explicitly overload the addition assignment operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="63c2f-116">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="63c2f-116">C# language specification</span></span>

<span data-ttu-id="63c2f-117">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[複合代入](~/_csharplang/spec/expressions.md#compound-assignment)と[イベント代入](~/_csharplang/spec/expressions.md#event-assignment)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="63c2f-117">For more information, see the [Compound assignment](~/_csharplang/spec/expressions.md#compound-assignment) and [Event assignment](~/_csharplang/spec/expressions.md#event-assignment) sections of the [C# language specification](../language-specification/index.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63c2f-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="63c2f-118">See also</span></span>

- [<span data-ttu-id="63c2f-119">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="63c2f-119">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="63c2f-120">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="63c2f-120">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="63c2f-121">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="63c2f-121">C# Operators</span></span>](index.md)
- [<span data-ttu-id="63c2f-122">イベント</span><span class="sxs-lookup"><span data-stu-id="63c2f-122">Events</span></span>](../../programming-guide/events/index.md)
- [<span data-ttu-id="63c2f-123">デリゲート</span><span class="sxs-lookup"><span data-stu-id="63c2f-123">Delegates</span></span>](../../programming-guide/delegates/index.md)
