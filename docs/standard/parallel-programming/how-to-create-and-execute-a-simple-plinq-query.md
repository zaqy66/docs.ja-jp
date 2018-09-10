---
title: '方法: 単純な PLINQ クエリを作成して実行する'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- PLINQ queries, how to create
ms.assetid: 983b4213-bddd-4a44-9262-cbe59186df4c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 544ea0f89dfa518c2ef18bffe2609d72e6fdee70
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44085041"
---
# <a name="how-to-create-and-execute-a-simple-plinq-query"></a><span data-ttu-id="3e082-102">方法: 単純な PLINQ クエリを作成して実行する</span><span class="sxs-lookup"><span data-stu-id="3e082-102">How to: Create and Execute a Simple PLINQ Query</span></span>
<span data-ttu-id="3e082-103">次の例に、ソース シーケンスに対する <xref:System.Linq.ParallelEnumerable.AsParallel%2A> 拡張メソッドを使用して単純な並列 LINQ クエリを作成し、<xref:System.Linq.ParallelEnumerable.ForAll%2A> メソッドを使用して、そのクエリを実行する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3e082-103">The following example shows how to create a simple Parallel LINQ query by using the <xref:System.Linq.ParallelEnumerable.AsParallel%2A> extension method on the source sequence, and executing the query by using the <xref:System.Linq.ParallelEnumerable.ForAll%2A> method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3e082-104">ここでは、ラムダ式を使用して PLINQ でデリゲートを定義します。</span><span class="sxs-lookup"><span data-stu-id="3e082-104">This documentation uses lambda expressions to define delegates in PLINQ.</span></span> <span data-ttu-id="3e082-105">C# または Visual Basic のラムダ式についての情報が必要な場合は、「[Lambda Expressions in PLINQ and TPL (PLINQ および TPL のラムダ式)](../../../docs/standard/parallel-programming/lambda-expressions-in-plinq-and-tpl.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e082-105">If you are not familiar with lambda expressions in C# or Visual Basic, see [Lambda Expressions in PLINQ and TPL](../../../docs/standard/parallel-programming/lambda-expressions-in-plinq-and-tpl.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="3e082-106">例</span><span class="sxs-lookup"><span data-stu-id="3e082-106">Example</span></span>  
 [!code-csharp[PLINQ#11](../../../samples/snippets/csharp/VS_Snippets_Misc/plinq/cs/create1.cs#11)]
 [!code-vb[PLINQ#11](../../../samples/snippets/visualbasic/VS_Snippets_Misc/plinq/vb/create1.vb#11)]  
  
 <span data-ttu-id="3e082-107">この例で示しているのは、結果シーケンスの順序付けが重要ではない場合に、並列 LINQ クエリを作成して実行する基本的なパターンです。通常、順序なしのクエリは、順序ありのクエリより高速になります。</span><span class="sxs-lookup"><span data-stu-id="3e082-107">This example demonstrates the basic pattern for creating and executing any Parallel LINQ query when the ordering of the result sequence is not important; unordered queries are generally faster than ordered queries.</span></span> <span data-ttu-id="3e082-108">このクエリはソースを、複数のスレッドで非同期的に実行した複数のタスクにパーティション分割します。</span><span class="sxs-lookup"><span data-stu-id="3e082-108">The query partitions the source into tasks that are executed asynchronously on multiple threads.</span></span> <span data-ttu-id="3e082-109">各タスクが完了する順序は、その特定のパーティションに含まれる要素を処理するために必要な作業量だけでなく、オペレーティング システムが各スレッドをどのようにスケジュールするかといった外部要因にも依存します。</span><span class="sxs-lookup"><span data-stu-id="3e082-109">The order in which each task completes depends not only on the amount of work involved to process the elements in the partition, but also on external factors such as how the operating system schedules each thread.</span></span> <span data-ttu-id="3e082-110">この例は、使用方法を示すことを意図したものであるため、同等の順次的な LINQ to Objects クエリほど高速ではない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3e082-110">This example is intended to demonstrate usage, and might not run faster than the equivalent sequential LINQ to Objects query.</span></span> <span data-ttu-id="3e082-111">高速化の詳細については、「[PLINQ での高速化について](../../../docs/standard/parallel-programming/understanding-speedup-in-plinq.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e082-111">For more information about speedup, see [Understanding Speedup in PLINQ](../../../docs/standard/parallel-programming/understanding-speedup-in-plinq.md).</span></span> <span data-ttu-id="3e082-112">クエリの要素の順序を保持する方法の詳細については、「[方法: PLINQ クエリの順序を制御する](../../../docs/standard/parallel-programming/how-to-control-ordering-in-a-plinq-query.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e082-112">For more information about how to preserve the ordering of elements in a query, see [How to: Control Ordering in a PLINQ Query](../../../docs/standard/parallel-programming/how-to-control-ordering-in-a-plinq-query.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e082-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="3e082-113">See also</span></span>

- [<span data-ttu-id="3e082-114">Parallel LINQ (PLINQ)</span><span class="sxs-lookup"><span data-stu-id="3e082-114">Parallel LINQ (PLINQ)</span></span>](../../../docs/standard/parallel-programming/parallel-linq-plinq.md)
