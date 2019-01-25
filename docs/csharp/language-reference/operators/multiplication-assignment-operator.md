---
title: '*= 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '*=_CSharpKeyword'
helpviewer_keywords:
- '*= operator [C#]'
- binary multiplication assignment operator (*=) [C#]
ms.assetid: 2e472155-59db-4dbf-bb94-bcccfa1a794d
ms.openlocfilehash: 2038f3b55d46f3503496275b3d25b17663b8c1db
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333435"
---
# <a name="-operator-c-reference"></a>\*= 演算子 (C# リファレンス)

二項乗算代入演算子です。

## <a name="remarks"></a>コメント

次のような `*=` 代入演算子を使用する式があるとします

```csharp
x *= y
```

上記の式は、次の式と同じです。

```csharp
x = x * y
```

ただし、`x` が評価されるのは 1 回だけです。 [\* 演算子](multiplication-operator.md)は、数値型の乗算のために事前定義されています。

`*=` 演算子は直接オーバーロードできませんが、ユーザー定義型は [\* 演算子](multiplication-operator.md)をオーバーロードできます (「[operator](../keywords/operator.md)」参照)。

## <a name="example"></a>例

[!code-csharp[csRefOperators#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#13)]

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
