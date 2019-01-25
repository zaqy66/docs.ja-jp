---
title: 構造体&#39; &lt;structurename&gt; &#39;に少なくとも 1 つのインスタンス メンバー変数またはマークされていない少なくとも 1 つのインスタンス イベント宣言を含める必要があります&#39;カスタム&#39;
ms.date: 07/20/2015
f1_keywords:
- bc30941
- vbc30941
helpviewer_keywords:
- BC30941
ms.assetid: 7054cc1e-bac3-4c3d-82f3-35772bd8dd3b
ms.openlocfilehash: d8c654c212a459d40c6cf20cd62c3e0fcda8511b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54603782"
---
# <a name="structure-39ltstructurenamegt39-must-contain-at-least-one-instance-member-variable-or-at-least-one-instance-event-declaration-not-marked-39custom39"></a><span data-ttu-id="3191b-102">構造体&#39; &lt;structurename&gt; &#39;に少なくとも 1 つのインスタンス メンバー変数またはマークされていない少なくとも 1 つのインスタンス イベント宣言を含める必要があります&#39;カスタム&#39;</span><span class="sxs-lookup"><span data-stu-id="3191b-102">Structure &#39;&lt;structurename&gt;&#39; must contain at least one instance member variable or at least one instance event declaration not marked &#39;Custom&#39;</span></span>
<span data-ttu-id="3191b-103">構造体の定義は、すべての非共有変数または非共有の非カスタム イベントには含まれません。</span><span class="sxs-lookup"><span data-stu-id="3191b-103">A structure definition does not include any nonshared variables or nonshared noncustom events.</span></span>  
  
 <span data-ttu-id="3191b-104">すべての構造体を変数またはイベントをまとめて、すべてのインスタンスに (共有) の代わりに特定のインスタンスに適用されますが適用される場合があります ([Shared](../../../visual-basic/language-reference/modifiers/shared.md))。</span><span class="sxs-lookup"><span data-stu-id="3191b-104">Every structure must have either a variable or an event that applies to each specific instance (nonshared) instead of to all instances collectively ([Shared](../../../visual-basic/language-reference/modifiers/shared.md)).</span></span> <span data-ttu-id="3191b-105">非共有の定数、プロパティ、およびプロシージャは、この要件を満たしていません。</span><span class="sxs-lookup"><span data-stu-id="3191b-105">Nonshared constants, properties, and procedures do not satisfy this requirement.</span></span> <span data-ttu-id="3191b-106">さらに、非共有変数がなく、1 つだけの非共有イベントがある場合は、そのイベントすることはできません、`Custom`イベント。</span><span class="sxs-lookup"><span data-stu-id="3191b-106">In addition, if there are no nonshared variables and only one nonshared event, that event cannot be a `Custom` event.</span></span>  
  
 <span data-ttu-id="3191b-107">**エラー ID:** BC30941</span><span class="sxs-lookup"><span data-stu-id="3191b-107">**Error ID:** BC30941</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="3191b-108">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="3191b-108">To correct this error</span></span>  
  
-   <span data-ttu-id="3191b-109">少なくとも 1 つの変数またはイベントでない定義`Shared`します。</span><span class="sxs-lookup"><span data-stu-id="3191b-109">Define at least one variable or event that is not `Shared`.</span></span> <span data-ttu-id="3191b-110">1 つのみのイベントを定義する場合は、カスタムではないと非共有があります。</span><span class="sxs-lookup"><span data-stu-id="3191b-110">If you define only one event, it must be noncustom as well as nonshared.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3191b-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="3191b-111">See also</span></span>
- [<span data-ttu-id="3191b-112">構造体</span><span class="sxs-lookup"><span data-stu-id="3191b-112">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="3191b-113">方法: 構造体を宣言する</span><span class="sxs-lookup"><span data-stu-id="3191b-113">How to: Declare a Structure</span></span>](../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
- [<span data-ttu-id="3191b-114">Structure ステートメント</span><span class="sxs-lookup"><span data-stu-id="3191b-114">Structure Statement</span></span>](../../../visual-basic/language-reference/statements/structure-statement.md)
