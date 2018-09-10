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
ms.openlocfilehash: 7602a61a4403b7ab85015876823aa41e250b23de
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43863310"
---
# <a name="autoresetevent"></a>AutoResetEvent
<xref:System.Threading.AutoResetEvent> クラスは、単一の待機スレッドを解放した後、シグナル状態になると自動的にリセットするローカル待機ハンドル イベントを表します。 このクラスは、その基底クラス <xref:System.Threading.EventWaitHandle> の特殊なケースを表します。 自動リセット イベントの使用方法と機能については、[EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) の概念に関する文書を参照してください。  
  
 <xref:System.Threading.AutoResetEvent> オブジェクトは、単一の待機スレッドが解放された後、システムによって自動的に非シグナルにリセットされます。 待機しているスレッドがない場合でも、イベント オブジェクトの状態はシグナルのままです。 <xref:System.Threading.AutoResetEvent> は、`bManualReset` 引数に対して `false` を指定する、Win32 `CreateEvent` 呼び出しに対応します。  
  
 <xref:System.Threading.AutoResetEvent> の使用例については、「<xref:System.Threading.Monitor>」を参照してください。  
  
## <a name="see-also"></a>関連項目

- <xref:System.Threading.ManualResetEvent>  
- <xref:System.Threading.Monitor>  
- [EventWaitHandle、AutoResetEvent、CountdownEvent、ManualResetEvent](../../../docs/standard/threading/eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)  
- [スレッド化](../../../docs/standard/threading/index.md)  
- [スレッド処理オブジェクトと機能](../../../docs/standard/threading/threading-objects-and-features.md)  
- [待機ハンドル](https://msdn.microsoft.com/library/48d10b6f-5fd7-407c-86ab-0179aef72489)
