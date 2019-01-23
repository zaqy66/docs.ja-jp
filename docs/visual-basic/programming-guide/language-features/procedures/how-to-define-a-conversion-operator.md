---
title: '方法: 変換演算子 (Visual Basic) を定義します。'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- operators [Visual Basic], defining
- procedures [Visual Basic], operator
- operators [Visual Basic], overloading
- return values [Visual Basic], Operator procedures
- operator overloading
ms.assetid: 54203dfa-c24b-463f-9942-d5153e89e762
ms.openlocfilehash: 76d0769456e30766b830023c1f27381ceca59cbb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54521531"
---
# <a name="how-to-define-a-conversion-operator-visual-basic"></a>方法: 変換演算子 (Visual Basic) を定義します。
クラスまたは構造体を定義している場合は、クラスまたは構造体の型と別のデータ型の間の型変換演算子を定義することができます (など`Integer`、 `Double`、または`String`)。  
  
 として型の変換を定義、 [CType Function](../../../../visual-basic/language-reference/functions/ctype-function.md)クラスまたは構造内のプロシージャです。 変換のすべてのプロシージャである必要があります`Public Shared`、いずれかを指定する必要がありますそれぞれ[Widening](../../../../visual-basic/language-reference/modifiers/widening.md)または[Narrowing](../../../../visual-basic/language-reference/modifiers/narrowing.md)します。  
  
 クラスまたは構造体で演算子を定義が呼び出されますも*オーバー ロード*演算子。  
  
## <a name="example"></a>例  
 次の例と呼ばれる構造間の変換演算子を定義する`digit`と`Byte`します。  
  
 [!code-vb[VbVbcnProcedures#27](./codesnippet/VisualBasic/how-to-define-a-conversion-operator_1.vb)]  
  
 構造体をテストする`digit`を次のコード。  
  
 [!code-vb[VbVbcnProcedures#28](./codesnippet/VisualBasic/how-to-define-a-conversion-operator_2.vb)]  
  
## <a name="see-also"></a>関連項目
- [演算子プロシージャ](./operator-procedures.md)
- [方法: 演算子を定義します。](./how-to-define-an-operator.md)
- [方法: 演算子プロシージャを呼び出す](./how-to-call-an-operator-procedure.md)
- [方法: 演算子を定義するクラスを使用して、](./how-to-use-a-class-that-defines-operators.md)
- [Operator ステートメント](../../../../visual-basic/language-reference/statements/operator-statement.md)
- [Structure ステートメント](../../../../visual-basic/language-reference/statements/structure-statement.md)
- [方法: 構造体を宣言する](../../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
- [暗黙の型変換と明示的な型変換](../../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
- [拡大変換と縮小変換](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
