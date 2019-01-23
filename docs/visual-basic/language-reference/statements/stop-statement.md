---
title: Stop ステートメント (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Stop
helpviewer_keywords:
- breakpoints, Stop statements
- Stop statements [Visual Basic], syntax
- Stop statements [Visual Basic]
- execution [Visual Basic], suspending
- processing, interrupting
- processes, interrupting
- execution [Visual Basic], stopping
ms.assetid: c9a9fde0-d649-4662-9bef-bd0146ebc2a7
ms.openlocfilehash: fa9a1942903dff6f673d87b67ebcad047a410425
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54624783"
---
# <a name="stop-statement-visual-basic"></a>Stop ステートメント (Visual Basic)
実行を中断します。  
  
## <a name="syntax"></a>構文  
  
```  
Stop  
```  
  
## <a name="remarks"></a>Remarks  
 配置できる`Stop`ステートメントの実行を中断する手順で任意の場所。 使用して、`Stop`ステートメントは、コード内のブレークポイントの設定に似ています。  
  
 `Stop`ステートメントのとは異なり、実行を中断`End`、すべてのファイルを終了したり、コンパイル済み実行可能 (.exe) ファイルで検出された場合を除き、任意の変数をクリアしません。  
  
> [!NOTE]
>  場合、`Stop`統合開発環境 (IDE) の外部で実行されているコードのステートメントが検出された場合、デバッガーが呼び出されます。 これは、コードがデバッグ、または製品のモードでコンパイルするかどうかに関係なく当てはまります。  
  
## <a name="example"></a>例  
 この例では、`Stop`ステートメント内の各繰り返しの実行を中断、`For...Next`ループします。  
  
 [!code-vb[VbVbalrStatements#56](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/stop-statement_1.vb)]  
  
## <a name="see-also"></a>関連項目
- [End ステートメント](../../../visual-basic/language-reference/statements/end-statement.md)
