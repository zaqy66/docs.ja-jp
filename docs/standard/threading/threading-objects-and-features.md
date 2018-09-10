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
# <a name="threading-objects-and-features"></a>スレッド処理オブジェクトと機能

.NET では、<xref:System.Threading.Thread?displayProperty=nameWithType> クラスの他に、マルチ スレッド アプリケーションを開発するのに役立つ複数のクラスが提供されます。 次の記事では、それらのクラスの概要を説明します。

|Title|説明|  
|-----------|-----------------|  
|[マネージド スレッド プール](the-managed-thread-pool.md)|.NET によって管理されるワーカー スレッドのプールを提供する <xref:System.Threading.ThreadPool?displayProperty=nameWithType> について説明します。|  
|[タイマー](timers.md)|マルチスレッド環境で使用できるタイマーについて説明します。|
|[同期プリミティブの概要](overview-of-synchronization-primitives.md)|データへのアクセスを同期化する場合や、スレッドの相互作用を制御する場合に使用できるクラスについて説明します。|
|[EventWaitHandle、AutoResetEvent、CountdownEvent、ManualResetEvent](eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)|通知を行ったり通知を待機したりすることによりスレッドの活動を同期するために使用するマネージド イベント待機ハンドルについて説明します。|
|[ミューテックス](mutexes.md)|<xref:System.Threading.Mutex?displayProperty=nameWithType> を使用してオブジェクトへのアクセスの同期化または独自の同期機構の構築を行う方法について説明します。|
|[インタロックされた操作](interlocked-operations.md)|複数のスレッドで共有される変数にアトミックの操作を提供する <xref:System.Threading.Interlocked?displayProperty=nameWithType> クラスについて説明します。|
|[読み取り/書き込みロック](reader-writer-locks.md)|単一ライター/複数参照セマンティクスを提供する <xref:System.Threading.ReaderWriterLockSlim?displayProperty=nameWithType> クラスについて説明します。|
|[Semaphore と SemaphoreSlim](semaphore-and-semaphoreslim.md)|<xref:System.Threading.Semaphore?displayProperty=nameWithType> クラスについて、さらにそのクラスを使用して制限されたリソースへのアクセスを制御する方法について説明します。|
|[バリア](barrier.md)|段階的な操作におけるスレッドの調整のためのバリア パターンを実装する <xref:System.Threading.Barrier?displayProperty=nameWithType> クラスについて説明します。|
|[SpinLock](spinlock.md)|特定の下位レベルのシナリオで <xref:System.Threading.Monitor?displayProperty=nameWithType> クラスの代わりに軽量クラスとして使用できる <xref:System.Threading.SpinLock?displayProperty=nameWithType> クラスについて説明します。|
|[SpinWait](spinwait.md)|カーネル ベースの待機を開始する前にビジー スピンを実行する下位レベルの同期プリミティブである <xref:System.Threading.SpinWait?displayProperty=nameWithType> クラスについて説明します。|

## <a name="see-also"></a>関連項目

- <xref:System.Threading.Monitor?displayProperty=nameWithType>
- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- <xref:System.ComponentModel.BackgroundWorker?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Parallel?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Task?displayProperty=nameWithType>
- [スレッドの使用とスレッド処理](using-threads-and-threading.md)
- [非同期ファイル I/O](../io/asynchronous-file-i-o.md)
- [並列プログラミング](../parallel-programming/index.md)
- [タスク並列ライブラリ (TPL)](../parallel-programming/task-parallel-library-tpl.md)
