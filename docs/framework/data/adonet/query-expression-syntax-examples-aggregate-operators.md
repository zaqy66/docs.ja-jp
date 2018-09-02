---
title: 'クエリ式の構文例 : 集計演算子 (LINQ to DataSet)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 85dafa07-e102-46e7-ab78-37bf06f257a6
ms.openlocfilehash: fe3bd69b17b98e923c6c31fec2611e7390894e4a
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43398538"
---
# <a name="query-expression-syntax-examples-aggregate-operators-linq-to-dataset"></a><span data-ttu-id="a8155-102">クエリ式の構文例 : 集計演算子 (LINQ to DataSet)</span><span class="sxs-lookup"><span data-stu-id="a8155-102">Query Expression Syntax Examples: Aggregate Operators (LINQ to DataSet)</span></span>
<span data-ttu-id="a8155-103">このトピックでは、<xref:System.Linq.Enumerable.Average%2A>、<xref:System.Linq.Enumerable.Count%2A>、<xref:System.Linq.Enumerable.Max%2A>、<xref:System.Linq.Enumerable.Min%2A>、および <xref:System.Linq.Enumerable.Sum%2A> の各メソッドで、クエリ式の構文を使って <xref:System.Data.DataSet> および集計データに対するクエリを実行する例を紹介しています。</span><span class="sxs-lookup"><span data-stu-id="a8155-103">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.Average%2A>, <xref:System.Linq.Enumerable.Count%2A>, <xref:System.Linq.Enumerable.Max%2A>, <xref:System.Linq.Enumerable.Min%2A>, and <xref:System.Linq.Enumerable.Sum%2A> methods to query a <xref:System.Data.DataSet> and aggregate data using query expression syntax.</span></span>  
  
 <span data-ttu-id="a8155-104">`FillDataSet`でこれらの例で使用されるメソッドが指定された[をデータセットにデータを読み込む](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)します。</span><span class="sxs-lookup"><span data-stu-id="a8155-104">The `FillDataSet` method used in these examples is specified in [Loading Data Into a DataSet](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md).</span></span>  
  
 <span data-ttu-id="a8155-105">このトピックの例には、AdventureWorks サンプル データベースの Contact、Address、Product、SalesOrderHeader、SalesOrderDetail の各テーブルが使用されています。</span><span class="sxs-lookup"><span data-stu-id="a8155-105">The examples in this topic use the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="a8155-106">このトピックの例では、次を使用して`using` / `Imports`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="a8155-106">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#importsusing)]  
  
 <span data-ttu-id="a8155-107">詳細については、次を参照してください。[方法: LINQ to Visual Studio でデータセット プロジェクトを作成](../../../../docs/framework/data/adonet/how-to-create-a-linq-to-dataset-project-in-vs.md)です。</span><span class="sxs-lookup"><span data-stu-id="a8155-107">For more information, see [How to: Create a LINQ to DataSet Project In Visual Studio](../../../../docs/framework/data/adonet/how-to-create-a-linq-to-dataset-project-in-vs.md).</span></span>  
  
## <a name="average"></a><span data-ttu-id="a8155-108">平均</span><span class="sxs-lookup"><span data-stu-id="a8155-108">Average</span></span>  
  
