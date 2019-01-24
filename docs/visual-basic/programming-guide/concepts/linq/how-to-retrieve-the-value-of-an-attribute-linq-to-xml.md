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
# <a name="how-to-retrieve-the-value-of-an-attribute-linq-to-xml-visual-basic"></a><span data-ttu-id="f91d3-102">方法: 属性 (LINQ to XML) の値を取得 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f91d3-102">How to: Retrieve the Value of an Attribute (LINQ to XML) (Visual Basic)</span></span>
<span data-ttu-id="f91d3-103">このトピックでは、属性の値を取得する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f91d3-103">This topic shows how to obtain the value of attributes.</span></span> <span data-ttu-id="f91d3-104">2 つの主な方法はあります。キャストすることができます、<xref:System.Xml.Linq.XAttribute>目的の型を明示的な変換演算子の内容を変換、要素または属性を指定した型にします。</span><span class="sxs-lookup"><span data-stu-id="f91d3-104">There are two main ways: You can cast an <xref:System.Xml.Linq.XAttribute> to the desired type; the explicit conversion operator then converts the contents of the element or attribute to the specified type.</span></span> <span data-ttu-id="f91d3-105">もう 1 つは、<xref:System.Xml.Linq.XAttribute.Value%2A> プロパティを使用する方法です。</span><span class="sxs-lookup"><span data-stu-id="f91d3-105">Alternatively, you can use the <xref:System.Xml.Linq.XAttribute.Value%2A> property.</span></span> <span data-ttu-id="f91d3-106">ただし、通常はキャストがより適切な方法です。</span><span class="sxs-lookup"><span data-stu-id="f91d3-106">However, casting is generally the better approach.</span></span> <span data-ttu-id="f91d3-107">属性を NULL 値が許容される型にキャストすると、存在が不明確な属性の値を取得する場合にコードをより簡単に記述できます。</span><span class="sxs-lookup"><span data-stu-id="f91d3-107">If you cast the attribute to a nullable type, the code is simpler to write when retrieving the value of an attribute that might or might not exist.</span></span> <span data-ttu-id="f91d3-108">この手法の例については、次を参照してください。[方法。要素 (LINQ to XML) の値を取得 (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-retrieve-the-value-of-an-element-linq-to-xml.md)します。</span><span class="sxs-lookup"><span data-stu-id="f91d3-108">For examples of this technique, see [How to: Retrieve the Value of an Element (LINQ to XML) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-retrieve-the-value-of-an-element-linq-to-xml.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="f91d3-109">例</span><span class="sxs-lookup"><span data-stu-id="f91d3-109">Example</span></span>  
 <span data-ttu-id="f91d3-110">Visual Basic では、統合属性プロパティを使用して属性の値を取得できます。</span><span class="sxs-lookup"><span data-stu-id="f91d3-110">In Visual Basic, you can use the integrated attribute property to retrieve the value of an attribute.</span></span>  
  
```vb  
Dim root As XElement = <Root Attr="abcde"/>  
Console.WriteLine(root)  
Dim str As String = root.@Attr  
Console.WriteLine(str)  
```  
  
 <span data-ttu-id="f91d3-111">この例を実行すると、次の出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f91d3-111">This example produces the following output:</span></span>  
  
```xml  
<Root Attr="abcde" />  
abcde  
```  
  
## <a name="example"></a><span data-ttu-id="f91d3-112">例</span><span class="sxs-lookup"><span data-stu-id="f91d3-112">Example</span></span>  
 <span data-ttu-id="f91d3-113">Visual Basic では、統合属性プロパティを使用して属性の値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="f91d3-113">In Visual Basic, you can use the integrated attribute property to set the value of an attribute.</span></span> <span data-ttu-id="f91d3-114">また、統合属性プロパティを使用して存在しない属性の値を設定すると、その属性が作成されます。</span><span class="sxs-lookup"><span data-stu-id="f91d3-114">Further, if you use the integrated attribute property to set the value of an attribute that does not exist, the attribute will be created.</span></span>  
  
```vb  
Dim root As XElement = <Root Att1="content"/>  
root.@Att1 = "new content"  
root.@Att2 = "new attribute"  
Console.WriteLine(root)  
```  
  
 <span data-ttu-id="f91d3-115">この例を実行すると、次の出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f91d3-115">This example produces the following output:</span></span>  
  
```xml  
<Root Att1="new content" Att2="new attribute" />  
```  
  
## <a name="example"></a><span data-ttu-id="f91d3-116">例</span><span class="sxs-lookup"><span data-stu-id="f91d3-116">Example</span></span>  
 <span data-ttu-id="f91d3-117">属性が名前空間内にある場合にその属性の値を取得する方法を次の例に示します。</span><span class="sxs-lookup"><span data-stu-id="f91d3-117">The following example shows how to retrieve the value of an attribute where the attribute is in a namespace.</span></span> <span data-ttu-id="f91d3-118">詳細については、次を参照してください。 [XML 名前空間 (Visual Basic) の使用](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md)します。</span><span class="sxs-lookup"><span data-stu-id="f91d3-118">For more information, see [Working with XML Namespaces (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span></span>  
  
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
  
 <span data-ttu-id="f91d3-119">この例を実行すると、次の出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f91d3-119">This example produces the following output:</span></span>  
  
```  
abcde  
```  
  
## <a name="see-also"></a><span data-ttu-id="f91d3-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="f91d3-120">See also</span></span>
- [<span data-ttu-id="f91d3-121">LINQ to XML 軸 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f91d3-121">LINQ to XML Axes (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-axes.md)
