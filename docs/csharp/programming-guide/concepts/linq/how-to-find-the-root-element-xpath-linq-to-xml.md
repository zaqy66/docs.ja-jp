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
# <a name="how-to-find-the-root-element-xpath-linq-to-xml-c"></a>方法: ルート要素を検索する (XPath-LINQ to XML) (C#)
このトピックでは、XPath および [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] を使用してルート要素を取得する方法について説明します。  
  
 XPath 式を次に示します。  
  
 `/PurchaseOrders`  
  
## <a name="example"></a>例  
 この例では、ルート要素を検索します。  
  
 この例では、次の XML ドキュメントを使用します。[サンプル XML ファイル:複数の購買発注書 (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-multiple-purchase-orders-linq-to-xml.md)。  
  
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
  
 この例を実行すると、次の出力が生成されます。  
  
```  
Results are identical  
PurchaseOrders  
```  
  
## <a name="see-also"></a>関連項目

- [XPath ユーザー向けの LINQ to XML (C#)](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
