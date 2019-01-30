---
title: "'typename' は Null 許容型であるため、'typename' 型の 'IsNot' オペランドは 'Nothing' とのみ比較できます"
ms.date: 07/20/2015
f1_keywords:
- bc32128
- vbc32128
helpviewer_keywords:
- BC32128
ms.assetid: 1155b23a-ad75-4bab-b9da-73f35c767a36
ms.openlocfilehash: caa009606825225dd4063780f9a22fb82f21cf4e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271291"
---
# <a name="isnot-operand-of-type-typename-can-only-be-compared-to-nothing-because-typename-is-a-nullable-type"></a><span data-ttu-id="c9fae-102">'typename' は Null 許容型であるため、'typename' 型の 'IsNot' オペランドは 'Nothing' とのみ比較できます</span><span class="sxs-lookup"><span data-stu-id="c9fae-102">'IsNot' operand of type 'typename' can only be compared to 'Nothing', because 'typename' is a nullable type</span></span>
<span data-ttu-id="c9fae-103">式に null 許容型として宣言された変数が以外に比較`Nothing`を使用して、`IsNot`演算子。</span><span class="sxs-lookup"><span data-stu-id="c9fae-103">A variable declared as nullable has been compared to an expression other than `Nothing` using the `IsNot` operator.</span></span>  
  
 <span data-ttu-id="c9fae-104">**エラー ID:** BC32128</span><span class="sxs-lookup"><span data-stu-id="c9fae-104">**Error ID:** BC32128</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="c9fae-105">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="c9fae-105">To correct this error</span></span>  
  
1.  <span data-ttu-id="c9fae-106">`Nothing` 演算子を使用して、Null 許容型を `IsNot` 以外の式と比較するには、次の例に示すように、Null 許容型に対して `GetType` メソッドを呼び出し、その結果を式と比較します。</span><span class="sxs-lookup"><span data-stu-id="c9fae-106">To compare a nullable type to an expression other than `Nothing` by using the `IsNot` operator, call the `GetType` method on the nullable type and compare the result to the expression, as shown in the following example.</span></span>  
  
```vb  
Dim number? As Integer = 5  
  
If number IsNot Nothing Then  
  If number.GetType() IsNot Type.GetType("System.Int32") Then   
  
  End If  
End If  
```  
  
## <a name="see-also"></a><span data-ttu-id="c9fae-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="c9fae-107">See also</span></span>
- [<span data-ttu-id="c9fae-108">null 許容値型</span><span class="sxs-lookup"><span data-stu-id="c9fae-108">Nullable Value Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
- [<span data-ttu-id="c9fae-109">IsNot 演算子</span><span class="sxs-lookup"><span data-stu-id="c9fae-109">IsNot Operator</span></span>](../../../visual-basic/language-reference/operators/isnot-operator.md)
