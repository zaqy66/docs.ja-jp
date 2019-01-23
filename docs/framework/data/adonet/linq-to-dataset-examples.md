---
title: LINQ to DataSet の例
ms.date: 03/30/2017
ms.assetid: dfd91658-8d8a-45a4-a356-e327e809f21d
ms.openlocfilehash: 8e6cce8ba79cad42ade6ac373631094f9e2d4e04
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54634533"
---
# <a name="linq-to-dataset-examples"></a><span data-ttu-id="5150b-102">LINQ to DataSet の例</span><span class="sxs-lookup"><span data-stu-id="5150b-102">LINQ to DataSet Examples</span></span>
<span data-ttu-id="5150b-103">このセクションでは[!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)]プログラミングの標準クエリ演算子を使用する例。</span><span class="sxs-lookup"><span data-stu-id="5150b-103">This section provides [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] programming examples that use the standard query operators.</span></span> <span data-ttu-id="5150b-104"><xref:System.Data.DataSet>これらの例で使用されるを使用して設定されますが、`FillDataSet`メソッドで指定されている[をデータセットにデータを読み込む](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)。</span><span class="sxs-lookup"><span data-stu-id="5150b-104">The <xref:System.Data.DataSet> used in these examples is populated by using the `FillDataSet` method, which is specified in [Loading Data Into a DataSet](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md).</span></span> <span data-ttu-id="5150b-105">詳細については、次を参照してください。[標準クエリ演算子の概要](https://msdn.microsoft.com/library/24cda21e-8af8-4632-b519-c404a839b9b2)します。</span><span class="sxs-lookup"><span data-stu-id="5150b-105">For more information, see [Standard Query Operators Overview](https://msdn.microsoft.com/library/24cda21e-8af8-4632-b519-c404a839b9b2).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="5150b-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="5150b-106">In This Section</span></span>  
 [<span data-ttu-id="5150b-107">クエリ式の例</span><span class="sxs-lookup"><span data-stu-id="5150b-107">Query Expression Examples</span></span>](../../../../docs/framework/data/adonet/query-expression-examples-linq-to-dataset.md)  
 <span data-ttu-id="5150b-108">次の例があります。</span><span class="sxs-lookup"><span data-stu-id="5150b-108">Contains the following examples:</span></span>  
  
-   [<span data-ttu-id="5150b-109">射影</span><span class="sxs-lookup"><span data-stu-id="5150b-109">Projection</span></span>](../../../../docs/framework/data/adonet/query-expression-syntax-examples-projection-linq-to-dataset.md)  
  
-   [<span data-ttu-id="5150b-110">制限</span><span class="sxs-lookup"><span data-stu-id="5150b-110">Restriction</span></span>](../../../../docs/framework/data/adonet/query-expression-syntax-examples-restriction-linq-to-dataset.md)  
  
-   [<span data-ttu-id="5150b-111">パーティション分割</span><span class="sxs-lookup"><span data-stu-id="5150b-111">Partitioning</span></span>](../../../../docs/framework/data/adonet/query-expression-syntax-examples-partitioning.md)  
  
-   [<span data-ttu-id="5150b-112">順序付け</span><span class="sxs-lookup"><span data-stu-id="5150b-112">Ordering</span></span>](../../../../docs/framework/data/adonet/query-expression-syntax-examples-ordering-linq-to-dataset.md)  
  
-   [<span data-ttu-id="5150b-113">要素演算子</span><span class="sxs-lookup"><span data-stu-id="5150b-113">Element Operators</span></span>](../../../../docs/framework/data/adonet/query-expression-syntax-examples-element-operators.md)  
  
-   [<span data-ttu-id="5150b-114">集計演算子</span><span class="sxs-lookup"><span data-stu-id="5150b-114">Aggregate Operators</span></span>](../../../../docs/framework/data/adonet/query-expression-syntax-examples-aggregate-operators.md)  
  
-   [<span data-ttu-id="5150b-115">結合演算子</span><span class="sxs-lookup"><span data-stu-id="5150b-115">Join Operators</span></span>](../../../../docs/framework/data/adonet/query-expression-syntax-examples-join-operators.md)  
  
 [<span data-ttu-id="5150b-116">メソッド ベースのクエリ例</span><span class="sxs-lookup"><span data-stu-id="5150b-116">Method-Based Query Examples</span></span>](../../../../docs/framework/data/adonet/method-based-query-examples-linq-to-dataset.md)  
 <span data-ttu-id="5150b-117">次の例があります。</span><span class="sxs-lookup"><span data-stu-id="5150b-117">Contains the following examples:</span></span>  
  
-   [<span data-ttu-id="5150b-118">射影</span><span class="sxs-lookup"><span data-stu-id="5150b-118">Projection</span></span>](../../../../docs/framework/data/adonet/method-based-query-syntax-examples-projection.md)  
  
-   [<span data-ttu-id="5150b-119">パーティション分割</span><span class="sxs-lookup"><span data-stu-id="5150b-119">Partitioning</span></span>](../../../../docs/framework/data/adonet/method-based-query-syntax-examples-partitioning-linq.md)  
  
-   [<span data-ttu-id="5150b-120">順序付け</span><span class="sxs-lookup"><span data-stu-id="5150b-120">Ordering</span></span>](../../../../docs/framework/data/adonet/method-based-query-syntax-examples-ordering-linq-to-dataset.md)  
  
-   [<span data-ttu-id="5150b-121">集合演算子</span><span class="sxs-lookup"><span data-stu-id="5150b-121">Set Operators</span></span>](../../../../docs/framework/data/adonet/method-based-query-syntax-examples-set-operators.md)  
  
-   [<span data-ttu-id="5150b-122">変換演算子</span><span class="sxs-lookup"><span data-stu-id="5150b-122">Conversion Operators</span></span>](../../../../docs/framework/data/adonet/method-based-query-syntax-examples-conversion-operators.md)  
  
-   [<span data-ttu-id="5150b-123">要素演算子</span><span class="sxs-lookup"><span data-stu-id="5150b-123">Element Operators</span></span>](../../../../docs/framework/data/adonet/method-based-query-syntax-examples-element-operators.md)  
  
-   [<span data-ttu-id="5150b-124">集計演算子</span><span class="sxs-lookup"><span data-stu-id="5150b-124">Aggregate Operators</span></span>](../../../../docs/framework/data/adonet/method-based-query-syntax-examples-aggregate-operators.md)  
  
-   [<span data-ttu-id="5150b-125">Join</span><span class="sxs-lookup"><span data-stu-id="5150b-125">Join</span></span>](../../../../docs/framework/data/adonet/method-based-query-syntax-examples-join-linq-to-dataset.md)  
  
 [<span data-ttu-id="5150b-126">DataSet 固有の演算子の例</span><span class="sxs-lookup"><span data-stu-id="5150b-126">DataSet-Specific Operator Examples</span></span>](../../../../docs/framework/data/adonet/dataset-specific-operator-examples-linq-to-dataset.md)  
 <span data-ttu-id="5150b-127"><xref:System.Data.DataTableExtensions.CopyToDataTable%2A> メソッドおよび <xref:System.Data.DataRowComparer> クラスの使用例を紹介しています。</span><span class="sxs-lookup"><span data-stu-id="5150b-127">Contains examples that demonstrate how to use the <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> method and the <xref:System.Data.DataRowComparer> class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5150b-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="5150b-128">See also</span></span>
- [<span data-ttu-id="5150b-129">プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="5150b-129">Programming Guide</span></span>](../../../../docs/framework/data/adonet/programming-guide-linq-to-dataset.md)
- [<span data-ttu-id="5150b-130">DataSet へのデータの読み込み</span><span class="sxs-lookup"><span data-stu-id="5150b-130">Loading Data Into a DataSet</span></span>](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)
