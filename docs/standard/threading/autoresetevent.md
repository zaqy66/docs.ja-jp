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
ms.openlocfilehash: c1785ce223f0dcd4da7ea6ef9fa3a3e897a39dca
ms.sourcegitcommit: dc02d7d95f1e3efcc7166eaf431b0ec0dc9d8dca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2018
ms.locfileid: "37143519"
---
# <a name="autoresetevent"></a>AutoResetEvent
<xref:System.Threading.AutoResetEvent> クラスは、単一の待機スレッドを解放した後、シグナル状態になると自動的にリセットするローカル待機ハンドル イベントを表します。 このクラスは、その基底クラス <xref:System.Threading.EventWaitHandle> の特殊なケースを表します。 自動リセット イベントの使用方法と機能については、[EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) の概念に関する文書を参照してください。  
  
 <xref:System.Threading.AutoResetEvent> オブジェクトは、単一の待機スレッドが解放された後、システムによって自動的に非シグナルにリセットされます。 待機しているスレッドがない場合でも、イベント オブジェクトの状態はシグナルのままです。 <xref:System.Threading.AutoResetEvent> は、`bManualReset` 引数に対して `false` を指定する、Win32 `CreateEvent` 呼び出しに対応します。  
  
 <xref:System.Threading.AutoResetEvent> の使用例については、「<xref:System.Threading.Monitor>」を参照してください。  
  
## <a name="see-also"></a>参照  
 <xref:System.Threading.ManualResetEvent>  
 <xref:System.Threading.Monitor>  
 [EventWaitHandle、AutoResetEvent、CountdownEvent、ManualResetEvent](../../../docs/standard/threading/eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)  
 [スレッド化](../../../docs/standard/threading/index.md)  
 [スレッド処理オブジェクトと機能](../../../docs/standard/threading/threading-objects-and-features.md)  
 [待機ハンドル](http://msdn.microsoft.com/library/48d10b6f-5fd7-407c-86ab-0179aef72489)
