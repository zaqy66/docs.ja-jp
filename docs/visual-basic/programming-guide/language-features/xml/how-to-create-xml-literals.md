---
title: '方法 : XML リテラルを作成する (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- XML literals [Visual Basic], creating
ms.assetid: 573a6db5-b14d-4e42-b356-8cc7e2d77745
ms.openlocfilehash: e5f8429b3ff02678bf8bf3e9e32bef6eb1a56831
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43483620"
---
# <a name="how-to-create-xml-literals-visual-basic"></a>方法 : XML リテラルを作成する (Visual Basic)
XML リテラルを使用して、XML ドキュメント、フラグメント、または要素をコード内で直接作成できます。 このトピックの例では、次の 3 つの子要素を持つ XML 要素を作成する方法と、XML ドキュメントを作成する方法を示します。  
  
 使用することも、 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] Api を作成する[!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)]オブジェクト。 詳細については、「<xref:System.Xml.Linq.XElement>」を参照してください。  
  
### <a name="to-create-an-xml-element"></a>XML 要素を作成するには  
  
-   実際の XML 構文と同じでは、XML リテラル構文を使用して XML インラインを作成します。  
  
     [!code-vb[VbXMLSamples#5](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-create-xml-literals_1.vb)]  
  
     コードを実行します。 このコードの出力は次のとおりです。  
  
     `<contact>`  
  
     `<name>Patrick Hines</name>`  
  
     `<phone type="home">206-555-0144</phone>`  
  
     `<phone type="work">425-555-0145</phone>`  
  
     `</contact>`  
  
### <a name="to-create-an-xml-document"></a>XML ドキュメントを作成するには  
  
-   XML ドキュメントのインラインを作成します。 次のコードは、リテラルの構文、XML 宣言、処理命令、コメント、および別の要素を格納する要素を含む XML ドキュメントを作成します。  
  
     [!code-vb[VbXMLSamples#30](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-create-xml-literals_2.vb)]  
  
     コードを実行します。 このコードの出力は次のとおりです。  
  
     `<?xml-stylesheet type="text/xsl" href="show_book.xsl"?>`  
  
     `<!-- Tests that the application works. -->`  
  
     `<books>`  
  
     `<book/>`  
  
     `</books>`  
  
## <a name="see-also"></a>関連項目  
 [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)  
 [Visual Basic での XML の作成](../../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)  
 [XML 要素リテラル](../../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)  
 [XML ドキュメント リテラル](../../../../visual-basic/language-reference/xml-literals/xml-document-literal.md)
