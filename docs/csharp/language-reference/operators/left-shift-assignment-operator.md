---
title: <<= 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- <<=_CSharpKeyword
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
ms.openlocfilehash: d2105fbee4ddfe1b2cb3325d82b0f2f8c5559297
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219452"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="46c31-102">\<\<= 演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="46c31-102">\<\<= operator (C# Reference)</span></span>

<span data-ttu-id="46c31-103">左シフト代入演算子。</span><span class="sxs-lookup"><span data-stu-id="46c31-103">The left-shift assignment operator.</span></span>

<span data-ttu-id="46c31-104">次のような `<<=` 演算子を使用する式があるとします</span><span class="sxs-lookup"><span data-stu-id="46c31-104">An expression using the `<<=` operator, such as</span></span>

```csharp
x <<= y
```

<span data-ttu-id="46c31-105">上記の式は、次の式と同じです。</span><span class="sxs-lookup"><span data-stu-id="46c31-105">is equivalent to</span></span>

```csharp
x = x << y
```

<span data-ttu-id="46c31-106">ただし、`x` が評価されるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="46c31-106">except that `x` is only evaluated once.</span></span>

<span data-ttu-id="46c31-107">[`<<` 演算子](left-shift-operator.md)では、最初のオペランドが 2 番目のオペランドで定義されたビット数だけ左にシフトされます。</span><span class="sxs-lookup"><span data-stu-id="46c31-107">The [`<<` operator](left-shift-operator.md) shifts its first operand left by the number of bits defined by its second operand.</span></span>

<span data-ttu-id="46c31-108">`<<=` 演算子の使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="46c31-108">The following example demonstrates the usage of the `<<=` operator:</span></span>

[!code-csharp-interactive[left shift assignment](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#LeftShiftAssignment)]

## <a name="operator-overloadability"></a><span data-ttu-id="46c31-109">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="46c31-109">Operator overloadability</span></span>

<span data-ttu-id="46c31-110">ユーザー定義型により、[`<<` 演算子](left-shift-operator.md)が[オーバーロード](../keywords/operator.md)される場合、左シフト代入演算子 `<<=` が暗黙的にオーバーロードされます。</span><span class="sxs-lookup"><span data-stu-id="46c31-110">If a user-defined type [overloads](../keywords/operator.md) the [`<<` operator](left-shift-operator.md), the left-shift assignment operator `<<=` is implicitly overloaded.</span></span> <span data-ttu-id="46c31-111">ユーザー定義型では、左シフト代入演算子を明示的にオーバーロードできません。</span><span class="sxs-lookup"><span data-stu-id="46c31-111">A user-defined type cannot explicitly overload the left-shift assignment operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="46c31-112">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="46c31-112">C# language specification</span></span>

<span data-ttu-id="46c31-113">詳細については、「[C# 言語仕様](../language-specification/index.md)」の[複合代入](~/_csharplang/spec/expressions.md#compound-assignment)に関するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="46c31-113">For more information, see the [Compound assignment](~/_csharplang/spec/expressions.md#compound-assignment) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="46c31-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="46c31-114">See also</span></span>

- [<span data-ttu-id="46c31-115">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="46c31-115">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="46c31-116">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="46c31-116">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="46c31-117">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="46c31-117">C# Operators</span></span>](index.md)
