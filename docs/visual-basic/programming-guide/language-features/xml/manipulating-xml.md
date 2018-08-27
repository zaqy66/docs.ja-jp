---
title: Visual Basic での XML の操作
ms.date: 07/20/2015
helpviewer_keywords:
- LINQ to XML [Visual Basic], manipulating XML
- Visual Basic code, XML
- XML [Visual Basic], manipulating
ms.assetid: da32cffb-198d-41b1-9af3-260fe32e3b7d
ms.openlocfilehash: 7fd111f5e885de3389b8f93002db22b48c4edd45
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42931105"
---
# <a name="manipulating-xml-in-visual-basic"></a><span data-ttu-id="ed325-102">Visual Basic での XML の操作</span><span class="sxs-lookup"><span data-stu-id="ed325-102">Manipulating XML in Visual Basic</span></span>
<span data-ttu-id="ed325-103">使用することができます*XML リテラル*文字列、ファイル、またはストリームなどの外部ソースから XML を読み込めません。</span><span class="sxs-lookup"><span data-stu-id="ed325-103">You can use *XML literals* to load XML from an external source such as a string, file, or stream.</span></span> <span data-ttu-id="ed325-104">使用することができますし、 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] 、XML を操作して、使用する[!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)]XML に対してクエリをします。</span><span class="sxs-lookup"><span data-stu-id="ed325-104">You can then use [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] to manipulate the XML and use [!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)] to query the XML.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="ed325-105">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="ed325-105">In This Section</span></span>  
 [<span data-ttu-id="ed325-106">方法 : ファイル、文字列、またはストリームからの XML の読み込み</span><span class="sxs-lookup"><span data-stu-id="ed325-106">How to: Load XML from a File, String, or Stream</span></span>](../../../../visual-basic/programming-guide/language-features/xml/how-to-load-xml-from-a-file-string-or-stream.md)  
 <span data-ttu-id="ed325-107">XML を読み込む方法を示します、<xref:System.Xml.Linq.XDocument>または<xref:System.Xml.Linq.XElement>テキスト ファイル、文字列、またはストリームからのオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="ed325-107">Demonstrates how to load XML into an <xref:System.Xml.Linq.XDocument> or <xref:System.Xml.Linq.XElement> object from a text file, string, or stream.</span></span>  
  
 [<span data-ttu-id="ed325-108">方法 : LINQ を使用した XML の変換</span><span class="sxs-lookup"><span data-stu-id="ed325-108">How to: Transform XML by Using LINQ</span></span>](../../../../visual-basic/programming-guide/language-features/xml/how-to-transform-xml-by-using-linq.md)  
 <span data-ttu-id="ed325-109">内容を変換する方法を示します、<xref:System.Xml.Linq.XDocument>を新しい XML ドキュメント オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="ed325-109">Demonstrates how to transform the contents of an <xref:System.Xml.Linq.XDocument> object into a new XML document.</span></span>  
  
 [<span data-ttu-id="ed325-110">方法 : XML リテラルの変更</span><span class="sxs-lookup"><span data-stu-id="ed325-110">How to: Modify XML Literals</span></span>](../../../../visual-basic/programming-guide/language-features/xml/how-to-modify-xml-literals.md)  
 <span data-ttu-id="ed325-111">要素、属性、および XML リテラルの値を変更する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ed325-111">Demonstrates how to modify the elements, attributes, and values in an XML literal.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="ed325-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed325-112">Related Sections</span></span>  
 [<span data-ttu-id="ed325-113">XML 軸プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed325-113">XML Axis Properties</span></span>](../../../../visual-basic/language-reference/xml-axis/index.md)  
 <span data-ttu-id="ed325-114">さまざまな XML へのアクセスのプロパティを説明するセクションへのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="ed325-114">Provides links to sections that describe the various XML access properties.</span></span>  
  
 [<span data-ttu-id="ed325-115">Visual Basic における LINQ to XML の概要</span><span class="sxs-lookup"><span data-stu-id="ed325-115">Overview of LINQ to XML in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/xml/overview-of-linq-to-xml.md)  
 <span data-ttu-id="ed325-116">使用の概要を提供します。 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] Visual Basic でします。</span><span class="sxs-lookup"><span data-stu-id="ed325-116">Provides an introduction to using [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] in Visual Basic.</span></span>  
  
 [<span data-ttu-id="ed325-117">Visual Basic での XML の作成</span><span class="sxs-lookup"><span data-stu-id="ed325-117">Creating XML in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)  
 <span data-ttu-id="ed325-118">Visual Basic での XML リテラルの使用の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="ed325-118">Provides an introduction to using XML literals in Visual Basic.</span></span>  
  
 [<span data-ttu-id="ed325-119">Visual Basic での XML へのアクセス</span><span class="sxs-lookup"><span data-stu-id="ed325-119">Accessing XML in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/xml/accessing-xml.md)  
 <span data-ttu-id="ed325-120">XML 要素または Visual Basic でのドキュメントの部分にアクセスする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ed325-120">Demonstrates how to access parts of an XML element or document in Visual Basic.</span></span>  
  
 [<span data-ttu-id="ed325-121">XML</span><span class="sxs-lookup"><span data-stu-id="ed325-121">XML</span></span>](../../../../visual-basic/programming-guide/language-features/xml/index.md)  
 <span data-ttu-id="ed325-122">使用する方法を説明するセクションへのリンクを提供します。 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] Visual Basic でします。</span><span class="sxs-lookup"><span data-stu-id="ed325-122">Provides links to sections that describe how to use [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] in Visual Basic.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed325-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed325-123">See Also</span></span>  
 [<span data-ttu-id="ed325-124">XML</span><span class="sxs-lookup"><span data-stu-id="ed325-124">XML</span></span>](../../../../visual-basic/programming-guide/language-features/xml/index.md)  
 [<span data-ttu-id="ed325-125">LINQ</span><span class="sxs-lookup"><span data-stu-id="ed325-125">LINQ</span></span>](../../../../visual-basic/programming-guide/language-features/linq/index.md)  
 [<span data-ttu-id="ed325-126">Visual Basic における LINQ の概要</span><span class="sxs-lookup"><span data-stu-id="ed325-126">Introduction to LINQ in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
