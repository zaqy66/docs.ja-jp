---
title: 参照できません&#39;&lt;名前&gt;&#39;値に型指定されたフィールドのメンバーであるため、 &#39;&lt;名前&gt;&#39;クラスの&#39; &lt;classname&gt; &#39;を持つ&#39;System.MarshalByRefObject&#39;基底クラスとして
ms.date: 07/20/2015
f1_keywords:
- vbc30310
- bc30310
helpviewer_keywords:
- BC30310
ms.assetid: 2aeb8872-7c87-4f01-98ef-9714ba3eebbe
ms.openlocfilehash: a6298c3e0f5102397d5cc3f237a186598c6b5ecc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54739298"
---
# <a name="cannot-refer-to-39ltnamegt39-because-it-is-a-member-of-the-value-typed-field-39ltnamegt39-of-class-39ltclassnamegt39-which-has-39systemmarshalbyrefobject39-as-a-base-class"></a>参照できません&#39;&lt;名前&gt;&#39;値に型指定されたフィールドのメンバーであるため、 &#39;&lt;名前&gt;&#39;クラスの&#39; &lt;classname&gt; &#39;を持つ&#39;System.MarshalByRefObject&#39;基底クラスとして
`System.MarshalByRefObject`クラスは、アプリケーション ドメイン境界を越えてオブジェクトへのリモート アクセスをサポートするアプリケーションを使用できます。 型を継承する必要があります、`MarshalByRejectObject`クラスの型がアプリケーション ドメイン境界を越えて使用するとします。 オブジェクトのメンバーが作成されたアプリケーション ドメインの外部で使用できないために、オブジェクトの状態はコピーされませんする必要があります。  
  
 **エラー ID:** BC30310  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  参照先のメンバーが有効かどうかを確認への参照を確認してください。  
  
2.  持つメンバーを明示的に修飾、`Me`キーワード。  
  
## <a name="see-also"></a>関連項目
- <xref:System.MarshalByRefObject>
- [Dim ステートメント](../../../visual-basic/language-reference/statements/dim-statement.md)
