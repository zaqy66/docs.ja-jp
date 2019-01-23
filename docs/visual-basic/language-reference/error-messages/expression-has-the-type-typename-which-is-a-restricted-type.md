---
title: 式の型&#39; &lt;typename&gt; &#39;は制限付きの型から継承されたメンバーのアクセスに使用することはできませんと&#39;オブジェクト&#39;または&#39;ValueType&#39;
ms.date: 07/20/2015
f1_keywords:
- bc31393
- vbc31393
helpviewer_keywords:
- BC31393
ms.assetid: 2963cf3f-c527-4aa7-b67c-ee80b6d23186
ms.openlocfilehash: d44b9a29f0848508d8cd814e857d9b01819ce7ab
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54535958"
---
# <a name="expression-has-the-type-39lttypenamegt39-which-is-a-restricted-type-and-cannot-be-used-to-access-members-inherited-from-39object39-or-39valuetype39"></a><span data-ttu-id="2c719-102">式の型&#39; &lt;typename&gt; &#39;は制限付きの型から継承されたメンバーのアクセスに使用することはできませんと&#39;オブジェクト&#39;または&#39;ValueType&#39;</span><span class="sxs-lookup"><span data-stu-id="2c719-102">Expression has the type &#39;&lt;typename&gt;&#39; which is a restricted type and cannot be used to access members inherited from &#39;Object&#39; or &#39;ValueType&#39;</span></span>
<span data-ttu-id="2c719-103">式では、共通言語ランタイム (CLR) でボックス化できない型に評価が、ボックス化を必要とするメンバーにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="2c719-103">An expression evaluates to a type that cannot be boxed by the common language runtime (CLR) but accesses a member that requires boxing.</span></span>  
  
 <span data-ttu-id="2c719-104">*ボックス化* とは、型を `Object` (場合によっては <xref:System.ValueType>) に変換するために不可欠な処理です。</span><span class="sxs-lookup"><span data-stu-id="2c719-104">*Boxing* refers to the processing necessary to convert a type to `Object` or, on occasion, to <xref:System.ValueType>.</span></span> <span data-ttu-id="2c719-105">共通言語ランタイムでは、特定の構造体の型をたとえばボックスことはできません<xref:System.ArgIterator>、 <xref:System.RuntimeArgumentHandle>、および<xref:System.TypedReference>します。</span><span class="sxs-lookup"><span data-stu-id="2c719-105">The common language runtime cannot box certain structure types, for example <xref:System.ArgIterator>, <xref:System.RuntimeArgumentHandle>, and <xref:System.TypedReference>.</span></span>  
  
 <span data-ttu-id="2c719-106">この式から継承されたメソッドの呼び出しに制限付きの型を使用しようとしました。<xref:System.Object>または<xref:System.ValueType>、など<xref:System.Object.GetHashCode%2A>または<xref:System.Object.ToString%2A>します。</span><span class="sxs-lookup"><span data-stu-id="2c719-106">This expression attempts to use the restricted type to call a method inherited from <xref:System.Object> or <xref:System.ValueType>, such as <xref:System.Object.GetHashCode%2A> or <xref:System.Object.ToString%2A>.</span></span> <span data-ttu-id="2c719-107">このメソッドにアクセスするには、Visual Basic はこのエラーが発生する暗黙的なボックス化変換をしようとしました。</span><span class="sxs-lookup"><span data-stu-id="2c719-107">To access this method, Visual Basic has attempted an implicit boxing conversion that causes this error.</span></span>  
  
 <span data-ttu-id="2c719-108">**エラー ID:** BC31393</span><span class="sxs-lookup"><span data-stu-id="2c719-108">**Error ID:** BC31393</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="2c719-109">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="2c719-109">To correct this error</span></span>  
  
1.  <span data-ttu-id="2c719-110">問題の型に評価される式を探します。</span><span class="sxs-lookup"><span data-stu-id="2c719-110">Locate the expression that evaluates to the cited type.</span></span>  
  
2.  <span data-ttu-id="2c719-111">継承されたメソッドを呼び出そうとすると、ステートメントの部分を探します<xref:System.Object>または<xref:System.ValueType>します。</span><span class="sxs-lookup"><span data-stu-id="2c719-111">Locate the part of your statement that attempts to call the method inherited from <xref:System.Object> or <xref:System.ValueType>.</span></span>  
  
3.  <span data-ttu-id="2c719-112">メソッドの呼び出しを回避するために、ステートメントを書き直してください。</span><span class="sxs-lookup"><span data-stu-id="2c719-112">Rewrite the statement to avoid the method call.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c719-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="2c719-113">See also</span></span>
- [<span data-ttu-id="2c719-114">暗黙の型変換と明示的な型変換</span><span class="sxs-lookup"><span data-stu-id="2c719-114">Implicit and Explicit Conversions</span></span>](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
