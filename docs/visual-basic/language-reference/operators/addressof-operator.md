---
title: AddressOf 演算子 (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- AddressOf
- vb.AddressOf
helpviewer_keywords:
- AddressOf operator [Visual Basic]
- addresses, passing to API procedures
ms.assetid: 8105a59d-60d8-4ab5-b221-5899cdfacbf4
ms.openlocfilehash: 4f4f88551b6708ac3d0ee0f0f5bdcbdec1dfaaa9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54721071"
---
# <a name="addressof-operator-visual-basic"></a>AddressOf 演算子 (Visual Basic)
特定のプロシージャを参照するプロシージャ デリゲート インスタンスを作成します。  
  
## <a name="syntax"></a>構文  
  
```  
AddressOf procedurename  
```  
  
## <a name="parts"></a>指定項目  
 `procedurename`  
 必須。 新しく作成されたプロシージャのデリゲートが参照するプロシージャを指定します。  
  
## <a name="remarks"></a>Remarks  
 `AddressOf`演算子で指定された関数を指す関数デリゲートを作成する`procedurename`します。 ときに、指定したプロシージャは、インスタンス メソッド、関数デリゲートがインスタンスとメソッドの両方を参照します。 次に、関数デリゲートが呼び出されたときに、指定したインスタンスの指定されたメソッドが呼び出されます。  
  
 `AddressOf` Delegate コンス トラクターのオペランドとして使用できる演算子またはにおいて、コンパイラによってデリゲートの型を決定するために使用できます。  
  
## <a name="example"></a>例  
 この例では、`AddressOf`を処理するデリゲートを指定する演算子、`Click`ボタンのイベント。  
  
 [!code-vb[VbVbalrDelegates#8](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/addressof-operator_1.vb)]  
  
## <a name="example"></a>例  
 次の例では、`AddressOf`スレッドのスタートアップ関数を指定する演算子。  
  
 [!code-vb[VbVbalrDelegates#9](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/addressof-operator_2.vb)]  
  
## <a name="see-also"></a>関連項目
- [Declare ステートメント](../../../visual-basic/language-reference/statements/declare-statement.md)
- [Function ステートメント](../../../visual-basic/language-reference/statements/function-statement.md)
- [Sub ステートメント](../../../visual-basic/language-reference/statements/sub-statement.md)
- [デリゲート](../../../visual-basic/programming-guide/language-features/delegates/index.md)
