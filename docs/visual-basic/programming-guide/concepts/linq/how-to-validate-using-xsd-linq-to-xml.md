---
title: '方法: XSD (LINQ to XML) を使用して検証 (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: a0fe88d4-4e77-49e7-90de-8953feeccc21
ms.openlocfilehash: 9e4250ac1da4b25ce3f1644b38ff0e71693ecc57
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54691217"
---
# <a name="how-to-validate-using-xsd-linq-to-xml-visual-basic"></a><span data-ttu-id="46940-102">方法: XSD (LINQ to XML) を使用して検証 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="46940-102">How to: Validate Using XSD (LINQ to XML) (Visual Basic)</span></span>
<span data-ttu-id="46940-103"><xref:System.Xml.Schema> 名前空間には、XML スキーマ定義言語 (XSD) ファイルに対して XML ツリーを簡単に検証できる拡張メソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="46940-103">The <xref:System.Xml.Schema> namespace contains extension methods that make it easy to validate an XML tree against an XML Schema Definition Language (XSD) file.</span></span> <span data-ttu-id="46940-104">詳細については、<xref:System.Xml.Schema.Extensions.Validate%2A> メソッドのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="46940-104">For more information, see the <xref:System.Xml.Schema.Extensions.Validate%2A> method documentation.</span></span>  
  
## <a name="example"></a><span data-ttu-id="46940-105">例</span><span class="sxs-lookup"><span data-stu-id="46940-105">Example</span></span>  
 <span data-ttu-id="46940-106">次の例では、<xref:System.Xml.Schema.XmlSchemaSet> を作成し、このスキーマ セットに対して 2 つの <xref:System.Xml.Linq.XDocument> オブジェクトを検証します。</span><span class="sxs-lookup"><span data-stu-id="46940-106">The following example creates an <xref:System.Xml.Schema.XmlSchemaSet>, then validates two <xref:System.Xml.Linq.XDocument> objects against the schema set.</span></span> <span data-ttu-id="46940-107">ドキュメントの 1 つは有効ですが、その他のドキュメントは無効です。</span><span class="sxs-lookup"><span data-stu-id="46940-107">One of the documents is valid, the other is not.</span></span>  
  
```vb  
Dim errors As Boolean = False  
  
Private Sub XSDErrors(ByVal o As Object, ByVal e As ValidationEventArgs)  
    Console.WriteLine("{0}", e.Message)  
    errors = True  
End Sub  
  
Sub Main()  
    Dim xsdMarkup As XElement = _  
        <xsd:schema xmlns:xsd='http://www.w3.org/2001/XMLSchema'>  
            <xsd:element name='Root'>  
                <xsd:complexType>  
                    <xsd:sequence>  
                        <xsd:element name='Child1' minOccurs='1' maxOccurs='1'/>  
                        <xsd:element name='Child2' minOccurs='1' maxOccurs='1'/>  
                    </xsd:sequence>  
                </xsd:complexType>  
            </xsd:element>  
        </xsd:schema>  
    Dim schemas As XmlSchemaSet = New XmlSchemaSet()  
    schemas.Add("", xsdMarkup.CreateReader)  
  
    Dim doc1 As XDocument = _  
        <?xml version='1.0'?>  
        <Root>  
            <Child1>content1</Child1>  
            <Child2>content1</Child2>  
        </Root>  
  
    Dim doc2 As XDocument = _  
        <?xml version='1.0'?>  
        <Root>  
            <Child1>content1</Child1>  
            <Child3>content1</Child3>  
        </Root>  
  
    Console.WriteLine("Validating doc1")  
    errors = False  
    doc1.Validate(schemas, AddressOf XSDErrors)  
    Console.WriteLine("doc1 {0}", IIf(errors = True, "did not validate", "validated"))  
  
    Console.WriteLine()  
    Console.WriteLine("Validating doc2")  
    errors = False  
    doc2.Validate(schemas, AddressOf XSDErrors)  
    Console.WriteLine("doc2 {0}", IIf(errors = True, "did not validate", "validated"))  
End Sub  
```  
  
 <span data-ttu-id="46940-108">この例を実行すると、次の出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="46940-108">This example produces the following output:</span></span>  
  
```  
Validating doc1  
doc1 validated  
  
Validating doc2  
The element 'Root' has invalid child element 'Child3'. List of possible elements expected: 'Child2'.  
doc2 did not validate  
```  
  
