---
title: Thread.Suspend、ガベージ コレクション、およびセーフ ポイント
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- suspending threads
- safe points
- threading [.NET Framework], suspending
- threading [.NET Framework], garbage collection
- garbage collection, threads
ms.assetid: e8f58e17-2714-4821-802a-f8eb3b2baa62
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fc3af01167fe97b701bdb0c7bc37af02d8e8a77c
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/18/2018
ms.locfileid: "46004180"
---
# <a name="threadsuspend-garbage-collection-and-safe-points"></a>Thread.Suspend、ガベージ コレクション、およびセーフ ポイント
スレッドで <xref:System.Threading.Thread.Suspend%2A?displayProperty=nameWithType> を呼び出すと、システムはスレッドの中断が要求されたことを示し、スレッドを実際に中断する前にセーフ ポイントに到達するまでスレッドを実行することができます。 スレッドのセーフ ポイントは、ガベージ コレクションを実行できる実行ポイントです。  
  
 セーフ ポイントに到達すると、ランタイムにより、中断されたスレッドがマネージド コードで続行されないことが保証されます。 マネージド コードの外部で実行中のスレッドは、通常、ガベージ コレクションでは安全であり、その実行はマネージド コードの実行再開が試行されるまで続行します。  
  
> [!NOTE]
>  ガベージ コレクションを実行するために、ランタイムはコレクションを実行中のスレッドを除くすべてのスレッドを中断する必要があります。 各スレッドを中断するには、セーフ ポイントに移動する必要があります。  
  
## <a name="see-also"></a>関連項目

- <xref:System.Threading.Thread>  
- <xref:System.GC>  
- [スレッド化](../../../docs/standard/threading/index.md)  
- [自動メモリ管理](../../../docs/standard/automatic-memory-management.md)
