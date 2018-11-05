---
title: '%= 演算子 (C# リファレンス)'
ms.date: 09/04/2018
f1_keywords:
- '%=_CSharpKeyword'
helpviewer_keywords:
- remainder assignment operator (%=) [C#]
- '%= assignment operator (remainder assignment) [C#]'
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
ms.openlocfilehash: ab3a6a8d5cbfeb4d527ca1f9c233ddfaba3d35ff
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188717"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="37c7a-102">%= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="37c7a-102">%= Operator (C# Reference)</span></span>

<span data-ttu-id="37c7a-103">剰余代入演算子です。</span><span class="sxs-lookup"><span data-stu-id="37c7a-103">The remainder assignment operator.</span></span>

<span data-ttu-id="37c7a-104">次のような `%=` 演算子を使用する式があるとします</span><span class="sxs-lookup"><span data-stu-id="37c7a-104">An expression using the `%=` operator, such as</span></span>  

```csharp
x %= y
```  

<span data-ttu-id="37c7a-105">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="37c7a-105">is equivalent to</span></span>  

```csharp
x = x % y
```  

<span data-ttu-id="37c7a-106">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="37c7a-106">except that `x` is only evaluated once.</span></span>
  
<span data-ttu-id="37c7a-107">[剰余演算子](remainder-operator.md) (`%`) は、オペランドを除算した後の剰余を計算します。</span><span class="sxs-lookup"><span data-stu-id="37c7a-107">The [remainder operator](remainder-operator.md) `%` computes the remainder after division of its operands.</span></span> <span data-ttu-id="37c7a-108">すべての数値型でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="37c7a-108">It's supported by all numeric types.</span></span>

<span data-ttu-id="37c7a-109">ユーザー定義型により[剰余演算子](remainder-operator.md) `%` が[オーバーロード](../keywords/operator.md)される場合、剰余代入演算子 `%=` が暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="37c7a-109">If a user-defined type [overloads](../keywords/operator.md) the [remainder operator](remainder-operator.md) `%`, the remainder assignment operator `%=` is implicitly overloaded.</span></span>
  
<span data-ttu-id="37c7a-110">`%=` 演算子の使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="37c7a-110">The following example demonstrates the usage of the `%=` operator:</span></span>

[!code-csharp-interactive[%= example](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#3)]

## <a name="see-also"></a><span data-ttu-id="37c7a-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="37c7a-111">See also</span></span>

- [<span data-ttu-id="37c7a-112">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="37c7a-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="37c7a-113">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="37c7a-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="37c7a-114">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="37c7a-114">C# Operators</span></span>](index.md)
