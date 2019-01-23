---
title: '&#39;IsNot&#39;型のオペランド&#39;typename&#39;のみに比較できるように&#39;Nothing&#39;ため、 &#39;typename&#39; null 許容型は、'
ms.date: 07/20/2015
f1_keywords:
- bc32128
- vbc32128
helpviewer_keywords:
- BC32128
ms.assetid: 1155b23a-ad75-4bab-b9da-73f35c767a36
ms.openlocfilehash: 65b04c85bccd169bbb2eea847d7b8af96c1a292f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54505719"
---
# <a name="39isnot39-operand-of-type-39typename39-can-only-be-compared-to-39nothing39-because-39typename39-is-a-nullable-type"></a>&#39;IsNot&#39;型のオペランド&#39;typename&#39;のみに比較できるように&#39;Nothing&#39;ため、 &#39;typename&#39; null 許容型は、
式に null 許容型として宣言された変数が以外に比較`Nothing`を使用して、`IsNot`演算子。  
  
 **エラー ID:** BC32128  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  `Nothing` 演算子を使用して、Null 許容型を `IsNot` 以外の式と比較するには、次の例に示すように、Null 許容型に対して `GetType` メソッドを呼び出し、その結果を式と比較します。  
  
```vb  
Dim number? As Integer = 5  
  
If number IsNot Nothing Then  
  If number.GetType() IsNot Type.GetType("System.Int32") Then   
  
  End If  
End If  
```  
  
## <a name="see-also"></a>関連項目
- [null 許容値型](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
- [IsNot 演算子](../../../visual-basic/language-reference/operators/isnot-operator.md)
