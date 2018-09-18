---
title: LINQ to DataSet
ms.date: 03/30/2017
ms.assetid: 743e3755-3ecb-45a2-8d9b-9ed41f0dcf17
ms.openlocfilehash: 5e1644af7e07ad3395a30e56df52b7f85cefa77c
ms.sourcegitcommit: f513a91160b3fec289dd06646d0d6f81f8fcf910
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/18/2018
ms.locfileid: "46006091"
---
# <a name="linq-to-dataset"></a>LINQ to DataSet
[!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] は、<xref:System.Data.DataSet> オブジェクトにキャッシュされたデータに対するクエリをより簡単に、より高速にします。 具体的には、[!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)]個別のクエリ言語を使用して、クエリの代わりに、プログラミング言語そのものを記述できるので、クエリを簡略化します。 これは、コンパイル時の構文チェック、静的な型指定、およびそのクエリで Visual Studio によって提供される IntelliSense サポートのメリットを得ることができます、Visual Studio 開発者に特に便利です。  
  
 また、[!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] を使用すると、1 つまたは複数のデータ ソースから取得して統合したデータを照会することもできます。 これにより、ローカルに集計されたデータのクエリや Web アプリケーションでの中間層のキャッシュなど、データの表現方法や扱いに柔軟性が要求されるさまざまなシナリオが実現します。 特に、汎用のレポート作成、分析、ビジネス インテリジェンスを行うアプリケーションでは、この手法を用いたデータ操作が欠かせません。  
  
 [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)]機能は、拡張メソッドによって主に公開されて、<xref:System.Data.DataRowExtensions>と<xref:System.Data.DataTableExtensions>クラス。 [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] ビルドされ、既存を使用して[!INCLUDE[ado_whidbey_long](../../../../includes/ado-whidbey-long-md.md)]のアーキテクチャを置き換えるものでありません[!INCLUDE[ado_whidbey_long](../../../../includes/ado-whidbey-long-md.md)]アプリケーション コードでします。 既存の ADO.NET 2.0 コードは [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] アプリケーションにおいても機能します。 [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] と [!INCLUDE[ado_whidbey_long](../../../../includes/ado-whidbey-long-md.md)] のリレーションシップとデータ ストアを次の図に示します。  
  
 ![ADO.NET プロバイダーに基づく LINQ to DataSet](../../../../docs/framework/data/adonet/media/linqtodataset.gif "LINQtoDataSet")  
  
## <a name="in-this-section"></a>このセクションの内容  
 [はじめに](../../../../docs/framework/data/adonet/getting-started-linq-to-dataset.md)  
  
 [プログラミング ガイド](../../../../docs/framework/data/adonet/programming-guide-linq-to-dataset.md)  
  
## <a name="reference"></a>参照  
 <xref:System.Data.DataTableExtensions>  
  
 <xref:System.Data.DataRowExtensions>  
  
 <xref:System.Data.DataRowComparer>  
  
## <a name="see-also"></a>関連項目  
 [統合言語クエリ (LINQ)](https://msdn.microsoft.com/library/a73c4aec-5d15-4e98-b962-1274021ea93d)  
 [LINQ と ADO.NET](../../../../docs/framework/data/adonet/linq-and-ado-net.md)  
 [ADO.NET](../../../../docs/framework/data/adonet/index.md)
