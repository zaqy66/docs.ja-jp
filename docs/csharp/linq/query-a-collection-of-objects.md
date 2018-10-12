---
title: オブジェクトのコレクションの照会 (C# での LINQ)
description: C# で LINQ を使用して、コレクションを照会する方法について説明します。
ms.date: 11/30/2016
ms.assetid: 87a76f8a-0b58-4791-90ea-2fe0a30416c9
ms.openlocfilehash: 7bc59e7009f9ae8d8f66c24e9519d9100404c9c4
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43511385"
---
# <a name="query-a-collection-of-objects"></a>オブジェクトのコレクションの照会

この例では、`Student` オブジェクトのリストに対してシンプルなクエリを実行する方法を示します。 各 `Student` オブジェクトには、生徒に関する基本情報と、4 回の試験での生徒の点数を表すリストが含まれています。  
  
このアプリケーションは、同じ `students` データ ソースを使用する、このセクション内のその他多くの例のフレームワークとして機能します。  
  
## <a name="example"></a>例

次のクエリは、最初の試験で 90 点以上を取った学生を返します。  
  
[!code-csharp[csProgGuideLINQ#15](~/samples/snippets/csharp/concepts/linq/how-to-query-a-collection-of-objects_1.cs)]  
  
このクエリは、実験用として意図的にシンプルに記述されています。 たとえば、`where` 句でより多く条件を試したり、`orderby` 句を使用して結果を並べ替えたりすることもできます。  
  
## <a name="see-also"></a>関連項目

- [統合言語クエリ (LINQ)](index.md)  
- [文字列補間](../language-reference/tokens/interpolated.md)