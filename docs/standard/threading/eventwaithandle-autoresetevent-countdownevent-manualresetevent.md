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
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "48583153"
---
# <a name="eventwaithandle-autoresetevent-countdownevent-manualresetevent"></a>EventWaitHandle、AutoResetEvent、CountdownEvent、ManualResetEvent

イベント待機ハンドルを使用して、スレッドでお互いにシグナル通知し、それぞれのシグナルを待機することで、スレッドの動作を同期できます。 これらの同期イベントはオペレーティング システムの待機ハンドルに基づいており、通知を受けると自動的にリセットされるものと、手動でリセットされるものの 2 種類があります。  
  
イベント待機ハンドルは、<xref:System.Threading.Monitor> クラスと同じ多くの同期シナリオで有用です。 イベント待機ハンドルは、多くの場合、<xref:System.Threading.Monitor.Wait%2A?displayProperty=nameWithType> および <xref:System.Threading.Monitor.Pulse%2A?displayProperty=nameWithType> メソッドより使いやすく、シグナル化を細かく制御できます。 名前付きのイベント待機ハンドルを使用して、アプリケーション ドメイン間やプロセス間で動作を同期させるためにも使用できます。これに対し、モニターはアプリケーション ドメインに対してローカルです。  
  
## <a name="in-this-section"></a>このセクションの内容

 [EventWaitHandle](eventwaithandle.md)  
 <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType> クラスは、自動または手動のリセット イベントを表します。また、ローカル イベントまたは名前付きのシステム イベントのいずれかです。  
  
 [AutoResetEvent](autoresetevent.md)  
 <xref:System.Threading.AutoResetEvent?displayProperty=nameWithType> クラスは <xref:System.Threading.EventWaitHandle> から派生し、自動的にリセットされるローカル イベントを表します。  
  
 [ManualResetEvent と ManualResetEventSlim](manualresetevent-and-manualreseteventslim.md)  
 <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> クラスは <xref:System.Threading.EventWaitHandle> から派生し、手動でリセットする必要があるローカル イベントを表します。 <xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> クラスは軽量で高速なバージョンであり、同じプロセス内のイベントに使用できます。  
  
 [CountdownEvent](countdownevent.md)  
 <xref:System.Threading.CountdownEvent?displayProperty=nameWithType> クラスは、待機ハンドルを使用するコード内の fork/join 並列処理パターンを簡単に実装する簡素化された方法を提供します。  

## <a name="see-also"></a>関連項目

- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- <xref:System.Threading.Barrier?displayProperty=nameWithType>
- [スレッド処理オブジェクトと機能](threading-objects-and-features.md)
- [マネージド スレッド処理の基本](managed-threading-basics.md)
