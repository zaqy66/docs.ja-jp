---
title: 'クエリ式の構文例: 射影'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 079926c5-e6b5-4fb9-b4cf-9c63886dd626
ms.openlocfilehash: cc50b2564d295f1c81feacdeb52008f9f0004adc
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43396630"
---
# <a name="query-expression-syntax-examples-projection"></a><span data-ttu-id="94185-102">クエリ式の構文例: 射影</span><span class="sxs-lookup"><span data-stu-id="94185-102">Query Expression Syntax Examples: Projection</span></span>
<span data-ttu-id="94185-103">このトピックの例では、使用する方法を示します、`Select`メソッドと`From … From …`クエリを実行するためのキーワード、 [AdventureWorks Sales Model](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832)クエリ式構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="94185-103">The examples in this topic demonstrate how to use the `Select` method and the `From … From …` keywords to query the [AdventureWorks Sales Model](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) using query expression syntax.</span></span> <span data-ttu-id="94185-104">`From … From …` は、メソッドは、`SelectMany` メソッドのクエリ ベース版に相当します。</span><span class="sxs-lookup"><span data-stu-id="94185-104">`From … From …` is the query based equivalent of the `SelectMany` method.</span></span> <span data-ttu-id="94185-105">これらの例で使用されている、AdventureWorks Sales Model は、AdventureWorks サンプル データベースの Contact、Address、Product、SalesOrderHeader、SalesOrderDetail の各テーブルから作成されています。</span><span class="sxs-lookup"><span data-stu-id="94185-105">The AdventureWorks Sales model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="94185-106">このトピックの例では、次を使用して`using` / `Imports`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="94185-106">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="select"></a><span data-ttu-id="94185-107">選択</span><span class="sxs-lookup"><span data-stu-id="94185-107">Select</span></span>  
  
### <a name="example"></a><span data-ttu-id="94185-108">例</span><span class="sxs-lookup"><span data-stu-id="94185-108">Example</span></span>  
 <span data-ttu-id="94185-109">次の例では、<xref:System.Linq.Enumerable.Select%2A> メソッドを使用して `Product` テーブルからすべての行を取得し、製品名を表示しています。</span><span class="sxs-lookup"><span data-stu-id="94185-109">The following example uses the <xref:System.Linq.Enumerable.Select%2A> method to return all the rows from the `Product` table and display the product names.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectSimple1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectsimple1)]
 [!code-vb[DP L2E Examples#SelectSimple1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectsimple1)]  
  
### <a name="example"></a><span data-ttu-id="94185-110">例</span><span class="sxs-lookup"><span data-stu-id="94185-110">Example</span></span>  
 <span data-ttu-id="94185-111">次の例では、<xref:System.Linq.Enumerable.Select%2A> を使用して、一連の製品名だけを取得しています。</span><span class="sxs-lookup"><span data-stu-id="94185-111">The following example uses <xref:System.Linq.Enumerable.Select%2A> to return a sequence of only product names.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectSimple2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectsimple2)]
 [!code-vb[DP L2E Examples#SelectSimple2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectsimple2)]  
  
### <a name="example"></a><span data-ttu-id="94185-112">例</span><span class="sxs-lookup"><span data-stu-id="94185-112">Example</span></span>  
 <span data-ttu-id="94185-113">次の例では、<xref:System.Linq.Queryable.Select%2A> メソッドを使用して、`Product.Name` プロパティおよび `Product.ProductID` プロパティを一連の匿名型に射影します。</span><span class="sxs-lookup"><span data-stu-id="94185-113">The following example uses the <xref:System.Linq.Queryable.Select%2A> method to project the `Product.Name` and `Product.ProductID` properties into a sequence of anonymous types.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectAnonymousTypes](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectanonymoustypes)]
 [!code-vb[DP L2E Examples#SelectAnonymousTypes](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectanonymoustypes)]  
  
## <a name="from--from--selectmany"></a><span data-ttu-id="94185-114">差出人。</span><span class="sxs-lookup"><span data-stu-id="94185-114">From …</span></span> <span data-ttu-id="94185-115">差出人。</span><span class="sxs-lookup"><span data-stu-id="94185-115">From …</span></span> <span data-ttu-id="94185-116">(SelectMany)</span><span class="sxs-lookup"><span data-stu-id="94185-116">(SelectMany)</span></span>  
  
### <a name="example"></a><span data-ttu-id="94185-117">例</span><span class="sxs-lookup"><span data-stu-id="94185-117">Example</span></span>  
 <span data-ttu-id="94185-118">次の例では、`From … From …` (<xref:System.Linq.Enumerable.SelectMany%2A> メソッドと等価) を使用して、`TotalDue` が 500.00 に満たないすべての注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="94185-118">The following example uses `From … From …` (the equivalent of the <xref:System.Linq.Enumerable.SelectMany%2A> method) to select all orders where `TotalDue` is less than 500.00.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectManyCompoundFrom](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectmanycompoundfrom)]
 [!code-vb[DP L2E Examples#SelectManyCompoundFrom](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectmanycompoundfrom)]  
  
### <a name="example"></a><span data-ttu-id="94185-119">例</span><span class="sxs-lookup"><span data-stu-id="94185-119">Example</span></span>  
 <span data-ttu-id="94185-120">次の例では、`From … From …` (<xref:System.Linq.Enumerable.SelectMany%2A> メソッドと等価) を使用して、2002 年 10 月 1 日以降に受けたすべての注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="94185-120">The following example uses `From … From …` (the equivalent of the <xref:System.Linq.Enumerable.SelectMany%2A> method) to select all orders where the order was made on October 1, 2002 or later.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectManyCompoundFrom2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectmanycompoundfrom2)]
 [!code-vb[DP L2E Examples#SelectManyCompoundFrom2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectmanycompoundfrom2)]  
  
### <a name="example"></a><span data-ttu-id="94185-121">例</span><span class="sxs-lookup"><span data-stu-id="94185-121">Example</span></span>  
 <span data-ttu-id="94185-122">次の例では、`From … From …` (<xref:System.Linq.Enumerable.SelectMany%2A> メソッドと等価) を使用して、注文の合計が 10000.00 を超えるすべての注文を選択します。このとき、`From` 割り当てを使用して、合計を 2 回要求しないようにしています。</span><span class="sxs-lookup"><span data-stu-id="94185-122">The following example uses a `From … From …` (the equivalent of the <xref:System.Linq.Enumerable.SelectMany%2A> method) to select all orders where the order total is greater than 10000.00 and uses `From` assignment to avoid requesting the total twice.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectManyFromAssignment](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectmanyfromassignment)]
 [!code-vb[DP L2E Examples#SelectManyFromAssignment](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectmanyfromassignment)]  
  
## <a name="see-also"></a><span data-ttu-id="94185-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="94185-123">See Also</span></span>  
 [<span data-ttu-id="94185-124">LINQ to Entities でのクエリ</span><span class="sxs-lookup"><span data-stu-id="94185-124">Queries in LINQ to Entities</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
