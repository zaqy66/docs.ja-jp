---
title: System.Xml の使用法
ms.date: 10/22/2008
ms.technology: dotnet-standard
ms.assetid: 82302f0d-a621-4c6f-b57d-999bd61f21a6
author: KrzysztofCwalina
ms.openlocfilehash: fb0e1d3dc851f9726905dc375d50cf211dba8400
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53149544"
---
# <a name="systemxml-usage"></a>System.Xml の使用法
このセクションで内に存在するいくつかの型の使用方法について説明<xref:System.Xml?displayProperty=nameWithType>XML データを表すために使用する名前空間。  
  
 **X DO NOT** 使用<xref:System.Xml.XmlNode>または<xref:System.Xml.XmlDocument>XML データを表します。 インスタンスを使用して優先<xref:System.Xml.XPath.IXPathNavigable>、 <xref:System.Xml.XmlReader>、 <xref:System.Xml.XmlWriter>、またはのサブタイプ<xref:System.Xml.Linq.XNode>代わりにします。 `XmlNode` `XmlDocument`パブリック Api で公開するために設計されていません。  
  
 **✓ DO** 使用`XmlReader`、 `IXPathNavigable`、またはのサブタイプ`XNode`をそのまま使用したり、XML を返すメンバーの入力または出力として。  
  
 代わりにこれらの抽象化を使用して、 `XmlDocument`、 `XmlNode`、または<xref:System.Xml.XPath.XPathDocument>これ、インメモリ XML ドキュメントの特定の実装からメソッドを分離し、公開仮想の XML データ ソースを操作することができますので、 `XNode`、 `XmlReader`、または<xref:System.Xml.XPath.XPathNavigator>します。  
  
 **X DO NOT** サブクラス`XmlDocument`を基になるオブジェクト モデルまたはデータ ソースの XML ビューを表す型を作成するかどうか。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *Pearson Education, Inc. からのアクセス許可によって了承を得て転載[Framework デザイン ガイドライン。規則、手法、および再利用可能な .NET ライブラリの第 2 版のパターン](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)Krzysztof Cwalina、Brad 内容では、Microsoft Windows の開発シリーズの一部として、Addison-wesley Professional、2008 年 10 月 22日を公開します。*  
  
## <a name="see-also"></a>関連項目

- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)  
- [使用方法のガイドライン](../../../docs/standard/design-guidelines/usage-guidelines.md)
