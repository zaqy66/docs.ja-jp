---
title: remove コンテキスト キーワード (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- remove_CSharpKeyword
helpviewer_keywords:
- remove event accessor [C#]
ms.assetid: c8223426-c17b-4fe2-8406-01564cf1dd2b
ms.openlocfilehash: 70b324b8bca09701ead398eb6586ad181826e5f4
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2018
ms.locfileid: "43457139"
---
# <a name="remove-c-reference"></a>remove (C# リファレンス)

`remove` コンテキスト キーワードは、カスタム イベント アクセサーを定義するときに使用されます。このアクセサーは、クライアント コードが[イベント](event.md)から登録を解除するときに呼び出されます。 カスタムの `remove` アクセサーを指定するときは、[add](add.md) アクセサーも指定する必要があります。

## <a name="example"></a>例

次の例は、カスタムの [add](add.md) アクセサーと `remove` アクセサーが指定されているイベントを示しています。 サンプル全体については、「[方法: インターフェイス イベントを実装する](../../programming-guide/events/how-to-implement-interface-events.md)」を参照してください。

 [!code-csharp[csrefKeywordsContextual#15](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#15)]

通常は、独自のカスタム イベント アクセサーを提供する必要はありません。 イベントを宣言するときにコンパイラで自動生成されるアクセサーは、ほとんどのシナリオで利用することができます。

## <a name="see-also"></a>関連項目

- [イベント](../../programming-guide/events/index.md)