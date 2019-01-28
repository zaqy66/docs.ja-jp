---
title: AutoResetEvent
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], AutoResetEvent class
- AutoResetEvent class
ms.assetid: 6d39c48d-6b37-4a9b-8631-f2924cfd9c18
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 70af739bdb90a70a1319354b4964c261e432912b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54729958"
---
# <a name="autoresetevent"></a><span data-ttu-id="57ad6-102">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="57ad6-102">AutoResetEvent</span></span>
<span data-ttu-id="57ad6-103"><xref:System.Threading.AutoResetEvent> クラスは、単一の待機スレッドを解放した後、シグナル状態になると自動的にリセットするローカル待機ハンドル イベントを表します。</span><span class="sxs-lookup"><span data-stu-id="57ad6-103">The <xref:System.Threading.AutoResetEvent> class represents a local wait handle event that resets automatically when signaled, after releasing a single waiting thread.</span></span> <span data-ttu-id="57ad6-104">このクラスは、その基底クラス <xref:System.Threading.EventWaitHandle> の特殊なケースを表します。</span><span class="sxs-lookup"><span data-stu-id="57ad6-104">This class represents a special case of its base class, <xref:System.Threading.EventWaitHandle>.</span></span> <span data-ttu-id="57ad6-105">自動リセット イベントの使用方法と機能については、[EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) の概念に関する文書を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57ad6-105">See the [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) conceptual documentation for the use and features of automatic reset events.</span></span>  
  
 <span data-ttu-id="57ad6-106"><xref:System.Threading.AutoResetEvent> オブジェクトは、単一の待機スレッドが解放された後、システムによって自動的に非シグナルにリセットされます。</span><span class="sxs-lookup"><span data-stu-id="57ad6-106">An <xref:System.Threading.AutoResetEvent> object is automatically reset to non-signaled by the system after a single waiting thread has been released.</span></span> <span data-ttu-id="57ad6-107">待機しているスレッドがない場合でも、イベント オブジェクトの状態はシグナルのままです。</span><span class="sxs-lookup"><span data-stu-id="57ad6-107">If no threads are waiting, the event object's state remains signaled.</span></span>
  
 <span data-ttu-id="57ad6-108"><xref:System.Threading.AutoResetEvent> の使用例については、「<xref:System.Threading.Monitor>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57ad6-108">For an example that uses <xref:System.Threading.AutoResetEvent>, see <xref:System.Threading.Monitor>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57ad6-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="57ad6-109">See also</span></span>

- <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType>
- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- [<span data-ttu-id="57ad6-110">EventWaitHandle、AutoResetEvent、CountdownEvent、ManualResetEvent</span><span class="sxs-lookup"><span data-stu-id="57ad6-110">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span></span>](eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)
- [<span data-ttu-id="57ad6-111">スレッド処理オブジェクトと機能</span><span class="sxs-lookup"><span data-stu-id="57ad6-111">Threading objects and features</span></span>](threading-objects-and-features.md)
- [<span data-ttu-id="57ad6-112">スレッド化</span><span class="sxs-lookup"><span data-stu-id="57ad6-112">Threading</span></span>](index.md)
