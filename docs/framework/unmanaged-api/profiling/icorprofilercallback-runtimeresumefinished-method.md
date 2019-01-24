---
title: ICorProfilerCallback::RuntimeResumeFinished メソッド
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RuntimeResumeFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RuntimeResumeFinished
helpviewer_keywords:
- RuntimeResumeFinished method [.NET Framework profiling]
- ICorProfilerCallback::RuntimeResumeFinished method [.NET Framework profiling]
ms.assetid: 76de0494-dc49-426b-887d-bee98806a982
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a2cf80c7e02d706b0b00ea87aa62986107cdd6a2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54689745"
---
# <a name="icorprofilercallbackruntimeresumefinished-method"></a><span data-ttu-id="b6e63-102">ICorProfilerCallback::RuntimeResumeFinished メソッド</span><span class="sxs-lookup"><span data-stu-id="b6e63-102">ICorProfilerCallback::RuntimeResumeFinished Method</span></span>
<span data-ttu-id="b6e63-103">ランタイムはランタイムのすべてのスレッドが再開し、通常の操作に返されますが、プロファイラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="b6e63-103">Notifies the profiler that the runtime has resumed all runtime threads and has returned to normal operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b6e63-104">構文</span><span class="sxs-lookup"><span data-stu-id="b6e63-104">Syntax</span></span>  
  
```  
HRESULT RuntimeResumeFinished();  
```  
  
## <a name="remarks"></a><span data-ttu-id="b6e63-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="b6e63-105">Remarks</span></span>  
 <span data-ttu-id="b6e63-106">`RuntimeResumeFinished`コールバックと同じスレッドで発生する保証はありません、 [icorprofilercallback::runtimesuspendstarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendstarted-method.md)コールバック。</span><span class="sxs-lookup"><span data-stu-id="b6e63-106">The `RuntimeResumeFinished` callback is not guaranteed to occur on the same thread as the [ICorProfilerCallback::RuntimeSuspendStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendstarted-method.md) callback.</span></span> <span data-ttu-id="b6e63-107">ただしと同じスレッドで発生することに保証、 [icorprofilercallback::runtimeresumestarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimeresumestarted-method.md)コールバック。</span><span class="sxs-lookup"><span data-stu-id="b6e63-107">However, it is guaranteed to occur on the same thread as the [ICorProfilerCallback::RuntimeResumeStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimeresumestarted-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b6e63-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="b6e63-108">Requirements</span></span>  
 <span data-ttu-id="b6e63-109">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6e63-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b6e63-110">**ヘッダー:** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b6e63-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b6e63-111">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b6e63-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b6e63-112">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b6e63-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6e63-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="b6e63-113">See also</span></span>
- [<span data-ttu-id="b6e63-114">ICorProfilerCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b6e63-114">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
