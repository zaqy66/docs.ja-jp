---
title: 名前&lt;membername&gt; CLS 準拠ではありません
ms.date: 07/20/2015
f1_keywords:
- bc40031
- vbc40031
helpviewer_keywords:
- BC40031
ms.assetid: e2b885dc-cbf9-49ff-bbbe-531657ea99f7
ms.openlocfilehash: b950be530eb80fd1c65b48e1625eb344c642d260
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54626369"
---
# <a name="name-ltmembernamegt-is-not-cls-compliant"></a>名前&lt;membername&gt; CLS 準拠ではありません
アセンブリをマーク`<CLSCompliant(True)>`アンダー スコアで始まる名前を持つメンバーを公開しますが、(`_`)。  
  
 プログラミング要素ですが準拠するため、1 つまたは複数アンダー スコアを含めることができます、 [Language Independence and Language-independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS) にする必要がありますされませんアンダー スコアで始まりです。 「 [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)」を参照してください。  
  
 プログラミング要素に <xref:System.CLSCompliantAttribute> を適用する場合は、属性の `isCompliant` パラメーターを `True` または `False` のどちらかに設定して、準拠または非準拠を示します。 このパラメーターには既定値がありません。値を指定する必要があります。  
  
 要素に <xref:System.CLSCompliantAttribute> を適用しないと、その要素は非準拠と見なされます。  
  
 既定では、このメッセージは警告です。 警告を非表示にする方法や、警告をエラーとして扱う方法の詳細については、「 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)」をご覧ください。  
  
 **エラー ID:** BC40031  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   ソース コード制御を使用する場合は、メンバー名を変更してから、アンダー スコアで始まらないようにします。  
  
-   メンバー名が変わらない場合は、削除、<xref:System.CLSCompliantAttribute>その定義からとしてマークまたは`<CLSCompliant(False)>`します。 アセンブリをマークすることも`<CLSCompliant(True)>`します。  
  
## <a name="see-also"></a>関連項目
- [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)
- [Visual Basic の名前付け規則](../../../visual-basic/programming-guide/program-structure/naming-conventions.md)

