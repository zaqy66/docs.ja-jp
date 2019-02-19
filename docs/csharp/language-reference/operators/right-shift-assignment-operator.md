---
title: '>>= 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- '>>=_CSharpKeyword'
helpviewer_keywords:
- right shift assignment operator (>>=) [C#]
- '>>= operator (right-shift assignment) [C#]'
ms.assetid: b593778c-b9b4-440d-8b29-c1ac22cb81c0
ms.openlocfilehash: 51914bb5e9ebffd5d868528b5a8d3072a956cea6
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56220914"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="5d8d0-102">>>= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="5d8d0-102">>>= operator (C# Reference)</span></span>

<span data-ttu-id="5d8d0-103">右シフト代入演算子。</span><span class="sxs-lookup"><span data-stu-id="5d8d0-103">The right-shift assignment operator.</span></span>

<span data-ttu-id="5d8d0-104">次のような `>>=` 演算子を使用する式があるとします</span><span class="sxs-lookup"><span data-stu-id="5d8d0-104">An expression using the `>>=` operator, such as</span></span>

```csharp
x >>= y
```

<span data-ttu-id="5d8d0-105">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="5d8d0-105">is equivalent to</span></span>

```csharp
x = x >> y
```

<span data-ttu-id="5d8d0-106">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="5d8d0-106">except that `x` is only evaluated once.</span></span>

<span data-ttu-id="5d8d0-107">[`>>` 演算子](right-shift-operator.md)では、最初のオペランドが 2 番目のオペランドで定義されたビット数だけ右にシフトされます。</span><span class="sxs-lookup"><span data-stu-id="5d8d0-107">The [`>>` operator](right-shift-operator.md) shifts its first operand right by the number of bits defined by its second operand.</span></span>

<span data-ttu-id="5d8d0-108">`>>=` 演算子の使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5d8d0-108">The following example demonstrates the usage of the `>>=` operator:</span></span>

[!code-csharp-interactive[right shift assignment](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShiftAssignment)]

## <a name="operator-overloadability"></a><span data-ttu-id="5d8d0-109">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="5d8d0-109">Operator overloadability</span></span>

<span data-ttu-id="5d8d0-110">ユーザー定義型により、[`>>` 演算子](right-shift-operator.md)が[オーバーロード](../keywords/operator.md)される場合、右シフト代入演算子 `>>=` が暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="5d8d0-110">If a user-defined type [overloads](../keywords/operator.md) the [`>>` operator](right-shift-operator.md), the right-shift assignment operator `>>=` is implicitly overloaded.</span></span> <span data-ttu-id="5d8d0-111">ユーザー定義型では、右シフト代入演算子を明示的にオーバーロードできません。</span><span class="sxs-lookup"><span data-stu-id="5d8d0-111">A user-defined type cannot explicitly overload the right-shift assignment operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="5d8d0-112">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="5d8d0-112">C# language specification</span></span>

<span data-ttu-id="5d8d0-113">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[複合代入](~/_csharplang/spec/expressions.md#compound-assignment)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d8d0-113">For more information, see the [Compound assignment](~/_csharplang/spec/expressions.md#compound-assignment) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5d8d0-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d8d0-114">See also</span></span>

- [<span data-ttu-id="5d8d0-115">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="5d8d0-115">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="5d8d0-116">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="5d8d0-116">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="5d8d0-117">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="5d8d0-117">C# operators</span></span>](index.md)