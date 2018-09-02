---
title: fatalExecutionEngineError MDA
ms.date: 03/30/2017
helpviewer_keywords:
- corrupted CLR
- fatal execution error
- terminated processes
- unexpected terminations
- fatal errors
- MDAs (managed debugging assistants), fatal errors
- process termination
- FatalExecutionEngineError MDA
- managed debugging assistants (MDAs), fatal errors
ms.assetid: 8b559e44-2393-4e4e-8160-7558d37a4a89
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f12b94198b88111d559cfe372c28bdbf4b37e3fe
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43419788"
---
# <a name="fatalexecutionengineerror-mda"></a><span data-ttu-id="12783-102">fatalExecutionEngineError MDA</span><span class="sxs-lookup"><span data-stu-id="12783-102">fatalExecutionEngineError MDA</span></span>
<span data-ttu-id="12783-103">`fatalExecutionEngineError` マネージド デバッグ アシスタント (MDA) は、共通言語ランタイム (CLR) で致命的なエラーが検出されたときにアクティブ化されます。</span><span class="sxs-lookup"><span data-stu-id="12783-103">The `fatalExecutionEngineError` managed debugging assistant (MDA) is activated when a fatal error in the common language runtime (CLR) has been detected.</span></span> <span data-ttu-id="12783-104">プロセスは終了されます。</span><span class="sxs-lookup"><span data-stu-id="12783-104">The process will be terminated.</span></span>  
  
## <a name="symptoms"></a><span data-ttu-id="12783-105">現象</span><span class="sxs-lookup"><span data-stu-id="12783-105">Symptoms</span></span>  
 <span data-ttu-id="12783-106">予期せずにプロセスが終了します。</span><span class="sxs-lookup"><span data-stu-id="12783-106">Unexpected process termination.</span></span> <span data-ttu-id="12783-107">CLR エラーは、さまざまな理由により発生する可能性があるため、他の症状を特定できません。</span><span class="sxs-lookup"><span data-stu-id="12783-107">Other symptoms cannot be determined because a CLR failure can occur for a variety of reasons.</span></span>  
  
## <a name="cause"></a><span data-ttu-id="12783-108">原因</span><span class="sxs-lookup"><span data-stu-id="12783-108">Cause</span></span>  
 <span data-ttu-id="12783-109">CLR が致命的に破損しています。</span><span class="sxs-lookup"><span data-stu-id="12783-109">The CLR has been fatally corrupted.</span></span> <span data-ttu-id="12783-110">これはほとんどの場合、データの破損により発生します。データの破損は、不正なプラットフォームの呼び出し関数への呼び出しや、CLR に無効なデータを渡すといった、多くの問題が原因で発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="12783-110">This is most often caused by data corruption, which can be caused by a number of problems, such as calls to malformed platform invoke functions and passing invalid data to the CLR.</span></span>  
  
## <a name="resolution"></a><span data-ttu-id="12783-111">解像度</span><span class="sxs-lookup"><span data-stu-id="12783-111">Resolution</span></span>  
 <span data-ttu-id="12783-112">追加の MDA を有効にすると、問題を特定するのに役立つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="12783-112">Enabling additional MDAs might help identify the problem.</span></span> <span data-ttu-id="12783-113">次の MDA は、問題を診断する際に特に有用です。</span><span class="sxs-lookup"><span data-stu-id="12783-113">The following MDAs can be particularly helpful in diagnosing the issue:</span></span>  
  
-   [<span data-ttu-id="12783-114">invalidOverlappedToPinvoke</span><span class="sxs-lookup"><span data-stu-id="12783-114">invalidOverlappedToPinvoke</span></span>](../../../docs/framework/debug-trace-profile/invalidoverlappedtopinvoke-mda.md)  
  
-   [<span data-ttu-id="12783-115">overlappedFreeError</span><span class="sxs-lookup"><span data-stu-id="12783-115">overlappedFreeError</span></span>](../../../docs/framework/debug-trace-profile/overlappedfreeerror-mda.md)  
  
-   [<span data-ttu-id="12783-116">pInvokeStackImbalance</span><span class="sxs-lookup"><span data-stu-id="12783-116">pInvokeStackImbalance</span></span>](../../../docs/framework/debug-trace-profile/pinvokestackimbalance-mda.md)  
  
