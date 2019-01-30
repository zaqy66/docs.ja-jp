---
title: "'Custom' 修飾子は、明示的なデリゲート型なしで宣言されたイベントでは無効です。"
ms.date: 07/20/2015
f1_keywords:
- vbc31122
- bc31122
helpviewer_keywords:
- BC31122
ms.assetid: 6911f0d1-641a-473b-906d-8ee5681194be
ms.openlocfilehash: c1b57ccdaa9e04c837ecf7572bc164683a934b2d
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55273518"
---
# <a name="custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types"></a><span data-ttu-id="86fc7-102">'Custom' 修飾子は、明示的なデリゲート型なしで宣言されたイベントでは無効です。</span><span class="sxs-lookup"><span data-stu-id="86fc7-102">'Custom' modifier is not valid on events declared without explicit delegate types</span></span>
<span data-ttu-id="86fc7-103">非カスタム イベントとは異なり、`Custom Event`宣言が必要です、`As`句は次のイベント名を明示的にイベントのデリゲート型を指定します。</span><span class="sxs-lookup"><span data-stu-id="86fc7-103">Unlike a non-custom event, a `Custom Event` declaration requires an `As` clause following the event name that explicitly specifies the delegate type for the event.</span></span>  
  
 <span data-ttu-id="86fc7-104">非カスタム イベントは、いずれかで定義されている、`As`句と明示的なデリゲート型、またはすぐにパラメーターを持つリスト次のイベント名。</span><span class="sxs-lookup"><span data-stu-id="86fc7-104">Non-custom events can be defined either with an `As` clause and an explicit delegate type, or with a parameter list immediately following the event name.</span></span>  
  
 <span data-ttu-id="86fc7-105">**エラー ID:** BC31122</span><span class="sxs-lookup"><span data-stu-id="86fc7-105">**Error ID:** BC31122</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="86fc7-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="86fc7-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="86fc7-107">カスタム イベントと同じパラメーター リストを持つデリゲートを定義します。</span><span class="sxs-lookup"><span data-stu-id="86fc7-107">Define a delegate with the same parameter list as the custom event.</span></span>  
  
     <span data-ttu-id="86fc7-108">たとえば場合、`Custom Event`で定義された`Custom Event Test(ByVal sender As Object, ByVal i As Integer)`、対応するデリゲートは、次になります。</span><span class="sxs-lookup"><span data-stu-id="86fc7-108">For example, if the `Custom Event` was defined by `Custom Event Test(ByVal sender As Object, ByVal i As Integer)`, then the corresponding delegate would be the following.</span></span>  
  
     [!code-vb[VbVbalrEventError#18](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types_1.vb)]  
  
2.  <span data-ttu-id="86fc7-109">カスタム イベントのパラメーターのリストを置き換える、`As`デリゲート型を指定する句。</span><span class="sxs-lookup"><span data-stu-id="86fc7-109">Replace the parameter list of the custom event with an `As` clause specifying the delegate type.</span></span>  
  
     <span data-ttu-id="86fc7-110">先ほどの例では、`Custom Event`宣言を次のように書き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="86fc7-110">Continuing with the example, `Custom Event` declaration would be rewritten as follows.</span></span>  
  
     [!code-vb[VbVbalrEventError#19](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types_2.vb)]  
  
## <a name="example"></a><span data-ttu-id="86fc7-111">例</span><span class="sxs-lookup"><span data-stu-id="86fc7-111">Example</span></span>  
 <span data-ttu-id="86fc7-112">この例で宣言、`Custom Event`し、必要なを指定します`As`デリゲート型を含む句。</span><span class="sxs-lookup"><span data-stu-id="86fc7-112">This example declares a `Custom Event` and specifies the required `As` clause with a delegate type.</span></span>  
  
 [!code-vb[VbVbalrEventError#2](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types_3.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="86fc7-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="86fc7-113">See also</span></span>
- [<span data-ttu-id="86fc7-114">Event ステートメント</span><span class="sxs-lookup"><span data-stu-id="86fc7-114">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)
- [<span data-ttu-id="86fc7-115">Delegate ステートメント</span><span class="sxs-lookup"><span data-stu-id="86fc7-115">Delegate Statement</span></span>](../../../visual-basic/language-reference/statements/delegate-statement.md)
- [<span data-ttu-id="86fc7-116">イベント</span><span class="sxs-lookup"><span data-stu-id="86fc7-116">Events</span></span>](../../../visual-basic/programming-guide/language-features/events/index.md)
