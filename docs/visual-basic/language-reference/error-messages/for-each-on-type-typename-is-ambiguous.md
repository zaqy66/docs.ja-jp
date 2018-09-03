---
title: "&#39;各&#39;型&#39; &lt;typename&gt; &#39;が型の複数のインスタンスを実装しているために、あいまいな&#39;'system.collections.generic.ienumerable(of T)&#39;"
ms.date: 07/20/2015
f1_keywords:
- vbc32096
- bc32096
helpviewer_keywords:
- BC32096
ms.assetid: ed20d09c-913f-482e-89f8-c0a596c3ec24
ms.openlocfilehash: 8c48a7134eb8da83fb418b9aa91d55dcbe8e8bcb
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43456306"
---
# <a name="39for-each39-on-type-39lttypenamegt39-is-ambiguous-because-the-type-implements-multiple-instantiations-of-39systemcollectionsgenericienumerableof-t39"></a><span data-ttu-id="67699-102">&#39;各&#39;型&#39; &lt;typename&gt; &#39;が型の複数のインスタンスを実装しているために、あいまいな&#39;'system.collections.generic.ienumerable(of T)&#39;</span><span class="sxs-lookup"><span data-stu-id="67699-102">&#39;For Each&#39; on type &#39;&lt;typename&gt;&#39; is ambiguous because the type implements multiple instantiations of &#39;System.Collections.Generic.IEnumerable(Of T)&#39;</span></span>
<span data-ttu-id="67699-103">A`For Each`ステートメントで指定する反復子変数を 1 つ以上持つ<xref:System.Collections.IEnumerable.GetEnumerator%2A>メソッド。</span><span class="sxs-lookup"><span data-stu-id="67699-103">A `For Each` statement specifies an iterator variable that has more than one <xref:System.Collections.IEnumerable.GetEnumerator%2A> method.</span></span>  
  
 <span data-ttu-id="67699-104">実装する型の反復子変数がある必要があります、<xref:System.Collections.IEnumerable?displayProperty=nameWithType>または<xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType>インターフェイスのいずれかで、`Collections`の名前空間、[!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]します。</span><span class="sxs-lookup"><span data-stu-id="67699-104">The iterator variable must be of a type that implements the <xref:System.Collections.IEnumerable?displayProperty=nameWithType> or <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> interface in one of the `Collections` namespaces of the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)].</span></span> <span data-ttu-id="67699-105">それぞれの構築についての別の型引数を使用して、構築された 1 つ以上のジェネリック インターフェイスを実装するクラスのことができます。</span><span class="sxs-lookup"><span data-stu-id="67699-105">It is possible for a class to implement more than one constructed generic interface, using a different type argument for each construction.</span></span> <span data-ttu-id="67699-106">その変数が 1 つ以上の反復子変数は、このクラスを使用する場合<xref:System.Collections.IEnumerable.GetEnumerator%2A>メソッド。</span><span class="sxs-lookup"><span data-stu-id="67699-106">If a class that does this is used for the iterator variable, that variable has more than one <xref:System.Collections.IEnumerable.GetEnumerator%2A> method.</span></span> <span data-ttu-id="67699-107">このような場合は、Visual Basic は、どのメソッドを呼び出すを選択できません。</span><span class="sxs-lookup"><span data-stu-id="67699-107">In such a case, Visual Basic cannot choose which method to call.</span></span>  
  
 <span data-ttu-id="67699-108">**エラー ID:** BC32096</span><span class="sxs-lookup"><span data-stu-id="67699-108">**Error ID:** BC32096</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="67699-109">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="67699-109">To correct this error</span></span>  
  
-   <span data-ttu-id="67699-110">使用して、 [DirectCast 演算子](../../../visual-basic/language-reference/operators/directcast-operator.md)または[TryCast 演算子](../../../visual-basic/language-reference/operators/trycast-operator.md)インターフェイスを定義する反復子変数の型にキャスト、<xref:System.Collections.IEnumerable.GetEnumerator%2A>メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="67699-110">Use [DirectCast Operator](../../../visual-basic/language-reference/operators/directcast-operator.md) or [TryCast Operator](../../../visual-basic/language-reference/operators/trycast-operator.md) to cast the iterator variable type to the interface defining the <xref:System.Collections.IEnumerable.GetEnumerator%2A> method you want to use.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="67699-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="67699-111">See Also</span></span>  
 [<span data-ttu-id="67699-112">For Each...Next ステートメント</span><span class="sxs-lookup"><span data-stu-id="67699-112">For Each...Next Statement</span></span>](../../../visual-basic/language-reference/statements/for-each-next-statement.md)  
 [<span data-ttu-id="67699-113">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="67699-113">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
