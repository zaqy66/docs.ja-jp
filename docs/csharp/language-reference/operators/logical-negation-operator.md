---
title: '! 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 02/14/2019
f1_keywords:
- '!_CSharpKeyword'
helpviewer_keywords:
- '! operator [C#]'
- logical negation operator (!) [C#]
- NOT operator [C#]
ms.assetid: f5ae133f-8f64-4560-b34f-cd9cd5eed4ad
ms.openlocfilehash: 464bd658c9bf430191d84d3d5ad8d57173ab87c5
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2019
ms.locfileid: "56303713"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="6460f-103">!</span><span class="sxs-lookup"><span data-stu-id="6460f-103">!</span></span> <span data-ttu-id="6460f-104">演算子 (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="6460f-104">operator (C# Reference)</span></span>

<span data-ttu-id="6460f-105">論理否定演算子 `!` は、[bool](../keywords/bool.md) オペランドの論理否定を計算する単項演算子です。</span><span class="sxs-lookup"><span data-stu-id="6460f-105">The logical negation operator `!` is a unary operator that computes logical negation of its [bool](../keywords/bool.md) operand.</span></span> <span data-ttu-id="6460f-106">つまり、オペランドが `false` の場合は `true` を生成し、オペランドが `true` の場合は `false` を生成します:</span><span class="sxs-lookup"><span data-stu-id="6460f-106">That is, it produces `true`, if the operand is `false`, and `false`, if the operand is `true`:</span></span>

[!code-csharp-interactive[logical negation](~/samples/snippets/csharp/language-reference/operators/LogicalNegationExamples.cs#Example)]

## <a name="operator-overloadability"></a><span data-ttu-id="6460f-107">演算子のオーバーロード可/不可</span><span class="sxs-lookup"><span data-stu-id="6460f-107">Operator overloadability</span></span>

<span data-ttu-id="6460f-108">ユーザー定義型は `!` 演算子を[オーバーロード](../keywords/operator.md)できます。</span><span class="sxs-lookup"><span data-stu-id="6460f-108">User-defined types can [overload](../keywords/operator.md) the `!` operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="6460f-109">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="6460f-109">C# language specification</span></span>

<span data-ttu-id="6460f-110">詳細については、[C# 言語仕様](../language-specification/index.md)に関するページの「[論理否定演算子](~/_csharplang/spec/expressions.md#logical-negation-operator)」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6460f-110">For more information, see the [Logical negation operator](~/_csharplang/spec/expressions.md#logical-negation-operator) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6460f-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="6460f-111">See also</span></span>

- [<span data-ttu-id="6460f-112">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="6460f-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="6460f-113">C# プログラミングガイド</span><span class="sxs-lookup"><span data-stu-id="6460f-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="6460f-114">C# 演算子</span><span class="sxs-lookup"><span data-stu-id="6460f-114">C# Operators</span></span>](index.md)