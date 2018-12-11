---
title: ADO.NET コード サンプルについては、サンプルの SQL Server データベースを取得します。
description: ADO.NET のドキュメントと SQL Server および管理ツールのコード サンプルで使用されるサンプルの SQL Server データベースをダウンロードします。
ms.date: 10/18/2018
ms.assetid: ef9d69a1-9461-43fe-94bb-7c836754bcb5
ms.openlocfilehash: 8ab65f992c9cf2b65271a237fa06eb96e358ae6a
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53153489"
---
# <a name="get-the-sample-databases-for-adonet-code-samples"></a><span data-ttu-id="567b0-103">ADO.NET コード サンプルについては、サンプル データベースを取得します。</span><span class="sxs-lookup"><span data-stu-id="567b0-103">Get the sample databases for ADO.NET code samples</span></span>

<span data-ttu-id="567b0-104">さまざまな例とチュートリアルで、[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]ドキュメントは、SQL Server のサンプル データベースおよび SQL Server Express を使用します。</span><span class="sxs-lookup"><span data-stu-id="567b0-104">A number of examples and walkthroughs in the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] documentation use sample SQL Server databases and SQL Server Express.</span></span> <span data-ttu-id="567b0-105">これらの製品を無料では、Microsoft からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="567b0-105">You can download these products free of charge from Microsoft.</span></span>

## <a name="get-the-northwind-sample-database-for-sql-server"></a><span data-ttu-id="567b0-106">SQL Server の Northwind サンプル データベースを取得します。</span><span class="sxs-lookup"><span data-stu-id="567b0-106">Get the Northwind sample database for SQL Server</span></span>

<span data-ttu-id="567b0-107">スクリプトをダウンロードする`instnwnd.sql`作成し、SQL Server の Northwind サンプル データベースを読み込むには、次の GitHub リポジトリから。</span><span class="sxs-lookup"><span data-stu-id="567b0-107">Download the script `instnwnd.sql` from the following GitHub repository to create and load the Northwind sample database for SQL Server:</span></span>

