---
title: XML リテラルでの空白文字 (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- white space [XML in Visual Basic]
- XML literals [Visual Basic], white space
ms.assetid: dfe3a9ff-d69a-418e-a6b5-476f4ed84219
ms.openlocfilehash: 56466856bc70f4bde428f7087efdf4e71a50021f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54689147"
---
# <a name="white-space-in-xml-literals-visual-basic"></a><span data-ttu-id="32549-102">XML リテラルでの空白文字 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="32549-102">White Space in XML Literals (Visual Basic)</span></span>
<span data-ttu-id="32549-103">作成時に、Visual Basic コンパイラは XML リテラルの有意の空白文字だけが組み込まれて、[!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)]オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="32549-103">The Visual Basic compiler incorporates only the significant white space characters from an XML literal when it creates a [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] object.</span></span> <span data-ttu-id="32549-104">余分な空白文字は組み込まれません。</span><span class="sxs-lookup"><span data-stu-id="32549-104">The insignificant white space characters are not incorporated.</span></span>  
  
## <a name="significant-and-insignificant-white-space"></a><span data-ttu-id="32549-105">有意の空白文字</span><span class="sxs-lookup"><span data-stu-id="32549-105">Significant and Insignificant White Space</span></span>  
 <span data-ttu-id="32549-106">XML リテラルの空白文字は、のみの 3 つの領域には重要です。</span><span class="sxs-lookup"><span data-stu-id="32549-106">White space characters in XML literals are significant in only three areas:</span></span>  
  
-   <span data-ttu-id="32549-107">属性値に含まれる場合。</span><span class="sxs-lookup"><span data-stu-id="32549-107">When they are in an attribute value.</span></span>  
  
-   <span data-ttu-id="32549-108">要素のテキスト コンテンツの一部であるし、テキストには、その他の文字も含まれています。</span><span class="sxs-lookup"><span data-stu-id="32549-108">When they are part of an element's text content and the text also contains other characters.</span></span>  
  
-   <span data-ttu-id="32549-109">要素のテキスト コンテンツの埋め込み式に含まれる場合。</span><span class="sxs-lookup"><span data-stu-id="32549-109">When they are in an embedded expression for an element's text content.</span></span>  
  
 <span data-ttu-id="32549-110">それ以外の場合、コンパイラとして意味のない空白文字を処理しでは、含まれません、[!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)]リテラルのオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="32549-110">Otherwise, the compiler treats white space characters as insignificant and does not include then in the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] object for the literal.</span></span>  
  
 <span data-ttu-id="32549-111">余分な空白を XML リテラルに含めるには、文字列リテラルの空白を含む埋め込み式を使用します。</span><span class="sxs-lookup"><span data-stu-id="32549-111">To include insignificant white space in an XML literal, use an embedded expression that contains a string literal with the white space.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="32549-112">場合、 `xml:space` XML 要素リテラルの属性が表示されたら、Visual Basic コンパイラにはで属性が含まれています、<xref:System.Xml.Linq.XElement>オブジェクトが、この属性は、コンパイラによる空白の処理方法を変更していないを追加します。</span><span class="sxs-lookup"><span data-stu-id="32549-112">If the `xml:space` attribute appears in an XML element literal, the Visual Basic compiler includes the attribute in the <xref:System.Xml.Linq.XElement> object, but adding this attribute does not change how the compiler treats white space.</span></span>  
  
## <a name="examples"></a><span data-ttu-id="32549-113">使用例</span><span class="sxs-lookup"><span data-stu-id="32549-113">Examples</span></span>  
 <span data-ttu-id="32549-114">次の例には、外部と内部の 2 つの XML 要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="32549-114">The following example contains two XML elements, outer and inner.</span></span> <span data-ttu-id="32549-115">両方の要素には、そのテキスト コンテンツ内の空白が含まれます。</span><span class="sxs-lookup"><span data-stu-id="32549-115">Both elements contain white space in their text content.</span></span> <span data-ttu-id="32549-116">空白と XML 要素のみが含まれているため、外側の要素内の空白は意味はありません。</span><span class="sxs-lookup"><span data-stu-id="32549-116">The white space in the outer element is insignificant because it contains only white space and an XML element.</span></span> <span data-ttu-id="32549-117">空白文字とテキストが含まれているために、内部の要素内の空白は重要です。</span><span class="sxs-lookup"><span data-stu-id="32549-117">The white space in the inner element is significant because it contains white space and text.</span></span>  
  
 [!code-vb[VbXMLSamples#29](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/white-space-in-xml-literals_1.vb)]  
  
 <span data-ttu-id="32549-118">実行すると、このコードは、次のテキストを表示します。</span><span class="sxs-lookup"><span data-stu-id="32549-118">When run, this code displays the following text.</span></span>  
  
```xml  
<outer>  
  <inner>  
                                          Inner text  
                                      </inner>  
</outer>  
```  
  
## <a name="see-also"></a><span data-ttu-id="32549-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="32549-119">See also</span></span>
- [<span data-ttu-id="32549-120">Visual Basic での XML の作成</span><span class="sxs-lookup"><span data-stu-id="32549-120">Creating XML in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
