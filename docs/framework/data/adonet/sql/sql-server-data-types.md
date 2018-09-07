---
title: SQL Server データ型と ADO.NET
ms.date: 03/30/2017
ms.assetid: 81b43550-23e8-43bb-b460-7eb8ac825c33
ms.openlocfilehash: 878bbe41f259f1e50cd0a41669c7a352e78bc0f1
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44097036"
---
# <a name="sql-server-data-types-and-adonet"></a><span data-ttu-id="f42e5-102">SQL Server データ型と ADO.NET</span><span class="sxs-lookup"><span data-stu-id="f42e5-102">SQL Server Data Types and ADO.NET</span></span>
<span data-ttu-id="f42e5-103">SQL Server と .NET Framework は異なる型システムに基づいているので、両者間でデータ損失が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f42e5-103">SQL Server and the .NET Framework are based on different type systems, which can result in potential data loss.</span></span> <span data-ttu-id="f42e5-104">データの整合性を維持するために、.NET Framework Data Provider for SQL Server (<xref:System.Data.SqlClient>) では、SQL Server データを処理するための型指定されたアクセサー メソッドが提供されています。</span><span class="sxs-lookup"><span data-stu-id="f42e5-104">To preserve data integrity, the .NET Framework Data Provider for SQL Server (<xref:System.Data.SqlClient>) provides typed accessor methods for working with SQL Server data.</span></span> <span data-ttu-id="f42e5-105"><xref:System.Data.SqlDbType> クラスの列挙値を使用して、<xref:System.Data.SqlClient.SqlParameter> データ型を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f42e5-105">You can use the enumerations in the <xref:System.Data.SqlDbType> classes to specify <xref:System.Data.SqlClient.SqlParameter> data types.</span></span>  
  
 <span data-ttu-id="f42e5-106">テーブル データを記述する型の SQL Server と .NET Framework データ型間のマッピングと詳細については、次を参照してください。 [SQL Server データ型のマッピング](../../../../../docs/framework/data/adonet/sql-server-data-type-mappings.md)します。</span><span class="sxs-lookup"><span data-stu-id="f42e5-106">For more information and a table that that describes the data type mappings between SQL Server and .NET Framework data types, see [SQL Server Data Type Mappings](../../../../../docs/framework/data/adonet/sql-server-data-type-mappings.md).</span></span>  
  
 <span data-ttu-id="f42e5-107">SQL Server 2008 では、業務上のニーズに対応して、日時データ、構造化データ、半構造化データ、および非構造化データを扱うための新しいデータ型が導入されました。</span><span class="sxs-lookup"><span data-stu-id="f42e5-107">SQL Server 2008 introduces new data types that are designed to meet business needs to work with date and time, structured, semi-structured, and unstructured data.</span></span> <span data-ttu-id="f42e5-108">新しいデータ型は、SQL Server 2008 オンライン ブックで説明されています。</span><span class="sxs-lookup"><span data-stu-id="f42e5-108">These are documented in SQL Server 2008 Books Online.</span></span>  
  
 <span data-ttu-id="f42e5-109">アプリケーションで使用可能な SQL Server のデータ型は、使用する SQL Server のバージョンによって異なります。</span><span class="sxs-lookup"><span data-stu-id="f42e5-109">The SQL Server data types that are available for use in your application depends on the version of SQL Server that you are using.</span></span> <span data-ttu-id="f42e5-110">詳細については、次の表にある各バージョンの SQL Server オンライン ブックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f42e5-110">For more information, see the relevant version of SQL Server Books Online in the following table.</span></span>  
  
 <span data-ttu-id="f42e5-111">**SQL Server オンライン ブック**</span><span class="sxs-lookup"><span data-stu-id="f42e5-111">**SQL Server Books Online**</span></span>  
  
