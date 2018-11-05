---
title: += 演算子 (C# リファレンス)
ms.date: 10/22/2018
f1_keywords:
- +=_CSharpKeyword
helpviewer_keywords:
- += operator [C#]
- addition assignment operator (+=) [C#]
- event subscription [C#]
ms.assetid: 9cdf97e6-331d-492b-85e1-3ec3171484e9
ms.openlocfilehash: ee335e3e2e7d352d4e26b802bad2b08a05c666ab
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50192032"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="37c68-102">+= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="37c68-102">+= Operator (C# Reference)</span></span>

<span data-ttu-id="37c68-103">加算代入演算子です。</span><span class="sxs-lookup"><span data-stu-id="37c68-103">The addition assignment operator.</span></span>

<span data-ttu-id="37c68-104">次のような `+=` 演算子を使用する式があるとします</span><span class="sxs-lookup"><span data-stu-id="37c68-104">An expression using the `+=` operator, such as</span></span>  

```csharp
x += y
```  

<span data-ttu-id="37c68-105">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="37c68-105">is equivalent to</span></span>  

```csharp
x = x + y
```  

<span data-ttu-id="37c68-106">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="37c68-106">except that `x` is only evaluated once.</span></span>
  
<span data-ttu-id="37c68-107">数値型の場合、[加算演算子](addition-operator.md) `+` によってそのオペランドの合計が計算されます。</span><span class="sxs-lookup"><span data-stu-id="37c68-107">For numeric types, the [addition operator](addition-operator.md) `+` computes the sum of its operands.</span></span> <span data-ttu-id="37c68-108">一方または両方のオペランドが[文字列型](../keywords/string.md)である場合、そのオペランドの文字列表現を連結します。</span><span class="sxs-lookup"><span data-stu-id="37c68-108">If one or both operands is of type [string](../keywords/string.md), it concatenates the string representations of its operands.</span></span> <span data-ttu-id="37c68-109">デリゲート型の場合、`+` 演算子によって、そのオペランドの組み合わせである新しいデリゲート インスタンスが返されます。</span><span class="sxs-lookup"><span data-stu-id="37c68-109">For delegate types, the `+` operator returns a new delegate instance that is combination of its operands.</span></span>

<span data-ttu-id="37c68-110">ユーザー定義型により[加算演算子](addition-operator.md) `+` が[オーバーロード](../keywords/operator.md)される場合、加算代入演算子 `+=` が暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="37c68-110">If a user-defined type [overloads](../keywords/operator.md) the [addition operator](addition-operator.md) `+`, the addition assignment operator `+=` is implicitly overloaded.</span></span>

<span data-ttu-id="37c68-111">[イベント](../keywords/event.md)をサブスクライブするとき、`+=` 演算子を使用してイベント ハンドラー メソッドを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="37c68-111">You also use the `+=` operator to specify an event handler method when you subscribe to an [event](../keywords/event.md).</span></span> <span data-ttu-id="37c68-112">詳細については、「[方法: イベント サブスクリプションとサブスクリプションの解除](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37c68-112">For more information, see [How to: Subscribe to and Unsubscribe from Events](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).</span></span>

<span data-ttu-id="37c68-113">`+=` 演算子の使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="37c68-113">The following example demonstrates the usage of the `+=` operator:</span></span>

[!code-csharp-interactive[+= examples](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddAndAssign)]
  
## <a name="see-also"></a><span data-ttu-id="37c68-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="37c68-114">See also</span></span>

- [<span data-ttu-id="37c68-115">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="37c68-115">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="37c68-116">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="37c68-116">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="37c68-117">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="37c68-117">C# Operators</span></span>](index.md)
- [<span data-ttu-id="37c68-118">イベント</span><span class="sxs-lookup"><span data-stu-id="37c68-118">Events</span></span>](../../programming-guide/events/index.md)
- [<span data-ttu-id="37c68-119">デリゲート</span><span class="sxs-lookup"><span data-stu-id="37c68-119">Delegates</span></span>](../../programming-guide/delegates/index.md)
