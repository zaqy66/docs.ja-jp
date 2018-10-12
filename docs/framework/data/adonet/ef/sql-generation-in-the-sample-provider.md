---
title: サンプル プロバイダーでの SQL 生成
ms.date: 03/30/2017
ms.assetid: e70f553d-4622-4627-928e-1aa2ee605d8e
ms.openlocfilehash: cba1cec6d7ef0fdf8d4d4cf6c8e44fb325cf6447
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "44041299"
---
# <a name="sql-generation-in-the-sample-provider"></a>サンプル プロバイダーでの SQL 生成
[Entity Framework サンプル プロバイダー](https://go.microsoft.com/fwlink/?LinkId=180616)をサポートする ADO.NET データ プロバイダーの新しいコンポーネントを示して、[!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]します。  これは、SQL Server 2005 データベースで動作し、System.Data.SqlClient ADO.NET 2.0 データ プロバイダーのラッパーとして実装されます。  
  
 サンプル プロバイダーの SQL 生成モジュール (DmlSqlGenerator.cs ファイルを除き、SQL Generation フォルダーにあります) では、入力として DbQueryCommandTree を使用し、単一の SQL SELECT ステートメントを生成します。  
  
## <a name="in-this-section"></a>このセクションの内容  
 ここでは、次のトピックについて説明します。  
  
 [アーキテクチャとデザイン](../../../../../docs/framework/data/adonet/ef/architecture-and-design.md)  
  
 [チュートリアル: SQL 生成](../../../../../docs/framework/data/adonet/ef/walkthrough-sql-generation.md)  
  
## <a name="see-also"></a>関連項目  
 [SQL 生成](../../../../../docs/framework/data/adonet/ef/sql-generation.md)
