---
title: '&#39;カスタム&#39;修飾子は、明示的なデリゲート型なしで宣言されたイベントでは無効です'
ms.date: 07/20/2015
f1_keywords:
- vbc31122
- bc31122
helpviewer_keywords:
- BC31122
ms.assetid: 6911f0d1-641a-473b-906d-8ee5681194be
ms.openlocfilehash: c909973ef1c00cb01179b0e5527dfecd6f41e577
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574782"
---
# <a name="39custom39-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types"></a><span data-ttu-id="74d8d-102">&#39;カスタム&#39;修飾子は、明示的なデリゲート型なしで宣言されたイベントでは無効です</span><span class="sxs-lookup"><span data-stu-id="74d8d-102">&#39;Custom&#39; modifier is not valid on events declared without explicit delegate types</span></span>
<span data-ttu-id="74d8d-103">非カスタム イベントとは異なり、`Custom Event`宣言が必要です、`As`句は次のイベント名を明示的にイベントのデリゲート型を指定します。</span><span class="sxs-lookup"><span data-stu-id="74d8d-103">Unlike a non-custom event, a `Custom Event` declaration requires an `As` clause following the event name that explicitly specifies the delegate type for the event.</span></span>  
  
 <span data-ttu-id="74d8d-104">非カスタム イベントは、いずれかで定義されている、`As`句と明示的なデリゲート型、またはすぐにパラメーターを持つリスト次のイベント名。</span><span class="sxs-lookup"><span data-stu-id="74d8d-104">Non-custom events can be defined either with an `As` clause and an explicit delegate type, or with a parameter list immediately following the event name.</span></span>  
  
 <span data-ttu-id="74d8d-105">**エラー ID:** BC31122</span><span class="sxs-lookup"><span data-stu-id="74d8d-105">**Error ID:** BC31122</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="74d8d-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="74d8d-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="74d8d-107">カスタム イベントと同じパラメーター リストを持つデリゲートを定義します。</span><span class="sxs-lookup"><span data-stu-id="74d8d-107">Define a delegate with the same parameter list as the custom event.</span></span>  
  
     <span data-ttu-id="74d8d-108">たとえば場合、`Custom Event`で定義された`Custom Event Test(ByVal sender As Object, ByVal i As Integer)`、対応するデリゲートは、次になります。</span><span class="sxs-lookup"><span data-stu-id="74d8d-108">For example, if the `Custom Event` was defined by `Custom Event Test(ByVal sender As Object, ByVal i As Integer)`, then the corresponding delegate would be the following.</span></span>  
  
     [!code-vb[VbVbalrEventError#18](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types_1.vb)]  
  
2.  <span data-ttu-id="74d8d-109">カスタム イベントのパラメーターのリストを置き換える、`As`デリゲート型を指定する句。</span><span class="sxs-lookup"><span data-stu-id="74d8d-109">Replace the parameter list of the custom event with an `As` clause specifying the delegate type.</span></span>  
  
     <span data-ttu-id="74d8d-110">先ほどの例では、`Custom Event`宣言を次のように書き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="74d8d-110">Continuing with the example, `Custom Event` declaration would be rewritten as follows.</span></span>  
  
     [!code-vb[VbVbalrEventError#19](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types_2.vb)]  
  
## <a name="example"></a><span data-ttu-id="74d8d-111">例</span><span class="sxs-lookup"><span data-stu-id="74d8d-111">Example</span></span>  
 <span data-ttu-id="74d8d-112">この例で宣言、`Custom Event`し、必要なを指定します`As`デリゲート型を含む句。</span><span class="sxs-lookup"><span data-stu-id="74d8d-112">This example declares a `Custom Event` and specifies the required `As` clause with a delegate type.</span></span>  
  
 [!code-vb[VbVbalrEventError#2](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types_3.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="74d8d-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="74d8d-113">See also</span></span>
- [<span data-ttu-id="74d8d-114">Event ステートメント</span><span class="sxs-lookup"><span data-stu-id="74d8d-114">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)
- [<span data-ttu-id="74d8d-115">Delegate ステートメント</span><span class="sxs-lookup"><span data-stu-id="74d8d-115">Delegate Statement</span></span>](../../../visual-basic/language-reference/statements/delegate-statement.md)
- [<span data-ttu-id="74d8d-116">イベント</span><span class="sxs-lookup"><span data-stu-id="74d8d-116">Events</span></span>](../../../visual-basic/programming-guide/language-features/events/index.md)
