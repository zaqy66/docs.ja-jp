---
title: -= 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- -=_CSharpKeyword
helpviewer_keywords:
- subtraction assignment operator (-=) [C#]
- -= operator (subtraction assignment ) [C#]
ms.assetid: 05c7d68a-423f-4de8-891b-cf24e8fb6ed7
ms.openlocfilehash: 3b6890be4460a599a5d2f5f5f6ee1627be933f0b
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333331"
---
# <a name="--operator-c-reference"></a><span data-ttu-id="9f61a-102">-= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="9f61a-102">-= operator (C# Reference)</span></span>

<span data-ttu-id="9f61a-103">減算代入演算子です。</span><span class="sxs-lookup"><span data-stu-id="9f61a-103">The subtraction assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f61a-104">コメント</span><span class="sxs-lookup"><span data-stu-id="9f61a-104">Remarks</span></span>

<span data-ttu-id="9f61a-105">次のような `-=` 代入演算子を使用する式があるとします</span><span class="sxs-lookup"><span data-stu-id="9f61a-105">An expression using the `-=` assignment operator, such as</span></span>

```csharp
x -= y
```

 <span data-ttu-id="9f61a-106">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="9f61a-106">is equivalent to</span></span>

```csharp
x = x - y
```

<span data-ttu-id="9f61a-107">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="9f61a-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="9f61a-108">[- 演算子](subtraction-operator.md)の意味は、`x` および `y` の型によって異なります (数値オペランドの場合は減算、デリゲート オペランドの場合はデリゲートの削除、など)。</span><span class="sxs-lookup"><span data-stu-id="9f61a-108">The meaning of the [- operator](subtraction-operator.md) is dependent on the types of `x` and `y` (subtraction for numeric operands, delegate removal for delegate operands, and so forth).</span></span>

<span data-ttu-id="9f61a-109">`-=` 演算子は直接オーバーロードできませんが、ユーザー定義型は [- 演算子](subtraction-operator.md)をオーバーロードできます (「[operator](../keywords/operator.md)」参照)。</span><span class="sxs-lookup"><span data-stu-id="9f61a-109">The `-=` operator cannot be overloaded directly, but user-defined types can overload the [- operator](subtraction-operator.md) (see [operator](../keywords/operator.md)).</span></span>

<span data-ttu-id="9f61a-110">-= 演算子は、C# でイベント サブスクリプションを解除するときにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="9f61a-110">The -= operator is also used in C# to unsubscribe from an event.</span></span> <span data-ttu-id="9f61a-111">詳細については、「[方法 :イベント サブスクリプションとサブスクリプションの解除](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f61a-111">For more information, see [How to: Subscribe to and Unsubscribe from Events](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).</span></span>

## <a name="example"></a><span data-ttu-id="9f61a-112">例</span><span class="sxs-lookup"><span data-stu-id="9f61a-112">Example</span></span>

[!code-csharp[csRefOperators#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#6)]

## <a name="see-also"></a><span data-ttu-id="9f61a-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="9f61a-113">See also</span></span>

- [<span data-ttu-id="9f61a-114">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="9f61a-114">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="9f61a-115">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="9f61a-115">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="9f61a-116">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="9f61a-116">C# operators</span></span>](index.md)
