---
title: '&#39;拡張機能&#39;にのみ適用できる属性&#39;モジュール&#39;、 &#39;Sub&#39;、または&#39;関数&#39;宣言'
ms.date: 07/20/2015
f1_keywords:
- bc36550
- vbc36550
helpviewer_keywords:
- BC36550
ms.assetid: 4387a51f-733c-45d7-abdb-eb64d4f51078
ms.openlocfilehash: fabd602f31a362fe33954253d565e86a065e0a83
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54718235"
---
# <a name="39extension39-attribute-can-be-applied-only-to-39module39-39sub39-or-39function39-declarations"></a>&#39;拡張機能&#39;にのみ適用できる属性&#39;モジュール&#39;、 &#39;Sub&#39;、または&#39;関数&#39;宣言
Visual Basic でのデータ型を拡張する唯一の方法では、標準のモジュール内で拡張メソッドを定義します。 拡張メソッドになる、`Sub`プロシージャまたは`Function`プロシージャ。 すべての拡張メソッドは、拡張機能の属性でマークする必要があります`<Extension()>`から、<xref:System.Runtime.CompilerServices?displayProperty=nameWithType>名前空間。 必要に応じて、拡張メソッドを含むモジュールの場合は、同じ方法でマークされている可能性があります。 拡張属性の他の使用が有効ではありません。  
  
 **エラー ID:** BC36550  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   拡張属性を削除します。  
  
-   外側のモジュールで定義されている、方法として、拡張機能を再設計します。  
  
## <a name="example"></a>例  
 次の例では、定義、`Print`のメソッド、`String`データ型。  
  
```  
Imports StringUtility  
Imports System.Runtime.CompilerServices  
Namespace StringUtility  
    <Extension()>   
    Module StringExtensions  
        <Extension()>   
        Public Sub Print (ByVal str As String)  
            Console.WriteLine(str)  
        End Sub  
    End Module  
End Namespace  
```  
  
## <a name="see-also"></a>関連項目
- [属性の概要](../../../visual-basic/programming-guide/concepts/attributes/index.md)
- [拡張メソッド](../../../visual-basic/programming-guide/language-features/procedures/extension-methods.md)
- [Module ステートメント](../../../visual-basic/language-reference/statements/module-statement.md)
