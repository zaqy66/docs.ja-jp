---
title: ADO.NET コード サンプルについては、サンプル データベースを取得します。
description: ADO.NET のドキュメントと SQL Server および管理ツールのコード サンプルで使用されるサンプル データベースをダウンロードします。
ms.date: 10/12/2018
ms.assetid: ef9d69a1-9461-43fe-94bb-7c836754bcb5
ms.openlocfilehash: 75ae1895d683b669f51b33130fc2f47010e39814
ms.sourcegitcommit: fd8d4587cc26e53f0e27e230d6e27d828ef4306b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2018
ms.locfileid: "49347517"
---
# <a name="get-the-sample-databases-for-adonet-code-samples"></a><span data-ttu-id="a60dd-103">ADO.NET コード サンプルについては、サンプル データベースを取得します。</span><span class="sxs-lookup"><span data-stu-id="a60dd-103">Get the sample databases for ADO.NET code samples</span></span>

<span data-ttu-id="a60dd-104">さまざまなサンプルおよびチュートリアルで、[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]ドキュメントは、サンプル データベースと SQL Server Express を使用します。</span><span class="sxs-lookup"><span data-stu-id="a60dd-104">A number of samples and walkthroughs in the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] documentation use sample databases and SQL Server Express.</span></span> <span data-ttu-id="a60dd-105">これらの製品を無料では、Microsoft からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="a60dd-105">You can download these products free of charge from Microsoft.</span></span>

## <a name="get-the-adventureworks-sample-database"></a><span data-ttu-id="a60dd-106">AdventureWorks サンプル データベースします。</span><span class="sxs-lookup"><span data-stu-id="a60dd-106">Get the AdventureWorks sample database</span></span>

<span data-ttu-id="a60dd-107">次の GitHub リポジトリから AdventureWorks サンプル データベースをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a60dd-107">Download the AdventureWorks sample database from the following GitHub repository:</span></span>

[<span data-ttu-id="a60dd-108">AdventureWorks サンプル データベース</span><span class="sxs-lookup"><span data-stu-id="a60dd-108">AdventureWorks sample databases</span></span>](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks)

