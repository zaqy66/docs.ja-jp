---
title: Oracle 分散トランザクション
ms.date: 03/30/2017
ms.assetid: c340ca81-ef79-402f-b204-c5156b890fe5
ms.openlocfilehash: 8e7530621254881402570b59b47a22052b40f2b5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54713247"
---
# <a name="oracle-distributed-transactions"></a>Oracle 分散トランザクション
<xref:System.Data.OracleClient.OracleConnection> オブジェクトはトランザクションがアクティブであると判断した場合、既存の分散トランザクションに自動的に参加します。 自動トランザクション参加は、接続が開かれた場合または接続プールから取得された場合に行われます。 既存のトランザクションへの自動参加を無効にするには、  
  
```  
Enlist=false  
```  
  
 を <xref:System.Data.OracleClient.OracleConnection> の接続文字列パラメーターとして指定します。  
  
## <a name="see-also"></a>関連項目
- [Oracle および ADO.NET](../../../../docs/framework/data/adonet/oracle-and-adonet.md)
- [ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター](https://go.microsoft.com/fwlink/?LinkId=217917)