-   [<span data-ttu-id="12783-117">gcUnmanagedToManaged</span><span class="sxs-lookup"><span data-stu-id="12783-117">gcUnmanagedToManaged</span></span>](../../../docs/framework/debug-trace-profile/gcunmanagedtomanaged-mda.md)  
  
-   [<span data-ttu-id="12783-118">gcManagedToUnmanaged</span><span class="sxs-lookup"><span data-stu-id="12783-118">gcManagedToUnmanaged</span></span>](../../../docs/framework/debug-trace-profile/gcmanagedtounmanaged-mda.md)  
  
-   [<span data-ttu-id="12783-119">callbackOnCollectedDelegate</span><span class="sxs-lookup"><span data-stu-id="12783-119">callbackOnCollectedDelegate</span></span>](../../../docs/framework/debug-trace-profile/callbackoncollecteddelegate-mda.md)  
  
-   [<span data-ttu-id="12783-120">reportAvOnComRelease</span><span class="sxs-lookup"><span data-stu-id="12783-120">reportAvOnComRelease</span></span>](../../../docs/framework/debug-trace-profile/reportavoncomrelease-mda.md)  
  
-   [<span data-ttu-id="12783-121">invalidVariant</span><span class="sxs-lookup"><span data-stu-id="12783-121">invalidVariant</span></span>](../../../docs/framework/debug-trace-profile/invalidvariant-mda.md)  
  
-   [<span data-ttu-id="12783-122">invalidIUnknown</span><span class="sxs-lookup"><span data-stu-id="12783-122">invalidIUnknown</span></span>](../../../docs/framework/debug-trace-profile/invalidiunknown-mda.md)  
  
-   [<span data-ttu-id="12783-123">raceOnRCWCleanup</span><span class="sxs-lookup"><span data-stu-id="12783-123">raceOnRCWCleanup</span></span>](../../../docs/framework/debug-trace-profile/raceonrcwcleanup-mda.md)  
  
-   [<span data-ttu-id="12783-124">invalidFunctionPointerInDelegate</span><span class="sxs-lookup"><span data-stu-id="12783-124">invalidFunctionPointerInDelegate</span></span>](../../../docs/framework/debug-trace-profile/invalidfunctionpointerindelegate-mda.md)  
  
-   [<span data-ttu-id="12783-125">invalidGCHandleCookie</span><span class="sxs-lookup"><span data-stu-id="12783-125">invalidGCHandleCookie</span></span>](../../../docs/framework/debug-trace-profile/invalidgchandlecookie-mda.md)  
  
## <a name="effect-on-the-runtime"></a><span data-ttu-id="12783-126">ランタイムへの影響</span><span class="sxs-lookup"><span data-stu-id="12783-126">Effect on the Runtime</span></span>  
 <span data-ttu-id="12783-127">この MDA は、ランタイムの動作への影響はありません。</span><span class="sxs-lookup"><span data-stu-id="12783-127">This MDA has no effect on the runtime's behavior.</span></span>  
  
## <a name="output"></a><span data-ttu-id="12783-128">出力</span><span class="sxs-lookup"><span data-stu-id="12783-128">Output</span></span>  
 <span data-ttu-id="12783-129">致命的なエラーの原因となった CLR 関数のアドレス、エラーが発生したスレッドの ID、およびエラー コード。</span><span class="sxs-lookup"><span data-stu-id="12783-129">The address of the CLR function that caused the fatal error, the ID of the thread where the error occurred, and the error code.</span></span>  
  
## <a name="configuration"></a><span data-ttu-id="12783-130">構成</span><span class="sxs-lookup"><span data-stu-id="12783-130">Configuration</span></span>  
  
```xml  
<mdaConfig>  
  <assistants>  
    <fatalExecutionEngineError />  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a><span data-ttu-id="12783-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="12783-131">See Also</span></span>  
 <xref:System.Runtime.CompilerServices.RuntimeHelpers.PrepareMethod%2A>  
 <xref:System.Runtime.ConstrainedExecution.Cer>  
 [<span data-ttu-id="12783-132">マネージド デバッグ アシスタントによるエラーの診断</span><span class="sxs-lookup"><span data-stu-id="12783-132">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
