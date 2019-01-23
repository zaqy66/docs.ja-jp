---
title: シーケンス内の要素数のカウント
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: ccbe5d54-c9eb-4b14-b0ab-f628483c5f99
ms.openlocfilehash: 546417cc0b4aed7fa092ddb25fe37fa8d95d0e91
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54510483"
---
# <a name="count-the-number-of-elements-in-a-sequence"></a><span data-ttu-id="d8052-102">シーケンス内の要素数のカウント</span><span class="sxs-lookup"><span data-stu-id="d8052-102">Count the Number of Elements in a Sequence</span></span>
<span data-ttu-id="d8052-103"><xref:System.Linq.Enumerable.Count%2A> 演算子を使用すると、シーケンス内の要素数をカウントできます。</span><span class="sxs-lookup"><span data-stu-id="d8052-103">Use the <xref:System.Linq.Enumerable.Count%2A> operator to count the number of elements in a sequence.</span></span>  
  
 <span data-ttu-id="d8052-104">Northwind サンプル データベースに対してこのクエリを実行すると、出力は `91` になります。</span><span class="sxs-lookup"><span data-stu-id="d8052-104">Running this query against the Northwind sample database produces an output of `91`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d8052-105">例</span><span class="sxs-lookup"><span data-stu-id="d8052-105">Example</span></span>  
 <span data-ttu-id="d8052-106">データベース内の `Customers` の数をカウントする例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d8052-106">The following example counts the number of `Customers` in the database.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#4)]
 [!code-vb[DLinqQueryExamples#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#4)]  
  
## <a name="example"></a><span data-ttu-id="d8052-107">例</span><span class="sxs-lookup"><span data-stu-id="d8052-107">Example</span></span>  
 <span data-ttu-id="d8052-108">データベース内の製品のうち、生産中止になっていない製品の数をカウントする例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d8052-108">The following example counts the number of products in the database that have not been discontinued.</span></span>  
  
 <span data-ttu-id="d8052-109">Northwind サンプル データベースに対してこのクエリを実行すると、出力は `69` になります。</span><span class="sxs-lookup"><span data-stu-id="d8052-109">Running this example against the Northwind sample database produces an output of `69`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#5](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#5)]
 [!code-vb[DLinqQueryExamples#5](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#5)]  
  
## <a name="see-also"></a><span data-ttu-id="d8052-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="d8052-110">See also</span></span>
- [<span data-ttu-id="d8052-111">集計クエリ</span><span class="sxs-lookup"><span data-stu-id="d8052-111">Aggregate Queries</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/aggregate-queries.md)
- [<span data-ttu-id="d8052-112">サンプル データベースのダウンロード</span><span class="sxs-lookup"><span data-stu-id="d8052-112">Downloading Sample Databases</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)
