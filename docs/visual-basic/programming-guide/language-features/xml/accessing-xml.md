---
title: Visual Basic での XML へのアクセス
ms.date: 07/20/2015
helpviewer_keywords:
- LINQ to XML [Visual Basic], accessing XML
- Visual Basic code, XML
- accessing XML [Visual Basic], axis properties
- XML [Visual Basic], axis properties
- XML [Visual Basic], accessing
ms.assetid: c47f88b2-3cbc-4bb1-b4b9-be60f71ffc6a
ms.openlocfilehash: 0540c52cf3e4cd7594f051c10832ea99cf58a34e
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43734383"
---
# <a name="accessing-xml-in-visual-basic"></a>Visual Basic での XML へのアクセス
Visual Basic では XML 軸のプロパティにアクセスすると、移動[!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)]構造体。 これらのプロパティは、要素と属性を XML の名前を指定することでアクセスするために特別な構文を使用します。  
  
 次の表では、Visual Basic の XML 要素と属性にアクセスするための言語機能を示します。  
  
### <a name="xml-axis-properties"></a>XML 軸プロパティ  
  
|プロパティの説明|例|説明|  
|--------------------------|-------------|-----------------|  
|*子軸*|`contact.<phone>`|すべて取得`phone`要素の子要素である、`contact`要素。|  
|*attribute 軸*|`phone.@type`|すべて取得`type`の属性、`phone`要素。|  
|*descendant 軸*|`contacts...<name>`|すべて取得`name`の要素、`contacts`が発生した階層の深さに関係なく、要素。|  
|*拡張機能インデクサー*|`contacts...<name>(0)`|最初に取得`name`シーケンスから要素。|  
|*値*|`contacts...<name>.Value`|シーケンスの最初のオブジェクトの文字列表現を取得または`Nothing`シーケンスが空の場合。|  
  
## <a name="in-this-section"></a>このセクションの内容  
 [方法: XML 子孫要素にアクセスする](../../../../visual-basic/programming-guide/language-features/xml/how-to-access-xml-descendant-elements.md)  
 子孫軸プロパティを使用して、指定した名前を持ち、指定された XML 要素に含まれるすべての XML 要素にアクセスする方法を示しています。  
  
 [方法: XML 子要素にアクセスする](../../../../visual-basic/programming-guide/language-features/xml/how-to-access-xml-child-elements.md)  
 軸のプロパティを XML 要素で指定した名前を持つすべての XML 子要素にアクセスする子を使用する方法を示します。  
  
 [方法: XML 属性にアクセスする](../../../../visual-basic/programming-guide/language-features/xml/how-to-access-xml-attributes.md)  
 属性軸プロパティを使用して、指定した名前の XML 要素であるすべての XML 属性にアクセスする方法を示しています。  
  
 [方法 : XML 名前空間プレフィックスを宣言して使用する](../../../../visual-basic/programming-guide/language-features/xml/how-to-declare-and-use-xml-namespace-prefixes.md)  
 XML 名前空間プレフィックスを宣言し、それを使用して作成し、XML 要素にアクセスする方法を示しています。  
  
## <a name="related-sections"></a>関連項目  
 [XML 軸プロパティ](../../../../visual-basic/language-reference/xml-axis/index.md)  
 さまざまな XML へのアクセスのプロパティを記述するセクションへのリンクを提供します。  
  
 [Visual Basic における LINQ to XML の概要](../../../../visual-basic/programming-guide/language-features/xml/overview-of-linq-to-xml.md)  
 使用の概要を提供します。 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] Visual Basic でします。  
  
 [Visual Basic での XML の作成](../../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)  
 Visual Basic での XML リテラルの使用の概要を提供します。  
  
 [Visual Basic での XML の操作](../../../../visual-basic/programming-guide/language-features/xml/manipulating-xml.md)  
 読み込みと Visual Basic における XML の変更についてのセクションへのリンクを提供します。  
  
 [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)  
 使用する方法を説明するセクションへのリンクを提供します。 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] Visual Basic でします。
