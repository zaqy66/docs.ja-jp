---
title: '方法: Visual Basic では、StringBuilder を使用して文字列を作成します。'
ms.date: 07/20/2015
helpviewer_keywords:
- StringBuilder class
- strings [Visual Basic], using StringBuilder
ms.assetid: 9c042880-aa16-432e-9ccb-cd00abda9ae3
ms.openlocfilehash: 84f0f41cf8ee23466d47dae3b1068c3bc5334072
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54528447"
---
# <a name="how-to-create-strings-using-a-stringbuilder-in-visual-basic"></a><span data-ttu-id="6b69b-102">方法: Visual Basic では、StringBuilder を使用して文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="6b69b-102">How to: Create Strings Using a StringBuilder in Visual Basic</span></span>
<span data-ttu-id="6b69b-103">この例を使用して多数の小さな文字列から長い文字列を構築します、<xref:System.Text.StringBuilder>クラス。</span><span class="sxs-lookup"><span data-stu-id="6b69b-103">This example constructs a long string from many smaller strings using the <xref:System.Text.StringBuilder> class.</span></span> <span data-ttu-id="6b69b-104"><xref:System.Text.StringBuilder>クラスより効率的、`&=`演算子の多くの文字列を連結します。</span><span class="sxs-lookup"><span data-stu-id="6b69b-104">The <xref:System.Text.StringBuilder> class is more efficient than the `&=` operator for concatenating many strings.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6b69b-105">例</span><span class="sxs-lookup"><span data-stu-id="6b69b-105">Example</span></span>  
 <span data-ttu-id="6b69b-106">次の例のインスタンスを作成する、<xref:System.Text.StringBuilder>クラス、1,000 の文字列をそのインスタンスに追加し、その文字列表現を返します。</span><span class="sxs-lookup"><span data-stu-id="6b69b-106">The following example creates an instance of the <xref:System.Text.StringBuilder> class, appends 1,000 strings to that instance, and then returns its string representation.</span></span>  
  
 [!code-vb[VbVbalrStrings#70](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-create-strings-using-a-stringbuilder_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="6b69b-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b69b-107">See also</span></span>
- [<span data-ttu-id="6b69b-108">StringBuilder クラスの使用</span><span class="sxs-lookup"><span data-stu-id="6b69b-108">Using the StringBuilder Class</span></span>](../../../../standard/base-types/stringbuilder.md)
- [<span data-ttu-id="6b69b-109">& = 演算子</span><span class="sxs-lookup"><span data-stu-id="6b69b-109">&= Operator</span></span>](../../../../visual-basic/language-reference/operators/and-assignment-operator.md)
- [<span data-ttu-id="6b69b-110">文字列</span><span class="sxs-lookup"><span data-stu-id="6b69b-110">Strings</span></span>](../../../../visual-basic/programming-guide/language-features/strings/index.md)
- [<span data-ttu-id="6b69b-111">新しい文字列の作成</span><span class="sxs-lookup"><span data-stu-id="6b69b-111">Creating New Strings</span></span>](../../../../standard/base-types/creating-new.md)
- [<span data-ttu-id="6b69b-112">文字列の操作</span><span class="sxs-lookup"><span data-stu-id="6b69b-112">Manipulating Strings</span></span>](../../../../standard/base-types/manipulating-strings.md)
- <span data-ttu-id="6b69b-113">[文字列のサンプル](https://msdn.microsoft.com/library/be9e82a3-dc95-4aaa-9396-61b66e467e02(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="6b69b-113">[Strings Sample](https://msdn.microsoft.com/library/be9e82a3-dc95-4aaa-9396-61b66e467e02(v=vs.100))</span></span>
