---
title: ASP.NET での LINQ to SQL N 層
ms.date: 03/30/2017
ms.assetid: f6cc863a-d6a6-4281-ba8b-197c01cf6c6f
ms.openlocfilehash: 0ea202f7259034614eed6968397e270807626172
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43799724"
---
# <a name="linq-to-sql-n-tier-with-aspnet"></a>ASP.NET での LINQ to SQL N 層
[!INCLUDE[vstecasp](../../../../../../includes/vstecasp-md.md)] を使用する [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]アプリケーションでは、 <xref:System.Web.UI.WebControls.LinqDataSource> Web サーバー コントロールが使われます。 このコントロールは、 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]に対するクエリ実行、ブラウザーへのデータ送信、データの取得、データベースを更新する [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.DataContext> へのデータ送信など、必要なほとんどのロジックを扱います。 マークアップでこのコントロールを構成するだけで、 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] とブラウザーの間のすべてのデータ転送をコントロールが処理するようになります。 このコントロールがプレゼンテーション層との対話を処理し、 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] がデータ層との通信を処理するため、 [!INCLUDE[vstecasp](../../../../../../includes/vstecasp-md.md)] 多層アプリケーションでは、カスタム ビジネス ロジックを作成することが開発者の主な作業になります。  
  
 詳細については`LINQDataSource`を参照してください[NIB: LinqDataSource Web サーバー コントロールの概要](https://msdn.microsoft.com/library/104cfc3f-7385-47d3-8a51-830dfa791136)します。  
  
## <a name="see-also"></a>関連項目  
 [LINQ to SQL を使用する n 層アプリケーションとリモート アプリケーション](../../../../../../docs/framework/data/adonet/sql/linq/n-tier-and-remote-applications-with-linq-to-sql.md)
