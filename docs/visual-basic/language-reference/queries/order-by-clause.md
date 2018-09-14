---
title: Order By 句 (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryOrderBy
- vb.QueryAscending
- vb.QueryDescending
helpviewer_keywords:
- queries [Visual Basic], Order By
- Order By clause [Visual Basic]
- Order By statement [Visual Basic]
ms.assetid: fa911282-6b81-44c7-acfa-46b5bb93df75
ms.openlocfilehash: d4abb5f0b75ae4069c1dbe695a5c810b1f7aa6e1
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/13/2018
ms.locfileid: "45558013"
---
# <a name="order-by-clause-visual-basic"></a><span data-ttu-id="15127-102">Order By 句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="15127-102">Order By Clause (Visual Basic)</span></span>
<span data-ttu-id="15127-103">クエリ結果の並べ替え順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="15127-103">Specifies the sort order for a query result.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="15127-104">構文</span><span class="sxs-lookup"><span data-stu-id="15127-104">Syntax</span></span>  
  
```  
Order By orderExp1 [ Ascending | Descending ] [, orderExp2 [...] ]  
```  
  
## <a name="parts"></a><span data-ttu-id="15127-105">指定項目</span><span class="sxs-lookup"><span data-stu-id="15127-105">Parts</span></span>  
 `orderExp1`  
 <span data-ttu-id="15127-106">必須。</span><span class="sxs-lookup"><span data-stu-id="15127-106">Required.</span></span> <span data-ttu-id="15127-107">1 つまたは複数のフィールド現在のクエリ結果からの返された値を並べ替える方法を識別します。</span><span class="sxs-lookup"><span data-stu-id="15127-107">One or more fields from the current query result that identify how to order the returned values.</span></span> <span data-ttu-id="15127-108">フィールド名は、コンマ (,) で区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="15127-108">The field names must be separated by commas (,).</span></span> <span data-ttu-id="15127-109">昇順または降順を使用して、ソート済みとしては、各フィールドを識別できます、`Ascending`または`Descending`キーワード。</span><span class="sxs-lookup"><span data-stu-id="15127-109">You can identify each field as sorted in ascending or descending order by using the `Ascending` or `Descending` keywords.</span></span> <span data-ttu-id="15127-110">ない場合は`Ascending`または`Descending`キーワードを指定すると、既定の並べ替え順序は昇順です。</span><span class="sxs-lookup"><span data-stu-id="15127-110">If no `Ascending` or `Descending` keyword is specified, the default sort order is ascending.</span></span> <span data-ttu-id="15127-111">並べ替え順序のフィールドには、左から右への優先順位が与えられます。</span><span class="sxs-lookup"><span data-stu-id="15127-111">The sort order fields are given precedence from left to right.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="15127-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="15127-112">Remarks</span></span>  
 <span data-ttu-id="15127-113">使用することができます、`Order By`句、クエリの結果を並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="15127-113">You can use the `Order By` clause to sort the results of a query.</span></span> <span data-ttu-id="15127-114">`Order By`句では、現在のスコープの範囲変数に基づく結果を並べ替えることができますのみです。</span><span class="sxs-lookup"><span data-stu-id="15127-114">The `Order By` clause can only sort a result based on the range variable for the current scope.</span></span> <span data-ttu-id="15127-115">たとえば、`Select`句にそのスコープの新しい反復変数をクエリ式での新しいスコープが導入されています。</span><span class="sxs-lookup"><span data-stu-id="15127-115">For example, the `Select` clause introduces a new scope in a query expression with new iteration variables for that scope.</span></span> <span data-ttu-id="15127-116">範囲変数を定義する前に、`Select`クエリ句は使用後に、`Select`句。</span><span class="sxs-lookup"><span data-stu-id="15127-116">Range variables defined before a `Select` clause in a query are not available after the `Select` clause.</span></span> <span data-ttu-id="15127-117">そのため、記載されていないフィールドで、結果の順序をする場合、`Select`句に配置する必要がある、`Order By`句の前に、`Select`句。</span><span class="sxs-lookup"><span data-stu-id="15127-117">Therefore, if you want to order your results by a field that is not available in the `Select` clause, you must put the `Order By` clause before the `Select` clause.</span></span> <span data-ttu-id="15127-118">1 つのときにこれを行う必要があるには例が、結果の一部として返されないフィールドで、クエリの並べ替えを行うときにします。</span><span class="sxs-lookup"><span data-stu-id="15127-118">One example of when you would have to do this is when you want to sort your query by fields that are not returned as part of the result.</span></span>  
  
 <span data-ttu-id="15127-119">昇順と降順の実装によって、フィールドが特定の順序、<xref:System.IComparable>フィールドのデータ型のインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="15127-119">Ascending and descending order for a field is determined by the implementation of the <xref:System.IComparable> interface for the data type of the field.</span></span> <span data-ttu-id="15127-120">データ型が実装していない場合、<xref:System.IComparable>インターフェイス、並べ替え順序は無視されます。</span><span class="sxs-lookup"><span data-stu-id="15127-120">If the data type does not implement the <xref:System.IComparable> interface, the sort order is ignored.</span></span>  
  
## <a name="example"></a><span data-ttu-id="15127-121">例</span><span class="sxs-lookup"><span data-stu-id="15127-121">Example</span></span>  
 <span data-ttu-id="15127-122">次のクエリ式は、`From`範囲変数を宣言する句`book`の`books`コレクション。</span><span class="sxs-lookup"><span data-stu-id="15127-122">The following query expression uses a `From` clause to declare a range variable `book` for the `books` collection.</span></span> <span data-ttu-id="15127-123">`Order By`句で昇順に並べ替えます (既定値) の価格をクエリの結果を並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="15127-123">The `Order By` clause sorts the query result by price in ascending order (the default).</span></span> <span data-ttu-id="15127-124">同じ価格ブックは、タイトルの昇順で並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="15127-124">Books with the same price are sorted by title in ascending order.</span></span> <span data-ttu-id="15127-125">`Select`句を選択、`Title`と`Price`プロパティとして、クエリによって返される値。</span><span class="sxs-lookup"><span data-stu-id="15127-125">The `Select` clause selects the `Title` and `Price` properties as the values returned by the query.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#24](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/order-by-clause_1.vb)]  
  
## <a name="example"></a><span data-ttu-id="15127-126">例</span><span class="sxs-lookup"><span data-stu-id="15127-126">Example</span></span>  
 <span data-ttu-id="15127-127">次のクエリ式は、`Order By`降順で価格をクエリ結果を並べ替えるための句。</span><span class="sxs-lookup"><span data-stu-id="15127-127">The following query expression uses the `Order By` clause to sort the query result by price in descending order.</span></span> <span data-ttu-id="15127-128">同じ価格ブックは、タイトルの昇順で並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="15127-128">Books with the same price are sorted by title in ascending order.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#25](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/order-by-clause_2.vb)]  
  
## <a name="example"></a><span data-ttu-id="15127-129">例</span><span class="sxs-lookup"><span data-stu-id="15127-129">Example</span></span>  
 <span data-ttu-id="15127-130">次のクエリ式は、`Select`句を書籍のタイトルを選択し、価格、発行日、作成します。</span><span class="sxs-lookup"><span data-stu-id="15127-130">The following query expression uses a `Select` clause to select the book title, price, publish date, and author.</span></span> <span data-ttu-id="15127-131">設定し、 `Title`、 `Price`、`PublishDate`と`Author`新しいスコープの範囲変数のフィールド。</span><span class="sxs-lookup"><span data-stu-id="15127-131">It then populates the `Title`, `Price`, `PublishDate`, and `Author` fields of the range variable for the new scope.</span></span> <span data-ttu-id="15127-132">`Order By`句の作成者の名前、書籍のタイトル、および価格によって新しい範囲変数の順序。</span><span class="sxs-lookup"><span data-stu-id="15127-132">The `Order By` clause orders the new range variable by author name, book title, and then price.</span></span> <span data-ttu-id="15127-133">各列は、既定の順序 (昇順) で並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="15127-133">Each column is sorted in the default order (ascending).</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#26](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/order-by-clause_3.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="15127-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="15127-134">See Also</span></span>  
 [<span data-ttu-id="15127-135">Visual Basic における LINQ の概要</span><span class="sxs-lookup"><span data-stu-id="15127-135">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
 [<span data-ttu-id="15127-136">クエリ</span><span class="sxs-lookup"><span data-stu-id="15127-136">Queries</span></span>](../../../visual-basic/language-reference/queries/index.md)  
 [<span data-ttu-id="15127-137">Select 句</span><span class="sxs-lookup"><span data-stu-id="15127-137">Select Clause</span></span>](../../../visual-basic/language-reference/queries/select-clause.md)  
 [<span data-ttu-id="15127-138">From 句</span><span class="sxs-lookup"><span data-stu-id="15127-138">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)
