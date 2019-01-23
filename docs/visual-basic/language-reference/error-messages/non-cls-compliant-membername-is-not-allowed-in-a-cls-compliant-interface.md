---
title: 非 CLS 準拠&lt;membername&gt; CLS 準拠インターフェイスでは許可されません
ms.date: 07/20/2015
f1_keywords:
- bc40033
- vbc40033
helpviewer_keywords:
- BC40033
ms.assetid: 060c4b08-798e-40f1-94cf-c05c524f1b8a
ms.openlocfilehash: c837065d2d448fc2523cfbd18efac962445f8bf0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54627696"
---
# <a name="non-cls-compliant-ltmembernamegt-is-not-allowed-in-a-cls-compliant-interface"></a>非 CLS 準拠&lt;membername&gt; CLS 準拠インターフェイスでは許可されません
プロパティ、プロシージャ、またはインターフェイスでイベントがマーク`<CLSCompliant(True)>`インターフェイス自体としてマークされている場合`<CLSCompliant(False)>`またはマークされていません。  
  
 準拠するためのインターフェイスの[Language Independence and Language-independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS) にすべてのメンバーは、準拠である必要があります。  
  
 プログラミング要素に <xref:System.CLSCompliantAttribute> を適用する場合は、属性の `isCompliant` パラメーターを `True` または `False` のどちらかに設定して、準拠または非準拠を示します。 このパラメーターには既定値がありません。値を指定する必要があります。  
  
 要素に <xref:System.CLSCompliantAttribute> を適用しないと、その要素は非準拠と見なされます。  
  
 既定では、このメッセージは警告です。 警告を非表示にする方法や、警告をエラーとして扱う方法の詳細については、「 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)」をご覧ください。  
  
 **エラー ID:** BC40033  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   CLS 準拠をする必要があり、インターフェイスのソース コードを制御、マーク、インターフェイスとして`<CLSCompliant(True)>`すべてのメンバーが準拠している場合。  
  
-   インターフェイスのソース コードを制御することはできません、CLS 準拠が必要な場合、または準拠しているが明確でない場合は、このメンバーを別のインターフェイスを定義します。  
  
-   このメンバーが、現在のインターフェイス内に維持されることが必要な場合は、削除、<xref:System.CLSCompliantAttribute>その定義からとしてマークまたは`<CLSCompliant(False)>`します。  
  
## <a name="see-also"></a>関連項目
- [Interface ステートメント](../../../visual-basic/language-reference/statements/interface-statement.md)

