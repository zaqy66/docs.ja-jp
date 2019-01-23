---
title: 入れ子になった関数にデリゲートと互換性のあるシグネチャがない&#39; &lt;delegatename&gt;&#39;
ms.date: 07/20/2015
f1_keywords:
- vbc36532
- bc36532
helpviewer_keywords:
- BC36532
ms.assetid: 493f292c-d81e-40ef-8b47-61f020571829
ms.openlocfilehash: abfda4ee6064ec9ea54b8a3c383d10f8263a1458
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506408"
---
# <a name="nested-function-does-not-have-a-signature-that-is-compatible-with-delegate-39ltdelegatenamegt39"></a>入れ子になった関数にデリゲートと互換性のあるシグネチャがない&#39; &lt;delegatename&gt;&#39;
ラムダ式は、互換性のないシグネチャを持つデリゲートに割り当てられています。 たとえば、次のコードでは、委任`Del`は 2 つの整数パラメーターがあります。  
  
```vb  
Delegate Function Del(ByVal p As Integer, ByVal q As Integer) As Integer  
```  
  
 1 つの引数があるラムダ式が型として宣言されている場合、エラーが発生した`Del`:  
  
```vb  
' Neither of these is valid.   
' Dim lambda1 As Del = Function(n As Integer) n + 1  
' Dim lambda2 As Del = Function(n) n + 1  
```  
  
 **エラー ID:** BC36532  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   シグネチャに互換性があるように、デリゲートの定義または割り当てられているラムダ式のいずれかを調整します。  
  
## <a name="see-also"></a>関連項目
- [厳密でないデリゲート変換](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md)
- [ラムダ式](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
