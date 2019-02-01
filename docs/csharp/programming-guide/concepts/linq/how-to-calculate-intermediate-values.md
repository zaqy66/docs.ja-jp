---
title: '方法: 中間値を計算する (C#)'
ms.date: 07/20/2015
ms.assetid: 7fd3001f-f8f9-4bce-879f-d4c7af8a04fe
ms.openlocfilehash: 12c8a87114859ce7b47b8206acb454cdc2838470
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54604329"
---
# <a name="how-to-calculate-intermediate-values-c"></a><span data-ttu-id="346e4-102">方法: 中間値を計算する (C#)</span><span class="sxs-lookup"><span data-stu-id="346e4-102">How to: Calculate Intermediate Values (C#)</span></span>
<span data-ttu-id="346e4-103">この例では、並べ替え、フィルタリング、および選択を実行する際に使用できる中間値を計算する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="346e4-103">This example shows how to calculate intermediate values that can be used in sorting, filtering, and selecting.</span></span>  
  
## <a name="example"></a><span data-ttu-id="346e4-104">例</span><span class="sxs-lookup"><span data-stu-id="346e4-104">Example</span></span>  
 <span data-ttu-id="346e4-105">次の例では、`Let` 句を使用します。</span><span class="sxs-lookup"><span data-stu-id="346e4-105">The following example uses the `Let` clause.</span></span>  
  
 <span data-ttu-id="346e4-106">この例では、XML ドキュメント、[サンプル XML ファイル: 数値データ (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-linq-to-xml.md) を使用します。</span><span class="sxs-lookup"><span data-stu-id="346e4-106">This example uses the following XML document: [Sample XML File: Numerical Data (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-linq-to-xml.md).</span></span>  
  
```csharp  
XElement root = XElement.Load("Data.xml");  
IEnumerable<decimal> extensions =  
    from el in root.Elements("Data")  
    let extension = (decimal)el.Element("Quantity") * (decimal)el.Element("Price")  
    where extension >= 25  
    orderby extension  
    select extension;  
foreach (decimal ex in extensions)  
    Console.WriteLine(ex);  
```  
  
 <span data-ttu-id="346e4-107">このコードを実行すると、次の出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="346e4-107">This code produces the following output:</span></span>  
  
```  
55.92  
73.50  
89.99  
198.00  
435.00  
```  
  
## <a name="example"></a><span data-ttu-id="346e4-108">例</span><span class="sxs-lookup"><span data-stu-id="346e4-108">Example</span></span>  
 <span data-ttu-id="346e4-109">次の例は名前空間に含まれている XML 用のクエリです。これらのクエリは上の例と同じ機能を表しています。</span><span class="sxs-lookup"><span data-stu-id="346e4-109">The following example shows the same query for XML that is in a namespace.</span></span> <span data-ttu-id="346e4-110">詳細については、「[XML 名前空間の使用 (C#)](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="346e4-110">For more information, see [Working with XML Namespaces (C#)](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span></span>  
  
 <span data-ttu-id="346e4-111">この例では、XML ドキュメント、[サンプル XML ファイル: 名前空間内の数値データ](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-in-a-namespace.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="346e4-111">This example uses the following XML document: [Sample XML File: Numerical Data in a Namespace](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-in-a-namespace.md).</span></span>  
  
```csharp  
XElement root = XElement.Load("DataInNamespace.xml");  
XNamespace ad = "http://www.adatum.com";  
IEnumerable<decimal> extensions =  
    from el in root.Elements(ad + "Data")  
    let extension = (decimal)el.Element(ad + "Quantity") * (decimal)el.Element(ad + "Price")  
    where extension >= 25  
    orderby extension  
    select extension;  
foreach (decimal ex in extensions)  
    Console.WriteLine(ex);  
```  
  
 <span data-ttu-id="346e4-112">このコードを実行すると、次の出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="346e4-112">This code produces the following output:</span></span>  
  
```  
55.92  
73.50  
89.99  
198.00  
435.00  
```  
  
## <a name="see-also"></a><span data-ttu-id="346e4-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="346e4-113">See also</span></span>

- [<span data-ttu-id="346e4-114">基本的なクエリ (LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="346e4-114">Basic Queries (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/basic-queries-linq-to-xml.md)
