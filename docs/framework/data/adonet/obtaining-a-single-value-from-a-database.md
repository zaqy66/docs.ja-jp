---
title: データベースからの単一の値の取得
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: b38526cd-a62a-48cb-822a-e91dfa68e02d
ms.openlocfilehash: 1a0d92c7acad58d3618c3f50b7463022352cf542
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43560858"
---
# <a name="obtaining-a-single-value-from-a-database"></a><span data-ttu-id="e8280-102">データベースからの単一の値の取得</span><span class="sxs-lookup"><span data-stu-id="e8280-102">Obtaining a Single Value from a Database</span></span>
<span data-ttu-id="e8280-103">テーブルやデータ ストリームの形式ではなく、単に 1 つの値をデータベース情報として返すことが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="e8280-103">You may need to return database information that is simply a single value rather than in the form of a table or data stream.</span></span> <span data-ttu-id="e8280-104">たとえば、数などの集約関数の結果を返すようにする可能性があります (\*)、SUM(Price)、または AVG(Quantity) します。</span><span class="sxs-lookup"><span data-stu-id="e8280-104">For example, you may want to return the result of an aggregate function such as COUNT(\*), SUM(Price), or AVG(Quantity).</span></span> <span data-ttu-id="e8280-105">**コマンド**オブジェクトを使用して 1 つの値を返す機能を提供する、 **ExecuteScalar**メソッド。</span><span class="sxs-lookup"><span data-stu-id="e8280-105">The **Command** object provides the capability to return single values using the **ExecuteScalar** method.</span></span> <span data-ttu-id="e8280-106">**ExecuteScalar**メソッドはスカラー値、結果セットの最初の行の最初の列の値として返します。</span><span class="sxs-lookup"><span data-stu-id="e8280-106">The **ExecuteScalar** method returns, as a scalar value, the value of the first column of the first row of the result set.</span></span>  
  
 <span data-ttu-id="e8280-107"><xref:System.Data.SqlClient.SqlCommand> を使用して新しい値をデータベースに挿入するコード サンプルを次に示します。</span><span class="sxs-lookup"><span data-stu-id="e8280-107">The following code example inserts a new value in the database using a <xref:System.Data.SqlClient.SqlCommand>.</span></span> <span data-ttu-id="e8280-108">挿入したレコードの ID 列の値を取得するために、<xref:System.Data.SqlClient.SqlCommand.ExecuteScalar%2A> メソッドが使用されています。</span><span class="sxs-lookup"><span data-stu-id="e8280-108">The <xref:System.Data.SqlClient.SqlCommand.ExecuteScalar%2A> method is used to return the identity column value for the inserted record.</span></span>  
  
 [!code-csharp[DataWorks SqlCommand.ExecuteScalar#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlCommand.ExecuteScalar/CS/source.cs#1)]
 [!code-vb[DataWorks SqlCommand.ExecuteScalar#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlCommand.ExecuteScalar/VB/source.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="e8280-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="e8280-109">See Also</span></span>  
 [<span data-ttu-id="e8280-110">コマンドおよびパラメーター</span><span class="sxs-lookup"><span data-stu-id="e8280-110">Commands and Parameters</span></span>](../../../../docs/framework/data/adonet/commands-and-parameters.md)  
 [<span data-ttu-id="e8280-111">コマンドの実行</span><span class="sxs-lookup"><span data-stu-id="e8280-111">Executing a Command</span></span>](../../../../docs/framework/data/adonet/executing-a-command.md)  
 [<span data-ttu-id="e8280-112">DbConnection、DbCommand、および DbException</span><span class="sxs-lookup"><span data-stu-id="e8280-112">DbConnection, DbCommand and DbException</span></span>](../../../../docs/framework/data/adonet/dbconnection-dbcommand-and-dbexception.md)  
 [<span data-ttu-id="e8280-113">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="e8280-113">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
