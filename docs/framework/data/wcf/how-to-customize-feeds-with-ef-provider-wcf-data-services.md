---
title: '方法: Entity Framework プロバイダー (WCF Data Services) を使用したフィードをカスタマイズします。'
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, customizing
- WCF Data Services, customizing feeds
ms.assetid: fd16272e-36f2-415e-850e-8a81f2b17525
ms.openlocfilehash: 51e85fa108775806d2c92935868d7ed68534818f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54587974"
---
# <a name="how-to-customize-feeds-with-the-entity-framework-provider-wcf-data-services"></a>方法: Entity Framework プロバイダー (WCF Data Services) を使用したフィードをカスタマイズします。
[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] では、データ サービス応答の Atom シリアル化をカスタマイズして、AtomPub プロトコルで定義されている未使用の要素にエンティティのプロパティをマップできます。 このトピックでは、Entity Framework を使用して、.edmx ファイルで定義されているデータ モデルのエンティティ型のマッピング属性を定義する方法について説明します。 詳細については、次を参照してください。[フィードのカスタマイズ](../../../../docs/framework/data/wcf/feed-customization-wcf-data-services.md)します。  
  
 このトピックでは、ツールによって生成された .edmx file ファイルを手動で変更します (このファイルには、データ モデルが含まれます)。 エンティティ デザイナーではデータ モデルへの拡張がサポートされていないので、このファイルは手動で変更する必要があります。 Entity Data Model ツールによって生成される .edmx ファイルの詳細については、次を参照してください。 [.edmx ファイルの概要](https://msdn.microsoft.com/library/f4c8e7ce-1db6-417e-9759-15f8b55155d4)します。 このトピックの例では、Northwind サンプル データ サービスおよび自動生成されたクライアント データ サービス クラスを使用します。 このサービスとクライアント データ クラスを作成を完了すると、 [WCF Data Services クイック スタート](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md)します。  
  
### <a name="to-manually-modify-the-northwindedmx-file-to-add-feed-customization-attributes"></a>Northwind.edmx ファイルを手動で変更してフィードのカスタマイズ属性を追加するには  
  
1.  **ソリューション エクスプ ローラー**を右クリックし、`Northwind.edmx`ファイルを開き、をクリックし、**プログラムから開く**します。  
  
2.  **プログラム開く - Northwind.edmx から**ダイアログ ボックスで、 **XML エディター**、順にクリックします**OK**します。  
  
3.  `ConceptualModels` 要素を見つけて、フィードのカスタマイズ マッピング属性を含む次の要素で既存の `Customers` エンティティ型を置き換えます。  
  
     [!code-xml[Astoria Custom Feeds#EdmFeedCustomers](../../../../samples/snippets/xml/VS_Snippets_Misc/astoria custom feeds/xml/northwind.csdl#edmfeedcustomers)]  
  
4.  変更を保存して Northwind.edmx ファイルを閉じます。  
  
5.  (省略可能)Northwind.edmx ファイルを右クリックし、をクリックし、**カスタム ツールの実行**します。  
  
     オブジェクト レイヤー ファイルが再生成されます。このファイルが必要になる場合があります。  
  
6.  プロジェクトを再コンパイルします。  
  
## <a name="example"></a>例  
 前の例では、URI `http://myservice/``Northwind.svc/Customers('ALFKI')` に次の結果が返されます。  
  
 [!code-xml[Astoria Custom Feeds#EdmFeedResult](../../../../samples/snippets/xml/VS_Snippets_Misc/astoria custom feeds/xml/edmfeedresult.xml#edmfeedresult)]  
  
## <a name="see-also"></a>関連項目
- [Entity Framework プロバイダー](../../../../docs/framework/data/wcf/entity-framework-provider-wcf-data-services.md)
