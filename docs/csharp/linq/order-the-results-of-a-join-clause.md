---
title: join 句の結果の順序指定 (C# での LINQ)
description: C# で LINQ join 句の結果の順序を指定する方法について説明します。
ms.date: 12/1/2016
ms.assetid: a7458901-1201-4c25-b8d9-c04ca52e0eb9
ms.openlocfilehash: e4a12b6f9b4a99decb1f64524ebe67a196084a04
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/03/2018
ms.locfileid: "37404737"
---
# <a name="order-the-results-of-a-join-clause"></a>join 句の結果の順序指定

この例では、結合操作の結果の順序を指定する方法を示しています。 順序付けは結合後に実行されることに注意してください。 結合の前に 1 つ以上のソース シーケンスを指定した `orderby` 句を使用することもできますが、一般にこの方法は推奨されません。 LINQ プロバイダーによっては、結合後にその順序付けを維持しない場合があります。

## <a name="example"></a>例

このクエリは、グループ結合を作成した後、スコープ内に残っているカテゴリ要素に基づいてグループを並べ替えます。 匿名型初期化子の内部では、結果のシーケンス内の一致するすべての要素がサブクエリによって順序付けられます。

[!code-csharp[csProgGuideLINQ#81](~/samples/snippets/csharp/concepts/linq/how-to-order-the-results-of-a-join-clause_1.cs)]

## <a name="see-also"></a>関連項目

[統合言語クエリ (LINQ)](index.md)  
[orderby 句](../language-reference/keywords/orderby-clause.md)  
[join 句](../language-reference/keywords/join-clause.md)  