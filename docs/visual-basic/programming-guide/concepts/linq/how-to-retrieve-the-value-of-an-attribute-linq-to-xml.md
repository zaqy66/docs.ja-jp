---
title: '方法: 属性 (LINQ to XML) の値を取得 (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: 5f4b3790-c83f-4eb3-a889-e3587edf3ca1
ms.openlocfilehash: ab14072317bf963e87534b743e3c5a6c39ee39c8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54690723"
---
# <a name="how-to-retrieve-the-value-of-an-attribute-linq-to-xml-visual-basic"></a>方法: 属性 (LINQ to XML) の値を取得 (Visual Basic)
このトピックでは、属性の値を取得する方法について説明します。 2 つの主な方法はあります。キャストすることができます、<xref:System.Xml.Linq.XAttribute>目的の型を明示的な変換演算子の内容を変換、要素または属性を指定した型にします。 もう 1 つは、<xref:System.Xml.Linq.XAttribute.Value%2A> プロパティを使用する方法です。 ただし、通常はキャストがより適切な方法です。 属性を NULL 値が許容される型にキャストすると、存在が不明確な属性の値を取得する場合にコードをより簡単に記述できます。 この手法の例については、次を参照してください。[方法。要素 (LINQ to XML) の値を取得 (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-retrieve-the-value-of-an-element-linq-to-xml.md)します。  
  
## <a name="example"></a>例  
 Visual Basic では、統合属性プロパティを使用して属性の値を取得できます。  
  
```vb  
Dim root As XElement = <Root Attr="abcde"/>  
Console.WriteLine(root)  
Dim str As String = root.@Attr  
Console.WriteLine(str)  
```  
  
 この例を実行すると、次の出力が生成されます。  
  
```xml  
<Root Attr="abcde" />  
abcde  
```  
  
## <a name="example"></a>例  
 Visual Basic では、統合属性プロパティを使用して属性の値を設定できます。 また、統合属性プロパティを使用して存在しない属性の値を設定すると、その属性が作成されます。  
  
```vb  
Dim root As XElement = <Root Att1="content"/>  
root.@Att1 = "new content"  
root.@Att2 = "new attribute"  
Console.WriteLine(root)  
```  
  
 この例を実行すると、次の出力が生成されます。  
  
```xml  
<Root Att1="new content" Att2="new attribute" />  
```  
  
## <a name="example"></a>例  
 属性が名前空間内にある場合にその属性の値を取得する方法を次の例に示します。 詳細については、次を参照してください。 [XML 名前空間 (Visual Basic) の使用](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md)します。  
  
```vb  
Imports <xmlns:aw="http://www.adventure-works.com">  
  
Module Module1  
    Sub Main()  
        Dim root As XElement = <aw:Root aw:Attr="abcde"/>  
        Dim str As String = root.@aw:Attr  
        Console.WriteLine(str)  
    End Sub  
End Module  
```  
  
 この例を実行すると、次の出力が生成されます。  
  
```  
abcde  
```  
  
## <a name="see-also"></a>関連項目
- [LINQ to XML 軸 (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-axes.md)
