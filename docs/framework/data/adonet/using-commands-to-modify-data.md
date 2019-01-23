---
title: コマンドを使用したデータ変更
ms.date: 03/30/2017
ms.assetid: f4160389-b9ff-4b74-b655-437c76dcd586
ms.openlocfilehash: cec079d16c6dc3d98cee9bf17b4201654e9ba10a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54509268"
---
# <a name="using-commands-to-modify-data"></a><span data-ttu-id="4df57-102">コマンドを使用したデータ変更</span><span class="sxs-lookup"><span data-stu-id="4df57-102">Using Commands to Modify Data</span></span>
<span data-ttu-id="4df57-103">.NET Framework データ プロバイダーを使用すると、ストアド プロシージャまたはデータ定義言語のステートメント (たとえば、CREATE TABLE、ALTER COLUMN など) を実行して、データベースやカタログに対するスキーマ操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="4df57-103">Using a .NET Framework data provider, you can execute stored procedures or data definition language statements (for example, CREATE TABLE and ALTER COLUMN) to perform schema manipulation on a database or catalog.</span></span> <span data-ttu-id="4df57-104">クエリとは、これらのコマンドは行を返しませんため、**コマンド**オブジェクトは、提供、 **ExecuteNonQuery**それらを処理します。</span><span class="sxs-lookup"><span data-stu-id="4df57-104">These commands do not return rows as a query would, so the **Command** object provides an **ExecuteNonQuery** to process them.</span></span>  
  
 <span data-ttu-id="4df57-105">使用するだけでなく**ExecuteNonQuery**スキーマを変更するには、データを変更するが、INSERT、UPDATE などの行を返すなく、削除のプロセスの SQL ステートメントには、このメソッドも使用できます。</span><span class="sxs-lookup"><span data-stu-id="4df57-105">In addition to using **ExecuteNonQuery** to modify schema, you can also use this method to process SQL statements that modify data but that do not return rows, such as INSERT, UPDATE, and DELETE.</span></span>  
  
 <span data-ttu-id="4df57-106">行は返されませんが、 **ExecuteNonQuery**メソッド、入力と出力パラメーターと戻り値を渡すし、を介して返されます、**パラメーター**のコレクション、**コマンド**オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="4df57-106">Although rows are not returned by the **ExecuteNonQuery** method, input and output parameters and return values can be passed and returned via the **Parameters** collection of the **Command** object.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="4df57-107">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="4df57-107">In This Section</span></span>  
 [<span data-ttu-id="4df57-108">データ ソースのデータの更新</span><span class="sxs-lookup"><span data-stu-id="4df57-108">Updating Data in a Data Source</span></span>](../../../../docs/framework/data/adonet/updating-data-in-a-data-source.md)  
 <span data-ttu-id="4df57-109">データベース内のデータを変更するコマンドまたはストアド プロシージャを実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4df57-109">Describes how to execute commands or stored procedures that modify data in a database.</span></span>  
  
 [<span data-ttu-id="4df57-110">カタログ操作の実行</span><span class="sxs-lookup"><span data-stu-id="4df57-110">Performing Catalog Operations</span></span>](../../../../docs/framework/data/adonet/performing-catalog-operations.md)  
 <span data-ttu-id="4df57-111">データベース スキーマを変更するコマンドを実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4df57-111">Describes how to execute commands that modify database schema.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4df57-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="4df57-112">See also</span></span>
- [<span data-ttu-id="4df57-113">ADO.NET でのデータの取得および変更</span><span class="sxs-lookup"><span data-stu-id="4df57-113">Retrieving and Modifying Data in ADO.NET</span></span>](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)
- [<span data-ttu-id="4df57-114">コマンドおよびパラメーター</span><span class="sxs-lookup"><span data-stu-id="4df57-114">Commands and Parameters</span></span>](../../../../docs/framework/data/adonet/commands-and-parameters.md)
- [<span data-ttu-id="4df57-115">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="4df57-115">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
