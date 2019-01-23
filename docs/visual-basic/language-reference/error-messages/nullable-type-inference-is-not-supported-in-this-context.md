---
title: Null 許容型の推論はこのコンテキストではサポートされていません
ms.date: 07/20/2015
f1_keywords:
- vbc36629
- bc36629
helpviewer_keywords:
- BC36629
ms.assetid: 0a1e2dbc-d9a4-433d-9306-c5540782b81d
ms.openlocfilehash: 7dffc5233656257cd892f573a2f8b9f91d781c21
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54611892"
---
# <a name="nullable-type-inference-is-not-supported-in-this-context"></a>Null 許容型の推論はこのコンテキストではサポートされていません
値型と構造体が null 許容宣言できます。  
  
```vb  
Dim a? As Integer  
Dim b As Integer?  
```  
  
 ただし、型の推定と組み合わせて、null 許容型の宣言を使用することはできません。 次の例では、このエラーが発生します。  
  
```vb  
' Not valid.  
' Dim c? = 10  
' Dim d? = a  
```  
  
 **エラー ID:** BC36629  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   使用して、 `As` null 許容型として変数を宣言する句。  
  
## <a name="see-also"></a>関連項目
- [null 許容値型](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
- [ローカル型の推論](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
