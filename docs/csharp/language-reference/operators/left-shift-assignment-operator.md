---
title: <<= 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- <<=_CSharpKeyword
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
ms.openlocfilehash: 0a005efa19be24f9adbf9031f562a30f9c1b0e34
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55258735"
---
# <a name="-operator-c-reference"></a>\<\<= 演算子 (C# リファレンス)

左シフト代入演算子。

## <a name="remarks"></a>コメント

次のような形式の式があります。

```csharp
x <<= y
```

これが次のように評価されます。

```csharp
x = x << y
```

ただし、`x` が評価されるのは 1 回だけです。 [<< 演算子](left-shift-operator.md) は、`y` で指定されたビット数だけ `x` を左にシフトします。

`<<=` 演算子は直接オーバーロードできませんが、ユーザー定義型は [<< 演算子](left-shift-operator.md) をオーバーロードできます (「[operator](../keywords/operator.md)」参照)。

## <a name="example"></a>例

[!code-csharp[csRefOperators#12](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#12)]

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
