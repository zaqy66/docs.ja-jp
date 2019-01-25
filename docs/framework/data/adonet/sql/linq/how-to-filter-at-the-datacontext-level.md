---
title: '方法: DataContext レベルでフィルター処理します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 15505cd7-0df2-427a-9f86-e0f96f60ee2e
ms.openlocfilehash: 66bbfe19c73f116b8f85cae829bb61bb2da3d4c2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54644219"
---
# <a name="how-to-filter-at-the-datacontext-level"></a><span data-ttu-id="c0033-102">方法: DataContext レベルでフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="c0033-102">How to: Filter at the DataContext Level</span></span>
<span data-ttu-id="c0033-103">`EntitySets` を `DataContext` レベルでフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="c0033-103">You can filter `EntitySets` at the `DataContext` level.</span></span> <span data-ttu-id="c0033-104">このフィルター処理は、対象の <xref:System.Data.Linq.DataContext> インスタンスを使って実行されたすべてのクエリに適用されます。</span><span class="sxs-lookup"><span data-stu-id="c0033-104">Such filters apply to all queries done with that <xref:System.Data.Linq.DataContext> instance.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c0033-105">例</span><span class="sxs-lookup"><span data-stu-id="c0033-105">Example</span></span>  
 <span data-ttu-id="c0033-106">次の例では、あらかじめ読み込まれた顧客からの注文を <xref:System.Data.Linq.DataLoadOptions.AssociateWith%28System.Linq.Expressions.LambdaExpression%29?displayProperty=nameWithType> に基づいてフィルター処理するために `ShippedDate` が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c0033-106">In the following example, <xref:System.Data.Linq.DataLoadOptions.AssociateWith%28System.Linq.Expressions.LambdaExpression%29?displayProperty=nameWithType> is used to filter the pre-loaded orders for customers by `ShippedDate`.</span></span>  
  
 [!code-csharp[DLinqQueryConcepts#10](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryConcepts/cs/Program.cs#10)]
 [!code-vb[DLinqQueryConcepts#10](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryConcepts/vb/Module1.vb#10)]  
  
## <a name="see-also"></a><span data-ttu-id="c0033-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="c0033-107">See also</span></span>
- [<span data-ttu-id="c0033-108">クエリの概念</span><span class="sxs-lookup"><span data-stu-id="c0033-108">Query Concepts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)
