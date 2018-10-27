---
title: ADO.NET コード サンプルについては、サンプル データベースを取得します。
description: ADO.NET のドキュメントと SQL Server および管理ツールのコード サンプルで使用されるサンプル データベースをダウンロードします。
ms.date: 10/18/2018
ms.assetid: ef9d69a1-9461-43fe-94bb-7c836754bcb5
ms.openlocfilehash: 9779300288135cb9332a028d547ce55a07e89471
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188392"
---
# <a name="get-the-sample-databases-for-adonet-code-samples"></a>ADO.NET コード サンプルについては、サンプル データベースを取得します。

さまざまなサンプルおよびチュートリアルで、[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]ドキュメントは、サンプル データベースと SQL Server Express を使用します。 これらの製品を無料では、Microsoft からダウンロードできます。

## <a name="get-the-northwind-sample-database"></a>Northwind サンプル データベースします。

Microsoft ダウンロード センターの次のページからは、Northwind サンプル データベースをダウンロードします。

[Northwind および Pubs サンプル データベース](https://go.microsoft.com/fwlink?linkid=64296)

ファイルがダウンロードされた後は、データベースとスクリプトを抽出するファイルをダブルクリックします。 フォルダーに既定では、ファイルがインストールされている`<drive>:\SQL Server 2000 Sample Databases`します。

使用して SQL Server のインスタンス上のデータベースを再作成する必要がある、Northwind データベースを使用する前に[SQL Server Management Studio](#get_ssms)または同様のツールを実行する、`instnwnd.sql`インストール フォルダーにスクリプト ファイル。

## <a name="get-the-adventureworks-sample-database"></a>AdventureWorks サンプル データベースします。

次の GitHub リポジトリから AdventureWorks サンプル データベースをダウンロードします。

[AdventureWorks サンプル データベース](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks)

データベースのバックアップのいずれかをダウンロードした後 (\*.bak) ファイル、SQL Server のインスタンスに SQL Server Management Studio (SSMS) を使用して、バックアップを復元します。 参照してください[SQL Server Management Studio を入手する](#get_ssms)します。

## <a name="get_sql"></a> SQL Server Express の入手します。

SQL Server Express は、アプリケーションで再配布する SQL Server の無料のエントリー エディションです。 次のページから SQL Server Express をダウンロードします。
  
[SQL Server Express Edition](https://www.microsoft.com/sql-server/sql-server-editions-express)

使用している場合[Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)、SQL Server Express LocalDB は、無料の Community edition と Professional 以上のエディションに含まれています。  

## <a name="get_ssms"></a> SQL Server Management Studio を入手します。
表示またはダウンロードしたデータベースを変更する場合は、SQL Server Management Studio (SSMS) を使用することができます。 次のページから SSMS をダウンロードします。

[SQL Server Management Studio (SSMS) のダウンロードします。](/sql/ssms/download-sql-server-management-studio-ssms) 

また、表示、Visual Studio 統合開発環境 (IDE) でデータベースを管理およびできます。 [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)からデータベースに接続する**SQL Server オブジェクト エクスプ ローラー**、データベースにデータ接続を作成または**サーバー エクスプ ローラー**します。 これらのエクスプ ローラー ウィンドウを開き、**ビュー**メニュー。
  
## <a name="see-also"></a>関連項目

- [はじめに](../../../../../../docs/framework/data/adonet/sql/linq/getting-started.md)
