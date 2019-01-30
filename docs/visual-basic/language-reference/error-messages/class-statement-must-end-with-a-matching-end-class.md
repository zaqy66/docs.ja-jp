---
title: "'Class' ステートメントの終わりには、対応する 'End Class' を指定しなければなりません。"
ms.date: 07/20/2015
f1_keywords:
- vbc30481
- bc30481
helpviewer_keywords:
- BC30481
ms.assetid: 583f3029-bc3a-4e06-866f-92dbecc46f19
ms.openlocfilehash: 572e1d74810aad6d24e6eefc8d37729f5dc950c9
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55286950"
---
# <a name="class-statement-must-end-with-a-matching-end-class"></a><span data-ttu-id="87743-102">'Class' ステートメントの終わりには、対応する 'End Class' を指定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="87743-102">'Class' statement must end with a matching 'End Class'</span></span>
<span data-ttu-id="87743-103">`Class` 開始するために使用、 `Class` block; ために、対応する、ブロックの先頭に記述できますのみ`End Class`ステートメント ブロックを終了します。</span><span class="sxs-lookup"><span data-stu-id="87743-103">`Class` is used to initiate a `Class` block; hence it can only appear at the beginning of the block, with a matching `End Class` statement ending the block.</span></span> <span data-ttu-id="87743-104">冗長ながあるか、`Class`ステートメントは終了しませんが、`Class`ブロックと一緒に`End Class`します。</span><span class="sxs-lookup"><span data-stu-id="87743-104">Either you have a redundant `Class` statement, or you have not ended your `Class` block with `End Class`.</span></span>  
  
 <span data-ttu-id="87743-105">**エラー ID:** BC30481</span><span class="sxs-lookup"><span data-stu-id="87743-105">**Error ID:** BC30481</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="87743-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="87743-106">To correct this error</span></span>  
  
-   <span data-ttu-id="87743-107">不要な `Class` ステートメントを見つけて削除します。</span><span class="sxs-lookup"><span data-stu-id="87743-107">Locate and remove the unnecessary `Class` statement.</span></span>  
  
-   <span data-ttu-id="87743-108">最後に、 `Class` 、対応するブロック`End Class`します。</span><span class="sxs-lookup"><span data-stu-id="87743-108">Conclude the `Class` block with a matching `End Class`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="87743-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="87743-109">See also</span></span>
- [<span data-ttu-id="87743-110">終了\<キーワード > ステートメント</span><span class="sxs-lookup"><span data-stu-id="87743-110">End \<keyword> Statement</span></span>](../../../visual-basic/language-reference/statements/end-keyword-statement.md)
- [<span data-ttu-id="87743-111">Class ステートメント</span><span class="sxs-lookup"><span data-stu-id="87743-111">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)
