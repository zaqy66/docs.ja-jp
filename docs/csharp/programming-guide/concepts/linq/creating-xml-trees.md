---
title: XML ツリーの作成 (C#)
ms.date: 07/20/2015
ms.assetid: bccc3e0a-c08c-468e-9d30-e075670fdace
ms.openlocfilehash: 64aed2a02f2f31036458ae878a3cbd21d9526d9b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54515850"
---
# <a name="creating-xml-trees-c"></a><span data-ttu-id="f6ac5-102">XML ツリーの作成 (C#)</span><span class="sxs-lookup"><span data-stu-id="f6ac5-102">Creating XML Trees (C#)</span></span>
<span data-ttu-id="f6ac5-103">最も一般的な XML タスクの 1 つは、XML ツリーの構築です。</span><span class="sxs-lookup"><span data-stu-id="f6ac5-103">One of the most common XML tasks is constructing an XML tree.</span></span> <span data-ttu-id="f6ac5-104">ここでは、XML ツリーを作成するいくつかの方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f6ac5-104">This section describes several ways to create them.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f6ac5-105">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="f6ac5-105">In This Section</span></span>  
  
|<span data-ttu-id="f6ac5-106">トピック</span><span class="sxs-lookup"><span data-stu-id="f6ac5-106">Topic</span></span>|<span data-ttu-id="f6ac5-107">説明</span><span class="sxs-lookup"><span data-stu-id="f6ac5-107">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="f6ac5-108">関数型構築 (LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="f6ac5-108">Functional Construction (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/functional-construction-linq-to-xml.md)|<span data-ttu-id="f6ac5-109">[!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] の関数型構築の概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="f6ac5-109">Provides an overview of functional construction in [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span></span> <span data-ttu-id="f6ac5-110">関数型構築は、単一のステートメントで XML ツリーの全体または一部を作成するための機能です。</span><span class="sxs-lookup"><span data-stu-id="f6ac5-110">Functional construction enables you to create all or part of your XML tree in a single statement.</span></span> <span data-ttu-id="f6ac5-111">このトピックでは、XML ツリーを構築する際にクエリを組み込む方法も示します。</span><span class="sxs-lookup"><span data-stu-id="f6ac5-111">This topic also shows how to embed queries when constructing an XML tree.</span></span>|  
|[<span data-ttu-id="f6ac5-112">C# での XML ツリーの作成 (LINQ to XML)</span><span class="sxs-lookup"><span data-stu-id="f6ac5-112">Creating XML Trees in C# (LINQ to XML)</span></span>](../../../../csharp/programming-guide/concepts/linq/creating-xml-trees-linq-to-xml-2.md)|<span data-ttu-id="f6ac5-113">C# でツリーを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f6ac5-113">Shows how to create trees in C#.</span></span>|  
|[<span data-ttu-id="f6ac5-114">XML の解析 (C#)</span><span class="sxs-lookup"><span data-stu-id="f6ac5-114">Parsing XML (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/parsing-xml.md)|<span data-ttu-id="f6ac5-115">さまざまなソースの XML を解析する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f6ac5-115">Shows how to parse XML from a variety of sources.</span></span> [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] <span data-ttu-id="f6ac5-116">は、XML の解析に使用する <xref:System.Xml.XmlReader> の上位に階層化されます。</span><span class="sxs-lookup"><span data-stu-id="f6ac5-116">is layered on top of <xref:System.Xml.XmlReader>, which is used to parse the XML.</span></span>|  
|[<span data-ttu-id="f6ac5-117">方法: XmlWriter を使用して XML ツリーを設定する (LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="f6ac5-117">How to: Populate an XML Tree with an XmlWriter (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-populate-an-xml-tree-with-an-xmlwriter-linq-to-xml.md)|<span data-ttu-id="f6ac5-118"><xref:System.Xml.XmlWriter> を使用して XML ツリーを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f6ac5-118">Shows how to populate an XML tree by using an <xref:System.Xml.XmlWriter>.</span></span>|  
|[<span data-ttu-id="f6ac5-119">方法: XSD を使用して検証する (LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="f6ac5-119">How to: Validate Using XSD (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-validate-using-xsd-linq-to-xml.md)|<span data-ttu-id="f6ac5-120">XSD を使用して XML ツリーを検証する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f6ac5-120">Shows how to validate an XML tree using XSD.</span></span>|  
|[<span data-ttu-id="f6ac5-121">XElement オブジェクトと XDocument オブジェクトの有効なコンテンツ</span><span class="sxs-lookup"><span data-stu-id="f6ac5-121">Valid Content of XElement and XDocument Objects</span></span>](../../../../csharp/programming-guide/concepts/linq/valid-content-of-xelement-and-xdocument-objects3.md)|<span data-ttu-id="f6ac5-122">コンストラクターやメソッドに渡すことができる有効な引数について説明します。これらのコンストラクターやメソッドは、コンテンツを要素やドキュメントに追加するためのものです。</span><span class="sxs-lookup"><span data-stu-id="f6ac5-122">Describes the valid arguments that can be passed to the constructors and methods that are used to add content to elements and documents.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f6ac5-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6ac5-123">See also</span></span>

- [<span data-ttu-id="f6ac5-124">プログラミング ガイド (LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="f6ac5-124">Programming Guide (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/programming-guide-linq-to-xml.md)
