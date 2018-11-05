---
title: '%= 演算子 (C# リファレンス)'
ms.date: 09/04/2018
f1_keywords:
- '%=_CSharpKeyword'
helpviewer_keywords:
- remainder assignment operator (%=) [C#]
- '%= assignment operator (remainder assignment) [C#]'
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
ms.openlocfilehash: ab3a6a8d5cbfeb4d527ca1f9c233ddfaba3d35ff
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188717"
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
