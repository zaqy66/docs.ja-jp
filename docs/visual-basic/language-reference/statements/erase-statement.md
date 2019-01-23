---
title: Erase ステートメント (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Erase
helpviewer_keywords:
- Erase keyword [Visual Basic]
- Erase statement [Visual Basic]
ms.assetid: 7a8133d7-b750-4d74-8b66-ba1dd9778d4b
ms.openlocfilehash: cab3da4465b4671d203036c2d9bcd40662dc234a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54522441"
---
# <a name="erase-statement-visual-basic"></a>Erase ステートメント (Visual Basic)
配列変数を解放し、その要素に使用されるメモリの割り当てを解除するために使用します。  
  
## <a name="syntax"></a>構文  
  
```  
Erase arraylist  
```  
  
## <a name="parts"></a>指定項目  
 `arraylist`  
 必須。 消去する配列変数の一覧。 複数の変数を指定するときは、コンマで区切ります。  
  
## <a name="remarks"></a>Remarks  
 `Erase`ステートメントは、プロシージャ レベルでのみ表示できます。 これは、クラスまたはモジュール レベルではなく、プロシージャ内部では配列を解放することを意味します。  
  
 `Erase`ステートメントは割り当てることと同じ`Nothing`各配列変数にします。  
  
## <a name="example"></a>例  
 次の例では、`Erase`を 2 つの配列をクリアし、そのメモリを解放ステートメント (1,000 と 100 のストレージ要素それぞれ)。 `ReDim`ステートメントし、配列の新しいインスタンスを 3 次元の配列に割り当てられます。  
  
 [!code-vb[VbVbalrStatements#19](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/erase-statement_1.vb)]  
  
## <a name="see-also"></a>関連項目
- [Nothing](../../../visual-basic/language-reference/nothing.md)
- [ReDim ステートメント](../../../visual-basic/language-reference/statements/redim-statement.md)
