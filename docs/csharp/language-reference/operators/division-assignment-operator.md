---
title: /= 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 12/13/2018
f1_keywords:
- /=_CSharpKeyword
helpviewer_keywords:
- division assignment operator (/=) [C#]
- /= (division assignment operator) [C#]
ms.assetid: 50fc02b0-ee9c-4c3e-b58d-d591282caf1c
ms.openlocfilehash: ed4dd6c0c944b77543aae4de8d51534b4df4f4ef
ms.sourcegitcommit: d6e419f9d9cd7e8f21ebf5acde6d016c16332579
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/12/2018
ms.locfileid: "53286521"
---
# <a name="-operator-c-reference"></a>/= 演算子 (C# リファレンス)

除算代入演算子です。

次のような `/=` 演算子を使用する式があるとします

```csharp
x /= y
```

上記の式は、次の式と同じです。

```csharp
x = x / y
```

ただし、`x` が評価されるのは 1 回だけです。

[除算演算子](division-operator.md) `/` は、1 つ目のオペランドを 2 つ目のオペランドで除算します。 すべての数値型でサポートされます。

`/=` 演算子の使用例を次に示します。

[!code-csharp-interactive[divide and assign](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#DivisionAssignment)]

## <a name="operator-overloadability"></a>演算子のオーバーロード可/不可

ユーザー定義型により[除算演算子](division-operator.md) `/` が[オーバーロード](../keywords/operator.md)される場合、除算代入演算子 `/=` が暗黙的にオーバーロードされます。 ユーザー定義型は、除算代入演算子を明示的にオーバー ロードできません。

## <a name="c-language-specification"></a>C# 言語仕様

詳細については、「[C# 言語仕様](../language-specification/index.md)」の[複合代入](~/_csharplang/spec/expressions.md#compound-assignment)に関するセクションを参照してください。

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
