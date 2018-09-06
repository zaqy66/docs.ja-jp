---
title: SQL Server のバイナリ データと大きな値のデータ
ms.date: 03/30/2017
ms.assetid: e00827b3-7511-4b2d-91d7-851ca86cc6b5
ms.openlocfilehash: 9ebbe23dfbcac7825ce449dd40f62b921d13ab4a
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43879104"
---
# <a name="sql-server-binary-and-large-value-data"></a>SQL Server のバイナリ データと大きな値のデータ
SQL Server では `max` 指定子が提供されています。これにより、`varchar`、`nvarchar`、および `varbinary` データ型の記憶容量が拡張されています。 `varchar(max)`、 `nvarchar(max)`、および`varbinary(max)`は、総称*大きな値データ型*します。 大きな値のデータ型を使用すると、最大で 2^31-1 バイトのデータを格納できます。  
  
 SQL Server 2008 では FILESTREAM 属性が導入されました。これはデータ型ではありませんが、列に定義できる属性であり、これを使用すると大きな値のデータをデータベースではなくファイル システムに格納できます。  
  
## <a name="in-this-section"></a>このセクションの内容  
 [ADO.NET での大きい値 (max) データの変更](../../../../../docs/framework/data/adonet/sql/modifying-large-value-max-data.md)  
 大きな値のデータ型を扱う方法について説明します。  
  
 [FILESTREAM データ](../../../../../docs/framework/data/adonet/sql/filestream-data.md)  
 SQL Server 2008 で FILESTREAM 属性を使用して保存された大きな値のデータを扱う方法について説明します。  
  
## <a name="see-also"></a>関連項目  
 [SQL Server データ型と ADO.NET](../../../../../docs/framework/data/adonet/sql/sql-server-data-types.md)  
 [ADO.NET における SQL Server データ操作](../../../../../docs/framework/data/adonet/sql/sql-server-data-operations.md)  
 [ADO.NET でのデータの取得および変更](../../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)  
 [ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター](https://go.microsoft.com/fwlink/?LinkId=217917)
