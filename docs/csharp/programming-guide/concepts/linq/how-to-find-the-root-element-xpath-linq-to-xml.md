---
title: '方法: ルート要素を検索する (XPath-LINQ to XML) (C#)'
ms.date: 07/20/2015
ms.assetid: 4fd824e0-4d39-429b-b092-f6a5c046ee6c
ms.openlocfilehash: a74556e4b05bc3ae02998eeb6dd3190a3bade36a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54697167"
---
# <a name="how-to-find-the-root-element-xpath-linq-to-xml-c"></a><span data-ttu-id="da3c7-102">方法: ルート要素を検索する (XPath-LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="da3c7-102">How to: Find the Root Element (XPath-LINQ to XML) (C#)</span></span>
<span data-ttu-id="da3c7-103">このトピックでは、XPath および [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] を使用してルート要素を取得する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="da3c7-103">This topic shows how to get the root element with XPath and [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span></span>  
  
 <span data-ttu-id="da3c7-104">XPath 式を次に示します。</span><span class="sxs-lookup"><span data-stu-id="da3c7-104">The XPath expression is:</span></span>  
  
 `/PurchaseOrders`  
  
## <a name="example"></a><span data-ttu-id="da3c7-105">例</span><span class="sxs-lookup"><span data-stu-id="da3c7-105">Example</span></span>  
 <span data-ttu-id="da3c7-106">この例では、ルート要素を検索します。</span><span class="sxs-lookup"><span data-stu-id="da3c7-106">This example finds the root element.</span></span>  
  
 <span data-ttu-id="da3c7-107">この例では、次の XML ドキュメントを使用します。[サンプル XML ファイル:複数の購買発注書 (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-multiple-purchase-orders-linq-to-xml.md)。</span><span class="sxs-lookup"><span data-stu-id="da3c7-107">This example uses the following XML document: [Sample XML File: Multiple Purchase Orders (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-multiple-purchase-orders-linq-to-xml.md).</span></span>  
  
```csharp  
XDocument po = XDocument.Load("PurchaseOrders.xml");  
  
// LINQ to XML query  
XElement el1 = po.Root;  
  
// XPath expression  
XElement el2 = po.XPathSelectElement("/PurchaseOrders");  
  
if (el1 == el2)  
    Console.WriteLine("Results are identical");  
else  
    Console.WriteLine("Results differ");  
Console.WriteLine(el1.Name);  
```  
  
 <span data-ttu-id="da3c7-108">この例を実行すると、次の出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="da3c7-108">This example produces the following output:</span></span>  
  
```  
Results are identical  
PurchaseOrders  
```  
  
## <a name="see-also"></a><span data-ttu-id="da3c7-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="da3c7-109">See also</span></span>

- [<span data-ttu-id="da3c7-110">XPath ユーザー向けの LINQ to XML (C#)</span><span class="sxs-lookup"><span data-stu-id="da3c7-110">LINQ to XML for XPath Users (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
