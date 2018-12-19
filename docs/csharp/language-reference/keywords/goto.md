---
title: goto ステートメント - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- goto_CSharpKeyword
- goto
helpviewer_keywords:
- goto keyword [C#]
ms.assetid: 2c03c9c1-8119-44ef-b740-fb3d287a42fe
ms.openlocfilehash: bfc997631cc147bf5718ec91a57e2995cead052f
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236766"
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
