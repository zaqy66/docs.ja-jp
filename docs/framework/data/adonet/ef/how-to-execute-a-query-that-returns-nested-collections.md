---
title: '方法: 入れ子になったコレクションを返すクエリを実行します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: f7f385f3-ffcf-4f3b-af35-de8818938e5f
ms.openlocfilehash: f429b8e8f546669fba64b9ee04222d399971936e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654517"
---
# <a name="how-to-execute-a-query-that-returns-nested-collections"></a>方法: 入れ子になったコレクションを返すクエリを実行します。
ここでは、<xref:System.Data.EntityClient.EntityCommand> オブジェクトを使用して概念モデルに対してコマンドを実行する方法、および <xref:System.Data.EntityClient.EntityDataReader> を使用して入れ子になったコレクションの結果を取得する方法について説明します。  
  
### <a name="to-run-the-code-in-this-example"></a>この例のコードを実行するには  
  
1.  追加、 [AdventureWorks Sales Model](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832)をプロジェクトに使用するプロジェクトを構成して、[!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]します。 詳細については、「[方法 :エンティティ データ モデル ウィザードを使用して](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d)します。  
  
2.  アプリケーションのコード ページで、次の `using` ステートメント (Visual Basic の場合は `Imports`) を追加します。  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
## <a name="example"></a>例  
 A*コレクションを入れ子になった*は別のコレクション内にあるコレクションです。 次に示すコードでは、`Contacts` のコレクションと、それぞれの `SalesOrderHeaders` に関連付けられている、`Contact` の入れ子になったコレクションを取得します。  
  
 [!code-csharp[DP EntityServices Concepts#ReturnNestedCollectionWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#returnnestedcollectionwithentitycommand)]
 [!code-vb[DP EntityServices Concepts#ReturnNestedCollectionWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#returnnestedcollectionwithentitycommand)]  
  
## <a name="see-also"></a>関連項目
- [Entity Framework 用の EntityClient プロバイダー](../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md)
