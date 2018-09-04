---
title: ポリモーフィック クエリを実行する方法
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 2f05da1e-845b-4f14-83e4-c6353a850553
ms.openlocfilehash: ae491d0eeda7f8703dca174bdf4c5c847f78e675
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43489696"
---
# <a name="how-to-execute-a-polymorphic-query"></a>ポリモーフィック クエリを実行する方法
このトピックでは、ポリモーフィックなを実行する方法を示しています。[!INCLUDE[esql](../../../../../includes/esql-md.md)]クエリを使用して、 [OFTYPE](../../../../../docs/framework/data/adonet/ef/language-reference/oftype-entity-sql.md)演算子。  
  
### <a name="to-run-the-code-in-this-example"></a>この例のコードを実行するには  
  
1.  追加、 [School モデル](https://msdn.microsoft.com/library/859a9587-81ea-4a45-9bc0-f8d330e1adac)をプロジェクトに Entity Framework を使用してプロジェクトを構成するとします。 詳細については、次を参照してください。[方法: Entity Data Model ウィザードを使用して、](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d)します。  
  
2.  アプリケーションのコード ページで、次の `using` ステートメント (Visual Basic の場合は `Imports`) を追加します。  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
3.  次の手順に従ってテーブル-hierrachy ごとの継承を有効にして、概念モデルを変更[チュートリアル: 継承のマッピング-Table-per-hierarchy](https://msdn.microsoft.com/library/49b685cf-9db8-4d6d-b885-8837ed238f55)します。  
  
## <a name="example"></a>例  
 次の例では、OFTYPE 演算子を使用し、`OnsiteCourses` のコレクションから `Courses` のコレクションだけを取得して表示します。  
  
 [!code-csharp[DP EntityServices Concepts#PolymorphicQuery](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#polymorphicquery)]
 [!code-vb[DP EntityServices Concepts#PolymorphicQuery](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#polymorphicquery)]  
  
## <a name="see-also"></a>関連項目  
 [Entity Framework 用の EntityClient プロバイダー](../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md)  
 [Entity SQL 言語](../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-language.md)
