---
title: ICorProfilerCallback8 インターフェイス
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback8
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a3bdf79582619777a22c80caac5b4e90d603f3a8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54675016"
---
# <a name="icorprofilercallback8-interface"></a><span data-ttu-id="d7fa4-102">ICorProfilerCallback8 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d7fa4-102">ICorProfilerCallback8 Interface</span></span>
<span data-ttu-id="d7fa4-103">[.NET Framework 4.7 以降のバージョンでサポートされます]</span><span class="sxs-lookup"><span data-stu-id="d7fa4-103">[Supported in the .NET Framework 4.7 and later versions]</span></span>  

 <span data-ttu-id="d7fa4-104">サブクラス[ICorProfilerCallback7](icorprofilercallback7-interface.md)動的メソッドの JIT コンパイルが開始して完了したことをプロファイラーに通知する、共通言語ランタイムで使用されるコールバック メソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="d7fa4-104">A subclass of [ICorProfilerCallback7](icorprofilercallback7-interface.md) that provides callback methods used by the common language runtime to notify the profiler that JIT compilation of a dynamic method has started and finished.</span></span> 
  
## <a name="methods"></a><span data-ttu-id="d7fa4-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="d7fa4-105">Methods</span></span>  
  
|<span data-ttu-id="d7fa4-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="d7fa4-106">Method</span></span>|<span data-ttu-id="d7fa4-107">説明</span><span class="sxs-lookup"><span data-stu-id="d7fa4-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d7fa4-108">DynamicMethodJITCompilationStarted メソッド</span><span class="sxs-lookup"><span data-stu-id="d7fa4-108">DynamicMethodJITCompilationStarted Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)|<span data-ttu-id="d7fa4-109">動的メソッドの JIT コンパイルが開始されたことをプロファイラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="d7fa4-109">Notifies the profiler that JIT compilation of a dynamic method has started.</span></span>|  
|[<span data-ttu-id="d7fa4-110">DynamicMethodJITCompilationFinished メソッド</span><span class="sxs-lookup"><span data-stu-id="d7fa4-110">DynamicMethodJITCompilationFinished Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)|<span data-ttu-id="d7fa4-111">動的メソッドの JIT コンパイルが完了したことをプロファイラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="d7fa4-111">Notifies the profiler that JIT compilation of a dynamic method has finished.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d7fa4-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="d7fa4-112">Requirements</span></span>  
 <span data-ttu-id="d7fa4-113">**プラットフォーム:**[システム要件](../../get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7fa4-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d7fa4-114">**ヘッダー:** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d7fa4-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
<span data-ttu-id="d7fa4-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="d7fa4-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="d7fa4-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="d7fa4-116">See also</span></span>
- [<span data-ttu-id="d7fa4-117">プロファイリングのインターフェイス</span><span class="sxs-lookup"><span data-stu-id="d7fa4-117">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="d7fa4-118">ICorProfilerCallback9 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d7fa4-118">ICorProfilerCallback9 Interface</span></span>](icorprofilercallback9-interface.md)
