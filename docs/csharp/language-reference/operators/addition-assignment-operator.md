---
title: += 演算子 (C# リファレンス)
ms.date: 10/22/2018
f1_keywords:
- +=_CSharpKeyword
helpviewer_keywords:
- += operator [C#]
- addition assignment operator (+=) [C#]
- event subscription [C#]
ms.assetid: 9cdf97e6-331d-492b-85e1-3ec3171484e9
ms.openlocfilehash: ee335e3e2e7d352d4e26b802bad2b08a05c666ab
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50192032"
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

ユーザー定義型により[加算演算子](addition-operator.md) `+` が[オーバーロード](../keywords/operator.md)される場合、加算代入演算子 `+=` が暗黙的にオーバーロードされます。

[イベント](../keywords/event.md)をサブスクライブするとき、`+=` 演算子を使用してイベント ハンドラー メソッドを指定することもできます。 詳細については、「[方法: イベント サブスクリプションとサブスクリプションの解除](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md)」を参照してください。

`+=` 演算子の使用例を次に示します。

[!code-csharp-interactive[+= examples](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddAndAssign)]
  
## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
- [イベント](../../programming-guide/events/index.md)
- [デリゲート](../../programming-guide/delegates/index.md)
