---
title: 異なるストアでの XSLT 変換
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 369850e9-004a-45d2-b5c3-5060d9135adb
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0b5ff264f9a781c95ccf9bdbabf4b29806016362
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43890842"
---
# <a name="xslt-transformations-over-different-stores"></a>異なるストアでの XSLT 変換
> [!NOTE]
>  <xref:System.Xml.Xsl.XslTransform> では、[!INCLUDE[dnprdnext](../../../../includes/dnprdnext-md.md)] クラスが廃止されています。 <xref:System.Xml.Xsl.XslCompiledTransform> クラスを使用して XSLT (Extensible Stylesheet Language for Transformations) 変換を実行できます。 詳しくは、「[XslCompiledTransform クラスの使用](../../../../docs/standard/data/xml/using-the-xslcompiledtransform-class.md)」および「[XslTransform クラスからの移行](../../../../docs/standard/data/xml/migrating-from-the-xsltransform-class.md)」をご覧ください。  
  
 ADO.NET と [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] の XML クラスは、データ アクセス用の統合プログラミング モデルとして機能します。 そのデータは、XML データ (タグで区切られたテキスト) とリレーショナル データ (行と列で構成されたテーブル) のどちらとしても表されます。 [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] の XML は、XML データを任意のデータ ストリームから XML ドキュメント オブジェクト モデル (DOM) ノード ツリーに読み込みます。読み込まれたデータにはプログラムからアクセスできます。一方、ADO.NET は、<xref:System.Data.DataSet> オブジェクト内のリレーショナル データにアクセスし、それを操作する手段を提供します。  
  
 XML DOM により、XML ドキュメント内のデータや追加のクラスにアクセスして、XML ドキュメント内で読み取り、書き込み、および移動を行うことができます。 これらのクラスは、<xref:System.Xml> 名前空間でサポートされます。この名前空間は、XML DOM と ADO.NET が提供するデータ アクセス サービスを統合する役割も果たします。 <xref:System.Xml.XmlDataDocument> は、データへのリレーショナル アクセスを可能にします。 <xref:System.Xml.XmlDataDocument> は、XML を ADO.NET <xref:System.Data.DataSet> 内のリレーショナル データに対応付けます。 [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] ベースのアプリケーションであれば、<xref:System.Xml> 名前空間内のクラスを使用して、XML ドキュメントと <xref:System.Xml.XmlDataDocument> 内のリレーショナル データの両方にアクセスし、それらを操作できます。 この実装は、データを収集したり、分散させたりするための n 層アーキテクチャをサポートします。 詳細については、「[XML とリレーショナル データおよび ADO.NET との統合](../../../../docs/standard/data/xml/xml-integration-with-relational-data-and-adonet.md)」を参照してください。  
  
## <a name="see-also"></a>関連項目

- [XslTransform クラスによる XSLT プロセッサの実装](../../../../docs/standard/data/xml/xsltransform-class-implements-the-xslt-processor.md)
