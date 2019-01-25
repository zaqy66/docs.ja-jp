---
title: Key (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.AnonymousKey
helpviewer_keywords:
- anonymous types [Visual Basic], key
- Key [Visual Basic]
- Key keyword [Visual Basic]
ms.assetid: 7697a928-7d14-4430-a72a-c9e96e8d6c11
ms.openlocfilehash: 695f356f44bfd6ea5ad3c0a977ec31ddfbea2b05
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54668224"
---
# <a name="key-visual-basic"></a>Key (Visual Basic)
`Key`キーワードでは、匿名型のプロパティの動作を指定することができます。 匿名型のインスタンス、またはハッシュ コード値の計算の間での等価テストでキー プロパティとしてを指定したプロパティのみです。 キー プロパティの値を変更できません。  
  
 キー プロパティとして、キーワードを配置することで、匿名型のプロパティを指定する`Key`初期化リストでの宣言の前にします。 次の例では、`Airline`と`FlightNo`キーのプロパティが`Gate`はありません。  
  
 [!code-vb[VbVbalrAnonymousTypes#26](../../../visual-basic/language-reference/modifiers/codesnippet/VisualBasic/key_1.vb)]  
  
 直接継承する新しい匿名型が作成されると、<xref:System.Object>します。 コンパイラは、次の 3 つの継承されたメンバーをオーバーライドします。 <xref:System.Object.Equals%2A>、 <xref:System.Object.GetHashCode%2A>、および<xref:System.Object.ToString%2A>します。 生成されたオーバーライド コードは、<xref:System.Object.Equals%2A>と<xref:System.Object.GetHashCode%2A>キー プロパティに基づきます。 種類でキー プロパティがない場合<xref:System.Object.GetHashCode%2A>と<xref:System.Object.Equals%2A>は上書きされません。  
  
## <a name="equality"></a>等価比較  
 匿名型の 2 つのインスタンスは、キー プロパティの値が等しい場合、同じ型のインスタンスと等しくなります。 次の例で`flight2`と等しい`flight1`から前の例では、同じ匿名のインスタンスであるための種類とそれらが一致する、キー プロパティの値。 ただし、`flight3`が等しくない`flight1`別のキーのプロパティの値があるため、`FlightNo`します。 インスタンス`flight4`と同じ型でない`flight1`キー プロパティとしてさまざまなプロパティを指定するためです。  
  
 [!code-vb[VbVbalrAnonymousTypes#27](../../../visual-basic/language-reference/modifiers/codesnippet/VisualBasic/key_2.vb)]  
  
 プロパティを持つのみ非キーと同じ名前、種類、順序、および値である 2 つのインスタンスが宣言されている場合は 2 つのインスタンスが等しくないです。 キー プロパティを持たないインスタンスはのみにします。  
  
 匿名型の 2 つのインスタンスを同じ匿名型のインスタンスである条件の詳細については、次を参照してください。[匿名型](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md)します。  
  
## <a name="hash-code-calculation"></a>ハッシュ コードの計算  
 ような<xref:System.Object.Equals%2A>、ハッシュ関数で定義されている<xref:System.Object.GetHashCode%2A>匿名型が、型のキー プロパティに基づいています。 次の例では、コードの値のキー プロパティとハッシュ間のやり取りを示します。  
  
 すべてのキー プロパティの同じ値を持つ匿名型のインスタンスでは、キー以外のプロパティは一致する値を持っていない場合でも、同じハッシュ コード値があります。 次のステートメントから`True`します。  
  
 [!code-vb[VbVbalrAnonymousTypes#37](../../../visual-basic/language-reference/modifiers/codesnippet/VisualBasic/key_3.vb)]  
  
 1 つまたは複数のキー プロパティの異なる値を持つ匿名型のインスタンスでは、別のハッシュ コード値があります。 次のステートメントから`False`します。  
  
 [!code-vb[VbVbalrAnonymousTypes#38](../../../visual-basic/language-reference/modifiers/codesnippet/VisualBasic/key_4.vb)]  
  
 キー プロパティとしてさまざまなプロパティを指定する匿名型のインスタンスは、同じ型のインスタンスではありません。 名前とすべてのプロパティの値が同じ場合でも他のハッシュ コード値があります。 次のステートメントから`False`します。  
  
 [!code-vb[VbVbalrAnonymousTypes#39](../../../visual-basic/language-reference/modifiers/codesnippet/VisualBasic/key_5.vb)]  
  
## <a name="read-only-values"></a>読み取り専用の値  
 キー プロパティの値を変更できません。 たとえば、`flight1`前の例で、`Airline`と`FlightNo`フィールドは読み取り専用が`Gate`変更できます。  
  
 [!code-vb[VbVbalrAnonymousTypes#28](../../../visual-basic/language-reference/modifiers/codesnippet/VisualBasic/key_6.vb)]  
  
## <a name="see-also"></a>関連項目
- [匿名型の定義](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-type-definition.md)
- [方法: 匿名型の宣言におけるプロパティ名と型を推論します。](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-infer-property-names-and-types-in-anonymous-type-declarations.md)
- [匿名型](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md)
