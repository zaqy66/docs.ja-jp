---
title: 先頭&#39;します。&#39;または&#39;!&#39;内でのみ表示できます、&#39;で&#39;ステートメント
ms.date: 07/20/2015
f1_keywords:
- vbc30157
- bc30157
helpviewer_keywords:
- BC30157
ms.assetid: 70daaee1-14f9-45b7-9f30-53794310b95e
ms.openlocfilehash: e64318d4ececbd887f55a1a202cc2d58c90c8fc7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54625953"
---
# <a name="leading-3939-or-3939-can-only-appear-inside-a-39with39-statement"></a><span data-ttu-id="97b84-102">先頭&#39;します。&#39;または&#39;!&#39;内でのみ表示できます、&#39;で&#39;ステートメント</span><span class="sxs-lookup"><span data-stu-id="97b84-102">Leading &#39;.&#39; or &#39;!&#39; can only appear inside a &#39;With&#39; statement</span></span>
<span data-ttu-id="97b84-103">ピリオド (.) または感嘆符 (!) でない内部、`With`左の式がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="97b84-103">A period (.) or exclamation point (!) that is not inside a `With` block occurs without an expression on the left.</span></span> <span data-ttu-id="97b84-104">メンバー アクセス (`.`) およびディクショナリ メンバー アクセス (`!`) メンバーを含む要素を指定する式が必要です。</span><span class="sxs-lookup"><span data-stu-id="97b84-104">Member access (`.`) and dictionary member access (`!`) require an expression specifying the element that contains the member.</span></span> <span data-ttu-id="97b84-105">これは、アクセサーのまたはのターゲットとしての左側にすぐに表示する必要があります、`With`メンバー アクセスを含むブロックします。</span><span class="sxs-lookup"><span data-stu-id="97b84-105">This must appear immediately to the left of the accessor or as the target of a `With` block containing the member access.</span></span>  
  
 <span data-ttu-id="97b84-106">**エラー ID:** BC30157</span><span class="sxs-lookup"><span data-stu-id="97b84-106">**Error ID:** BC30157</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="97b84-107">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="97b84-107">To correct this error</span></span>  
  
1.  <span data-ttu-id="97b84-108">いることを確認、`With`ブロックが正しく書式設定します。</span><span class="sxs-lookup"><span data-stu-id="97b84-108">Ensure that the `With` block is correctly formatted.</span></span>  
  
2.  <span data-ttu-id="97b84-109">存在する場合ありません`With`ブロック、メンバーを含む定義の要素に評価されるアクセサーの左側に式を追加します。</span><span class="sxs-lookup"><span data-stu-id="97b84-109">If there is no `With` block, add an expression to the left of the accessor that evaluates to a defined element containing the member.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="97b84-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="97b84-110">See also</span></span>
- [<span data-ttu-id="97b84-111">コード内の特殊文字</span><span class="sxs-lookup"><span data-stu-id="97b84-111">Special Characters in Code</span></span>](../../../visual-basic/programming-guide/program-structure/special-characters-in-code.md)
- [<span data-ttu-id="97b84-112">With...End With ステートメント</span><span class="sxs-lookup"><span data-stu-id="97b84-112">With...End With Statement</span></span>](../../../visual-basic/language-reference/statements/with-end-with-statement.md)
