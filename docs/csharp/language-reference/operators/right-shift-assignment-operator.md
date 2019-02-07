---
title: '>>= 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '>>=_CSharpKeyword'
helpviewer_keywords:
- right shift assignment operator (>>=) [C#]
- '>>= operator (right-shift assignment) [C#]'
ms.assetid: b593778c-b9b4-440d-8b29-c1ac22cb81c0
ms.openlocfilehash: 8cc341c14ee1b90fde2abb369c187e57b4ce5c00
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55278981"
---
# <a name="-operator-c-reference"></a>>>= 演算子 (C# リファレンス)

右シフト代入演算子。

## <a name="remarks"></a>コメント

次のような形式の式があります。

```csharp
x >>= y
```

これが次のように評価されます。

```csharp
x = x >> y
```

ただし、`x` が評価されるのは 1 回だけです。 [>> 演算子](right-shift-operator.md)は、`y` で指定された量だけ `x` を右にシフトします。

>>= 演算子は直接オーバーロードできませんが、ユーザー定義型は [>> 演算子](right-shift-operator.md)をオーバーロードできます (「[operator](../keywords/operator.md)」参照)。

## <a name="example"></a>例

[!code-csharp[csRefOperators#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#11)]

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミング ガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)