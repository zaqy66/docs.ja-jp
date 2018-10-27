---
title: '方法 : Visual Basic で文字列を文字の配列に変換する'
ms.date: 07/20/2015
helpviewer_keywords:
- character arrays [Visual Basic], converting strings
- arrays [Visual Basic], converting strings to
- examples [Visual Basic], string conversion
- strings [Visual Basic], converting to arrays
- string conversion [Visual Basic], arrays
ms.assetid: 1b54b686-ab29-413b-adce-6bd5422376eb
ms.openlocfilehash: cc12b70cddcb93a72b4421a8ddd93542ef84f55b
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/26/2018
ms.locfileid: "50041155"
---
# <a name="how-to-convert-a-string-to-an-array-of-characters-in-visual-basic"></a><span data-ttu-id="bfc1e-102">方法 : Visual Basic で文字列を文字の配列に変換する</span><span class="sxs-lookup"><span data-stu-id="bfc1e-102">How to: Convert a String to an Array of Characters in Visual Basic</span></span>
<span data-ttu-id="bfc1e-103">場合によっては文字、文字列および文字列を解析する際など、文字列内の文字の位置に関するデータを使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="bfc1e-103">Sometimes it is useful to have data about the characters in your string and the positions of those characters within your string, such as when you are parsing a string.</span></span> <span data-ttu-id="bfc1e-104">この例を呼び出して、文字列の文字列で文字の配列を取得する方法を示しています。<xref:System.String.ToCharArray%2A>メソッド。</span><span class="sxs-lookup"><span data-stu-id="bfc1e-104">This example shows how you can get an array of the characters in a string by calling the string's <xref:System.String.ToCharArray%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bfc1e-105">例</span><span class="sxs-lookup"><span data-stu-id="bfc1e-105">Example</span></span>  
 <span data-ttu-id="bfc1e-106">文字列を分割する方法を示します、`Char`に文字列を分割する方法と、配列、 `String` Unicode テキスト文字の配列。</span><span class="sxs-lookup"><span data-stu-id="bfc1e-106">This example demonstrates how to split a string into a `Char` array, and how to split a string into a `String` array of its Unicode text characters.</span></span> <span data-ttu-id="bfc1e-107">この違いの理由は 2 つ以上の Unicode テキスト文字で構成されること`Char`文字 (サロゲート ペアや組み合わせ文字のシーケンス)。</span><span class="sxs-lookup"><span data-stu-id="bfc1e-107">The reason for this distinction is that Unicode text characters can be composed of two or more `Char` characters (such as a surrogate pair or a combining character sequence).</span></span> <span data-ttu-id="bfc1e-108">詳細については、次を参照してください。<xref:System.Globalization.TextElementEnumerator>と[Unicode 標準](https://www.unicode.org/standard/standard.html)します。</span><span class="sxs-lookup"><span data-stu-id="bfc1e-108">For more information, see <xref:System.Globalization.TextElementEnumerator> and [The Unicode Standard](https://www.unicode.org/standard/standard.html).</span></span>  
  
 [!code-vb[VbVbalrStrings#75](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-convert-a-string-to-an-array-of-characters_1.vb)]  
  
## <a name="example"></a><span data-ttu-id="bfc1e-109">例</span><span class="sxs-lookup"><span data-stu-id="bfc1e-109">Example</span></span>  
 <span data-ttu-id="bfc1e-110">Unicode テキスト文字、文字列を分割することが難しくなりますが、これは、文字列の視覚的表現についての情報が必要な場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="bfc1e-110">It is more difficult to split a string into its Unicode text characters, but this is necessary if you need information about the visual representation of a string.</span></span> <span data-ttu-id="bfc1e-111">この例では、<xref:System.Globalization.StringInfo.SubstringByTextElements%2A>文字列を構成する Unicode 文字に関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="bfc1e-111">This example uses the <xref:System.Globalization.StringInfo.SubstringByTextElements%2A> method to get information about the Unicode text characters that make up a string.</span></span>  
  
 [!code-vb[VbVbalrStrings#76](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-convert-a-string-to-an-array-of-characters_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="bfc1e-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="bfc1e-112">See Also</span></span>  
 <xref:System.String.Chars%2A>  
 <xref:System.Globalization.StringInfo?displayProperty=nameWithType>  
 [<span data-ttu-id="bfc1e-113">方法 : 文字列の文字にアクセスする</span><span class="sxs-lookup"><span data-stu-id="bfc1e-113">How to: Access Characters in Strings</span></span>](../../../../visual-basic/programming-guide/language-features/strings/how-to-access-characters-in-strings.md)  
 [<span data-ttu-id="bfc1e-114">Visual Basic で、文字列型とその他のデータ型との変換を行う</span><span class="sxs-lookup"><span data-stu-id="bfc1e-114">Converting Between Strings and Other Data Types in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/converting-between-strings-and-other-data-types.md)  
 [<span data-ttu-id="bfc1e-115">文字列</span><span class="sxs-lookup"><span data-stu-id="bfc1e-115">Strings</span></span>](../../../../visual-basic/programming-guide/language-features/strings/index.md)
