---
title: 入れ子になった関数に、デリゲート '<delegatename>' と互換性のあるシグネチャがありません。
ms.date: 07/20/2015
f1_keywords:
- vbc36532
- bc36532
helpviewer_keywords:
- BC36532
ms.assetid: 493f292c-d81e-40ef-8b47-61f020571829
ms.openlocfilehash: ea6f230715520cb35809d57db76b300da326ec9a
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55283466"
---
# <a name="nested-function-does-not-have-a-signature-that-is-compatible-with-delegate-delegatename"></a>入れ子になった関数には、デリゲートと互換性のあるシグネチャはありません '\<delegatename >'。
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
