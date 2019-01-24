---
title: '&#39;クラス&#39;、対応するステートメントの終わりにする必要があります&#39;End クラス&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30481
- bc30481
helpviewer_keywords:
- BC30481
ms.assetid: 583f3029-bc3a-4e06-866f-92dbecc46f19
ms.openlocfilehash: 4e80ce58048bfa7f2fecc65e7167479df07bf57c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54715089"
---
# <a name="39class39-statement-must-end-with-a-matching-39end-class39"></a><span data-ttu-id="f99e0-102">&#39;クラス&#39;、対応するステートメントの終わりにする必要があります&#39;End クラス&#39;</span><span class="sxs-lookup"><span data-stu-id="f99e0-102">&#39;Class&#39; statement must end with a matching &#39;End Class&#39;</span></span>
<span data-ttu-id="f99e0-103">`Class` 開始するために使用、 `Class` block; ために、対応する、ブロックの先頭に記述できますのみ`End Class`ステートメント ブロックを終了します。</span><span class="sxs-lookup"><span data-stu-id="f99e0-103">`Class` is used to initiate a `Class` block; hence it can only appear at the beginning of the block, with a matching `End Class` statement ending the block.</span></span> <span data-ttu-id="f99e0-104">冗長ながあるか、`Class`ステートメントは終了しませんが、`Class`ブロックと一緒に`End Class`します。</span><span class="sxs-lookup"><span data-stu-id="f99e0-104">Either you have a redundant `Class` statement, or you have not ended your `Class` block with `End Class`.</span></span>  
  
 <span data-ttu-id="f99e0-105">**エラー ID:** BC30481</span><span class="sxs-lookup"><span data-stu-id="f99e0-105">**Error ID:** BC30481</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f99e0-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="f99e0-106">To correct this error</span></span>  
  
-   <span data-ttu-id="f99e0-107">不要な `Class` ステートメントを見つけて削除します。</span><span class="sxs-lookup"><span data-stu-id="f99e0-107">Locate and remove the unnecessary `Class` statement.</span></span>  
  
-   <span data-ttu-id="f99e0-108">最後に、 `Class` 、対応するブロック`End Class`します。</span><span class="sxs-lookup"><span data-stu-id="f99e0-108">Conclude the `Class` block with a matching `End Class`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f99e0-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="f99e0-109">See also</span></span>
- [<span data-ttu-id="f99e0-110">終了\<キーワード > ステートメント</span><span class="sxs-lookup"><span data-stu-id="f99e0-110">End \<keyword> Statement</span></span>](../../../visual-basic/language-reference/statements/end-keyword-statement.md)
- [<span data-ttu-id="f99e0-111">Class ステートメント</span><span class="sxs-lookup"><span data-stu-id="f99e0-111">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)
