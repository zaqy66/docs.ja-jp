---
title: SQL Server における XML データ
ms.date: 03/30/2017
ms.assetid: 9849d319-f518-4e3d-a7cd-f8fdcaaa1d4d
ms.openlocfilehash: 71933640f2b333aa4be40416db346b5accf2ae73
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54725624"
---
# <a name="xml-data-in-sql-server"></a><span data-ttu-id="6a5b3-102">SQL Server における XML データ</span><span class="sxs-lookup"><span data-stu-id="6a5b3-102">XML Data in SQL Server</span></span>
<span data-ttu-id="6a5b3-103">SQL Server は、.NET Framework 内部の SQLXML の機能を公開します。</span><span class="sxs-lookup"><span data-stu-id="6a5b3-103">SQL Server exposes the functionality of SQLXML inside the .NET Framework.</span></span> <span data-ttu-id="6a5b3-104">開発者は、SQL Server のインスタンスから XML データにアクセスし、データを .NET Framework 環境に持ち込んで処理し、更新を SQL Server に送り返すアプリケーションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6a5b3-104">Developers can write applications that access XML data from an instance of SQL Server, bring the data into the .NET Framework environment, process the data, and send the updates back to SQL Server.</span></span> <span data-ttu-id="6a5b3-105">SQL Server では、XML データをデータ ストレージなどの目的に、あるいはデータを取得するときのパラメーター値として使用できます。</span><span class="sxs-lookup"><span data-stu-id="6a5b3-105">XML data can be used in several ways in SQL Server, including data storage, and as parameter values for retrieving data.</span></span> <span data-ttu-id="6a5b3-106">**SqlXml** .NET Framework クラスは、SQL Server 内の XML 列に格納されたデータを操作するため、クライアント側のサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="6a5b3-106">The **SqlXml** class in the .NET Framework provides the client-side support for working with data stored in an XML column within SQL Server.</span></span> <span data-ttu-id="6a5b3-107">詳細については、SQL Server オンライン ブックの「SQLXML マネージド クラス」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a5b3-107">For more information, see "SQLXML Managed Classes" in SQL Server Books Online.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="6a5b3-108">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="6a5b3-108">In This Section</span></span>  
 [<span data-ttu-id="6a5b3-109">SQL XML 列値</span><span class="sxs-lookup"><span data-stu-id="6a5b3-109">SQL XML Column Values</span></span>](../../../../../docs/framework/data/adonet/sql/sql-xml-column-values.md)  
 <span data-ttu-id="6a5b3-110">SQL Server から XML データを取得し、使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6a5b3-110">Demonstrates how to retrieve and work with XML data retrieved from SQL Server.</span></span>  
  
 [<span data-ttu-id="6a5b3-111">パラメーターとしての XML 値の指定</span><span class="sxs-lookup"><span data-stu-id="6a5b3-111">Specifying XML Values as Parameters</span></span>](../../../../../docs/framework/data/adonet/sql/specifying-xml-values-as-parameters.md)  
 <span data-ttu-id="6a5b3-112">コマンドに XML データをパラメーターとして渡す方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6a5b3-112">Demonstrates how to pass XML data as a parameter to a command.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6a5b3-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="6a5b3-113">See also</span></span>
- [<span data-ttu-id="6a5b3-114">SQL Server と ADO.NET</span><span class="sxs-lookup"><span data-stu-id="6a5b3-114">SQL Server and ADO.NET</span></span>](../../../../../docs/framework/data/adonet/sql/index.md)
- [<span data-ttu-id="6a5b3-115">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="6a5b3-115">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
