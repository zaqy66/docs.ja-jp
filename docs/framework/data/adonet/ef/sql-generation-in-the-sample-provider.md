---
title: サンプル プロバイダーでの SQL 生成
ms.date: 03/30/2017
ms.assetid: e70f553d-4622-4627-928e-1aa2ee605d8e
ms.openlocfilehash: 5aa6e31cfc93a4ae1871da63f466864b4ea6f5d9
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53149719"
---
# <a name="sql-generation-in-the-sample-provider"></a>サンプル プロバイダーでの SQL 生成
[Entity Framework サンプル プロバイダー](https://code.msdn.microsoft.com/windowsdesktop/Entity-Framework-Sample-6a9801d0)をサポートする ADO.NET データ プロバイダーの新しいコンポーネントを示して、[!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]します。  これは、SQL Server 2005 データベースで動作し、System.Data.SqlClient ADO.NET 2.0 データ プロバイダーのラッパーとして実装されます。  
  
 サンプル プロバイダーの SQL 生成モジュール (DmlSqlGenerator.cs ファイルを除き、SQL Generation フォルダーにあります) では、入力として DbQueryCommandTree を使用し、単一の SQL SELECT ステートメントを生成します。  
  
## <a name="in-this-section"></a>このセクションの内容  
 ここでは、次のトピックについて説明します。  
  
 [アーキテクチャとデザイン](../../../../../docs/framework/data/adonet/ef/architecture-and-design.md)  
  
 [チュートリアル:SQL 生成](../../../../../docs/framework/data/adonet/ef/walkthrough-sql-generation.md)  
  
## <a name="see-also"></a>関連項目  
 [SQL 生成](../../../../../docs/framework/data/adonet/ef/sql-generation.md)
