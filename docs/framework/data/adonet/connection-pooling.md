---
title: 接続プール
ms.date: 03/30/2017
ms.assetid: 955c057f-aea8-4ba8-aa6d-e3dfa18ba8d5
ms.openlocfilehash: 28a1036f377326b5f1fdfafa1eaffd8a47bc05bc
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2018
ms.locfileid: "45678510"
---
# <a name="connection-pooling"></a><span data-ttu-id="594ae-102">接続プール</span><span class="sxs-lookup"><span data-stu-id="594ae-102">Connection Pooling</span></span>
<span data-ttu-id="594ae-103">データ ソースへの接続は時間のかかる処理です。</span><span class="sxs-lookup"><span data-stu-id="594ae-103">Connecting to a data source can be time consuming.</span></span> <span data-ttu-id="594ae-104">ADO.NET 接続を開くコストを最小限に抑えると呼ばれる最適化手法を使用して*接続プール*、繰り返しの接続の開閉のコストを最小限に抑えられます。</span><span class="sxs-lookup"><span data-stu-id="594ae-104">To minimize the cost of opening connections, ADO.NET uses an optimization technique called *connection pooling*, which minimizes the cost of repeatedly opening and closing connections.</span></span> <span data-ttu-id="594ae-105">接続プールは、.NET Framework データ プロバイダーに応じて異なる処理が行われます。</span><span class="sxs-lookup"><span data-stu-id="594ae-105">Connection pooling is handled differently for the .NET Framework data providers.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="594ae-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="594ae-106">In This Section</span></span>  
 [<span data-ttu-id="594ae-107">SQL Server の接続プール (ADO.NET)</span><span class="sxs-lookup"><span data-stu-id="594ae-107">SQL Server Connection Pooling (ADO.NET)</span></span>](../../../../docs/framework/data/adonet/sql-server-connection-pooling.md)  
 <span data-ttu-id="594ae-108">接続プールの概要し、SQL Server の接続プールのしくみについて説明します。</span><span class="sxs-lookup"><span data-stu-id="594ae-108">Provides an overview of connection pooling and describes how connection pooling works in SQL Server.</span></span>  
  
 [<span data-ttu-id="594ae-109">OLE DB、ODBC、および Oracle 接続プール</span><span class="sxs-lookup"><span data-stu-id="594ae-109">OLE DB, ODBC, and Oracle Connection Pooling</span></span>](../../../../docs/framework/data/adonet/ole-db-odbc-and-oracle-connection-pooling.md)  
 <span data-ttu-id="594ae-110">.NET Framework Data Provider for OLE DB、.NET Framework Data Provider for ODBC、および .NET Framework Data Provider for Oracle の接続プールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="594ae-110">Describes connection pooling for the .NET Framework Data Provider for OLE DB, the .NET Framework Data Provider for ODBC, and the .NET Framework Data Provider for Oracle.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="594ae-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="594ae-111">See Also</span></span>  
 [<span data-ttu-id="594ae-112">ADO.NET でのデータの取得および変更</span><span class="sxs-lookup"><span data-stu-id="594ae-112">Retrieving and Modifying Data in ADO.NET</span></span>](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)  
 [<span data-ttu-id="594ae-113">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="594ae-113">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
