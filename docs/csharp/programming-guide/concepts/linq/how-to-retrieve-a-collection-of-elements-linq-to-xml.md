---
title: '方法: 要素のコレクションを取得する (LINQ to XML) (C#)'
ms.date: 07/20/2015
ms.assetid: b849668c-7976-4974-b8e1-1cd587d34258
ms.openlocfilehash: 8d01c0499f031ae22fd6383dd77b36e444704c46
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54675003"
---
# <a name="how-to-retrieve-a-collection-of-elements-linq-to-xml-c"></a><span data-ttu-id="ad269-102">方法: 要素のコレクションを取得する (LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="ad269-102">How to: Retrieve a Collection of Elements (LINQ to XML) (C#)</span></span>
<span data-ttu-id="ad269-103">このトピックでは、<xref:System.Xml.Linq.XContainer.Elements%2A> メソッドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ad269-103">This topic demonstrates the <xref:System.Xml.Linq.XContainer.Elements%2A> method.</span></span> <span data-ttu-id="ad269-104">このメソッドは、要素の子要素のコレクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="ad269-104">This method retrieves a collection of the child elements of an element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ad269-105">例</span><span class="sxs-lookup"><span data-stu-id="ad269-105">Example</span></span>  
 <span data-ttu-id="ad269-106">この例では、`purchaseOrder` 要素の子要素を反復処理します。</span><span class="sxs-lookup"><span data-stu-id="ad269-106">This example iterates through the child elements of the `purchaseOrder` element.</span></span>  
  
 <span data-ttu-id="ad269-107">この例では、XML ドキュメント、[サンプル XML ファイル: 一般的な購買発注書 (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-typical-purchase-order-linq-to-xml-1.md) を使用します。</span><span class="sxs-lookup"><span data-stu-id="ad269-107">This example uses the following XML document: [Sample XML File: Typical Purchase Order (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-typical-purchase-order-linq-to-xml-1.md).</span></span>  
  
```csharp  
XElement po = XElement.Load("PurchaseOrder.xml");  
IEnumerable<XElement> childElements =  
    from el in po.Elements()  
    select el;  
foreach (XElement el in childElements)  
    Console.WriteLine("Name: " + el.Name);  
```  
  
 <span data-ttu-id="ad269-108">この例を実行すると、次の出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="ad269-108">This example produces the following output.</span></span>  
  
```  
Name: Address  
Name: Address  
Name: DeliveryNotes  
Name: Items  
```  
  
## <a name="see-also"></a><span data-ttu-id="ad269-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="ad269-109">See also</span></span>

- [<span data-ttu-id="ad269-110">LINQ to XML 軸 (C#)</span><span class="sxs-lookup"><span data-stu-id="ad269-110">LINQ to XML Axes (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-axes.md)
