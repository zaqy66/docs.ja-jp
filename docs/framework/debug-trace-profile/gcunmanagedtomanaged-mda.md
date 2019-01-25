---
title: gcUnmanagedToManaged MDA
ms.date: 03/30/2017
helpviewer_keywords:
- MDAs (managed debugging assistants), garbage collection
- GC unmanaged to managed
- transitioning threads unmanaged to managed code
- GcUnmanagedToManaged MDA
- threading [.NET Framework], garbage collection
- managed debugging assistants (MDAs), garbage collection
- threading [.NET Framework], managed debugging assistants
- garbage collection, run-time errors
- unmanaged to managed garbage collection
ms.assetid: 103eb3a3-1cf0-4406-8a9a-a7798fdc22d1
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c99ae7d222db2e44de471eb9a41fed614362e300
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54614381"
---
# <a name="gcunmanagedtomanaged-mda"></a>gcUnmanagedToManaged MDA
`gcUnmanagedToManaged` マネージド デバッグ アシスタント (MDA: Managed Debugging Assistant) は、スレッドがアンマネージド コードからマネージド コードに遷移する時に、毎回ガベージ コレクションが行われるようにします。  
  
## <a name="symptoms"></a>症状  
 COM およびプラットフォーム呼び出しを使用してアンマネージ ユーザー コンポーネントを実行中のアプリケーションによって、CLR で非確定的なアクセス違反が発生します。  
  
## <a name="cause"></a>原因  
 アプリケーションがアンマネージ ユーザー コンポーネントを実行中の場合、それらのコンポーネントによって、ガベージ コレクトされたヒープが破損された可能性があります。 これが原因で、ガベージ コレクターがオブジェクト グラフをウォークしようとしたときに、CLR でアクセス違反が発生します。  
  
## <a name="resolution"></a>解像度  
 このアシスタントを有効にすると、各マネージ遷移の前にガベージ コレクションが必ず行われるようになるため、アンマネージ コンポーネントがガベージ コレクトされたヒープを破損してから、アクセス違反が発生するまでの時間が短縮されます。  
  
## <a name="effect-on-the-runtime"></a>ランタイムへの影響  
 スレッドがアンマネージド コードからマネージド コードに遷移する時に、毎回ガベージ コレクションが行われるようになります。  
  
## <a name="output"></a>出力  
 この MDA は、出力を生成しません。  
  
## <a name="configuration"></a>構成  
  
```xml  
<mdaConfig>  
  <assistants>  
    <gcUnmanagedToManaged/>  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a>関連項目
- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [マネージド デバッグ アシスタントによるエラーの診断](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
- [gcManagedToUnmanaged](../../../docs/framework/debug-trace-profile/gcmanagedtounmanaged-mda.md)
- [相互運用マーシャリング](../../../docs/framework/interop/interop-marshaling.md)
