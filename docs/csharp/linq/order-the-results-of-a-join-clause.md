---
title: join 句の結果の順序指定 (C# での LINQ)
description: C# で LINQ join 句の結果の順序を指定する方法について説明します。
ms.date: 12/1/2016
ms.assetid: a7458901-1201-4c25-b8d9-c04ca52e0eb9
ms.openlocfilehash: 13cd6cb202cf67def17310db6d98e368ce837646
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43516987"
---
# <a name="order-the-results-of-a-join-clause"></a>join 句の結果の順序指定

この例では、結合操作の結果の順序を指定する方法を示しています。 順序付けは結合後に実行されることに注意してください。 結合の前に 1 つ以上のソース シーケンスを指定した `orderby` 句を使用することもできますが、一般にこの方法は推奨されません。 LINQ プロバイダーによっては、結合後にその順序付けを維持しない場合があります。

## <a name="example"></a>例

このクエリは、グループ結合を作成した後、スコープ内に残っているカテゴリ要素に基づいてグループを並べ替えます。 匿名型初期化子の内部では、結果のシーケンス内の一致するすべての要素がサブクエリによって順序付けられます。

[!code-csharp[csProgGuideLINQ#81](~/samples/snippets/csharp/concepts/linq/how-to-order-the-results-of-a-join-clause_1.cs)]

## <a name="see-also"></a>関連項目

- [統合言語クエリ (LINQ)](index.md)  
- [orderby 句](../language-reference/keywords/orderby-clause.md)  
- [join 句](../language-reference/keywords/join-clause.md)  