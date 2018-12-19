---
title: += 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 10/29/2018
f1_keywords:
- +=_CSharpKeyword
helpviewer_keywords:
- += operator [C#]
- addition assignment operator (+=) [C#]
- event subscription [C#]
ms.assetid: 9cdf97e6-331d-492b-85e1-3ec3171484e9
ms.openlocfilehash: 5d48f2fe53a9bb6f781f8d35f1e0983bcaa30f88
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53240932"
---
# <a name="-operator-c-reference"></a>+= 演算子 (C# リファレンス)

加算代入演算子です。

次のような `+=` 演算子を使用する式があるとします

```csharp
x += y
```

上記の式は、次の式と同じです。

```csharp
x = x + y
```

ただし、`x` が評価されるのは 1 回だけです。
  
数値型の場合、[加算演算子](addition-operator.md) `+` によってそのオペランドの合計が計算されます。 一方または両方のオペランドが[文字列型](../keywords/string.md)である場合、そのオペランドの文字列表現を連結します。 デリゲート型の場合、`+` 演算子によって、そのオペランドの組み合わせである新しいデリゲート インスタンスが返されます。

[イベント](../keywords/event.md)をサブスクライブするとき、`+=` 演算子を使用してイベント ハンドラー メソッドを指定することもできます。 詳細については、「[方法 :イベント サブスクリプションとサブスクリプションの解除](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md)」を参照してください。

`+=` 演算子の使用例を次に示します。

[!code-csharp-interactive[+= examples](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddAndAssign)]

## <a name="operator-overloadability"></a>演算子のオーバーロード可/不可

ユーザー定義型により[加算演算子](addition-operator.md) `+` が[オーバーロード](../keywords/operator.md)される場合、加算代入演算子 `+=` が暗黙的にオーバーロードされます。 ユーザー定義型は、加算代入演算子を明示的にオーバー ロードできません。

## <a name="c-language-specification"></a>C# 言語仕様

詳細については、「[C# 言語仕様](../language-specification/index.md)」の[複合代入](~/_csharplang/spec/expressions.md#compound-assignment)と[イベント代入](~/_csharplang/spec/expressions.md#event-assignment)に関するセクションを参照してください。
  
## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
- [イベント](../../programming-guide/events/index.md)
- [デリゲート](../../programming-guide/delegates/index.md)
