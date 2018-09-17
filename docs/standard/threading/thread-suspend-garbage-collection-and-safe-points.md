---
title: Thread.Suspend、ガベージ コレクション、およびセーフ ポイント
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- suspending threads
- safe points
- threading [.NET Framework], suspending
- threading [.NET Framework], garbage collection
- garbage collection, threads
ms.assetid: e8f58e17-2714-4821-802a-f8eb3b2baa62
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fc3af01167fe97b701bdb0c7bc37af02d8e8a77c
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2018
ms.locfileid: "45658588"
---
# <a name="threadsuspend-garbage-collection-and-safe-points"></a><span data-ttu-id="f3cde-102">Thread.Suspend、ガベージ コレクション、およびセーフ ポイント</span><span class="sxs-lookup"><span data-stu-id="f3cde-102">Thread.Suspend, Garbage Collection, and Safe Points</span></span>
<span data-ttu-id="f3cde-103">スレッドで <xref:System.Threading.Thread.Suspend%2A?displayProperty=nameWithType> を呼び出すと、システムはスレッドの中断が要求されたことを示し、スレッドを実際に中断する前にセーフ ポイントに到達するまでスレッドを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="f3cde-103">When you call <xref:System.Threading.Thread.Suspend%2A?displayProperty=nameWithType> on a thread, the system notes that a thread suspension has been requested and allows the thread to execute until it has reached a safe point before actually suspending the thread.</span></span> <span data-ttu-id="f3cde-104">スレッドのセーフ ポイントは、ガベージ コレクションを実行できる実行ポイントです。</span><span class="sxs-lookup"><span data-stu-id="f3cde-104">A safe point for a thread is a point in its execution at which garbage collection can be performed.</span></span>  
  
 <span data-ttu-id="f3cde-105">セーフ ポイントに到達すると、ランタイムにより、中断されたスレッドがマネージド コードで続行されないことが保証されます。</span><span class="sxs-lookup"><span data-stu-id="f3cde-105">Once a safe point is reached, the runtime guarantees that the suspended thread will not make any further progress in managed code.</span></span> <span data-ttu-id="f3cde-106">マネージド コードの外部で実行中のスレッドは、通常、ガベージ コレクションでは安全であり、その実行はマネージド コードの実行再開が試行されるまで続行します。</span><span class="sxs-lookup"><span data-stu-id="f3cde-106">A thread executing outside managed code is always safe for garbage collection, and its execution continues until it attempts to resume execution of managed code.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f3cde-107">ガベージ コレクションを実行するために、ランタイムはコレクションを実行中のスレッドを除くすべてのスレッドを中断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3cde-107">In order to perform a garbage collection, the runtime must suspend all the threads except the thread performing the collection.</span></span> <span data-ttu-id="f3cde-108">各スレッドを中断するには、セーフ ポイントに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3cde-108">Each thread must be brought to a safe point before it can be suspended.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3cde-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="f3cde-109">See also</span></span>

- <xref:System.Threading.Thread>  
- <xref:System.GC>  
- [<span data-ttu-id="f3cde-110">スレッド化</span><span class="sxs-lookup"><span data-stu-id="f3cde-110">Threading</span></span>](../../../docs/standard/threading/index.md)  
- [<span data-ttu-id="f3cde-111">自動メモリ管理</span><span class="sxs-lookup"><span data-stu-id="f3cde-111">Automatic Memory Management</span></span>](../../../docs/standard/automatic-memory-management.md)
