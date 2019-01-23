---
title: "&#39;各&#39;型&#39; &lt;typename&gt; &#39;が型の複数のインスタンスを実装しているために、あいまいな&#39;'system.collections.generic.ienumerable(of T)&#39;"
ms.date: 07/20/2015
f1_keywords:
- vbc32096
- bc32096
helpviewer_keywords:
- BC32096
ms.assetid: ed20d09c-913f-482e-89f8-c0a596c3ec24
ms.openlocfilehash: 7fd779ba34afa2a59fa6c42971597df8ce01495a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54597347"
---
# <a name="39for-each39-on-type-39lttypenamegt39-is-ambiguous-because-the-type-implements-multiple-instantiations-of-39systemcollectionsgenericienumerableof-t39"></a>&#39;各&#39;型&#39; &lt;typename&gt; &#39;が型の複数のインスタンスを実装しているために、あいまいな&#39;'system.collections.generic.ienumerable(of T)&#39;
A`For Each`ステートメントで指定する反復子変数を 1 つ以上持つ<xref:System.Collections.IEnumerable.GetEnumerator%2A>メソッド。  
  
 実装する型の反復子変数がある必要があります、<xref:System.Collections.IEnumerable?displayProperty=nameWithType>または<xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType>インターフェイスのいずれかで、`Collections`の名前空間、[!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]します。 それぞれの構築についての別の型引数を使用して、構築された 1 つ以上のジェネリック インターフェイスを実装するクラスのことができます。 その変数が 1 つ以上の反復子変数は、このクラスを使用する場合<xref:System.Collections.IEnumerable.GetEnumerator%2A>メソッド。 このような場合は、Visual Basic は、どのメソッドを呼び出すを選択できません。  
  
 **エラー ID:** BC32096  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   使用して、 [DirectCast 演算子](../../../visual-basic/language-reference/operators/directcast-operator.md)または[TryCast 演算子](../../../visual-basic/language-reference/operators/trycast-operator.md)インターフェイスを定義する反復子変数の型にキャスト、<xref:System.Collections.IEnumerable.GetEnumerator%2A>メソッドを使用します。  
  
## <a name="see-also"></a>関連項目
- [For Each...Next ステートメント](../../../visual-basic/language-reference/statements/for-each-next-statement.md)
- [インターフェイス](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
