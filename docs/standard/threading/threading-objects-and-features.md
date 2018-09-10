---
title: スレッド処理オブジェクトと機能
ms.date: 08/16/2018
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], features
- managed threading
ms.assetid: 239b2e8d-581b-4ca3-992b-0e8525b9321c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2d56d962279120a03a6e4b89154ac1429ea5479e
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "44039330"
---
# <a name="threading-objects-and-features"></a><span data-ttu-id="86cda-102">スレッド処理オブジェクトと機能</span><span class="sxs-lookup"><span data-stu-id="86cda-102">Threading objects and features</span></span>

<span data-ttu-id="86cda-103">.NET では、<xref:System.Threading.Thread?displayProperty=nameWithType> クラスの他に、マルチ スレッド アプリケーションを開発するのに役立つ複数のクラスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="86cda-103">Along with the <xref:System.Threading.Thread?displayProperty=nameWithType> class, .NET provides a number of classes that help you develop multithreaded applications.</span></span> <span data-ttu-id="86cda-104">次の記事では、それらのクラスの概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="86cda-104">The following articles provide overview of those classes:</span></span>

|<span data-ttu-id="86cda-105">Title</span><span class="sxs-lookup"><span data-stu-id="86cda-105">Title</span></span>|<span data-ttu-id="86cda-106">説明</span><span class="sxs-lookup"><span data-stu-id="86cda-106">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="86cda-107">マネージド スレッド プール</span><span class="sxs-lookup"><span data-stu-id="86cda-107">The managed thread pool</span></span>](the-managed-thread-pool.md)|<span data-ttu-id="86cda-108">.NET によって管理されるワーカー スレッドのプールを提供する <xref:System.Threading.ThreadPool?displayProperty=nameWithType> について説明します。</span><span class="sxs-lookup"><span data-stu-id="86cda-108">Describes the <xref:System.Threading.ThreadPool?displayProperty=nameWithType> class, which provides a pool of worker threads that are managed by .NET.</span></span>|  
|[<span data-ttu-id="86cda-109">タイマー</span><span class="sxs-lookup"><span data-stu-id="86cda-109">Timers</span></span>](timers.md)|<span data-ttu-id="86cda-110">マルチスレッド環境で使用できるタイマーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="86cda-110">Describes timers that can be used in a multithreaded environment.</span></span>|
|[<span data-ttu-id="86cda-111">同期プリミティブの概要</span><span class="sxs-lookup"><span data-stu-id="86cda-111">Overview of synchronization primitives</span></span>](overview-of-synchronization-primitives.md)|<span data-ttu-id="86cda-112">データへのアクセスを同期化する場合や、スレッドの相互作用を制御する場合に使用できるクラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="86cda-112">Describes classes that can be used to synchronize access to data or control thread interaction.</span></span>|
|[<span data-ttu-id="86cda-113">EventWaitHandle、AutoResetEvent、CountdownEvent、ManualResetEvent</span><span class="sxs-lookup"><span data-stu-id="86cda-113">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span></span>](eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)|<span data-ttu-id="86cda-114">通知を行ったり通知を待機したりすることによりスレッドの活動を同期するために使用するマネージド イベント待機ハンドルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="86cda-114">Describes managed event wait handles, which are used to synchronize thread activities by signaling and waiting for signals.</span></span>|
|[<span data-ttu-id="86cda-115">ミューテックス</span><span class="sxs-lookup"><span data-stu-id="86cda-115">Mutexes</span></span>](mutexes.md)|<span data-ttu-id="86cda-116"><xref:System.Threading.Mutex?displayProperty=nameWithType> を使用してオブジェクトへのアクセスの同期化または独自の同期機構の構築を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="86cda-116">Describes how to use a <xref:System.Threading.Mutex?displayProperty=nameWithType> to synchronize access to an object or to build your own synchronization mechanisms.</span></span>|
|[<span data-ttu-id="86cda-117">インタロックされた操作</span><span class="sxs-lookup"><span data-stu-id="86cda-117">Interlocked operations</span></span>](interlocked-operations.md)|<span data-ttu-id="86cda-118">複数のスレッドで共有される変数にアトミックの操作を提供する <xref:System.Threading.Interlocked?displayProperty=nameWithType> クラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="86cda-118">Describes the <xref:System.Threading.Interlocked?displayProperty=nameWithType> class, which provides atomic operations for variables that are shared by multiple threads.</span></span>|
|[<span data-ttu-id="86cda-119">読み取り/書き込みロック</span><span class="sxs-lookup"><span data-stu-id="86cda-119">Reader-Writer Locks</span></span>](reader-writer-locks.md)|<span data-ttu-id="86cda-120">単一ライター/複数参照セマンティクスを提供する <xref:System.Threading.ReaderWriterLockSlim?displayProperty=nameWithType> クラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="86cda-120">Describes the <xref:System.Threading.ReaderWriterLockSlim?displayProperty=nameWithType> class, which provides single-writer/multiple-reader semantics.</span></span>|
|[<span data-ttu-id="86cda-121">Semaphore と SemaphoreSlim</span><span class="sxs-lookup"><span data-stu-id="86cda-121">Semaphore and SemaphoreSlim</span></span>](semaphore-and-semaphoreslim.md)|<span data-ttu-id="86cda-122"><xref:System.Threading.Semaphore?displayProperty=nameWithType> クラスについて、さらにそのクラスを使用して制限されたリソースへのアクセスを制御する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="86cda-122">Describes the <xref:System.Threading.Semaphore?displayProperty=nameWithType> class and explains how to use it to control access to limited resources.</span></span>|
|[<span data-ttu-id="86cda-123">バリア</span><span class="sxs-lookup"><span data-stu-id="86cda-123">Barrier</span></span>](barrier.md)|<span data-ttu-id="86cda-124">段階的な操作におけるスレッドの調整のためのバリア パターンを実装する <xref:System.Threading.Barrier?displayProperty=nameWithType> クラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="86cda-124">Describes the <xref:System.Threading.Barrier?displayProperty=nameWithType> class that implements the barrier pattern for coordination of threads in phased operations.</span></span>|
|[<span data-ttu-id="86cda-125">SpinLock</span><span class="sxs-lookup"><span data-stu-id="86cda-125">SpinLock</span></span>](spinlock.md)|<span data-ttu-id="86cda-126">特定の下位レベルのシナリオで <xref:System.Threading.Monitor?displayProperty=nameWithType> クラスの代わりに軽量クラスとして使用できる <xref:System.Threading.SpinLock?displayProperty=nameWithType> クラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="86cda-126">Describes the <xref:System.Threading.SpinLock?displayProperty=nameWithType> class, which is a lightweight alternative to the <xref:System.Threading.Monitor?displayProperty=nameWithType> class for certain low-level scenarios.</span></span>|
|[<span data-ttu-id="86cda-127">SpinWait</span><span class="sxs-lookup"><span data-stu-id="86cda-127">SpinWait</span></span>](spinwait.md)|<span data-ttu-id="86cda-128">カーネル ベースの待機を開始する前にビジー スピンを実行する下位レベルの同期プリミティブである <xref:System.Threading.SpinWait?displayProperty=nameWithType> クラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="86cda-128">Describes the <xref:System.Threading.SpinWait?displayProperty=nameWithType> class, which is a low-level synchronization primitive that performs busy spinning prior to initiating a kernel-based wait.</span></span>|

## <a name="see-also"></a><span data-ttu-id="86cda-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="86cda-129">See also</span></span>

- <xref:System.Threading.Monitor?displayProperty=nameWithType>
- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- <xref:System.ComponentModel.BackgroundWorker?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Parallel?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Task?displayProperty=nameWithType>
- [<span data-ttu-id="86cda-130">スレッドの使用とスレッド処理</span><span class="sxs-lookup"><span data-stu-id="86cda-130">Using threads and threading</span></span>](using-threads-and-threading.md)
- [<span data-ttu-id="86cda-131">非同期ファイル I/O</span><span class="sxs-lookup"><span data-stu-id="86cda-131">Asynchronous File I/O</span></span>](../io/asynchronous-file-i-o.md)
- [<span data-ttu-id="86cda-132">並列プログラミング</span><span class="sxs-lookup"><span data-stu-id="86cda-132">Parallel Programming</span></span>](../parallel-programming/index.md)
- [<span data-ttu-id="86cda-133">タスク並列ライブラリ (TPL)</span><span class="sxs-lookup"><span data-stu-id="86cda-133">Task Parallel Library (TPL)</span></span>](../parallel-programming/task-parallel-library-tpl.md)
