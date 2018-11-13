---
title: '&amp;= 演算子 (C# リファレンス)'
ms.date: 10/29/2018
f1_keywords:
- '&=_CSharpKeyword'
helpviewer_keywords:
- AND assignment operator (&=) [C#]
- '&= operator [C#]'
ms.assetid: e8d58f3f-72dd-4b5a-b995-452fcce7e6bb
ms.openlocfilehash: 8ce27c999cf21a9059ba23ee3c86b8fa024c7341
ms.sourcegitcommit: 3b1cb8467bd73dee854b604e306c0e7e3882d91a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "50980610"
---
# <a name="amp-operator-c-reference"></a>&amp;= 演算子 (C# リファレンス)

AND 代入演算子です。

次のような `&=` 演算子を使用する式があるとします

```csharp
x &= y
```

上記の式は、次の式と同じです。

```csharp
x = x & y
```

ただし、`x` が評価されるのは 1 回だけです。

整数オペランドの場合、[`&` 演算子](and-operator.md)はそのオペランドのビット演算論理 AND を計算しますが、[bool](../keywords/bool.md) オペランドの場合は、そのオペランドの論理 AND を計算します。

`&=` 演算子の使用例を次に示します。

[!code-csharp-interactive[AND assignment example](~/samples/snippets/csharp/language-reference/operators/AndOperatorExamples.cs#AndAssignmentExample)]

## <a name="operator-overloadability"></a>演算子のオーバーロード可/不可

ユーザー定義型により、[`&` 演算子](and-operator.md)が[オーバーロード](../keywords/operator.md)される場合、AND 代入演算子 `&=` が暗黙的にオーバーロードされます。 ユーザー定義型は、AND 代入演算子を明示的にオーバー ロードできません。

## <a name="c-language-specification"></a>C# 言語仕様

詳細については、「[C# 言語仕様](../language-specification/index.md)」の[複合代入](~/_csharplang/spec/expressions.md#compound-assignment)に関するセクションを参照してください。

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
