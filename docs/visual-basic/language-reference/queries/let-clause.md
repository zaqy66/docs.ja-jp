---
title: Let 句 (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryLet
helpviewer_keywords:
- queries [Visual Basic], Let
- Let clause [Visual Basic]
- Let statement [Visual Basic]
ms.assetid: 981aa516-16eb-4c53-b1f1-5aa3e82f316e
ms.openlocfilehash: 34c0fd239d9e08dab4a107cb8447941e7ab3ecbe
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43480373"
---
# <a name="let-clause-visual-basic"></a><span data-ttu-id="19dd7-102">Let 句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="19dd7-102">Let Clause (Visual Basic)</span></span>
<span data-ttu-id="19dd7-103">値を計算し、クエリ内で新しい変数に代入します。</span><span class="sxs-lookup"><span data-stu-id="19dd7-103">Computes a value and assigns it to a new variable within the query.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19dd7-104">構文</span><span class="sxs-lookup"><span data-stu-id="19dd7-104">Syntax</span></span>  
  
```  
Let variable = expression [, ...]  
```  
  
## <a name="parts"></a><span data-ttu-id="19dd7-105">指定項目</span><span class="sxs-lookup"><span data-stu-id="19dd7-105">Parts</span></span>  
  
|<span data-ttu-id="19dd7-106">用語</span><span class="sxs-lookup"><span data-stu-id="19dd7-106">Term</span></span>|<span data-ttu-id="19dd7-107">定義</span><span class="sxs-lookup"><span data-stu-id="19dd7-107">Definition</span></span>|  
|---|---|  
|`variable`|<span data-ttu-id="19dd7-108">必須。</span><span class="sxs-lookup"><span data-stu-id="19dd7-108">Required.</span></span> <span data-ttu-id="19dd7-109">指定された式の結果を参照に使用できるエイリアスです。</span><span class="sxs-lookup"><span data-stu-id="19dd7-109">An alias that can be used to reference the results of the supplied expression.</span></span>|  
|`expression`|<span data-ttu-id="19dd7-110">必須。</span><span class="sxs-lookup"><span data-stu-id="19dd7-110">Required.</span></span> <span data-ttu-id="19dd7-111">評価し、指定された変数に代入する式。</span><span class="sxs-lookup"><span data-stu-id="19dd7-111">An expression that will be evaluated and assigned to the specified variable.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="19dd7-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="19dd7-112">Remarks</span></span>  
 <span data-ttu-id="19dd7-113">`Let`句では、コンピューティングの各値がクエリの結果と、エイリアスを使用してそれらを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="19dd7-113">The `Let` clause enables you to compute values for each query result and reference them by using an alias.</span></span> <span data-ttu-id="19dd7-114">別名をなど、他の句で使用することができます、`Where`句。</span><span class="sxs-lookup"><span data-stu-id="19dd7-114">The alias can be used in other clauses, such as the `Where` clause.</span></span> <span data-ttu-id="19dd7-115">`Let`句では、クエリに含まれる式の句の別名を指定でき、式の句が使用されるたびに、エイリアスを置き換えるため、読みやすくクエリ ステートメントを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="19dd7-115">The `Let` clause enables you to create a query statement that is easier to read because you can specify an alias for an expression clause included in the query and substitute the alias each time the expression clause is used.</span></span>  
  
 <span data-ttu-id="19dd7-116">任意の数を含めることができます`variable`と`expression`で割り当て、`Let`句。</span><span class="sxs-lookup"><span data-stu-id="19dd7-116">You can include any number of `variable` and `expression` assignments in the `Let` clause.</span></span> <span data-ttu-id="19dd7-117">各割り当てをコンマ (,) で区切ります。</span><span class="sxs-lookup"><span data-stu-id="19dd7-117">Separate each assignment with a comma (,).</span></span>  
  
## <a name="example"></a><span data-ttu-id="19dd7-118">例</span><span class="sxs-lookup"><span data-stu-id="19dd7-118">Example</span></span>  
 <span data-ttu-id="19dd7-119">次のコード例では、`Let`製品の 10% の割引を計算する句。</span><span class="sxs-lookup"><span data-stu-id="19dd7-119">The following code example uses the `Let` clause to compute a 10 percent discount on products.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#16](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/let-clause_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="19dd7-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="19dd7-120">See Also</span></span>  
 [<span data-ttu-id="19dd7-121">Visual Basic における LINQ の概要</span><span class="sxs-lookup"><span data-stu-id="19dd7-121">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
 [<span data-ttu-id="19dd7-122">クエリ</span><span class="sxs-lookup"><span data-stu-id="19dd7-122">Queries</span></span>](../../../visual-basic/language-reference/queries/index.md)  
 [<span data-ttu-id="19dd7-123">Select 句</span><span class="sxs-lookup"><span data-stu-id="19dd7-123">Select Clause</span></span>](../../../visual-basic/language-reference/queries/select-clause.md)  
 [<span data-ttu-id="19dd7-124">From 句</span><span class="sxs-lookup"><span data-stu-id="19dd7-124">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)  
 [<span data-ttu-id="19dd7-125">WHERE 句</span><span class="sxs-lookup"><span data-stu-id="19dd7-125">Where Clause</span></span>](../../../visual-basic/language-reference/queries/where-clause.md)
