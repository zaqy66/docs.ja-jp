---
title: '%= 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 09/04/2018
f1_keywords:
- '%=_CSharpKeyword'
helpviewer_keywords:
- remainder assignment operator (%=) [C#]
- '%= assignment operator (remainder assignment) [C#]'
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
ms.openlocfilehash: d0732f9578b64c894ecc1d3bb15cee11a8d5b6a3
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245562"
---
# <a name="-operator-c-reference"></a>%= 演算子 (C# リファレンス)

剰余代入演算子です。

次のような `%=` 演算子を使用する式があるとします  

```csharp
x %= y
```  

上記の式は、次の式と同じです。  

```csharp
x = x % y
```  

ただし、`x` が評価されるのは 1 回だけです。
  
[剰余演算子](remainder-operator.md) (`%`) は、オペランドを除算した後の剰余を計算します。 すべての数値型でサポートされます。

ユーザー定義型により[剰余演算子](remainder-operator.md) `%` が[オーバーロード](../keywords/operator.md)される場合、剰余代入演算子 `%=` が暗黙的にオーバーロードされます。
  
`%=` 演算子の使用例を次に示します。

[!code-csharp-interactive[%= example](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#3)]

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
