---
title: '方法: Visual Basic における文字列の文字をアクセス'
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], accessing characters
- characters [Visual Basic], accessing in strings
ms.assetid: 02c5206c-ffab-494d-b648-3b2ea358dc34
ms.openlocfilehash: 9833b562fc0b4115448ebefb8631f0d73eb15f6f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54618923"
---
# <a name="how-to-access-characters-in-strings-in-visual-basic"></a><span data-ttu-id="7f61b-102">方法: Visual Basic における文字列の文字をアクセス</span><span class="sxs-lookup"><span data-stu-id="7f61b-102">How to: Access Characters in Strings in Visual Basic</span></span>
<span data-ttu-id="7f61b-103">この例では、使用、<xref:System.String.Chars%2A>文字列で指定した場所にある文字にアクセスするプロパティ。</span><span class="sxs-lookup"><span data-stu-id="7f61b-103">This example demonstrates how to use the <xref:System.String.Chars%2A> property to access the character at the specified location in a string.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7f61b-104">例</span><span class="sxs-lookup"><span data-stu-id="7f61b-104">Example</span></span>  
 <span data-ttu-id="7f61b-105">場合によっては文字、文字列と、文字列内の文字の位置に関するデータを使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="7f61b-105">Sometimes it is useful to have data about the characters in your string and the positions of those characters within your string.</span></span> <span data-ttu-id="7f61b-106">文字の配列としての文字列を考えることができます (`Char`インスタンス); を通じてその文字のインデックスを参照することで特定の文字を取得することができます、<xref:System.String.Chars%2A>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="7f61b-106">You can think of a string as an array of characters (`Char` instances); you can retrieve a particular character by referencing the index of that character through the <xref:System.String.Chars%2A> property.</span></span>  
  
 [!code-vb[VbVbalrStrings#49](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-access-characters-in-strings_1.vb)]  
  
 <span data-ttu-id="7f61b-107">`index`のパラメーター、<xref:System.String.Chars%2A>プロパティは 0 から始まります。</span><span class="sxs-lookup"><span data-stu-id="7f61b-107">The `index` parameter of the <xref:System.String.Chars%2A> property is zero-based.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="7f61b-108">信頼性の高いプログラミング</span><span class="sxs-lookup"><span data-stu-id="7f61b-108">Robust Programming</span></span>  
 <span data-ttu-id="7f61b-109"><xref:System.String.Chars%2A>プロパティが指定した位置にある文字を返します。</span><span class="sxs-lookup"><span data-stu-id="7f61b-109">The <xref:System.String.Chars%2A> property returns the character at the specified position.</span></span> <span data-ttu-id="7f61b-110">ただし、Unicode 文字の一部は、1 つ以上の文字で表されます。</span><span class="sxs-lookup"><span data-stu-id="7f61b-110">However, some Unicode characters can be represented by more than one character.</span></span> <span data-ttu-id="7f61b-111">Unicode 文字を使用する方法の詳細については、次を参照してください。[方法。文字列を文字の配列に変換](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-a-string-to-an-array-of-characters.md)します。</span><span class="sxs-lookup"><span data-stu-id="7f61b-111">For more information on how to work with Unicode characters, see [How to: Convert a String to an Array of Characters](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-a-string-to-an-array-of-characters.md).</span></span>  
  
 <span data-ttu-id="7f61b-112"><xref:System.String.Chars%2A>プロパティがスローされます、<xref:System.IndexOutOfRangeException>例外場合、`index`パラメーターは、文字列の長さ以上には 0 より小さい場合、または</span><span class="sxs-lookup"><span data-stu-id="7f61b-112">The <xref:System.String.Chars%2A> property throws an <xref:System.IndexOutOfRangeException> exception if the `index` parameter is greater than or equal to the length of the string, or if it is less than zero</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f61b-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="7f61b-113">See also</span></span>
- <xref:System.String.Chars%2A>
- [<span data-ttu-id="7f61b-114">方法: 文字列を文字の配列に変換します。</span><span class="sxs-lookup"><span data-stu-id="7f61b-114">How to: Convert a String to an Array of Characters</span></span>](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-a-string-to-an-array-of-characters.md)
- [<span data-ttu-id="7f61b-115">Visual Basic で、文字列型とその他のデータ型との変換を行う</span><span class="sxs-lookup"><span data-stu-id="7f61b-115">Converting Between Strings and Other Data Types in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/converting-between-strings-and-other-data-types.md)
- [<span data-ttu-id="7f61b-116">文字列</span><span class="sxs-lookup"><span data-stu-id="7f61b-116">Strings</span></span>](../../../../visual-basic/programming-guide/language-features/strings/index.md)