<span data-ttu-id="a60dd-109">データベースのバックアップのいずれかをダウンロードした後 (\*.bak) ファイル、SQL Server のインスタンスに SQL Server Management Studio (SSMS) を使用して、バックアップを復元します。</span><span class="sxs-lookup"><span data-stu-id="a60dd-109">After you download one of the database backup (\*.bak) files, restore the backup to an instance of SQL Server by using SQL Server Management Studio (SSMS).</span></span> <span data-ttu-id="a60dd-110">参照してください[SQL Server Management Studio を入手する](#get_ssms)します。</span><span class="sxs-lookup"><span data-stu-id="a60dd-110">See [Get SQL Server Management Studio](#get_ssms).</span></span>

## <a name="get-the-northwind-sample-database"></a><span data-ttu-id="a60dd-111">Northwind サンプル データベースします。</span><span class="sxs-lookup"><span data-stu-id="a60dd-111">Get the Northwind sample database</span></span>

<span data-ttu-id="a60dd-112">Microsoft ダウンロード センターの次のページからは、Northwind サンプル データベースをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a60dd-112">Download the Northwind sample database from the following page in the Microsoft Download Center:</span></span>

[<span data-ttu-id="a60dd-113">Northwind および Pubs サンプル データベース</span><span class="sxs-lookup"><span data-stu-id="a60dd-113">Northwind and Pubs Sample Databases</span></span>](https://go.microsoft.com/fwlink?linkid=64296)

<span data-ttu-id="a60dd-114">ファイルがダウンロードされた後は、データベースとスクリプトを抽出するファイルをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="a60dd-114">After the file has downloaded, double-click the file to extract the databases and scripts.</span></span> <span data-ttu-id="a60dd-115">フォルダーに既定では、ファイルがインストールされている`<drive>:\SQL Server 2000 Sample Databases`します。</span><span class="sxs-lookup"><span data-stu-id="a60dd-115">By default, the files are installed in the folder `<drive>:\SQL Server 2000 Sample Databases`.</span></span>

<span data-ttu-id="a60dd-116">Northwind データベースを使用するには、次のいずれかを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a60dd-116">Before you can use the Northwind database, you have to do one of the following things:</span></span>

- <span data-ttu-id="a60dd-117">SQL Server のインスタンス上のデータベースを再作成を実行して、`instnwnd.sql`インストール フォルダーにスクリプト ファイル。</span><span class="sxs-lookup"><span data-stu-id="a60dd-117">Recreate the database on an instance of SQL Server by running the `instnwnd.sql` script file in the installation folder.</span></span>

- <span data-ttu-id="a60dd-118">アタッチ、 `northwnd.mdf` 、対応するファイル`*.ldf`SQL Server のインスタンスにログ ファイル。</span><span class="sxs-lookup"><span data-stu-id="a60dd-118">Attach the `northwnd.mdf` file with its corresponding `*.ldf` log file to an instance of SQL Server.</span></span>

## <a name="get_sql"></a> <span data-ttu-id="a60dd-119">SQL Server Express の入手します。</span><span class="sxs-lookup"><span data-stu-id="a60dd-119">Get SQL Server Express</span></span>

<span data-ttu-id="a60dd-120">SQL Server Express は、アプリケーションで再配布する SQL Server の無料のエントリー エディションです。</span><span class="sxs-lookup"><span data-stu-id="a60dd-120">SQL Server Express is a free, entry-level edition of SQL Server that you can redistribute with applications.</span></span> <span data-ttu-id="a60dd-121">次のページから SQL Server Express をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a60dd-121">Download SQL Server Express from the following page:</span></span>
  
[<span data-ttu-id="a60dd-122">SQL Server Express Edition</span><span class="sxs-lookup"><span data-stu-id="a60dd-122">SQL Server Express Editions</span></span>](https://www.microsoft.com/sql-server/sql-server-editions-express)

<span data-ttu-id="a60dd-123">使用している場合[Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)、Community edition と Professional 以上のエディションに SQL Server Express LocalDB が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a60dd-123">If you're using [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), SQL Server Express LocalDB is included in the Community edition as well as the Professional and higher editions.</span></span>  

## <a name="get_ssms"></a> <span data-ttu-id="a60dd-124">SQL Server Management Studio を入手します。</span><span class="sxs-lookup"><span data-stu-id="a60dd-124">Get SQL Server Management Studio</span></span>
<span data-ttu-id="a60dd-125">表示またはダウンロードしたデータベースを変更する場合は、SQL Server Management Studio (SSMS) を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="a60dd-125">If you want to view or modify a database that you've downloaded, you can use SQL Server Management Studio (SSMS).</span></span> <span data-ttu-id="a60dd-126">次のページから SSMS をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a60dd-126">Download SSMS from the following page:</span></span>

[<span data-ttu-id="a60dd-127">SQL Server Management Studio (SSMS) のダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a60dd-127">Download SQL Server Management Studio (SSMS)</span></span>](/sql/ssms/download-sql-server-management-studio-ssms) 

<span data-ttu-id="a60dd-128">また、表示、Visual Studio 統合開発環境 (IDE) でデータベースを管理およびできます。</span><span class="sxs-lookup"><span data-stu-id="a60dd-128">You can also view and manage databases in the Visual Studio integrated development environment (IDE).</span></span> <span data-ttu-id="a60dd-129">[Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)からデータベースに接続する**SQL Server オブジェクト エクスプ ローラー**、データベースにデータ接続を作成または**サーバー エクスプ ローラー**します。</span><span class="sxs-lookup"><span data-stu-id="a60dd-129">In [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), connect to the database from **SQL Server Object Explorer**, or create a Data Connection to the database in **Server Explorer**.</span></span> <span data-ttu-id="a60dd-130">これらのエクスプ ローラー ウィンドウを開き、**ビュー**メニュー。</span><span class="sxs-lookup"><span data-stu-id="a60dd-130">Open these explorer panes from the **View** menu.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a60dd-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="a60dd-131">See also</span></span>

- [<span data-ttu-id="a60dd-132">はじめに</span><span class="sxs-lookup"><span data-stu-id="a60dd-132">Getting Started</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/getting-started.md)
