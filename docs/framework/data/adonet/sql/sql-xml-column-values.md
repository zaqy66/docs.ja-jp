---
title: SQL XML 列値
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d97ce4da-f09c-4d1e-85b7-a0ccedd7246a
ms.openlocfilehash: b46c763e7cddfc7617c9a6a23428f83a54955ba0
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "48781974"
---
# <a name="sql-xml-column-values"></a>SQL XML 列値
SQL Server では、`xml`データ型の場合は、開発者が標準の動作を使用してこの型を含む結果セットを取得し、<xref:System.Data.SqlClient.SqlCommand>クラス。 `xml` 列は、その他の列と同じようにして (<xref:System.Data.SqlClient.SqlDataReader> などに) 取得することができますが、その列の内容を XML として使用する場合は、<xref:System.Xml.XmlReader> を使用する必要があります。  
  
## <a name="example"></a>例  
 次のコンソール アプリケーションでは、それぞれ 2 つの行を選択します。、`xml`列から、 **Sales.Store**テーブルに、 **AdventureWorks**データベースを、<xref:System.Data.SqlClient.SqlDataReader>インスタンス。 それぞれの行について、`xml` 列の値は、<xref:System.Data.SqlClient.SqlDataReader.GetSqlXml%2A> の <xref:System.Data.SqlClient.SqlDataReader> メソッドを使用して読み取ります。 値は、<xref:System.Xml.XmlReader> に格納されます。 内容を <xref:System.Data.SqlClient.SqlDataReader.GetSqlXml%2A> 変数に設定する場合は、<xref:System.Data.IDataRecord.GetValue%2A> メソッドではなく <xref:System.Data.SqlTypes.SqlXml> を使用する必要があることに注意してください。<xref:System.Data.IDataRecord.GetValue%2A> は、`xml` 列の値を文字列として返します。  
  
> [!NOTE]
>  **AdventureWorks**既定では、SQL Server をインストールするときにサンプル データベースはインストールされません。 SQL Server Setup を実行してインストールします。  
  
 [!code-csharp[DataWorks SqlClient.GetXmlDataReader#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlClient.GetXmlDataReader/CS/source.cs#1)]
 [!code-vb[DataWorks SqlClient.GetXmlDataReader#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlClient.GetXmlDataReader/VB/source.vb#1)]  
  
## <a name="see-also"></a>関連項目  
 <xref:System.Data.SqlTypes.SqlXml>  
 [SQL Server における XML データ](../../../../../docs/framework/data/adonet/sql/xml-data-in-sql-server.md)  
 [ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター](https://go.microsoft.com/fwlink/?LinkId=217917)
