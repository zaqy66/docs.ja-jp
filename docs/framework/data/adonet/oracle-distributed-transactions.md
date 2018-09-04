---
title: Oracle 分散トランザクション
ms.date: 03/30/2017
ms.assetid: c340ca81-ef79-402f-b204-c5156b890fe5
ms.openlocfilehash: a3b8a50b42b945a0cdc1cbfbc4cc9eab835e90e4
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43505400"
---
# <a name="oracle-distributed-transactions"></a><span data-ttu-id="b9056-102">Oracle 分散トランザクション</span><span class="sxs-lookup"><span data-stu-id="b9056-102">Oracle Distributed Transactions</span></span>
<span data-ttu-id="b9056-103"><xref:System.Data.OracleClient.OracleConnection> オブジェクトはトランザクションがアクティブであると判断した場合、既存の分散トランザクションに自動的に参加します。</span><span class="sxs-lookup"><span data-stu-id="b9056-103">The <xref:System.Data.OracleClient.OracleConnection> object automatically enlists in an existing distributed transaction if it determines that a transaction is active.</span></span> <span data-ttu-id="b9056-104">自動トランザクション参加は、接続が開かれた場合または接続プールから取得された場合に行われます。</span><span class="sxs-lookup"><span data-stu-id="b9056-104">Automatic transaction enlistment occurs when the connection is opened or retrieved from the connection pool.</span></span> <span data-ttu-id="b9056-105">既存のトランザクションへの自動参加を無効にするには、</span><span class="sxs-lookup"><span data-stu-id="b9056-105">You can disable auto-enlistment in existing transactions by specifying</span></span>  
  
```  
Enlist=false  
```  
  
 <span data-ttu-id="b9056-106">を <xref:System.Data.OracleClient.OracleConnection> の接続文字列パラメーターとして指定します。</span><span class="sxs-lookup"><span data-stu-id="b9056-106">as a connection string parameter for an <xref:System.Data.OracleClient.OracleConnection>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b9056-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="b9056-107">See Also</span></span>  
 [<span data-ttu-id="b9056-108">Oracle および ADO.NET</span><span class="sxs-lookup"><span data-stu-id="b9056-108">Oracle and ADO.NET</span></span>](../../../../docs/framework/data/adonet/oracle-and-adonet.md)  
 [<span data-ttu-id="b9056-109">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="b9056-109">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
