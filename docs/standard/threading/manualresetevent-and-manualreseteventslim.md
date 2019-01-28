---
title: ManualResetEvent と ManualResetEventSlim
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], ManualResetEvent class
- ManualResetEvent class, about ManualResetEvent class
ms.assetid: 465fdcf9-ba24-4d8d-a43f-d983b7cb0cc6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 864c39aa6673537d66d8402896bce5b4fa92e5ac
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54602444"
---
# <a name="manualresetevent-and-manualreseteventslim"></a><span data-ttu-id="0a598-102">ManualResetEvent と ManualResetEventSlim</span><span class="sxs-lookup"><span data-stu-id="0a598-102">ManualResetEvent and ManualResetEventSlim</span></span>
<span data-ttu-id="0a598-103"><xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> クラスはローカル待機ハンドル イベントを表します。これは、シグナル状態になった後、手動でリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a598-103">The <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> class represents a local wait handle event that must be reset manually after it is signaled.</span></span> <span data-ttu-id="0a598-104">このクラスは、その基底クラス <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType> の特殊なケースを表します。</span><span class="sxs-lookup"><span data-stu-id="0a598-104">This class represents a special case of its base class, <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType>.</span></span> <span data-ttu-id="0a598-105">手動リセット イベントの使用方法と機能については、[EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) の概念に関する文書を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0a598-105">See the [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) conceptual documentation for the use and features of manual reset events.</span></span>  
  
 <span data-ttu-id="0a598-106"><xref:System.Threading.ManualResetEvent> オブジェクトは、<xref:System.Threading.EventWaitHandle.Reset%2A?displayProperty=nameWithType> メソッドが呼び出されるまでシグナル状態のままです。</span><span class="sxs-lookup"><span data-stu-id="0a598-106">A <xref:System.Threading.ManualResetEvent> object remains signaled until its <xref:System.Threading.EventWaitHandle.Reset%2A?displayProperty=nameWithType> method is called.</span></span> <span data-ttu-id="0a598-107">待機スレッド、つまりイベントがシグナル状態になるまで待機するスレッドは、そのオブジェクトがシグナル状態である間にいくつでも解放できます。</span><span class="sxs-lookup"><span data-stu-id="0a598-107">Any number of waiting threads, or threads that wait on the event after it has been signaled, can be released while the object's state is signaled.</span></span>
  
 <span data-ttu-id="0a598-108">[!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)] では、待機時間が非常に短いと予測される場合とイベントがプロセスの境界を越えない場合に、<xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> クラスを使用してパフォーマンスを高めることができます。</span><span class="sxs-lookup"><span data-stu-id="0a598-108">In the [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], you can use the <xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> class for better performance when wait times are expected to be very short, and when the event does not cross a process boundary.</span></span> <span data-ttu-id="0a598-109"><xref:System.Threading.ManualResetEventSlim> は、イベントがシグナル状態になるまで待機している間、ビジー スピンを短時間使用します。</span><span class="sxs-lookup"><span data-stu-id="0a598-109"><xref:System.Threading.ManualResetEventSlim> uses busy spinning for a short time while it waits for the event to become signaled.</span></span> <span data-ttu-id="0a598-110">待機時間が短い場合、待機ハンドルを使用して待機するより、スピンを使用するほうが負荷が大幅に低くなります。</span><span class="sxs-lookup"><span data-stu-id="0a598-110">When wait times are short, spinning can be much less expensive than waiting by using wait handles.</span></span> <span data-ttu-id="0a598-111">ただし、特定の期間内にイベントがシグナル状態にならない場合、<xref:System.Threading.ManualResetEventSlim> は通常のイベント ハンドル待機を使用します。</span><span class="sxs-lookup"><span data-stu-id="0a598-111">However, if the event does not become signaled within a certain period of time, <xref:System.Threading.ManualResetEventSlim> resorts to a regular event handle wait.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0a598-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="0a598-112">See also</span></span>

- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- [<span data-ttu-id="0a598-113">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="0a598-113">AutoResetEvent</span></span>](autoresetevent.md)
- [<span data-ttu-id="0a598-114">SpinWait</span><span class="sxs-lookup"><span data-stu-id="0a598-114">SpinWait</span></span>](spinwait.md)
- [<span data-ttu-id="0a598-115">Semaphore と SemaphoreSlim</span><span class="sxs-lookup"><span data-stu-id="0a598-115">Semaphore and SemaphoreSlim</span></span>](semaphore-and-semaphoreslim.md)
- [<span data-ttu-id="0a598-116">EventWaitHandle、AutoResetEvent、CountdownEvent、ManualResetEvent</span><span class="sxs-lookup"><span data-stu-id="0a598-116">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span></span>](eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)
- [<span data-ttu-id="0a598-117">スレッド処理オブジェクトと機能</span><span class="sxs-lookup"><span data-stu-id="0a598-117">Threading objects and features</span></span>](threading-objects-and-features.md)
- [<span data-ttu-id="0a598-118">スレッド化</span><span class="sxs-lookup"><span data-stu-id="0a598-118">Threading</span></span>](index.md)