### <a name="example"></a><span data-ttu-id="a8155-109">例</span><span class="sxs-lookup"><span data-stu-id="a8155-109">Example</span></span>  
 <span data-ttu-id="a8155-110">この例では、<xref:System.Linq.Enumerable.Average%2A> メソッドを使用して、各スタイルの製品の平均表示価格を取得します。</span><span class="sxs-lookup"><span data-stu-id="a8155-110">This example uses the <xref:System.Linq.Enumerable.Average%2A> method to find the average list price of the products of each style.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#Average2_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#average2_mq)]
 [!code-vb[DP LINQ to DataSet Examples#Average2_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#average2_mq)]  
  
### <a name="example"></a><span data-ttu-id="a8155-111">例</span><span class="sxs-lookup"><span data-stu-id="a8155-111">Example</span></span>  
 <span data-ttu-id="a8155-112">この例では、<xref:System.Linq.Enumerable.Average%2A> を使用して、それぞれの連絡先 ID について平均合計支払額を取得します。</span><span class="sxs-lookup"><span data-stu-id="a8155-112">This example uses <xref:System.Linq.Enumerable.Average%2A> to get the average total due for each contact ID.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#AverageGrouped_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#averagegrouped_mq)]
 [!code-vb[DP LINQ to DataSet Examples#AverageGrouped_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#averagegrouped_mq)]  
  
### <a name="example"></a><span data-ttu-id="a8155-113">例</span><span class="sxs-lookup"><span data-stu-id="a8155-113">Example</span></span>  
 <span data-ttu-id="a8155-114">この例では、<xref:System.Linq.Enumerable.Average%2A> を使用して、それぞれの連絡先について `TotalDue` が平均値の注文を取得します。</span><span class="sxs-lookup"><span data-stu-id="a8155-114">This example uses <xref:System.Linq.Enumerable.Average%2A> to get the orders with the average `TotalDue` for each contact.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#AverageElements_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#averageelements_mq)]
 [!code-vb[DP LINQ to DataSet Examples#AverageElements_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#averageelements_mq)]  
  
## <a name="count"></a><span data-ttu-id="a8155-115">Count</span><span class="sxs-lookup"><span data-stu-id="a8155-115">Count</span></span>  
  
### <a name="example"></a><span data-ttu-id="a8155-116">例</span><span class="sxs-lookup"><span data-stu-id="a8155-116">Example</span></span>  
 <span data-ttu-id="a8155-117">この例では、<xref:System.Linq.Enumerable.Count%2A> を使用して、連絡先 ID の一覧と、それぞれの注文数を返します。</span><span class="sxs-lookup"><span data-stu-id="a8155-117">This example uses <xref:System.Linq.Enumerable.Count%2A> to return a list of contact IDs and how many orders each has.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#CountNested](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#countnested)]
 [!code-vb[DP LINQ to DataSet Examples#CountNested](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#countnested)]  
  
### <a name="example"></a><span data-ttu-id="a8155-118">例</span><span class="sxs-lookup"><span data-stu-id="a8155-118">Example</span></span>  
 <span data-ttu-id="a8155-119">この例では、製品を色でグループ分けし、<xref:System.Linq.Enumerable.Count%2A> を使用してそれぞれの色グループに含まれる製品の数を返します。</span><span class="sxs-lookup"><span data-stu-id="a8155-119">This example groups products by color and uses <xref:System.Linq.Enumerable.Count%2A> to return the number of products in each color group.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#CountGrouped](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#countgrouped)]
 [!code-vb[DP LINQ to DataSet Examples#CountGrouped](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#countgrouped)]  
  
## <a name="max"></a><span data-ttu-id="a8155-120">最大</span><span class="sxs-lookup"><span data-stu-id="a8155-120">Max</span></span>  
  
### <a name="example"></a><span data-ttu-id="a8155-121">例</span><span class="sxs-lookup"><span data-stu-id="a8155-121">Example</span></span>  
 <span data-ttu-id="a8155-122">この例では、<xref:System.Linq.Enumerable.Max%2A> メソッドを使用して、それぞれの連絡先 ID について最大合計支払額を取得します。</span><span class="sxs-lookup"><span data-stu-id="a8155-122">This example uses the <xref:System.Linq.Enumerable.Max%2A> method to get the largest total due for each contact ID.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#MaxGrouped_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#maxgrouped_mq)]
 [!code-vb[DP LINQ to DataSet Examples#MaxGrouped_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#maxgrouped_mq)]  
  
### <a name="example"></a><span data-ttu-id="a8155-123">例</span><span class="sxs-lookup"><span data-stu-id="a8155-123">Example</span></span>  
 <span data-ttu-id="a8155-124">この例では、<xref:System.Linq.Enumerable.Max%2A> メソッドを使用して、それぞれの連絡先 ID について `TotalDue` が最大の注文を取得します。</span><span class="sxs-lookup"><span data-stu-id="a8155-124">This example uses the <xref:System.Linq.Enumerable.Max%2A> method to get the orders with the largest `TotalDue` for each contact ID.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#MaxElements_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#maxelements_mq)]
 [!code-vb[DP LINQ to DataSet Examples#MaxElements_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#maxelements_mq)]  
  
## <a name="min"></a><span data-ttu-id="a8155-125">最小</span><span class="sxs-lookup"><span data-stu-id="a8155-125">Min</span></span>  
  
### <a name="example"></a><span data-ttu-id="a8155-126">例</span><span class="sxs-lookup"><span data-stu-id="a8155-126">Example</span></span>  
 <span data-ttu-id="a8155-127">この例では、<xref:System.Linq.Enumerable.Min%2A> メソッドを使用して、それぞれの連絡先 ID について最小合計支払額を取得します。</span><span class="sxs-lookup"><span data-stu-id="a8155-127">This example uses the <xref:System.Linq.Enumerable.Min%2A> method to get the smallest total due for each contact ID.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#MinGrouped_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#mingrouped_mq)]
 [!code-vb[DP LINQ to DataSet Examples#MinGrouped_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#mingrouped_mq)]  
  
### <a name="example"></a><span data-ttu-id="a8155-128">例</span><span class="sxs-lookup"><span data-stu-id="a8155-128">Example</span></span>  
 <span data-ttu-id="a8155-129">この例では、<xref:System.Linq.Enumerable.Min%2A> メソッドを使用して、それぞれの連絡先について合計支払額が最小の注文を取得します。</span><span class="sxs-lookup"><span data-stu-id="a8155-129">This example uses the <xref:System.Linq.Enumerable.Min%2A> method to get the orders with the smallest total due for each contact.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#MinElements_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#minelements_mq)]
 [!code-vb[DP LINQ to DataSet Examples#MinElements_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#minelements_mq)]  
  
## <a name="sum"></a><span data-ttu-id="a8155-130">Sum</span><span class="sxs-lookup"><span data-stu-id="a8155-130">Sum</span></span>  
  
### <a name="example"></a><span data-ttu-id="a8155-131">例</span><span class="sxs-lookup"><span data-stu-id="a8155-131">Example</span></span>  
 <span data-ttu-id="a8155-132">この例では、<xref:System.Linq.Enumerable.Sum%2A> メソッドを使用して、それぞれの連絡先 ID について合計支払額を取得します。</span><span class="sxs-lookup"><span data-stu-id="a8155-132">This example uses the <xref:System.Linq.Enumerable.Sum%2A> method to get the total due for each contact ID.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#SumGrouped_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#sumgrouped_mq)]
 [!code-vb[DP LINQ to DataSet Examples#SumGrouped_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#sumgrouped_mq)]  
  
## <a name="see-also"></a><span data-ttu-id="a8155-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8155-133">See Also</span></span>  
 [<span data-ttu-id="a8155-134">DataSet へのデータの読み込み</span><span class="sxs-lookup"><span data-stu-id="a8155-134">Loading Data Into a DataSet</span></span>](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)  
 [<span data-ttu-id="a8155-135">LINQ to DataSet の例</span><span class="sxs-lookup"><span data-stu-id="a8155-135">LINQ to DataSet Examples</span></span>](../../../../docs/framework/data/adonet/linq-to-dataset-examples.md)  
 [<span data-ttu-id="a8155-136">標準クエリ演算子の概要</span><span class="sxs-lookup"><span data-stu-id="a8155-136">Standard Query Operators Overview</span></span>](https://msdn.microsoft.com/library/24cda21e-8af8-4632-b519-c404a839b9b2)
