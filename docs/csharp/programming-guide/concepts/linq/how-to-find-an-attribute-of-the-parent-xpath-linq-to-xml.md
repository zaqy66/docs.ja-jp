---
title: '方法: 親の属性を検索する (XPath-LINQ to XML) (C#)'
ms.date: 07/20/2015
ms.assetid: dbef9d89-a5c4-431f-80cc-7a2ebf323f86
ms.openlocfilehash: e139e278141a8f42cddf8103f1c5d8d3195751e4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54621813"
---
# <a name="how-to-find-an-attribute-of-the-parent-xpath-linq-to-xml-c"></a><span data-ttu-id="2a57a-102">方法: 親の属性を検索する (XPath-LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="2a57a-102">How to: Find an Attribute of the Parent (XPath-LINQ to XML) (C#)</span></span>
<span data-ttu-id="2a57a-103">このトピックでは、親要素に移動してその属性を検索する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2a57a-103">This topic shows how to navigate to the parent element and find an attribute of it.</span></span>  
  
 <span data-ttu-id="2a57a-104">XPath 式を次に示します。</span><span class="sxs-lookup"><span data-stu-id="2a57a-104">The XPath expression is:</span></span>  
  
 `../@id`  
  
## <a name="example"></a><span data-ttu-id="2a57a-105">例</span><span class="sxs-lookup"><span data-stu-id="2a57a-105">Example</span></span>  
 <span data-ttu-id="2a57a-106">この例では、まず `Author` 要素を検索します。</span><span class="sxs-lookup"><span data-stu-id="2a57a-106">This example first finds an `Author` element.</span></span> <span data-ttu-id="2a57a-107">次に、親要素の `id` 属性を検索します。</span><span class="sxs-lookup"><span data-stu-id="2a57a-107">It then finds the `id` attribute of the parent element.</span></span>  
  
 <span data-ttu-id="2a57a-108">この例では、XML ドキュメント、[サンプル XML ファイル:書籍 (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-books-linq-to-xml.md) を使用します。</span><span class="sxs-lookup"><span data-stu-id="2a57a-108">This example uses the following XML document: [Sample XML File: Books (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-books-linq-to-xml.md).</span></span>  
  
```csharp  
XDocument books = XDocument.Load("Books.xml");  
  
XElement author =   
    books  
    .Root  
    .Element("Book")  
    .Element("Author");  
  
// LINQ to XML query  
XAttribute att1 =  
    author  
    .Parent  
    .Attribute("id");  
  
// XPath expression  
XAttribute att2 = ((IEnumerable)author.XPathEvaluate("../@id")).Cast<XAttribute>().First();  
  
if (att1 == att2)  
    Console.WriteLine("Results are identical");  
else  
    Console.WriteLine("Results differ");  
Console.WriteLine(att1);  
```  
  
 <span data-ttu-id="2a57a-109">この例を実行すると、次の出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="2a57a-109">This example produces the following output:</span></span>  
  
```  
Results are identical  
id="bk101"  
```  
  
## <a name="see-also"></a><span data-ttu-id="2a57a-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a57a-110">See also</span></span>

- [<span data-ttu-id="2a57a-111">XPath ユーザー向けの LINQ to XML (C#)</span><span class="sxs-lookup"><span data-stu-id="2a57a-111">LINQ to XML for XPath Users (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