[<span data-ttu-id="567b0-108">Microsoft SQL Server 用の Northwind および pubs サンプル データベース</span><span class="sxs-lookup"><span data-stu-id="567b0-108">Northwind and pubs sample databases for Microsoft SQL Server</span></span>](https://github.com/Microsoft/sql-server-samples/tree/master/samples/databases/northwind-pubs)

<span data-ttu-id="567b0-109">Northwind データベースを使用する前に、ダウンロードした実行がある`instnwnd.sql`を使用して SQL Server のインスタンス上のデータベースを再作成するスクリプト ファイル[SQL Server Management Studio](#get_ssms)または同様のツール。</span><span class="sxs-lookup"><span data-stu-id="567b0-109">Before you can use the Northwind database, you have to run the downloaded `instnwnd.sql` script file to recreate the database on an instance of SQL Server by using [SQL Server Management Studio](#get_ssms) or a similar tool.</span></span> <span data-ttu-id="567b0-110">リポジトリに Readme ファイルの指示に従います。</span><span class="sxs-lookup"><span data-stu-id="567b0-110">Follow the instructions in the Readme file in the repository.</span></span>

> [!TIP]
> <span data-ttu-id="567b0-111">Microsoft Access の Northwind データベースで必要な場合を参照してください。 [Microsoft Access の Northwind サンプル データベースをインストール](#northwind_access)します。</span><span class="sxs-lookup"><span data-stu-id="567b0-111">If you're looking for the Northwind database for Microsoft Access, see [Install the Northwind sample database for Microsoft Access](#northwind_access).</span></span>

## <a name="get-the-adventureworks-sample-database-for-sql-server"></a><span data-ttu-id="567b0-112">SQL Server の AdventureWorks サンプル データベースを取得します。</span><span class="sxs-lookup"><span data-stu-id="567b0-112">Get the AdventureWorks sample database for SQL Server</span></span>

<span data-ttu-id="567b0-113">次の GitHub リポジトリからの SQL Server の AdventureWorks サンプル データベースをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="567b0-113">Download the AdventureWorks sample database for SQL Server from the following GitHub repository:</span></span>

[<span data-ttu-id="567b0-114">AdventureWorks サンプル データベース</span><span class="sxs-lookup"><span data-stu-id="567b0-114">AdventureWorks sample databases</span></span>](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks)

<span data-ttu-id="567b0-115">データベースのバックアップのいずれかをダウンロードした後 (\*.bak) ファイル、SQL Server のインスタンスに SQL Server Management Studio (SSMS) を使用して、バックアップを復元します。</span><span class="sxs-lookup"><span data-stu-id="567b0-115">After you download one of the database backup (\*.bak) files, restore the backup to an instance of SQL Server by using SQL Server Management Studio (SSMS).</span></span> <span data-ttu-id="567b0-116">参照してください[SQL Server Management Studio を入手する](#get_ssms)します。</span><span class="sxs-lookup"><span data-stu-id="567b0-116">See [Get SQL Server Management Studio](#get_ssms).</span></span>

## <a name="get_sql"></a> <span data-ttu-id="567b0-117">SQL Server Express の入手します。</span><span class="sxs-lookup"><span data-stu-id="567b0-117">Get SQL Server Express</span></span>

<span data-ttu-id="567b0-118">SQL Server Express は、アプリケーションで再配布する SQL Server の無料のエントリー エディションです。</span><span class="sxs-lookup"><span data-stu-id="567b0-118">SQL Server Express is a free, entry-level edition of SQL Server that you can redistribute with applications.</span></span> <span data-ttu-id="567b0-119">次のページから SQL Server Express をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="567b0-119">Download SQL Server Express from the following page:</span></span>
  
[<span data-ttu-id="567b0-120">SQL Server Express Edition</span><span class="sxs-lookup"><span data-stu-id="567b0-120">SQL Server Express Edition</span></span>](https://www.microsoft.com/sql-server/sql-server-editions-express)

<span data-ttu-id="567b0-121">使用している場合[Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)、SQL Server Express LocalDB は、Visual Studio の無料の Community edition と Professional 以上のエディションに含まれます。</span><span class="sxs-lookup"><span data-stu-id="567b0-121">If you're using [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), SQL Server Express LocalDB is included in the free Community edition of Visual Studio, as well as the Professional and higher editions.</span></span>  

## <a name="get_ssms"></a> <span data-ttu-id="567b0-122">SQL Server Management Studio を入手します。</span><span class="sxs-lookup"><span data-stu-id="567b0-122">Get SQL Server Management Studio</span></span>
<span data-ttu-id="567b0-123">表示またはダウンロードしたデータベースを変更する場合は、SQL Server Management Studio (SSMS) を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="567b0-123">If you want to view or modify a database that you've downloaded, you can use SQL Server Management Studio (SSMS).</span></span> <span data-ttu-id="567b0-124">次のページから SSMS をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="567b0-124">Download SSMS from the following page:</span></span>

[<span data-ttu-id="567b0-125">SQL Server Management Studio (SSMS) のダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="567b0-125">Download SQL Server Management Studio (SSMS)</span></span>](/sql/ssms/download-sql-server-management-studio-ssms) 

<span data-ttu-id="567b0-126">また、表示、Visual Studio 統合開発環境 (IDE) でデータベースを管理およびできます。</span><span class="sxs-lookup"><span data-stu-id="567b0-126">You can also view and manage databases in the Visual Studio integrated development environment (IDE).</span></span> <span data-ttu-id="567b0-127">[Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)からデータベースに接続する**SQL Server オブジェクト エクスプ ローラー**、データベースにデータ接続を作成または**サーバー エクスプ ローラー**します。</span><span class="sxs-lookup"><span data-stu-id="567b0-127">In [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), connect to the database from **SQL Server Object Explorer**, or create a Data Connection to the database in **Server Explorer**.</span></span> <span data-ttu-id="567b0-128">これらのエクスプ ローラー ウィンドウを開き、**ビュー**メニュー。</span><span class="sxs-lookup"><span data-stu-id="567b0-128">Open these explorer panes from the **View** menu.</span></span>

## <a name="northwind_access"></a> <span data-ttu-id="567b0-129">Microsoft Access の Northwind サンプル データベースをインストールします。</span><span class="sxs-lookup"><span data-stu-id="567b0-129">Install the Northwind sample database for Microsoft Access</span></span>

<span data-ttu-id="567b0-130">Microsoft ダウンロード センターでは、Microsoft Access の Northwind サンプル データベースを使用できません。</span><span class="sxs-lookup"><span data-stu-id="567b0-130">The Northwind sample database for Microsoft Access is not available on the Microsoft Download Center.</span></span> <span data-ttu-id="567b0-131">Access から直接 Northwind をインストールするには、次のことを行います。</span><span class="sxs-lookup"><span data-stu-id="567b0-131">To install Northwind directly from within Access, do the following things:</span></span>

1. <span data-ttu-id="567b0-132">アクセスを開きます。</span><span class="sxs-lookup"><span data-stu-id="567b0-132">Open Access.</span></span>

1. <span data-ttu-id="567b0-133">Enter **Northwind**で、**オンライン テンプレートの検索**ボックスを選び **」と入力**します。</span><span class="sxs-lookup"><span data-stu-id="567b0-133">Enter **Northwind** in the **Search for Online Templates** box, and then select **Enter**.</span></span>

1. <span data-ttu-id="567b0-134">[結果] 画面で選択**Northwind**します。</span><span class="sxs-lookup"><span data-stu-id="567b0-134">On the results screen, select **Northwind**.</span></span> <span data-ttu-id="567b0-135">Northwind データベースの説明では、新しいウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="567b0-135">A new window opens with a description of the Northwind database.</span></span>

1. <span data-ttu-id="567b0-136">新しいウィンドウで、**ファイル名**テキスト ボックスに、Northwind データベースのコピーのファイル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="567b0-136">In the new window, in the **File Name** text box, provide a filename for your copy of the Northwind database.</span></span>

1. <span data-ttu-id="567b0-137">**[作成]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="567b0-137">Select **Create**.</span></span> <span data-ttu-id="567b0-138">アクセスは、Northwind データベースをダウンロードし、ファイルを準備します。</span><span class="sxs-lookup"><span data-stu-id="567b0-138">Access downloads the Northwind database and prepares the file.</span></span>

1. <span data-ttu-id="567b0-139">このプロセスが完了したら、[ようこそ] 画面で、データベースを開きます。</span><span class="sxs-lookup"><span data-stu-id="567b0-139">When this process is complete, the database opens with a Welcome screen.</span></span>

## <a name="see-also"></a><span data-ttu-id="567b0-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="567b0-140">See also</span></span>

- [<span data-ttu-id="567b0-141">はじめに</span><span class="sxs-lookup"><span data-stu-id="567b0-141">Getting Started</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/getting-started.md)
