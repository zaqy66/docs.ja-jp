---
title: System.Xml の使用法
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 82302f0d-a621-4c6f-b57d-999bd61f21a6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5c3eb01e1050bc78d2b31de19a8a728af92777e8
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43863388"
---
# <a name="systemxml-usage"></a><span data-ttu-id="58f59-102">System.Xml の使用法</span><span class="sxs-lookup"><span data-stu-id="58f59-102">System.Xml Usage</span></span>
<span data-ttu-id="58f59-103">このセクションで内に存在するいくつかの型の使用方法について説明<xref:System.Xml?displayProperty=nameWithType>XML データを表すために使用する名前空間。</span><span class="sxs-lookup"><span data-stu-id="58f59-103">This section talks about usage of several types residing in <xref:System.Xml?displayProperty=nameWithType> namespaces that can be used to represent XML data.</span></span>  
  
 <span data-ttu-id="58f59-104">**X DO NOT** 使用<xref:System.Xml.XmlNode>または<xref:System.Xml.XmlDocument>XML データを表します。</span><span class="sxs-lookup"><span data-stu-id="58f59-104">**X DO NOT** use <xref:System.Xml.XmlNode> or <xref:System.Xml.XmlDocument> to represent XML data.</span></span> <span data-ttu-id="58f59-105">インスタンスを使用して優先<xref:System.Xml.XPath.IXPathNavigable>、 <xref:System.Xml.XmlReader>、 <xref:System.Xml.XmlWriter>、またはのサブタイプ<xref:System.Xml.Linq.XNode>代わりにします。</span><span class="sxs-lookup"><span data-stu-id="58f59-105">Favor using instances of <xref:System.Xml.XPath.IXPathNavigable>, <xref:System.Xml.XmlReader>, <xref:System.Xml.XmlWriter>, or subtypes of <xref:System.Xml.Linq.XNode> instead.</span></span> <span data-ttu-id="58f59-106">`XmlNode` `XmlDocument`パブリック Api で公開するために設計されていません。</span><span class="sxs-lookup"><span data-stu-id="58f59-106">`XmlNode` and `XmlDocument` are not designed for exposing in public APIs.</span></span>  
  
 <span data-ttu-id="58f59-107">**✓ DO** 使用`XmlReader`、 `IXPathNavigable`、またはのサブタイプ`XNode`をそのまま使用したり、XML を返すメンバーの入力または出力として。</span><span class="sxs-lookup"><span data-stu-id="58f59-107">**✓ DO** use `XmlReader`, `IXPathNavigable`, or subtypes of `XNode` as input or output of members that accept or return XML.</span></span>  
  
 <span data-ttu-id="58f59-108">代わりにこれらの抽象化を使用して、 `XmlDocument`、 `XmlNode`、または<xref:System.Xml.XPath.XPathDocument>これ、インメモリ XML ドキュメントの特定の実装からメソッドを分離し、公開仮想の XML データ ソースを操作することができますので、 `XNode`、 `XmlReader`、または<xref:System.Xml.XPath.XPathNavigator>します。</span><span class="sxs-lookup"><span data-stu-id="58f59-108">Use these abstractions instead of `XmlDocument`, `XmlNode`, or <xref:System.Xml.XPath.XPathDocument>, because this decouples the methods from specific implementations of an in-memory XML document and allows them to work with virtual XML data sources that expose `XNode`, `XmlReader`, or <xref:System.Xml.XPath.XPathNavigator>.</span></span>  
  
 <span data-ttu-id="58f59-109">**X DO NOT** サブクラス`XmlDocument`を基になるオブジェクト モデルまたはデータ ソースの XML ビューを表す型を作成するかどうか。</span><span class="sxs-lookup"><span data-stu-id="58f59-109">**X DO NOT** subclass `XmlDocument` if you want to create a type representing an XML view of an underlying object model or data source.</span></span>  
  
 <span data-ttu-id="58f59-110">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="58f59-110">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="58f59-111">*2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*</span><span class="sxs-lookup"><span data-stu-id="58f59-111">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58f59-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="58f59-112">See also</span></span>

- [<span data-ttu-id="58f59-113">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="58f59-113">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="58f59-114">使用方法のガイドライン</span><span class="sxs-lookup"><span data-stu-id="58f59-114">Usage Guidelines</span></span>](../../../docs/standard/design-guidelines/usage-guidelines.md)
