---
title: '方法: グループ化を使用して階層を作成する (C#)'
ms.date: 07/20/2015
ms.assetid: 0213d59e-5f76-438c-9cab-4bf11f7b971d
ms.openlocfilehash: 8fa384ced04a90002f8f721266f163c874d6e0ff
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2018
ms.locfileid: "45649693"
---
# <a name="how-to-create-hierarchy-using-grouping-c"></a><span data-ttu-id="7b460-102">方法: グループ化を使用して階層を作成する (C#)</span><span class="sxs-lookup"><span data-stu-id="7b460-102">How to: Create Hierarchy Using Grouping (C#)</span></span>
<span data-ttu-id="7b460-103">この例では、データをグループ化し、そのグループ化に基づいて XML を生成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7b460-103">This example shows how to group data, and then generate XML based on the grouping.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7b460-104">例</span><span class="sxs-lookup"><span data-stu-id="7b460-104">Example</span></span>  
 <span data-ttu-id="7b460-105">この例では、まずデータをカテゴリごとにグループ化し、次にグループ化を反映した XML 階層を含む新しい XML ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="7b460-105">This example first groups data by a category, then generates a new XML file in which the XML hierarchy reflects the grouping.</span></span>  
  
 <span data-ttu-id="7b460-106">この例では、「[サンプル XML ファイル: 数値データ (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-linq-to-xml.md)」の XML ドキュメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="7b460-106">This example uses the following XML document: [Sample XML File: Numerical Data (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-linq-to-xml.md).</span></span>  
  
```csharp  
XElement doc = XElement.Load("Data.xml");  
var newData =  
    new XElement("Root",  
        from data in doc.Elements("Data")  
        group data by (string)data.Element("Category") into groupedData  
        select new XElement("Group",  
            new XAttribute("ID", groupedData.Key),  
            from g in groupedData  
            select new XElement("Data",  
                g.Element("Quantity"),  
                g.Element("Price")  
            )  
        )  
    );  
Console.WriteLine(newData);  
```  
  
 <span data-ttu-id="7b460-107">この例を実行すると、次の出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="7b460-107">This example produces the following output:</span></span>  
  
```xml  
<Root>  
  <Group ID="A">  
    <Data>  
      <Quantity>3</Quantity>  
      <Price>24.50</Price>  
    </Data>  
    <Data>  
      <Quantity>5</Quantity>  
      <Price>4.95</Price>  
    </Data>  
    <Data>  
      <Quantity>3</Quantity>  
      <Price>66.00</Price>  
    </Data>  
    <Data>  
      <Quantity>15</Quantity>  
      <Price>29.00</Price>  
    </Data>  
  </Group>  
  <Group ID="B">  
    <Data>  
      <Quantity>1</Quantity>  
      <Price>89.99</Price>  
    </Data>  
    <Data>  
      <Quantity>10</Quantity>  
      <Price>.99</Price>  
    </Data>  
    <Data>  
      <Quantity>8</Quantity>  
      <Price>6.99</Price>  
    </Data>  
  </Group>  
</Root>  
```  
  
## <a name="see-also"></a><span data-ttu-id="7b460-108">参照</span><span class="sxs-lookup"><span data-stu-id="7b460-108">See Also</span></span>

- [<span data-ttu-id="7b460-109">高度なクエリ手法 (LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="7b460-109">Advanced Query Techniques (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/advanced-query-techniques-linq-to-xml.md)
