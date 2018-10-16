---
title: '%= 演算子 (C# リファレンス)'
ms.date: 09/04/2018
f1_keywords:
- '%=_CSharpKeyword'
helpviewer_keywords:
- remainder assignment operator (%=) [C#]
- '%= assignment operator (remainder assignment) [C#]'
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
ms.openlocfilehash: c475517666bdadaa457dbb4188808b3a96fcdf0e
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44085648"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="1b934-102">%= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="1b934-102">%= Operator (C# Reference)</span></span>

<span data-ttu-id="1b934-103">剰余代入演算子です。</span><span class="sxs-lookup"><span data-stu-id="1b934-103">The remainder assignment operator.</span></span>

<span data-ttu-id="1b934-104">次のような `%=` 演算子を使用する式があるとします</span><span class="sxs-lookup"><span data-stu-id="1b934-104">An expression using the `%=` operator, such as</span></span>  

```csharp
x %= y
```  

<span data-ttu-id="1b934-105">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="1b934-105">is equivalent to</span></span>  

```csharp
x = x % y
```  

<span data-ttu-id="1b934-106">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="1b934-106">except that `x` is only evaluated once.</span></span>
  
<span data-ttu-id="1b934-107">[剰余演算子](remainder-operator.md) `%` はあらゆる数値型でサポートされており、そのオペランドの除算後の剰余を計算します。</span><span class="sxs-lookup"><span data-stu-id="1b934-107">The [remainder operator](remainder-operator.md) `%` is supported by all numeric types and computes the remainder after division of its operands.</span></span>

<span data-ttu-id="1b934-108">ユーザー定義型により[剰余演算子](remainder-operator.md) `%` が[オーバーロード](../keywords/operator.md)される場合、剰余代入演算子 `%=` が暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="1b934-108">If a user-defined type [overloads](../keywords/operator.md) the [remainder operator](remainder-operator.md) `%`, the remainder assignment operator `%=` is implicitly overloaded.</span></span>
  
<span data-ttu-id="1b934-109">`%=` 演算子の使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="1b934-109">The following example demonstrates the usage of the `%=` operator:</span></span>

[!code-csharp-interactive[%= example](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#3)]

## <a name="see-also"></a><span data-ttu-id="1b934-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b934-110">See also</span></span>

- [<span data-ttu-id="1b934-111">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="1b934-111">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="1b934-112">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="1b934-112">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="1b934-113">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="1b934-113">C# Operators</span></span>](index.md)
