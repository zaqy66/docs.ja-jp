---
title: カタログ操作の実行
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e60f542f-6271-495b-a9e4-48553481c2a3
ms.openlocfilehash: 7588b2b4592a5298a69eb4adfbc06edb6913ef76
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43519097"
---
# <a name="performing-catalog-operations"></a><span data-ttu-id="d2a24-102">カタログ操作の実行</span><span class="sxs-lookup"><span data-stu-id="d2a24-102">Performing Catalog Operations</span></span>
<span data-ttu-id="d2a24-103">データベースまたは CREATE TABLE または CREATE PROCEDURE ステートメントなどのカタログを変更するコマンドを実行するには、作成、**コマンド**オブジェクト、適切な SQL ステートメントを使用して、**接続**オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="d2a24-103">To execute a command to modify a database or catalog, such as the CREATE TABLE or CREATE PROCEDURE statement, create a **Command** object using the appropriate SQL statements and a **Connection** object.</span></span> <span data-ttu-id="d2a24-104">コマンドを実行、 **ExecuteNonQuery**のメソッド、**コマンド**オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="d2a24-104">Execute the command with the **ExecuteNonQuery** method of the **Command** object.</span></span>  
  
 <span data-ttu-id="d2a24-105">Microsoft SQL Server データベースにストアド プロシージャを作成するコード サンプルを次に示します。</span><span class="sxs-lookup"><span data-stu-id="d2a24-105">The following code example creates a stored procedure in a Microsoft SQL Server database.</span></span>  
  
```vb  
' Assumes connection is a valid SqlConnection.  
Dim queryString As String = "CREATE PROCEDURE InsertCategory " & _  
    "@CategoryName nchar(15), " & _  
    "@Identity int OUT " & _  
    "AS " & _  
    "INSERT INTO Categories (CategoryName) VALUES(@CategoryName) " & _  
    "SET @Identity = @@Identity " & _  
    "RETURN @@ROWCOUNT"  
  
Dim command As SqlCommand = New SqlCommand(queryString, connection)  
command.ExecuteNonQuery()  
```  
  
```csharp  
// Assumes connection is a valid SqlConnection.  
string queryString = "CREATE PROCEDURE InsertCategory  " +   
    "@CategoryName nchar(15), " +  
    "@Identity int OUT " +  
    "AS " +   
    "INSERT INTO Categories (CategoryName) VALUES(@CategoryName) " +   
    "SET @Identity = @@Identity " +  
    "RETURN @@ROWCOUNT";  
  
SqlCommand command = new SqlCommand(queryString, connection);  
command.ExecuteNonQuery();  
```  
  
## <a name="see-also"></a><span data-ttu-id="d2a24-106">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2a24-106">See Also</span></span>  
 [<span data-ttu-id="d2a24-107">コマンドを使用したデータ変更</span><span class="sxs-lookup"><span data-stu-id="d2a24-107">Using Commands to Modify Data</span></span>](../../../../docs/framework/data/adonet/using-commands-to-modify-data.md)  
 [<span data-ttu-id="d2a24-108">コマンドおよびパラメーター</span><span class="sxs-lookup"><span data-stu-id="d2a24-108">Commands and Parameters</span></span>](../../../../docs/framework/data/adonet/commands-and-parameters.md)  
 [<span data-ttu-id="d2a24-109">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="d2a24-109">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
