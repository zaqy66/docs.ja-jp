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
# <a name="-operator-c-reference"></a>! 演算子 (C# リファレンス)

論理否定演算子 `!` は、[bool](../keywords/bool.md) オペランドの論理否定を計算する単項演算子です。 つまり、オペランドが `false` の場合は `true` を生成し、オペランドが `true` の場合は `false` を生成します:

[!code-csharp-interactive[logical negation](~/samples/snippets/csharp/language-reference/operators/LogicalNegationExamples.cs#Example)]

## <a name="operator-overloadability"></a>演算子のオーバーロード可/不可

ユーザー定義型は `!` 演算子を[オーバーロード](../keywords/operator.md)できます。

## <a name="c-language-specification"></a>C# 言語仕様

詳細については、[C# 言語仕様](../language-specification/index.md)に関するページの「[論理否定演算子](~/_csharplang/spec/expressions.md#logical-negation-operator)」セクションを参照してください。

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)