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
# <a name="custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types"></a>'Custom' 修飾子は、明示的なデリゲート型なしで宣言されたイベントでは無効です。
非カスタム イベントとは異なり、`Custom Event`宣言が必要です、`As`句は次のイベント名を明示的にイベントのデリゲート型を指定します。  
  
 非カスタム イベントは、いずれかで定義されている、`As`句と明示的なデリゲート型、またはすぐにパラメーターを持つリスト次のイベント名。  
  
 **エラー ID:** BC31122  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  カスタム イベントと同じパラメーター リストを持つデリゲートを定義します。  
  
     たとえば場合、`Custom Event`で定義された`Custom Event Test(ByVal sender As Object, ByVal i As Integer)`、対応するデリゲートは、次になります。  
  
     [!code-vb[VbVbalrEventError#18](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types_1.vb)]  
  
2.  カスタム イベントのパラメーターのリストを置き換える、`As`デリゲート型を指定する句。  
  
     先ほどの例では、`Custom Event`宣言を次のように書き換えることができます。  
  
     [!code-vb[VbVbalrEventError#19](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types_2.vb)]  
  
## <a name="example"></a>例  
 この例で宣言、`Custom Event`し、必要なを指定します`As`デリゲート型を含む句。  
  
 [!code-vb[VbVbalrEventError#2](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types_3.vb)]  
  
## <a name="see-also"></a>関連項目
- [Event ステートメント](../../../visual-basic/language-reference/statements/event-statement.md)
- [Delegate ステートメント](../../../visual-basic/language-reference/statements/delegate-statement.md)
- [イベント](../../../visual-basic/programming-guide/language-features/events/index.md)
