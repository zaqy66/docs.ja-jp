---
title: "'Is' には参照型を持つオペランドが必要ですが、このオペランドの値型は '<typename>' です。"
ms.date: 07/20/2015
f1_keywords:
- bc30020
- vbc30020
helpviewer_keywords:
- BC30020
ms.assetid: 228afebd-1203-4bd3-8d7a-c5c56f3cedc4
ms.openlocfilehash: fbd0011e76ccecc605b0355025b7ca131e44724e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55263931"
---
# <a name="is-requires-operands-that-have-reference-types-but-this-operand-has-the-value-type-typename"></a><span data-ttu-id="7ad31-102">'Is' には、参照の型を持つオペランドが必要ですが、このオペランドの値の型は '\<typename >'</span><span class="sxs-lookup"><span data-stu-id="7ad31-102">'Is' requires operands that have reference types, but this operand has the value type '\<typename>'</span></span>
<span data-ttu-id="7ad31-103">`Is`比較演算子は、同じインスタンスに 2 つのオブジェクト変数が参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="7ad31-103">The `Is` comparison operator determines whether two object variables refer to the same instance.</span></span> <span data-ttu-id="7ad31-104">この比較値の型が定義されていません。</span><span class="sxs-lookup"><span data-stu-id="7ad31-104">This comparison is not defined for value types.</span></span>  
  
 <span data-ttu-id="7ad31-105">**エラー ID:** BC30020</span><span class="sxs-lookup"><span data-stu-id="7ad31-105">**Error ID:** BC30020</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="7ad31-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="7ad31-106">To correct this error</span></span>  
  
-   <span data-ttu-id="7ad31-107">適切な算術比較演算子を使用して、または`Like`2 つの値の型を比較する演算子。</span><span class="sxs-lookup"><span data-stu-id="7ad31-107">Use the appropriate arithmetic comparison operator or the `Like` operator to compare two value types.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7ad31-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="7ad31-108">See also</span></span>
- [<span data-ttu-id="7ad31-109">Is 演算子</span><span class="sxs-lookup"><span data-stu-id="7ad31-109">Is Operator</span></span>](../../../visual-basic/language-reference/operators/is-operator.md)
- [<span data-ttu-id="7ad31-110">Like 演算子</span><span class="sxs-lookup"><span data-stu-id="7ad31-110">Like Operator</span></span>](../../../visual-basic/language-reference/operators/like-operator.md)
- [<span data-ttu-id="7ad31-111">比較演算子</span><span class="sxs-lookup"><span data-stu-id="7ad31-111">Comparison Operators</span></span>](../../../visual-basic/language-reference/operators/comparison-operators.md)
