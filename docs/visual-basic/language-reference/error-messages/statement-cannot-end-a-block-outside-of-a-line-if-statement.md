---
title: ステートメント行の外部でブロックを終了することはできません&#39;場合&#39;ステートメント
ms.date: 07/20/2015
f1_keywords:
- vbc32005
- bc32005
helpviewer_keywords:
- BC32005
ms.assetid: 4039f51b-e0ee-4789-a89b-45d06de06b5d
ms.openlocfilehash: 78fe136acbd09e202b1daeb16dd540cf42ada390
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574717"
---
# <a name="statement-cannot-end-a-block-outside-of-a-line-39if39-statement"></a><span data-ttu-id="9e007-102">ステートメント行の外部でブロックを終了することはできません&#39;場合&#39;ステートメント</span><span class="sxs-lookup"><span data-stu-id="9e007-102">Statement cannot end a block outside of a line &#39;If&#39; statement</span></span>
<span data-ttu-id="9e007-103">単一行`If`ステートメントには、コロン (:) のうちの 1 つで区切られた複数のステートメントが含まれています、`End`単一行の外側のコントロール ブロックのステートメント`If`します。</span><span class="sxs-lookup"><span data-stu-id="9e007-103">A single-line `If` statement contains several statements separated by colons (:), one of which is an `End` statement for a control block outside the single-line `If`.</span></span> <span data-ttu-id="9e007-104">単一行`If`ステートメントは使用しないでください、`End If`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="9e007-104">Single-line `If` statements do not use the `End If` statement.</span></span>  
  
 <span data-ttu-id="9e007-105">**エラー ID:** BC32005</span><span class="sxs-lookup"><span data-stu-id="9e007-105">**Error ID:** BC32005</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="9e007-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="9e007-106">To correct this error</span></span>  
  
-   <span data-ttu-id="9e007-107">単一行を移動`If`ステートメントを含むコントロール ブロックの外側、`End If`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="9e007-107">Move the single-line `If` statement outside the control block that contains the `End If` statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9e007-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="9e007-108">See also</span></span>
- [<span data-ttu-id="9e007-109">If...Then...Else ステートメント</span><span class="sxs-lookup"><span data-stu-id="9e007-109">If...Then...Else Statement</span></span>](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
