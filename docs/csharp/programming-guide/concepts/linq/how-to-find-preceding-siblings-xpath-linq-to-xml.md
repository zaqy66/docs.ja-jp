---
title: '方法: 先行する兄弟を検索する (XPath-LINQ to XML) (C#)'
ms.date: 07/20/2015
ms.assetid: b281ff99-d08a-43d0-bea1-eff831b2f8ae
ms.openlocfilehash: de5393f720a854b9644dc7cac7d73c3c6d380483
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54707428"
---
# <a name="how-to-find-preceding-siblings-xpath-linq-to-xml-c"></a><span data-ttu-id="d1328-102">方法: 先行する兄弟を検索する (XPath-LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="d1328-102">How to: Find Preceding Siblings (XPath-LINQ to XML) (C#)</span></span>
<span data-ttu-id="d1328-103">このトピックでは、XPath の `preceding-sibling` 軸と [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] の子 <xref:System.Xml.Linq.XNode.ElementsBeforeSelf%2A?displayProperty=nameWithType> 軸を比較します。</span><span class="sxs-lookup"><span data-stu-id="d1328-103">This topic compares the XPath `preceding-sibling` axis to the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] child <xref:System.Xml.Linq.XNode.ElementsBeforeSelf%2A?displayProperty=nameWithType> axis.</span></span>  
  
 <span data-ttu-id="d1328-104">XPath 式を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d1328-104">The XPath expression is:</span></span>  
  
 `preceding-sibling::*`  
  
 <span data-ttu-id="d1328-105"><xref:System.Xml.XPath.Extensions.XPathSelectElements%2A> と <xref:System.Xml.Linq.XNode.ElementsBeforeSelf%2A?displayProperty=nameWithType> の結果はドキュメント順になることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d1328-105">Note that the results of both <xref:System.Xml.XPath.Extensions.XPathSelectElements%2A> and <xref:System.Xml.Linq.XNode.ElementsBeforeSelf%2A?displayProperty=nameWithType> are in document order.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d1328-106">例</span><span class="sxs-lookup"><span data-stu-id="d1328-106">Example</span></span>  
 <span data-ttu-id="d1328-107">次の例では、`FullAddress` 要素を検索し、次に `preceding-sibling` 軸を使用して前の要素を取得します。</span><span class="sxs-lookup"><span data-stu-id="d1328-107">The following example finds the `FullAddress` element, and then retrieves the previous elements using the `preceding-sibling` axis.</span></span>  
  
 <span data-ttu-id="d1328-108">この例では、次の XML ドキュメントを使用します。[サンプル XML ファイル:顧客と注文 (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-customers-and-orders-linq-to-xml-2.md)。</span><span class="sxs-lookup"><span data-stu-id="d1328-108">This example uses the following XML document: [Sample XML File: Customers and Orders (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-customers-and-orders-linq-to-xml-2.md).</span></span>  
  
```csharp  
XElement co = XElement.Load("CustomersOrders.xml");  
  
XElement add = co.Element("Customers").Element("Customer").Element("FullAddress");  
  
// LINQ to XML query  
IEnumerable<XElement> list1 = add.ElementsBeforeSelf();  
  
// XPath expression  
IEnumerable<XElement> list2 = add.XPathSelectElements("preceding-sibling::*");  
  
if (list1.Count() == list2.Count() &&  
        list1.Intersect(list2).Count() == list1.Count())  
    Console.WriteLine("Results are identical");  
else  
    Console.WriteLine("Results differ");  
foreach (XElement el in list2)  
    Console.WriteLine(el);  
```  
  
 <span data-ttu-id="d1328-109">この例を実行すると、次の出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="d1328-109">This example produces the following output:</span></span>  
  
```  
Results are identical  
<CompanyName>Great Lakes Food Market</CompanyName>  
<ContactName>Howard Snyder</ContactName>  
<ContactTitle>Marketing Manager</ContactTitle>  
<Phone>(503) 555-7555</Phone>  
```  
  
## <a name="see-also"></a><span data-ttu-id="d1328-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1328-110">See also</span></span>

- [<span data-ttu-id="d1328-111">XPath ユーザー向けの LINQ to XML (C#)</span><span class="sxs-lookup"><span data-stu-id="d1328-111">LINQ to XML for XPath Users (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
