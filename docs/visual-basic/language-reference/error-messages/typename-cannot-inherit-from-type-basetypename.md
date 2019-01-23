---
title: '&#39;&lt;typename&gt; &#39;から継承できません&lt;型&gt; &#39; &lt;basetypename&gt; &#39;ベースのアクセスを展開するので、&lt;型&gt;アセンブリの外部'
ms.date: 07/20/2015
f1_keywords:
- vbc30910
- bc30910
helpviewer_keywords:
- BC30910
ms.assetid: 68fc05c5-5d55-4742-9a3b-ea04312594f4
ms.openlocfilehash: 108025132bdd0fa86df5ed142aaa39c7b7e18062
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54556484"
---
# <a name="39lttypenamegt39-cannot-inherit-from-lttypegt-39ltbasetypenamegt39-because-it-expands-the-access-of-the-base-lttypegt-outside-the-assembly"></a>&#39;&lt;typename&gt; &#39;から継承できません&lt;型&gt; &#39; &lt;basetypename&gt; &#39;ベースのアクセスを展開するので、&lt;型&gt;アセンブリの外部
クラスまたはインターフェイスは、基本クラスから継承されているかインターフェイスより制限の少ないアクセス レベル。  
  
 たとえば、`Public`インターフェイスから継承、`Friend`インターフェイス、または`Protected`クラスから継承、`Private`クラス。 これは、基底クラスまたはインターフェイスの目的のレベルを超えてへのアクセスに公開します。  
  
 **エラー ID:** BC30910  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   派生クラスまたは少なくとも基底クラスまたはインターフェイスの場合と同程度に制限するようにインターフェイスのアクセス レベルを変更します。  
  
     - または -  
  
-   制限の少ないアクセス レベルが必要な場合は、削除、`Inherits`ステートメント。 さらに制限された基底クラスまたはインターフェイスから継承することはできません。  
  
## <a name="see-also"></a>関連項目
- [Class ステートメント](../../../visual-basic/language-reference/statements/class-statement.md)
- [Interface ステートメント](../../../visual-basic/language-reference/statements/interface-statement.md)
- [Inherits ステートメント](../../../visual-basic/language-reference/statements/inherits-statement.md)
- [Visual Basic でのアクセス レベル](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
