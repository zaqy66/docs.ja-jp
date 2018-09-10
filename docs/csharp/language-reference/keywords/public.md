---
title: public キーワード (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- public
- public_CSharpKeyword
helpviewer_keywords:
- public keyword [C#]
ms.assetid: 0ae45d16-a551-4b74-9845-57208de1328e
ms.openlocfilehash: 84a3bc49b6eea047d518edc01dab7f2301854b6a
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43484158"
---
# <a name="public-c-reference"></a>public (C# リファレンス)

`public` キーワードは、型と型のメンバーを示すアクセス修飾子です。 パブリック アクセスは、最も制限の少ないアクセス レベルです。 次の例のように、パブリック メンバーへのアクセスには制限がありません。

```csharp
class SampleClass
{
    public int x; // No access restrictions.
}
```

詳しくは、「[アクセス修飾子](../../programming-guide/classes-and-structs/access-modifiers.md)」および「[アクセシビリティ レベル](accessibility-levels.md)」をご覧ください。

## <a name="example"></a>例

次の例では、2 つのクラス (`PointTest` と `MainClass`) が宣言されています。 `PointTest` のパブリック メンバー `x` および `y` は、`MainClass` から直接アクセスされます。

[!code-csharp[csrefKeywordsModifiers#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#13)]

`public` アクセス レベルを [private](private.md) または [protected](protected.md) に変更すると、次のエラー メッセージが表示されます。

'PointTest.y' はアクセスできない保護レベルになっています。

## <a name="c-language-specification"></a>C# 言語仕様

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)
- [C# プログラミング ガイド](../../programming-guide/index.md)
- [アクセス修飾子](../../programming-guide/classes-and-structs/access-modifiers.md)
- [C# のキーワード](index.md)
- [アクセス修飾子](access-modifiers.md)
- [アクセシビリティ レベル](accessibility-levels.md)
- [修飾子](modifiers.md)
- [private](private.md)
- [protected](protected.md)
- [internal](internal.md)