---
title: Exit ステートメント (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Exit
helpviewer_keywords:
- execution [Visual Basic], ending
- files [Visual Basic], closing
- programs [Visual Basic], quitting
- code, exiting
- Exit statement [Visual Basic]
- program termination
- execution [Visual Basic], stopping
ms.assetid: 760bfb32-5c3f-4bdb-a432-9a6001c92db7
ms.openlocfilehash: 63bcc5d5205681917ba30bdb73bc496307a6322a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672514"
---
# <a name="exit-statement-visual-basic"></a>Exit ステートメント (Visual Basic)
プロシージャまたはブロックを終了し、プロシージャの呼び出しまたはブロックの定義を次のステートメントに直ちに制御を転送します。  
  
## <a name="syntax"></a>構文  
  
```  
Exit { Do | For | Function | Property | Select | Sub | Try | While }  
```  
  
## <a name="statements"></a>ステートメント  
 `Exit Do`  
 すぐに終了させる、`Do`ループが表示されます。 ステートメントに次の実行が続行されます、`Loop`ステートメント。 `Exit Do` 内部でのみ使用できます、`Do`ループします。 使用すると内で入れ子になった`Do`ループ、`Exit Do`最も内側のループを終了し、入れ子の上位のレベルに制御を転送します。  
  
 `Exit For`  
 すぐに終了させる、`For`ループが表示されます。 ステートメントに次の実行が続行されます、`Next`ステートメント。 `Exit For` 内部でのみ使用できます、 `For`.`Next`または`For Each`.`Next`ループします。 使用すると内で入れ子になった`For`ループ、`Exit For`最も内側のループを終了し、入れ子の上位のレベルに制御を転送します。  
  
 `Exit Function`  
 すぐに終了させる、`Function`プロシージャが表示されます。 呼び出したステートメントの次のステートメントと実行が継続、`Function`プロシージャ。 `Exit Function` 内部でのみ使用できます、`Function`プロシージャ。  
  
 戻り値を指定するには前に、の行に関数名に値を割り当てることができます、`Exit Function`ステートメント。 戻り値を代入を 1 つのステートメント内の関数の終了は、代わりに使える、 [Return ステートメント](../../../visual-basic/language-reference/statements/return-statement.md)します。  
  
 `Exit Property`  
 すぐに終了させる、`Property`プロシージャが表示されます。 呼び出したステートメントと実行が継続、`Property`手順、つまり、要求またはプロパティの値を設定するステートメントを使用します。 `Exit Property` プロパティの内部でのみ使用できます`Get`または`Set`プロシージャ。  
  
 戻り値を指定する、`Get`プロシージャでは前に、の行に関数名に値を割り当てることができます、`Exit Property`ステートメント。 戻り値と終了を割り当てる、 `Get` 1 つのステートメントでプロシージャを使用する、`Return`ステートメント。  
  
 `Set`プロシージャ、`Exit Property`ステートメントは、`Return`ステートメント。  
  
 `Exit Select`  
 すぐに終了させる、`Select Case`ブロックが表示されます。 ステートメントに次の実行が続行されます、`End Select`ステートメント。 `Exit Select` 内部でのみ使用できます、`Select Case`ステートメント。  
  
 `Exit Sub`  
 すぐに終了させる、`Sub`プロシージャが表示されます。 呼び出したステートメントの次のステートメントと実行が継続、`Sub`プロシージャ。 `Exit Sub` 内部でのみ使用できます、`Sub`プロシージャ。  
  
 `Sub`プロシージャ、`Exit Sub`ステートメントは、`Return`ステートメント。  
  
 `Exit Try`  
 すぐに終了させる、`Try`または`Catch`ブロックが表示されます。 実行が継続、 `Finally` 、1 つである場合、またはステートメントに次のブロック、`End Try`ステートメントがそれ以外の場合。 `Exit Try` 内部でのみ使用できます、`Try`または`Catch`ブロック内部に存在しないと、`Finally`ブロックします。  
  
 `Exit While`  
 すぐに終了させる、`While`ループが表示されます。 ステートメントに次の実行が続行されます、`End While`ステートメント。 `Exit While` 内部でのみ使用できます、`While`ループします。 使用すると内で入れ子になった`While`ループ、`Exit While`ループの 1 つの入れ子になったレベルは、ループに制御を転送、`Exit While`に発生します。  
  
## <a name="remarks"></a>Remarks  
 混同しないでください`Exit`ステートメントと`End`ステートメント。 `Exit` ステートメントの末尾を一切定義しません。  
  
## <a name="example"></a>例  
 次の例では、ループの条件がループを終了時に、`index`変数が 100 より大きい。 `If`ループでは、ステートメントがただし、により、`Exit Do`インデックス変数が 10 より大きい場合は、ループを停止するステートメント。  
  
 [!code-vb[VbVbalrStatements#133](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/exit-statement_1.vb)]  
  
## <a name="example"></a>例  
 次の例では、関数名に、戻り値を割り当てて`myFunction`、しを使用して`Exit Function`関数から返される。  
  
 [!code-vb[VbVbalrStatements#23](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/exit-statement_2.vb)]  
  
## <a name="example"></a>例  
 次の例では、 [Return ステートメント](../../../visual-basic/language-reference/statements/return-statement.md)戻り値を代入し、関数を終了します。  
  
 [!code-vb[VbVbalrStatements#24](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/exit-statement_3.vb)]  
  
## <a name="see-also"></a>関連項目
- [Continue ステートメント](../../../visual-basic/language-reference/statements/continue-statement.md)
- [Do...Loop ステートメント](../../../visual-basic/language-reference/statements/do-loop-statement.md)
- [End ステートメント](../../../visual-basic/language-reference/statements/end-statement.md)
- [For Each...Next ステートメント](../../../visual-basic/language-reference/statements/for-each-next-statement.md)
- [For...Next ステートメント](../../../visual-basic/language-reference/statements/for-next-statement.md)
- [Function ステートメント](../../../visual-basic/language-reference/statements/function-statement.md)
- [Return ステートメント](../../../visual-basic/language-reference/statements/return-statement.md)
- [Stop ステートメント](../../../visual-basic/language-reference/statements/stop-statement.md)
- [Sub ステートメント](../../../visual-basic/language-reference/statements/sub-statement.md)
- [Try...Catch...Finally ステートメント](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
