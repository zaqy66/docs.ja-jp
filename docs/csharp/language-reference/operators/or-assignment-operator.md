---
title: '|= 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '|=_CSharpKeyword'
helpviewer_keywords:
- OR assignment operator (|=) [C#]
- '|= operator (OR assignment) [C#]'
ms.assetid: 8315b8cf-dd15-402f-92f0-c7db931696ca
ms.openlocfilehash: f4f7806c8679af400a371decd0c367929b3fb81d
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333266"
---
# <a name="-operator-c-reference"></a>|= 演算子 (C# リファレンス)

OR 代入演算子です。

## <a name="remarks"></a>コメント

次のような `|=` 代入演算子を使用する式があるとします

```csharp
x |= y
```

上記の式は、次の式と同じです。

```csharp
x = x | y
```

ただし、`x` が評価されるのは 1 回だけです。 [&#124; 演算子](or-operator.md)では、整数のオペランドではビットごとの論理 OR 演算、ブール オペランドでは論理 OR 演算が実行されます。

`|=` 演算子は直接オーバーロードできませんが、ユーザー定義型は [&#124; 演算子](or-operator.md)をオーバーロードできます (「[operator](../keywords/operator.md)」参照)。

## <a name="example"></a>例

[!code-csharp[csRefOperators#10](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#10)]

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミング ガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)