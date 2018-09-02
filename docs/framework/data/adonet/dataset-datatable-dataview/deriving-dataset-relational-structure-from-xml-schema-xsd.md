---
title: XML スキーマ (XSD) からの DataSet リレーショナル構造の派生
ms.date: 03/30/2017
ms.assetid: 8f6cd04d-6197-4bc4-9096-8c51c7e4acae
ms.openlocfilehash: fd5c41272d3b050427804f08f7387328012065f4
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43417205"
---
# <a name="deriving-dataset-relational-structure-from-xml-schema-xsd"></a><span data-ttu-id="0b77c-102">XML スキーマ (XSD) からの DataSet リレーショナル構造の派生</span><span class="sxs-lookup"><span data-stu-id="0b77c-102">Deriving DataSet Relational Structure from XML Schema (XSD)</span></span>
<span data-ttu-id="0b77c-103">ここでは、XML スキーマ定義言語 (XSD) スキーマ ドキュメントから `DataSet` のリレーショナル スキーマを生成する方法についての概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="0b77c-103">This section provides an overview of how the relational schema of a `DataSet` is built from an XML Schema definition language (XSD) schema document.</span></span> <span data-ttu-id="0b77c-104">一般の各`complexType`スキーマ要素の子要素で、テーブルが生成、`DataSet`します。</span><span class="sxs-lookup"><span data-stu-id="0b77c-104">In general, for each `complexType` child element of a schema element, a table is generated in the `DataSet`.</span></span> <span data-ttu-id="0b77c-105">テーブル構造は、複合型の定義に基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="0b77c-105">The table structure is determined by the definition of the complex type.</span></span> <span data-ttu-id="0b77c-106">作成されるテーブル、`DataSet`のスキーマの最上位の要素。</span><span class="sxs-lookup"><span data-stu-id="0b77c-106">Tables are created in the `DataSet` for top-level elements in the schema.</span></span> <span data-ttu-id="0b77c-107">ただし、テーブルを最上位レベルの作成のみ`complexType`要素と、`complexType`要素が別の内部で入れ子になった`complexType`を要素は、入れ子になった場合`complexType`要素にマップされます、`DataTable`内、`DataSet`します。</span><span class="sxs-lookup"><span data-stu-id="0b77c-107">However, a table is only created for a top-level `complexType` element when the `complexType` element is nested inside another `complexType` element, in which case the nested `complexType` element is mapped to a `DataTable` within the `DataSet`.</span></span>  
  
 <span data-ttu-id="0b77c-108">について、XSD の詳細については、World Wide Web Consortium (W3C) XML Schema Part 0: Primer Recommendation、XML スキーマのパート 1: Structures Recommendation、および、XML Schema Part 2: Datatypes Recommendation 』 にある[ http://www.w3.org/](http://www.w3.org/TR/).</span><span class="sxs-lookup"><span data-stu-id="0b77c-108">For more information about the XSD, see the World Wide Web Consortium (W3C) XML Schema Part 0: Primer Recommendation, the XML Schema Part 1: Structures Recommendation, and the XML Schema Part 2: Datatypes Recommendation, located at [http://www.w3.org/](http://www.w3.org/TR/).</span></span>  
  
 <span data-ttu-id="0b77c-109">次の例では、XML スキーマ、`customers`の子要素です、`MyDataSet`要素、**データセット**要素。</span><span class="sxs-lookup"><span data-stu-id="0b77c-109">The following example demonstrates an XML Schema where `customers` is the child element of the `MyDataSet` element, which is a **DataSet** element.</span></span>  
  
```xml  
<xs:schema id="SomeID"   
            xmlns=""   
            xmlns:xs="http://www.w3.org/2001/XMLSchema"   
            xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">  
   <xs:element name="MyDataSet" msdata:IsDataSet="true">  
     <xs:complexType>  
       <xs:choice maxOccurs="unbounded">  
         <xs:element name="customers" >   
           <xs:complexType >  
             <xs:sequence>  
               <xs:element name="CustomerID" type="xs:integer"   
                            minOccurs="0" />  
               <xs:element name="CompanyName" type="xs:string"   
                            minOccurs="0" />  
               <xs:element name="Phone" type="xs:string" />  
             </xs:sequence>  
           </xs:complexType>  
          </xs:element>  
       </xs:choice>  
     </xs:complexType>  
   </xs:element>  
 </xs:schema>  
```  
  
 <span data-ttu-id="0b77c-110">上記の例では、`customers` 要素は複合型の要素です。</span><span class="sxs-lookup"><span data-stu-id="0b77c-110">In the preceding example, the element `customers` is a complex type element.</span></span> <span data-ttu-id="0b77c-111">したがって、複合型の定義が解析され、割り当て処理によって次のテーブルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="0b77c-111">Therefore, the complex type definition is parsed, and the mapping process creates the following table.</span></span>  
  
```  
Customers (CustomerID , CompanyName, Phone)  
```  
  
 <span data-ttu-id="0b77c-112">テーブルの各列のデータ型は、それに対応する指定された要素または属性の XML スキーマ型から派生します。</span><span class="sxs-lookup"><span data-stu-id="0b77c-112">The data type of each column in the table is derived from the XML Schema type of the corresponding element or attribute specified.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0b77c-113">場合、要素`customers`などの単純な XML スキーマ データ型は**整数**テーブルは生成されません。</span><span class="sxs-lookup"><span data-stu-id="0b77c-113">If the element `customers` is of a simple XML Schema data type such as **integer**, no table is generated.</span></span> <span data-ttu-id="0b77c-114">テーブルが作成されるのは、複合型のトップレベル要素に対してだけです。</span><span class="sxs-lookup"><span data-stu-id="0b77c-114">Tables are only created for the top-level elements that are complex types.</span></span>  
  
 <span data-ttu-id="0b77c-115">次の XML スキーマで、**スキーマ**要素が 2 つの要素の子`InStateCustomers`と`OutOfStateCustomers`します。</span><span class="sxs-lookup"><span data-stu-id="0b77c-115">In the following XML Schema, the **Schema** element has two element children, `InStateCustomers` and `OutOfStateCustomers`.</span></span>  
  
```xml  
<xs:schema id="SomeID"   
            xmlns=""   
            xmlns:xs="http://www.w3.org/2001/XMLSchema"   
            xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">  
   <xs:element name="InStateCustomers" type="customerType" />  
   <xs:element name="OutOfStateCustomers" type="customerType" />  
    <xs:complexType name="customerType" >  
  
     </xs:complexType>  
  
   <xs:element name="MyDataSet" msdata:IsDataSet="true">  
     <xs:complexType>  
       <xs:choice maxOccurs="unbounded">  
         <xs:element ref="customers" />  
       </xs:choice>  
     </xs:complexType>  
   </xs:element>  
 </xs:schema>  
```  
  
 <span data-ttu-id="0b77c-116">`InStateCustomers` と `OutOfStateCustomers` の 2 つの子要素は、複合型の要素です (`customerType`)。</span><span class="sxs-lookup"><span data-stu-id="0b77c-116">Both the `InStateCustomers` and the `OutOfStateCustomers` child elements are complex type elements (`customerType`).</span></span> <span data-ttu-id="0b77c-117">したがって、マッピング プロセスを生成で次の 2 つの同一テーブル、`DataSet`します。</span><span class="sxs-lookup"><span data-stu-id="0b77c-117">Therefore, the mapping process generates the following two identical tables in the `DataSet`.</span></span>  
  
```  
InStateCustomers (CustomerID , CompanyName, Phone)  
OutOfStateCustomers (CustomerID , CompanyName, Phone)  
```  
  
## <a name="in-this-section"></a><span data-ttu-id="0b77c-118">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="0b77c-118">In This Section</span></span>  
 [<span data-ttu-id="0b77c-119">XML スキーマ (XSD) 制約の DataSet 制約への割り当て</span><span class="sxs-lookup"><span data-stu-id="0b77c-119">Mapping XML Schema (XSD) Constraints to DataSet Constraints</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/mapping-xml-schema-xsd-constraints-to-dataset-constraints.md)  
 <span data-ttu-id="0b77c-120">一意であり、外部キー制約を作成するために使用する XML スキーマの要素について説明します、`DataSet`します。</span><span class="sxs-lookup"><span data-stu-id="0b77c-120">Describes the XML Schema elements used to create unique and foreign key constraints in a `DataSet`.</span></span>  
  
 [<span data-ttu-id="0b77c-121">XML スキーマ (XSD) からの DataSet リレーションの生成</span><span class="sxs-lookup"><span data-stu-id="0b77c-121">Generating DataSet Relations from XML Schema (XSD)</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/generating-dataset-relations-from-xml-schema-xsd.md)  
 <span data-ttu-id="0b77c-122">テーブルの列間のリレーションを作成するために使用する XML スキーマの要素について説明します、`DataSet`します。</span><span class="sxs-lookup"><span data-stu-id="0b77c-122">Describes the XML Schema elements used to create relations between table columns in a `DataSet`.</span></span>  
  
 [<span data-ttu-id="0b77c-123">XML スキーマ制約およびリレーションシップ</span><span class="sxs-lookup"><span data-stu-id="0b77c-123">XML Schema Constraints and Relationships</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/xml-schema-constraints-and-relationships.md)  
 <span data-ttu-id="0b77c-124">XML スキーマの要素を使用して制約を作成するときに、リレーションは暗黙的に作成される方法について説明します、`DataSet`します。</span><span class="sxs-lookup"><span data-stu-id="0b77c-124">Describes how relations are created implicitly when using XML Schema elements to create constraints in a `DataSet`.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="0b77c-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="0b77c-125">Related Sections</span></span>  
 [<span data-ttu-id="0b77c-126">DataSet での XML の使用</span><span class="sxs-lookup"><span data-stu-id="0b77c-126">Using XML in a DataSet</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)  
 <span data-ttu-id="0b77c-127">読み込んで、リレーショナル構造とデータを永続化する方法について説明します、 `DataSet` XML データとして。</span><span class="sxs-lookup"><span data-stu-id="0b77c-127">Describes how to load and persist the relational structure and data in a `DataSet` as XML data.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b77c-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="0b77c-128">See Also</span></span>  
 [<span data-ttu-id="0b77c-129">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="0b77c-129">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
