---
title: goto ステートメント (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- goto_CSharpKeyword
- goto
helpviewer_keywords:
- goto keyword [C#]
ms.assetid: 2c03c9c1-8119-44ef-b740-fb3d287a42fe
ms.openlocfilehash: d4fd9f1f26b82b409d704c45e4bcf18cceef8282
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43405817"
---
# <a name="goto-c-reference"></a>goto (C# リファレンス)

`goto` ステートメントは、プログラムの制御をラベル付きステートメントに直接移します。

`goto` の一般的な用途は、特定の switch-case ラベルまたは `switch` ステートメントの既定のラベルに、制御を移動することです。

`goto` ステートメントは、深い入れ子のループから抜ける場合にも便利です。

## <a name="example"></a>例

次の例では、[switch](switch.md) ステートメントでの `goto` の使い方を示します。

[!code-csharp[csrefKeywordsJump#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsJump/CS/csrefKeywordsJump.cs#4)]

## <a name="example"></a>例

次の例では、`goto` を使って入れ子になったループから抜け出す方法を示します。

[!code-csharp[csrefKeywordsJump#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsJump/CS/csrefKeywordsJump.cs#5)]

## <a name="c-language-specification"></a>C# 言語仕様

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>関連項目

- [C# リファレンス](../index.md)  
- [C# プログラミング ガイド](../../programming-guide/index.md)  
- [C# のキーワード](index.md)  
- [goto ステートメント (C++)](/cpp/cpp/goto-statement-cpp)  
- [ジャンプ ステートメント](jump-statements.md)  
