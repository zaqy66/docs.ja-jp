---
title: "	'#Else' の前には、対応する '#If' または '#ElseIf' が必要です。"
ms.date: 07/20/2015
f1_keywords:
- vbc30014
- bc30014
helpviewer_keywords:
- BC30014
ms.assetid: 5215585e-2efa-485a-9efe-9833a1cc83a0
ms.openlocfilehash: d6fa76b2aba45e3455cef6ceafc0f737ef56225d
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271552"
---
# <a name="elseif-must-be-preceded-by-a-matching-if-or-elseif"></a><span data-ttu-id="9bdac-102">	'#Else' の前には、対応する '#If' または '#ElseIf' が必要です。</span><span class="sxs-lookup"><span data-stu-id="9bdac-102">'#ElseIf' must be preceded by a matching '#If' or '#ElseIf'</span></span>
<span data-ttu-id="9bdac-103">`#ElseIf` は条件付きコンパイル ディレクティブです。</span><span class="sxs-lookup"><span data-stu-id="9bdac-103">`#ElseIf` is a conditional compilation directive.</span></span> <span data-ttu-id="9bdac-104">`#ElseIf`句の前に、対応する`#If`または`#ElseIf`句が必要です。</span><span class="sxs-lookup"><span data-stu-id="9bdac-104">An `#ElseIf` clause must be preceded by a matching `#If` or `#ElseIf` clause.</span></span>  
  
 <span data-ttu-id="9bdac-105">**エラー ID:** BC30014</span><span class="sxs-lookup"><span data-stu-id="9bdac-105">**Error ID:** BC30014</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="9bdac-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="9bdac-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="9bdac-107">先行する`#If`または`#ElseIf`と、この`#ElseIf`とが、間に条件付きコンパイル ブロックを挿入することによって分離されていないこと、または`#End If`句を間違った場所に記述したために分離されていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="9bdac-107">Check that a preceding `#If` or `#ElseIf` has not been separated from this `#ElseIf` by an intervening conditional compilation block or an incorrectly placed `#End If`.</span></span>  
  
2.  <span data-ttu-id="9bdac-108">`#ElseIf`の前に`#Else`ディレクティブがある場合は、その`#Else`を削除するか、`#ElseIf`に変更します。</span><span class="sxs-lookup"><span data-stu-id="9bdac-108">If the `#ElseIf` is preceded by a `#Else` directive, either remove the `#Else` or change it to an `#ElseIf`.</span></span>  
  
3.  <span data-ttu-id="9bdac-109">すべて問題ない場合は、条件付きコンパイル ブロックの先頭に `#If` ディレクティブを追加します。</span><span class="sxs-lookup"><span data-stu-id="9bdac-109">If everything else is in order, add an `#If` directive to the beginning of the conditional compilation block.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9bdac-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="9bdac-110">See also</span></span>
- [<span data-ttu-id="9bdac-111">#If...Then...#Else ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="9bdac-111">#If...Then...#Else Directives</span></span>](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
