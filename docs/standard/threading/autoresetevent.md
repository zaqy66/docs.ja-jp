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
ms.openlocfilehash: 519776b5c1c237deb520476384495b8dd96a4e39
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50201307"
---
# <a name="autoresetevent"></a>AutoResetEvent
<xref:System.Threading.AutoResetEvent> クラスは、単一の待機スレッドを解放した後、シグナル状態になると自動的にリセットするローカル待機ハンドル イベントを表します。 このクラスは、その基底クラス <xref:System.Threading.EventWaitHandle> の特殊なケースを表します。 自動リセット イベントの使用方法と機能については、[EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) の概念に関する文書を参照してください。  
  
 <xref:System.Threading.AutoResetEvent> オブジェクトは、単一の待機スレッドが解放された後、システムによって自動的に非シグナルにリセットされます。 待機しているスレッドがない場合でも、イベント オブジェクトの状態はシグナルのままです。
  
 <xref:System.Threading.AutoResetEvent> の使用例については、「<xref:System.Threading.Monitor>」を参照してください。  
  
## <a name="see-also"></a>関連項目

- <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType>
- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- [EventWaitHandle、AutoResetEvent、CountdownEvent、ManualResetEvent](eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)  
- [スレッド処理オブジェクトと機能](threading-objects-and-features.md)  
- [スレッド化](index.md)  
