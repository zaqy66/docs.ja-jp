---
title: '&#39;&#39;オペランドが必要です、参照型がこのオペランドの値の型は&#39; &lt;typename&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- bc30020
- vbc30020
helpviewer_keywords:
- BC30020
ms.assetid: 228afebd-1203-4bd3-8d7a-c5c56f3cedc4
ms.openlocfilehash: 0b3f80e98087e455ec730dea8c57478528e9259c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54722921"
---
# <a name="39is39-requires-operands-that-have-reference-types-but-this-operand-has-the-value-type-39lttypenamegt39"></a><span data-ttu-id="4f437-102">&#39;&#39;オペランドが必要です、参照型がこのオペランドの値の型は&#39; &lt;typename&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="4f437-102">&#39;Is&#39; requires operands that have reference types, but this operand has the value type &#39;&lt;typename&gt;&#39;</span></span>
<span data-ttu-id="4f437-103">`Is`比較演算子は、同じインスタンスに 2 つのオブジェクト変数が参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="4f437-103">The `Is` comparison operator determines whether two object variables refer to the same instance.</span></span> <span data-ttu-id="4f437-104">この比較値の型が定義されていません。</span><span class="sxs-lookup"><span data-stu-id="4f437-104">This comparison is not defined for value types.</span></span>  
  
 <span data-ttu-id="4f437-105">**エラー ID:** BC30020</span><span class="sxs-lookup"><span data-stu-id="4f437-105">**Error ID:** BC30020</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="4f437-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="4f437-106">To correct this error</span></span>  
  
-   <span data-ttu-id="4f437-107">適切な算術比較演算子を使用して、または`Like`2 つの値の型を比較する演算子。</span><span class="sxs-lookup"><span data-stu-id="4f437-107">Use the appropriate arithmetic comparison operator or the `Like` operator to compare two value types.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4f437-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f437-108">See also</span></span>
- [<span data-ttu-id="4f437-109">Is 演算子</span><span class="sxs-lookup"><span data-stu-id="4f437-109">Is Operator</span></span>](../../../visual-basic/language-reference/operators/is-operator.md)
- [<span data-ttu-id="4f437-110">Like 演算子</span><span class="sxs-lookup"><span data-stu-id="4f437-110">Like Operator</span></span>](../../../visual-basic/language-reference/operators/like-operator.md)
- [<span data-ttu-id="4f437-111">比較演算子</span><span class="sxs-lookup"><span data-stu-id="4f437-111">Comparison Operators</span></span>](../../../visual-basic/language-reference/operators/comparison-operators.md)
