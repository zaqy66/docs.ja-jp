---
title: '\= 演算子 (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- '\='
- vb.\=
helpviewer_keywords:
- '\= operator [Visual Basic]'
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- operator \= [Visual Basic]
- compound assignment statements [Visual Basic]
ms.assetid: 6f39915d-e398-4045-afcc-da6885e57b9c
ms.openlocfilehash: bcfc59efda0627f83713fe9ada24cedc20d823e3
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42934514"
---
# <a name="-operator"></a>\\= 演算子
変数またはプロパティの値式の値で除算し、結果の整数値を変数またはプロパティに代入します。  
  
## <a name="syntax"></a>構文  
  
```  
variableorproperty \= expression  
```  
  
## <a name="parts"></a>指定項目  
 `variableorproperty`  
 必須。 任意の数値型の変数またはプロパティ。  
  
 `expression`  
 必須。 任意の数式。  
  
## <a name="remarks"></a>Remarks  
 左側にある要素、`\=`演算子は、単純なスカラー変数、プロパティ、または配列の要素。 変数またはプロパティにすることはできません[ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md)します。  
  
 `\=`演算子は、変数または、左側のプロパティの値の右側にある値で除算し、変数またはプロパティの左側に結果の整数値を割り当てます  
  
 整数の除算について詳しくは、次を参照してください。 [\ 演算子 (Visual Basic)](../../../visual-basic/language-reference/operators/integer-division-operator.md)します。  
  
## <a name="overloading"></a>オーバーロード  
 `\`演算子は、*オーバー ロードされた*、つまり、ことクラスまたは構造体を再定義できますその動作はそのクラスまたは構造体の型。 オーバー ロード、`\`演算子の動作に影響、`\=`演算子。 コードで使用する場合`\=`クラスまたは構造体をオーバー ロードで`\`、再定義された動作を確認してください。 詳細については、次を参照してください。[演算子プロシージャ](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md)します。  
  
## <a name="example"></a>例  
 次の例では、`\=`演算子を 1 つの分割`Integer`秒と、整数の結果が最初の変数に割り当てるのでは、変数。  
  
 [!code-vb[VbVbalrOperators#19](codesnippet/VisualBasic/integer-division-assignment-operator_1.vb)]  
  
## <a name="see-also"></a>関連項目  
 [\ 演算子 (Visual Basic)](../../../visual-basic/language-reference/operators/integer-division-operator.md)  
 [/= 演算子 (Visual Basic)](../../../visual-basic/language-reference/operators/floating-point-division-assignment-operator.md)  
 [代入演算子](../../../visual-basic/language-reference/operators/assignment-operators.md)  
 [算術演算子](../../../visual-basic/language-reference/operators/arithmetic-operators.md)  
 [Visual Basic における演算子の優先順位](../../../visual-basic/language-reference/operators/operator-precedence.md)  
 [機能別の演算子一覧](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)  
 [ステートメント](../../../visual-basic/programming-guide/language-features/statements.md)
