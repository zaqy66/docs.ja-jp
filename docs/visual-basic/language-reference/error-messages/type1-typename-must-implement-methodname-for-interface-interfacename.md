---
title: '&lt;type1&gt;&#39;&lt;typename&gt; &#39;実装する必要があります&#39; &lt;methodname&gt; &#39;インターフェイス&#39; &lt;interfacename&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30149
- bc30149
helpviewer_keywords:
- BC30149
ms.assetid: 29d1b7f4-dca7-478c-bbe7-c657f342c183
ms.openlocfilehash: ff9ffd50f7f21814d5e4c23fd8df50b12bf746f5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54642443"
---
# <a name="lttype1gt39lttypenamegt39-must-implement-39ltmethodnamegt39-for-interface-39ltinterfacenamegt39"></a>&lt;type1&gt;&#39;&lt;typename&gt; &#39;実装する必要があります&#39; &lt;methodname&gt; &#39;インターフェイス&#39; &lt;interfacename&gt;&#39;
クラスまたは構造体がインターフェイスを実装するために要求しているインターフェイスによって定義されたプロシージャを実装していません。 インターフェイスのすべてのメンバーを実装する必要があります。  
  
 **エラー ID:** BC30149  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  同じ名前と、インターフェイスで定義されたシグネチャを持つプロシージャを宣言します。 必ず含めて、少なくとも`End Function`または`End Sub`ステートメント。  
  
2.  追加、`Implements`句の末尾に、`Function`または`Sub`ステートメント。 例:  
  
    ```  
    Public Sub DoSomething() Implements IBaseInterface.DoSomething  
    ```  
  
## <a name="see-also"></a>関連項目
- [Implements ステートメント](../../../visual-basic/language-reference/statements/implements-statement.md)
- [インターフェイス](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