1.  [<span data-ttu-id="f42e5-112">データ型 (データベース エンジン)</span><span class="sxs-lookup"><span data-stu-id="f42e5-112">Data Types (Database Engine)</span></span>](https://go.microsoft.com/fwlink/?LinkID=107468)  
  
## <a name="in-this-section"></a><span data-ttu-id="f42e5-113">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="f42e5-113">In This Section</span></span>  
 [<span data-ttu-id="f42e5-114">SqlTypes と DataSet</span><span class="sxs-lookup"><span data-stu-id="f42e5-114">SqlTypes and the DataSet</span></span>](../../../../../docs/framework/data/adonet/sql/sqltypes-and-the-dataset.md)  
 <span data-ttu-id="f42e5-115">`SqlTypes` 内の `DataSet` に対する型のサポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f42e5-115">Describes type support for `SqlTypes` in the `DataSet`.</span></span>  
  
 [<span data-ttu-id="f42e5-116">null 値の処理</span><span class="sxs-lookup"><span data-stu-id="f42e5-116">Handling Null Values</span></span>](../../../../../docs/framework/data/adonet/sql/handling-null-values.md)  
 <span data-ttu-id="f42e5-117">null 値と 3 値ロジックの使用例を示します。</span><span class="sxs-lookup"><span data-stu-id="f42e5-117">Demonstrates how to work with null values and three-valued logic.</span></span>  
  
 [<span data-ttu-id="f42e5-118">GUID と uniqueidentifier 値の比較</span><span class="sxs-lookup"><span data-stu-id="f42e5-118">Comparing GUID and uniqueidentifier Values</span></span>](../../../../../docs/framework/data/adonet/sql/comparing-guid-and-uniqueidentifier-values.md)  
 <span data-ttu-id="f42e5-119">SQL Server と .NET Framework での GUID および uniqueidentifier 値の使用例を示します。</span><span class="sxs-lookup"><span data-stu-id="f42e5-119">Demonstrates how to work with GUID and uniqueidentifier values in SQL Server and the .NET Framework.</span></span>  
  
 [<span data-ttu-id="f42e5-120">日付と時刻のデータ</span><span class="sxs-lookup"><span data-stu-id="f42e5-120">Date and Time Data</span></span>](../../../../../docs/framework/data/adonet/sql/date-and-time-data.md)  
 <span data-ttu-id="f42e5-121">SQL Server 2008 で導入された新しい日付と時刻のデータ型の使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f42e5-121">Describes how to use the new date and time data types introduced in SQL Server 2008.</span></span>  
  
 [<span data-ttu-id="f42e5-122">大きな UDT</span><span class="sxs-lookup"><span data-stu-id="f42e5-122">Large UDTs</span></span>](../../../../../docs/framework/data/adonet/sql/large-udts.md)  
 <span data-ttu-id="f42e5-123">SQL Server 2008 で導入された大きな値の UDT からデータを取り出す方法の例を示します。</span><span class="sxs-lookup"><span data-stu-id="f42e5-123">Demonstrates how to retrieve data from large value UDTs introduced in SQL Server 2008.</span></span>  
  
 [<span data-ttu-id="f42e5-124">SQL Server における XML データ</span><span class="sxs-lookup"><span data-stu-id="f42e5-124">XML Data in SQL Server</span></span>](../../../../../docs/framework/data/adonet/sql/xml-data-in-sql-server.md)  
 <span data-ttu-id="f42e5-125">SQL Server から取得した XML データを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f42e5-125">Describes how to work with XML data retrieved from SQL Server.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="f42e5-126">参照</span><span class="sxs-lookup"><span data-stu-id="f42e5-126">Reference</span></span>  
 <xref:System.Data.DataSet>  
 <span data-ttu-id="f42e5-127">`DataSet` クラスおよびそのすべてのメンバーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f42e5-127">Describes the `DataSet` class and all of its members.</span></span>  
  
 <xref:System.Data.SqlTypes>  
 <span data-ttu-id="f42e5-128">`SqlTypes` 名前空間およびそのすべてのメンバーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f42e5-128">Describes the `SqlTypes` namespace and all of its members.</span></span>  
  
 <xref:System.Data.SqlDbType>  
 <span data-ttu-id="f42e5-129">`SqlDbType` 列挙型およびそのすべてのメンバーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f42e5-129">Describes the `SqlDbType` enumeration and all of its members.</span></span>  
  
 <xref:System.Data.DbType>  
 <span data-ttu-id="f42e5-130">`DbType` 列挙型およびそのすべてのメンバーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f42e5-130">Describes the `DbType` enumeration and all of its members.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f42e5-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="f42e5-131">See Also</span></span>  
 [<span data-ttu-id="f42e5-132">SQL Server データ型のマッピング</span><span class="sxs-lookup"><span data-stu-id="f42e5-132">SQL Server Data Type Mappings</span></span>](../../../../../docs/framework/data/adonet/sql-server-data-type-mappings.md)  
 [<span data-ttu-id="f42e5-133">パラメーターおよびパラメーター データ型の構成</span><span class="sxs-lookup"><span data-stu-id="f42e5-133">Configuring Parameters and Parameter Data Types</span></span>](../../../../../docs/framework/data/adonet/configuring-parameters-and-parameter-data-types.md)  
 [<span data-ttu-id="f42e5-134">テーブル値パラメーター</span><span class="sxs-lookup"><span data-stu-id="f42e5-134">Table-Valued Parameters</span></span>](../../../../../docs/framework/data/adonet/sql/table-valued-parameters.md)  
 [<span data-ttu-id="f42e5-135">SQL Server のバイナリ データと大きな値のデータ</span><span class="sxs-lookup"><span data-stu-id="f42e5-135">SQL Server Binary and Large-Value Data</span></span>](../../../../../docs/framework/data/adonet/sql/sql-server-binary-and-large-value-data.md)  
 [<span data-ttu-id="f42e5-136">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="f42e5-136">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
