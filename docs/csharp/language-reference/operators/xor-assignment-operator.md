---
title: ^= 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ^=_CSharpKeyword
helpviewer_keywords:
- ^= operator [C#]
ms.assetid: 3658ff9a-61cd-467e-ad6b-8fbf1cfbaae4
ms.openlocfilehash: 12189d6469a9716d3b7ebcffef23423a75692d1a
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333552"
---
# <a name="-operator-c-reference"></a>^= 演算子 (C# リファレンス)

排他的 OR 代入演算子。

## <a name="remarks"></a>コメント

次のような形式の式があります。

```csharp
x ^= y
```

これが次のように評価されます。

```csharp
x = x ^ y
```

ただし、`x` が評価されるのは 1 回だけです。 [^ 演算子](xor-operator.md)は整数オペランドにビット演算排他的 OR 操作を実行し、[ブール](../keywords/bool.md) オペランドに論理的 OR 操作を実行します。

^= 演算子は直接オーバーロードできませんが、ユーザー定義型は [^ 演算子](xor-operator.md)をオーバーロードできます (「[演算子](../keywords/operator.md)」参照)。

## <a name="example"></a>例

[!code-csharp[csRefOperators#23](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#23)]

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミング ガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)