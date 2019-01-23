---
title: 既定のプロパティ&#39; &lt;propertyname1&gt; &#39;既定のプロパティと競合して&#39; &lt;propertyname2&gt; &#39;で&#39; &lt;classname&gt; &#39;ため、宣言する必要があります&#39;シャドウ&#39;
ms.date: 07/20/2015
f1_keywords:
- vbc40007
- bc40007
helpviewer_keywords:
- BC40007
ms.assetid: 692ccf76-5715-4f11-a972-84cf9de30bc1
ms.openlocfilehash: 3099467fa3c5a162c13c9235fb8d55375953ba3a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54521427"
---
# <a name="default-property-39ltpropertyname1gt39-conflicts-with-default-property-39ltpropertyname2gt39-in-39ltclassnamegt39-and-so-should-be-declared-39shadows39"></a>既定のプロパティ&#39; &lt;propertyname1&gt; &#39;既定のプロパティと競合して&#39; &lt;propertyname2&gt; &#39;で&#39; &lt;classname&gt; &#39;ため、宣言する必要があります&#39;シャドウ&#39;
プロパティは、基底クラスで定義されたプロパティと同じ名前で宣言します。 このような状況では、このクラスのプロパティは、基底クラスのプロパティをシャドウする必要があります。  
  
 このメッセージは警告です。 `Shadows` は、既定で指定されていると見なされます。 警告を非表示にする方法や、警告をエラーとして扱う方法の詳細については、「 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)」をご覧ください。  
  
 **エラー ID:** BC40007  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   追加、`Shadows`プロパティの名前が宣言されているキーワードを宣言、または変更します。  
  
## <a name="see-also"></a>関連項目
- [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md)
- [Visual Basic におけるシャドウ](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
