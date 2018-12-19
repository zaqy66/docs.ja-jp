---
title: '|| 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 11/06/2018
f1_keywords:
- '||_CSharpKeyword'
helpviewer_keywords:
- logical OR operator [C#]
- conditional-OR operator (||) [C#]
- '|| operator [C#]'
ms.assetid: 7d442d8e-400d-421f-b4d2-034bf82bcbdc
ms.openlocfilehash: f4bb7ada12fbcebcb90fb7cd22d6e6bccad5fb57
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53244571"
---
# <a name="-operator-c-reference"></a>|| 演算子 (C# リファレンス)

条件論理 OR 演算子 `||` は、"短絡" 論理 OR 演算子とも呼ばれ、その [bool](../keywords/bool.md) オペランドの論理 OR を計算します。 `x` または `y` のどちらかが `true` と評価された場合、`x || y` の結果は `true` になります。 それ以外の場合、結果は `false` です。 最初のオペランドが `true` と評価されると、2 番目のオペランドは評価されず、演算の結果は `true` になります。 次の例は、その動作を示します。

[!code-csharp-interactive[conditional logical OR](~/samples/snippets/csharp/language-reference/operators/ConditionalLogicalOperatorsExamples.cs#Or)]

[論理 OR 演算子](or-operator.md) `|` もその `bool` オペランドの論理 OR を計算しますが、常に両方のオペランドを評価します。

## <a name="operator-overloadability"></a>演算子のオーバーロード可/不可

ユーザー定義型は条件論理 OR 演算子をオーバーロードできません。 ただし、ユーザー定義型が[論理 OR](or-operator.md) と [true および false 演算子](../keywords/true-false-operators.md)を特定の方法でオーバーロードしている場合は、その型のオペランドに対する `||` 演算の評価が可能になります。 詳細については、「[C# 言語仕様](../language-specification/index.md)」の[ユーザー定義型条件論理演算子](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators)に関するセクションを参照してください。

## <a name="c-language-specification"></a>C# 言語仕様

詳細については、「[C# 言語仕様](../language-specification/index.md)」の[条件論理演算子](~/_csharplang/spec/expressions.md#conditional-logical-operators)に関するセクションを参照してください。

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
- [&& 演算子](conditional-and-operator.md)
- [! 演算子](logical-negation-operator.md)
- [| 演算子](or-operator.md)
