---
title: '&gt;&gt;= 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '>>=_CSharpKeyword'
helpviewer_keywords:
- right shift assignment operator (>>=) [C#]
- '>>= operator (right-shift assignment) [C#]'
ms.assetid: b593778c-b9b4-440d-8b29-c1ac22cb81c0
ms.openlocfilehash: 02a9559a5c4086eeed09094c15c3620366ffad8c
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333691"
---
# <a name="gtgt-operator-c-reference"></a>&gt;&gt;= 演算子 (C# リファレンス)

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