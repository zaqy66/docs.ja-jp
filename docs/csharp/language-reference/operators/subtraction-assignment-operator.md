---
title: -= 演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- -=_CSharpKeyword
helpviewer_keywords:
- subtraction assignment operator (-=) [C#]
- -= operator (subtraction assignment ) [C#]
ms.assetid: 05c7d68a-423f-4de8-891b-cf24e8fb6ed7
ms.openlocfilehash: 3b6890be4460a599a5d2f5f5f6ee1627be933f0b
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333331"
---
# <a name="--operator-c-reference"></a>-= 演算子 (C# リファレンス)

減算代入演算子です。

## <a name="remarks"></a>コメント

次のような `-=` 代入演算子を使用する式があるとします

```csharp
x -= y
```

 上記の式は、次の式と同じです。

```csharp
x = x - y
```

ただし、`x` が評価されるのは 1 回だけです。 [- 演算子](subtraction-operator.md)の意味は、`x` および `y` の型によって異なります (数値オペランドの場合は減算、デリゲート オペランドの場合はデリゲートの削除、など)。

`-=` 演算子は直接オーバーロードできませんが、ユーザー定義型は [- 演算子](subtraction-operator.md)をオーバーロードできます (「[operator](../keywords/operator.md)」参照)。

-= 演算子は、C# でイベント サブスクリプションを解除するときにも使用されます。 詳細については、「[方法 :イベント サブスクリプションとサブスクリプションの解除](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md)」を参照してください。

## <a name="example"></a>例

[!code-csharp[csRefOperators#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#6)]

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミング ガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)
