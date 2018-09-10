---
title: 'サンプル XML ファイル: 名前空間内の数値データ 3'
ms.date: 07/20/2015
ms.assetid: 51750cab-3c66-4511-90fb-b9d211308d31
ms.openlocfilehash: 114657087a0aee69bc9be298025eac58923294b0
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2018
ms.locfileid: "44185611"
---
# <a name="sample-xml-file-numerical-data-in-a-namespace"></a>サンプル XML ファイル : 名前空間内の数値データ
次の XML ファイルは、[!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] ドキュメントのさまざまな例で使用されます。 このファイルには、集計、平均、およびグループ化用の数値データが含まれています。 XML は名前空間に含まれています。  
  
## <a name="data"></a>データ  
  
```xml  
<Root xmlns='http://www.adatum.com'>  
  <TaxRate>7.25</TaxRate>  
  <Data>  
    <Category>A</Category>  
    <Quantity>3</Quantity>  
    <Price>24.50</Price>  
  </Data>  
  <Data>  
    <Category>B</Category>  
    <Quantity>1</Quantity>  
    <Price>89.99</Price>  
  </Data>  
  <Data>  
    <Category>A</Category>  
    <Quantity>5</Quantity>  
    <Price>4.95</Price>  
  </Data>  
  <Data>  
    <Category>A</Category>  
    <Quantity>3</Quantity>  
    <Price>66.00</Price>  
  </Data>  
  <Data>  
    <Category>B</Category>  
    <Quantity>10</Quantity>  
    <Price>.99</Price>  
  </Data>  
  <Data>  
    <Category>A</Category>  
    <Quantity>15</Quantity>  
    <Price>29.00</Price>  
  </Data>  
  <Data>  
    <Category>B</Category>  
    <Quantity>8</Quantity>  
    <Price>6.99</Price>  
  </Data>  
</Root>  
```  
  
## <a name="see-also"></a>参照

- [サンプル XML ドキュメント (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-documents-linq-to-xml.md)
