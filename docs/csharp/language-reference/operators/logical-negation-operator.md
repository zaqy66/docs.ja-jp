---
title: '! 演算子 - C# リファレンス'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '!_CSharpKeyword'
helpviewer_keywords:
- '! operator [C#]'
- logical negation operator (!) [C#]
- NOT operator [C#]
ms.assetid: f5ae133f-8f64-4560-b34f-cd9cd5eed4ad
ms.openlocfilehash: 6b6d1796032f536aac0be49d4f101c1380b4e98f
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333227"
---
# <a name="-operator-c-reference"></a>! operator (C# リファレンス)

論理否定演算子 (`!`) は、オペランドを否定する単項演算子です。 この演算子は `bool` として定義され、オペランドが `false` の場合にのみ、`true` を返します。

## <a name="remarks"></a>コメント

ユーザー定義型は `!` 演算子をオーバーロードできます (「[演算子](../keywords/operator.md)」を参照)。

## <a name="example"></a>例

[!code-csharp[csRefOperators#7](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#7)]

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミングガイド](../../programming-guide/index.md)
- [C# 演算子](index.md)