---
title: '方法: 要素を並べ替える (C#)'
ms.date: 07/20/2015
ms.assetid: aee6fbbc-81fd-4b3e-b40f-6ed7b3bd3fee
ms.openlocfilehash: 66a41fc018b2df64aa95c24d1d698b6c38fd189a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54640785"
---
# <a name="how-to-sort-elements-c"></a><span data-ttu-id="391ce-102">方法: 要素を並べ替える (C#)</span><span class="sxs-lookup"><span data-stu-id="391ce-102">How to: Sort Elements (C#)</span></span>
<span data-ttu-id="391ce-103">この例では、結果を並べ替えるクエリの作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="391ce-103">This example shows how to write a query that sorts its results.</span></span>  
  
## <a name="example"></a><span data-ttu-id="391ce-104">例</span><span class="sxs-lookup"><span data-stu-id="391ce-104">Example</span></span>  
 <span data-ttu-id="391ce-105">この例では、XML ドキュメント、[サンプル XML ファイル: 数値データ (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-linq-to-xml.md) を使用します。</span><span class="sxs-lookup"><span data-stu-id="391ce-105">This example uses the following XML document: [Sample XML File: Numerical Data (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-linq-to-xml.md).</span></span>  
  
```csharp  
XElement root = XElement.Load("Data.xml");  
IEnumerable<decimal> prices =  
    from el in root.Elements("Data")  
    let price = (decimal)el.Element("Price")  
    orderby price  
    select price;  
foreach (decimal el in prices)  
    Console.WriteLine(el);  
```  
  
 <span data-ttu-id="391ce-106">このコードを実行すると、次の出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="391ce-106">This code produces the following output:</span></span>  
  
```  
0.99  
4.95  
6.99  
24.50  
29.00  
66.00  
89.99  
```  
  
## <a name="example"></a><span data-ttu-id="391ce-107">例</span><span class="sxs-lookup"><span data-stu-id="391ce-107">Example</span></span>  
 <span data-ttu-id="391ce-108">次の例は名前空間に含まれている XML 用のクエリです。これらのクエリは上の例と同じ機能を表しています。</span><span class="sxs-lookup"><span data-stu-id="391ce-108">The following example shows the same query for XML that is in a namespace.</span></span> <span data-ttu-id="391ce-109">詳細については、「[XML 名前空間の使用 (C#)](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="391ce-109">For more information, see [Working with XML Namespaces (C#)](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span></span>  
  
 <span data-ttu-id="391ce-110">この例では、XML ドキュメント、[サンプル XML ファイル: 名前空間内の数値データ](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-in-a-namespace.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="391ce-110">This example uses the following XML document: [Sample XML File: Numerical Data in a Namespace](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-in-a-namespace.md).</span></span>  
  
```csharp  
XElement root = XElement.Load("DataInNamespace.xml");  
XNamespace aw = "http://www.adatum.com";  
IEnumerable<decimal> prices =  
    from el in root.Elements(aw + "Data")  
    let price = (decimal)el.Element(aw + "Price")  
    orderby price  
    select price;  
foreach (decimal el in prices)  
    Console.WriteLine(el);  
```  
  
 <span data-ttu-id="391ce-111">このコードを実行すると、次の出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="391ce-111">This code produces the following output:</span></span>  
  
```  
0.99  
4.95  
6.99  
24.50  
29.00  
66.00  
89.99  
```  
  
## <a name="see-also"></a><span data-ttu-id="391ce-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="391ce-112">See also</span></span>

- [<span data-ttu-id="391ce-113">データの並べ替え (C#)</span><span class="sxs-lookup"><span data-stu-id="391ce-113">Sorting Data (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/sorting-data.md)
- [<span data-ttu-id="391ce-114">基本的なクエリ (LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="391ce-114">Basic Queries (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/basic-queries-linq-to-xml.md)
