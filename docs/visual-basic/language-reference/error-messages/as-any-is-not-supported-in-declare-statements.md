---
title: '&#39;いずれかとして&#39;でサポートされていない&#39;Declare&#39;ステートメント'
ms.date: 07/20/2015
f1_keywords:
- bc30828
- vbc30828
helpviewer_keywords:
- BC30828
ms.assetid: 7e5cf519-8b64-4ac5-8116-705fe26c846d
ms.openlocfilehash: 560ddc8674718f98f3e1a2f6d4facdb198f5e506
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54709860"
---
# <a name="39as-any39-is-not-supported-in-39declare39-statements"></a>&#39;いずれかとして&#39;でサポートされていない&#39;Declare&#39;ステートメント
`Any`データ型の併用`Declare`ステートメントでは、あらゆる種類のデータを含む可能性のある引数の使用を許可するには、Visual Basic 6.0 と以前のバージョン。 オーバー ロード、ただし、Visual Basic は、そのにより、`Any`データ型の廃止されています。  
  
 **エラー ID:** BC30828  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  を使用する特定の型のパラメーターを宣言します。例えば。  
  
     [!code-vb[VbVbalrStatements#95](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/as-any-is-not-supported-in-declare-statements_1.vb)]  
  
2.  使用して、<xref:System.Runtime.InteropServices.MarshalAsAttribute>属性を指定する`As Any`とき`Void*`によって呼び出されるプロシージャが必要です。  
  
     [!code-vb[VbVbalrStatements#96](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/as-any-is-not-supported-in-declare-statements_2.vb)]  
  
## <a name="see-also"></a>関連項目
- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [チュートリアル: Windows API の呼び出し](../../../visual-basic/programming-guide/com-interop/walkthrough-calling-windows-apis.md)
- [Declare ステートメント](../../../visual-basic/language-reference/statements/declare-statement.md)
- [マネージド コードでのプロトタイプの作成](../../../framework/interop/creating-prototypes-in-managed-code.md)
