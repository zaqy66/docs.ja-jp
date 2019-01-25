---
title: '方法: 日付または時刻を表す文字列を検証 (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], validating
- String data type [Visual Basic], validation
ms.assetid: ae7d4b29-3436-4032-bdbf-4650eb1c8e19
ms.openlocfilehash: 1a838d9d156ad9c05a70a4d4d72db1a288731c9b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54685400"
---
# <a name="how-to-validate-strings-that-represent-dates-or-times-visual-basic"></a><span data-ttu-id="22d8c-102">方法: 日付または時刻を表す文字列を検証 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="22d8c-102">How to: Validate Strings That Represent Dates or Times (Visual Basic)</span></span>
<span data-ttu-id="22d8c-103">次のコード例のセットを`Boolean`文字列が有効な日付または時刻を表すかどうかを示す値です。</span><span class="sxs-lookup"><span data-stu-id="22d8c-103">The following code example sets a `Boolean` value that indicates whether a string represents a valid date or time.</span></span>  
  
## <a name="example"></a><span data-ttu-id="22d8c-104">例</span><span class="sxs-lookup"><span data-stu-id="22d8c-104">Example</span></span>  
 [!code-vb[VbVbcnRegEx#2](../../../../visual-basic/programming-guide/language-features/strings/codesnippet/VisualBasic/how-to-validate-strings-that-represent-dates-or-times_1.vb)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="22d8c-105">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="22d8c-105">Compiling the Code</span></span>  
 <span data-ttu-id="22d8c-106">置換`("01/01/03")`と`"9:30 PM"`日付と時刻に検証したいとします。</span><span class="sxs-lookup"><span data-stu-id="22d8c-106">Replace `("01/01/03")` and `"9:30 PM"` with the date and time you want to validate.</span></span> <span data-ttu-id="22d8c-107">文字列を別のハード コーディングされた文字列を置き換えることができます、`String`など、文字列を返す変数、またはメソッドで`InputBox`します。</span><span class="sxs-lookup"><span data-stu-id="22d8c-107">You can replace the string with another hard-coded string, with a `String` variable, or with a method that returns a string, such as `InputBox`.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="22d8c-108">信頼性の高いプログラミング</span><span class="sxs-lookup"><span data-stu-id="22d8c-108">Robust Programming</span></span>  
 <span data-ttu-id="22d8c-109">このメソッドに変換する前に、文字列の検証を使用して、`String`を`DateTime`変数。</span><span class="sxs-lookup"><span data-stu-id="22d8c-109">Use this method to validate the string before trying to convert the `String` to a `DateTime` variable.</span></span> <span data-ttu-id="22d8c-110">最初の日付または時刻をチェックする場合は、実行時に例外を生成を回避できます。</span><span class="sxs-lookup"><span data-stu-id="22d8c-110">By checking the date or time first, you can avoid generating an exception at run time.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22d8c-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="22d8c-111">See also</span></span>
- <xref:Microsoft.VisualBasic.Information.IsDate%2A>
- <xref:Microsoft.VisualBasic.Interaction.InputBox%2A>
- [<span data-ttu-id="22d8c-112">Visual Basic における文字列の検証</span><span class="sxs-lookup"><span data-stu-id="22d8c-112">Validating Strings in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/validating-strings.md)
