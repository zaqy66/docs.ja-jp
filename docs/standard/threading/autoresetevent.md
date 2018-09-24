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
ms.openlocfilehash: 38efbe0ecd88c02752d610de4b1eec8b62eca1f8
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2018
ms.locfileid: "46937548"
---
# <a name="autoresetevent"></a><span data-ttu-id="2144b-102">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="2144b-102">AutoResetEvent</span></span>
<span data-ttu-id="2144b-103"><xref:System.Threading.AutoResetEvent> クラスは、単一の待機スレッドを解放した後、シグナル状態になると自動的にリセットするローカル待機ハンドル イベントを表します。</span><span class="sxs-lookup"><span data-stu-id="2144b-103">The <xref:System.Threading.AutoResetEvent> class represents a local wait handle event that resets automatically when signaled, after releasing a single waiting thread.</span></span> <span data-ttu-id="2144b-104">このクラスは、その基底クラス <xref:System.Threading.EventWaitHandle> の特殊なケースを表します。</span><span class="sxs-lookup"><span data-stu-id="2144b-104">This class represents a special case of its base class, <xref:System.Threading.EventWaitHandle>.</span></span> <span data-ttu-id="2144b-105">自動リセット イベントの使用方法と機能については、[EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) の概念に関する文書を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2144b-105">See the [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) conceptual documentation for the use and features of automatic reset events.</span></span>  
  
 <span data-ttu-id="2144b-106"><xref:System.Threading.AutoResetEvent> オブジェクトは、単一の待機スレッドが解放された後、システムによって自動的に非シグナルにリセットされます。</span><span class="sxs-lookup"><span data-stu-id="2144b-106">An <xref:System.Threading.AutoResetEvent> object is automatically reset to non-signaled by the system after a single waiting thread has been released.</span></span> <span data-ttu-id="2144b-107">待機しているスレッドがない場合でも、イベント オブジェクトの状態はシグナルのままです。</span><span class="sxs-lookup"><span data-stu-id="2144b-107">If no threads are waiting, the event object's state remains signaled.</span></span>
  
 <span data-ttu-id="2144b-108"><xref:System.Threading.AutoResetEvent> の使用例については、「<xref:System.Threading.Monitor>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2144b-108">For an example that uses <xref:System.Threading.AutoResetEvent>, see <xref:System.Threading.Monitor>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2144b-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="2144b-109">See also</span></span>

- <xref:System.Threading.ManualResetEvent>  
- <xref:System.Threading.Monitor>  
- [<span data-ttu-id="2144b-110">EventWaitHandle、AutoResetEvent、CountdownEvent、ManualResetEvent</span><span class="sxs-lookup"><span data-stu-id="2144b-110">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span></span>](../../../docs/standard/threading/eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)  
- [<span data-ttu-id="2144b-111">スレッド化</span><span class="sxs-lookup"><span data-stu-id="2144b-111">Threading</span></span>](../../../docs/standard/threading/index.md)  
- [<span data-ttu-id="2144b-112">スレッド処理オブジェクトと機能</span><span class="sxs-lookup"><span data-stu-id="2144b-112">Threading Objects and Features</span></span>](../../../docs/standard/threading/threading-objects-and-features.md)  
- [<span data-ttu-id="2144b-113">待機ハンドル</span><span class="sxs-lookup"><span data-stu-id="2144b-113">Wait Handles</span></span>](https://msdn.microsoft.com/library/48d10b6f-5fd7-407c-86ab-0179aef72489)
