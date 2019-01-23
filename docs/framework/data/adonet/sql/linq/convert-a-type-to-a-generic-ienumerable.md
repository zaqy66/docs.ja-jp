---
title: 汎用 IEnumerable への型の変換
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 64774fb5-7447-4296-ad3b-8a94346f99a1
ms.openlocfilehash: d1f4c1c4a561c893b5846e6ae0b08b2d78c3589d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54509598"
---
# <a name="convert-a-type-to-a-generic-ienumerable"></a><span data-ttu-id="64841-102">汎用 IEnumerable への型の変換</span><span class="sxs-lookup"><span data-stu-id="64841-102">Convert a Type to a Generic IEnumerable</span></span>
<span data-ttu-id="64841-103">汎用 `IEnumerable` として型指定された引数を返すには、<xref:System.Linq.Enumerable.AsEnumerable%2A> を使用します。</span><span class="sxs-lookup"><span data-stu-id="64841-103">Use <xref:System.Linq.Enumerable.AsEnumerable%2A> to return the argument typed as a generic `IEnumerable`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="64841-104">例</span><span class="sxs-lookup"><span data-stu-id="64841-104">Example</span></span>  
 <span data-ttu-id="64841-105">この例では、[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] (既定の汎用 `Query` を使用) は、クエリを SQL に変換し、サーバー上での実行を試みます。</span><span class="sxs-lookup"><span data-stu-id="64841-105">In this example, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] (using the default generic `Query`) would try to convert the query to SQL and execute it on the server.</span></span> <span data-ttu-id="64841-106">しかし、`where` 句が、SQL に変換できない、ユーザー定義のクライアント側メソッド (`isValidProduct`) を参照しています。</span><span class="sxs-lookup"><span data-stu-id="64841-106">But the `where` clause references a user-defined client-side method (`isValidProduct`), which cannot be converted to SQL.</span></span>  
  
 <span data-ttu-id="64841-107">これを解決するには、クライアント側の汎用 <xref:System.Collections.Generic.IEnumerable%601> 実装の `where` を指定し、汎用 <xref:System.Linq.IQueryable%601> を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="64841-107">The solution is to specify the client-side generic <xref:System.Collections.Generic.IEnumerable%601> implementation of `where` to replace the generic <xref:System.Linq.IQueryable%601>.</span></span> <span data-ttu-id="64841-108"><xref:System.Linq.Enumerable.AsEnumerable%2A> 演算子を呼び出すことによって、これを行います。</span><span class="sxs-lookup"><span data-stu-id="64841-108">You do this by invoking the <xref:System.Linq.Enumerable.AsEnumerable%2A> operator.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#46](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#46)]
 [!code-vb[DLinqQueryExamples#46](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#46)]  
  
## <a name="see-also"></a><span data-ttu-id="64841-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="64841-109">See also</span></span>
- [<span data-ttu-id="64841-110">クエリの例</span><span class="sxs-lookup"><span data-stu-id="64841-110">Query Examples</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)
