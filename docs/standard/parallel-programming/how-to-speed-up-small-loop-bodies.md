---
title: '方法: 小さいループ本体を高速化する'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- parallel loops, how to speed up
ms.assetid: c7a66677-cb59-4cbf-969a-d2e8fc61a6ce
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c5cb872acbe496f1f27ee9065dd3b276bbed349b
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2018
ms.locfileid: "44208414"
---
# <a name="how-to-speed-up-small-loop-bodies"></a><span data-ttu-id="ff549-102">方法: 小さいループ本体を高速化する</span><span class="sxs-lookup"><span data-stu-id="ff549-102">How to: Speed Up Small Loop Bodies</span></span>
<span data-ttu-id="ff549-103"><xref:System.Threading.Tasks.Parallel.For%2A?displayProperty=nameWithType> ループの本体が小さい場合、[for](~/docs/csharp/language-reference/keywords/for.md) ループ (C#)、[For](https://msdn.microsoft.com/library/c470a263-9b49-4308-8fd6-8592b84a7980) ループ (Visual Basic) など、同等の連続したループよりパフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ff549-103">When a <xref:System.Threading.Tasks.Parallel.For%2A?displayProperty=nameWithType> loop has a small body, it might perform more slowly than the equivalent sequential loop, such as the [for](~/docs/csharp/language-reference/keywords/for.md) loop in C# and the [For](https://msdn.microsoft.com/library/c470a263-9b49-4308-8fd6-8592b84a7980) loop in Visual Basic.</span></span> <span data-ttu-id="ff549-104">パフォーマンスの低下は、データのパーティション分割と、各ループのイテレーションでデリゲートを呼び出す負荷によって発生します。</span><span class="sxs-lookup"><span data-stu-id="ff549-104">Slower performance is caused by the overhead involved in partitioning the data and the cost of invoking a delegate on each loop iteration.</span></span> <span data-ttu-id="ff549-105">このようなシナリオに対処するため、<xref:System.Collections.Concurrent.Partitioner> クラスには <xref:System.Collections.Concurrent.Partitioner.Create%2A?displayProperty=nameWithType> メソッドが用意されています。このメソッドにより、デリゲートがイテレーションごとに 1 回ではなく、パーティションごとに 1 回だけ呼び出されるように、デリゲートの本体に順次ループを提供できるようになります。</span><span class="sxs-lookup"><span data-stu-id="ff549-105">To address such scenarios, the <xref:System.Collections.Concurrent.Partitioner> class provides the <xref:System.Collections.Concurrent.Partitioner.Create%2A?displayProperty=nameWithType> method, which enables you to provide a sequential loop for the delegate body, so that the delegate is invoked only once per partition, instead of once per iteration.</span></span> <span data-ttu-id="ff549-106">詳細については、「[Custom Partitioners for PLINQ and TPL (PLINQ および TPL 用のカスタム パーティショナー)](../../../docs/standard/parallel-programming/custom-partitioners-for-plinq-and-tpl.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ff549-106">For more information, see [Custom Partitioners for PLINQ and TPL](../../../docs/standard/parallel-programming/custom-partitioners-for-plinq-and-tpl.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ff549-107">例</span><span class="sxs-lookup"><span data-stu-id="ff549-107">Example</span></span>  
 [!code-csharp[TPL_Partitioners#01](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl_partitioners/cs/partitioner01.cs#01)]
 [!code-vb[TPL_Partitioners#01](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpl_partitioners/vb/partitionercreate01.vb#01)]  
  
 <span data-ttu-id="ff549-108">この例で示す方法は、ループが最小限の作業を実行するときに便利です。</span><span class="sxs-lookup"><span data-stu-id="ff549-108">The approach demonstrated in this example is useful when the loop performs a minimal amount of work.</span></span> <span data-ttu-id="ff549-109">作業がより負荷の大きい処理になるにつれ、既定のパーティショナーで <xref:System.Threading.Tasks.Parallel.For%2A> ループまたは <xref:System.Threading.Tasks.Parallel.ForEach%2A> ループを使用すると、同じまたはそれ以上のパフォーマンスが得られることがあります。</span><span class="sxs-lookup"><span data-stu-id="ff549-109">As the work becomes more computationally expensive, you will probably get the same or better performance by using a <xref:System.Threading.Tasks.Parallel.For%2A> or <xref:System.Threading.Tasks.Parallel.ForEach%2A> loop with the default partitioner.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff549-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="ff549-110">See also</span></span>

- [<span data-ttu-id="ff549-111">データの並列化</span><span class="sxs-lookup"><span data-stu-id="ff549-111">Data Parallelism</span></span>](../../../docs/standard/parallel-programming/data-parallelism-task-parallel-library.md)  
- [<span data-ttu-id="ff549-112">PLINQ および TPL 用のカスタム パーティショナー</span><span class="sxs-lookup"><span data-stu-id="ff549-112">Custom Partitioners for PLINQ and TPL</span></span>](../../../docs/standard/parallel-programming/custom-partitioners-for-plinq-and-tpl.md)  
- [<span data-ttu-id="ff549-113">反復子</span><span class="sxs-lookup"><span data-stu-id="ff549-113">Iterators</span></span>](https://msdn.microsoft.com/library/f45331db-d595-46ec-9142-551d3d1eb1a7)  
- [<span data-ttu-id="ff549-114">PLINQ および TPL のラムダ式</span><span class="sxs-lookup"><span data-stu-id="ff549-114">Lambda Expressions in PLINQ and TPL</span></span>](../../../docs/standard/parallel-programming/lambda-expressions-in-plinq-and-tpl.md)
