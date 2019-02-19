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
# <a name="-operator-c-reference"></a>>>= 演算子 (C# リファレンス)

右シフト代入演算子。

次のような `>>=` 演算子を使用する式があるとします

```csharp
x >>= y
```

上記の式は、次の式と同じです。

```csharp
x = x >> y
```

ただし、`x` が評価されるのは 1 回だけです。

[`>>` 演算子](right-shift-operator.md)では、最初のオペランドが 2 番目のオペランドで定義されたビット数だけ右にシフトされます。

`>>=` 演算子の使用例を次に示します。

[!code-csharp-interactive[right shift assignment](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShiftAssignment)]

## <a name="operator-overloadability"></a>演算子のオーバーロード可/不可

ユーザー定義型により、[`>>` 演算子](right-shift-operator.md)が[オーバーロード](../keywords/operator.md)される場合、右シフト代入演算子 `>>=` が暗黙的にオーバーロードされます。 ユーザー定義型では、右シフト代入演算子を明示的にオーバーロードできません。

## <a name="c-language-specification"></a>C# 言語仕様

詳細については、「[C# 言語仕様](../language-specification/index.md)」の[複合代入](~/_csharplang/spec/expressions.md#compound-assignment)に関するセクションを参照してください。

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミング ガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)