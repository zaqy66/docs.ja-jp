---
title: EventWaitHandle、AutoResetEvent、CountdownEvent、ManualResetEvent
ms.date: 09/14/2018
ms.technology: dotnet-standard
helpviewer_keywords:
- wait handles
- threading [.NET Framework], EventWaitHandle class
- event wait handles [.NET Framework]
ms.assetid: cd94fc34-ac15-427f-b723-a1240a4fab7d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: be9c858d7c76fdcc1b3e02485eb0b459f4e7555c
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2018
ms.locfileid: "47205921"
---
# <a name="eventwaithandle-autoresetevent-countdownevent-manualresetevent"></a><span data-ttu-id="b8a47-102">EventWaitHandle、AutoResetEvent、CountdownEvent、ManualResetEvent</span><span class="sxs-lookup"><span data-stu-id="b8a47-102">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span></span>

<span data-ttu-id="b8a47-103">イベント待機ハンドルを使用して、スレッドでお互いにシグナル通知し、それぞれのシグナルを待機することで、スレッドの動作を同期できます。</span><span class="sxs-lookup"><span data-stu-id="b8a47-103">Event wait handles allow threads to synchronize activities by signaling each other and by waiting on each other's signals.</span></span> <span data-ttu-id="b8a47-104">これらの同期イベントはオペレーティング システムの待機ハンドルに基づいており、通知を受けると自動的にリセットされるものと、手動でリセットされるものの 2 種類があります。</span><span class="sxs-lookup"><span data-stu-id="b8a47-104">These synchronization events are based on operating system wait handles and can be divided into two types: those that reset automatically when signaled and those that are reset manually.</span></span>  
  
<span data-ttu-id="b8a47-105">イベント待機ハンドルは、<xref:System.Threading.Monitor> クラスと同じ多くの同期シナリオで有用です。</span><span class="sxs-lookup"><span data-stu-id="b8a47-105">Event wait handles are useful in many of the same synchronization scenarios as the <xref:System.Threading.Monitor> class.</span></span> <span data-ttu-id="b8a47-106">イベント待機ハンドルは、多くの場合、<xref:System.Threading.Monitor.Wait%2A?displayProperty=nameWithType> および <xref:System.Threading.Monitor.Pulse%2A?displayProperty=nameWithType> メソッドより使いやすく、シグナル化を細かく制御できます。</span><span class="sxs-lookup"><span data-stu-id="b8a47-106">Event wait handles are often easier to use than the <xref:System.Threading.Monitor.Wait%2A?displayProperty=nameWithType> and <xref:System.Threading.Monitor.Pulse%2A?displayProperty=nameWithType> methods, and they offer more control over signaling.</span></span> <span data-ttu-id="b8a47-107">名前付きのイベント待機ハンドルを使用して、アプリケーション ドメイン間やプロセス間で動作を同期させるためにも使用できます。これに対し、モニターはアプリケーション ドメインに対してローカルです。</span><span class="sxs-lookup"><span data-stu-id="b8a47-107">Named event wait handles can also be used to synchronize activities across application domains and processes, whereas monitors are local to an application domain.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b8a47-108">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="b8a47-108">In this section</span></span>

 [<span data-ttu-id="b8a47-109">EventWaitHandle</span><span class="sxs-lookup"><span data-stu-id="b8a47-109">EventWaitHandle</span></span>](eventwaithandle.md)  
 <span data-ttu-id="b8a47-110"><xref:System.Threading.EventWaitHandle?displayProperty=nameWithType> クラスは、自動または手動のリセット イベントを表します。また、ローカル イベントまたは名前付きのシステム イベントのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="b8a47-110">The <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType> class can represent either automatic or manual reset events and either local events or named system events.</span></span>  
  
 [<span data-ttu-id="b8a47-111">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="b8a47-111">AutoResetEvent</span></span>](autoresetevent.md)  
 <span data-ttu-id="b8a47-112"><xref:System.Threading.AutoResetEvent?displayProperty=nameWithType> クラスは <xref:System.Threading.EventWaitHandle> から派生し、自動的にリセットされるローカル イベントを表します。</span><span class="sxs-lookup"><span data-stu-id="b8a47-112">The <xref:System.Threading.AutoResetEvent?displayProperty=nameWithType> class derives from <xref:System.Threading.EventWaitHandle> and represents a local event that resets automatically.</span></span>  
  
 [<span data-ttu-id="b8a47-113">ManualResetEvent と ManualResetEventSlim</span><span class="sxs-lookup"><span data-stu-id="b8a47-113">ManualResetEvent and ManualResetEventSlim</span></span>](manualresetevent-and-manualreseteventslim.md)  
 <span data-ttu-id="b8a47-114"><xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> クラスは <xref:System.Threading.EventWaitHandle> から派生し、手動でリセットする必要があるローカル イベントを表します。</span><span class="sxs-lookup"><span data-stu-id="b8a47-114">The <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> class derives from <xref:System.Threading.EventWaitHandle> and represents a local event that must be reset manually.</span></span> <span data-ttu-id="b8a47-115"><xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> クラスは軽量で高速なバージョンであり、同じプロセス内のイベントに使用できます。</span><span class="sxs-lookup"><span data-stu-id="b8a47-115">The <xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> class is a lightweight, faster version that can be used for events within the same process.</span></span>  
  
 [<span data-ttu-id="b8a47-116">CountdownEvent</span><span class="sxs-lookup"><span data-stu-id="b8a47-116">CountdownEvent</span></span>](countdownevent.md)  
 <span data-ttu-id="b8a47-117"><xref:System.Threading.CountdownEvent?displayProperty=nameWithType> クラスは、待機ハンドルを使用するコード内の fork/join 並列処理パターンを簡単に実装する簡素化された方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="b8a47-117">The <xref:System.Threading.CountdownEvent?displayProperty=nameWithType> class provides a simplified way to implement fork/join parallelism patterns in code that uses wait handles.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b8a47-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="b8a47-118">See also</span></span>

- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- <xref:System.Threading.Barrier?displayProperty=nameWithType>
- [<span data-ttu-id="b8a47-119">スレッド処理オブジェクトと機能</span><span class="sxs-lookup"><span data-stu-id="b8a47-119">Threading objects and features</span></span>](threading-objects-and-features.md)
- [<span data-ttu-id="b8a47-120">マネージド スレッド処理の基本</span><span class="sxs-lookup"><span data-stu-id="b8a47-120">Managed threading basics</span></span>](managed-threading-basics.md)