## <a name="example"></a><span data-ttu-id="46940-109">例</span><span class="sxs-lookup"><span data-stu-id="46940-109">Example</span></span>  
 <span data-ttu-id="46940-110">次の例は、XML ドキュメントからのことを検証[サンプル XML ファイル。顧客と注文 (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-customers-and-orders-linq-to-xml.md)がスキーマに従った有効[サンプル XSD ファイル。顧客と注文](../../../../visual-basic/programming-guide/concepts/linq/sample-xsd-file-customers-and-orders.md)します。</span><span class="sxs-lookup"><span data-stu-id="46940-110">The following example validates that the XML document from [Sample XML File: Customers and Orders (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-customers-and-orders-linq-to-xml.md) is valid per the schema from [Sample XSD File: Customers and Orders](../../../../visual-basic/programming-guide/concepts/linq/sample-xsd-file-customers-and-orders.md).</span></span> <span data-ttu-id="46940-111">次に、ソース XML ドキュメントを変更します。</span><span class="sxs-lookup"><span data-stu-id="46940-111">It then modifies the source XML document.</span></span> <span data-ttu-id="46940-112">変更するのは最初の顧客の `CustomerID` 属性です。</span><span class="sxs-lookup"><span data-stu-id="46940-112">It changes the `CustomerID` attribute on the first customer.</span></span> <span data-ttu-id="46940-113">変更が完了すると、存在しない顧客を注文が参照するようになります。したがって、この XML ドキュメントは有効ではなくなります。</span><span class="sxs-lookup"><span data-stu-id="46940-113">After the change, orders will then refer to a customer that does not exist, so the XML document will no longer validate.</span></span>  
  
 <span data-ttu-id="46940-114">この例では、次の XML ドキュメントを使用します。[サンプル XML ファイル:顧客と注文 (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-customers-and-orders-linq-to-xml.md)します。</span><span class="sxs-lookup"><span data-stu-id="46940-114">This example uses the following XML document: [Sample XML File: Customers and Orders (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-customers-and-orders-linq-to-xml.md).</span></span>  
  
 <span data-ttu-id="46940-115">この例では、次の XSD スキーマを使用します。[サンプル XSD ファイル:顧客と注文](../../../../visual-basic/programming-guide/concepts/linq/sample-xsd-file-customers-and-orders.md)します。</span><span class="sxs-lookup"><span data-stu-id="46940-115">This example uses the following XSD schema: [Sample XSD File: Customers and Orders](../../../../visual-basic/programming-guide/concepts/linq/sample-xsd-file-customers-and-orders.md).</span></span>  
  
```vb  
Dim errors As Boolean = False  
  
Private Sub XSDErrors(ByVal o As Object, ByVal e As ValidationEventArgs)  
    Console.WriteLine("{0}", e.Message)  
    errors = True  
End Sub  
  
Sub Main()  
    Dim schemas As XmlSchemaSet = New XmlSchemaSet()  
    schemas.Add("", "CustomersOrders.xsd")  
  
    Console.WriteLine("Attempting to validate")  
    Dim custOrdDoc As XDocument = XDocument.Load("CustomersOrders.xml")  
    errors = False  
    custOrdDoc.Validate(schemas, AddressOf XSDErrors)  
    Console.WriteLine("custOrdDoc {0}", IIf(errors, "did not validate", "validated"))  
  
    Console.WriteLine()  
    ' Modify the source document so that it will not validate.  
    custOrdDoc.<Root>.<Orders>.<Order>.<CustomerID>(0).Value = "AAAAA"  
    Console.WriteLine("Attempting to validate after modification")  
    errors = False  
    custOrdDoc.Validate(schemas, AddressOf XSDErrors)  
    Console.WriteLine("custOrdDoc {0}", IIf(errors, "did not validate", "validated"))  
End Sub  
```  
  
 <span data-ttu-id="46940-116">この例を実行すると、次の出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="46940-116">This example produces the following output:</span></span>  
  
```  
Attempting to validate  
custOrdDoc validated  
  
Attempting to validate after modification  
The key sequence 'AAAAA' in Keyref fails to refer to some key.  
custOrdDoc did not validate  
```  
  
## <a name="see-also"></a><span data-ttu-id="46940-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="46940-117">See also</span></span>
- <xref:System.Xml.Schema.Extensions.Validate%2A>
- [<span data-ttu-id="46940-118">XML ツリー (Visual Basic) の作成</span><span class="sxs-lookup"><span data-stu-id="46940-118">Creating XML Trees (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/creating-xml-trees.md)
