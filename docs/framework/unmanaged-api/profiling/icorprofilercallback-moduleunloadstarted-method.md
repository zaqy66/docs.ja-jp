---
title: ICorProfilerCallback::ModuleUnloadStarted メソッド
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ModuleUnloadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ModuleUnloadStarted
helpviewer_keywords:
- ModuleUnloadStarted method [.NET Framework profiling]
- ICorProfilerCallback::ModuleUnloadStarted method [.NET Framework profiling]
ms.assetid: 2debcaab-6005-4245-afdb-4268bb7e74bd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5981e9a193f4ebfc88628f56cf865523c9b87c6f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54744649"
---
# <a name="icorprofilercallbackmoduleunloadstarted-method"></a><span data-ttu-id="aad91-102">ICorProfilerCallback::ModuleUnloadStarted メソッド</span><span class="sxs-lookup"><span data-stu-id="aad91-102">ICorProfilerCallback::ModuleUnloadStarted Method</span></span>
<span data-ttu-id="aad91-103">モジュールがアンロードされることをプロファイラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="aad91-103">Notifies the profiler that a module is being unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aad91-104">構文</span><span class="sxs-lookup"><span data-stu-id="aad91-104">Syntax</span></span>  
  
```  
HRESULT ModuleUnloadStarted(  
    [in] ModuleID moduleId);   
```  
  
#### <a name="parameters"></a><span data-ttu-id="aad91-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="aad91-105">Parameters</span></span>  
 `moduleId`  
 <span data-ttu-id="aad91-106">[in]アンロードされているモジュールの ID。</span><span class="sxs-lookup"><span data-stu-id="aad91-106">[in] The ID of the module that is being unloaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="aad91-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="aad91-107">Remarks</span></span>  
 <span data-ttu-id="aad91-108">値`moduleId`は後の情報の要求は無効です、`ModuleUnloadStarted`メソッドを返します。-これは、このモジュールに関する情報を取得するプロファイラーの最後のチャンスです。</span><span class="sxs-lookup"><span data-stu-id="aad91-108">The value of `moduleId` is not valid for an information request after the `ModuleUnloadStarted` method returns — this is the profiler's last chance to get information about this module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aad91-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="aad91-109">Requirements</span></span>  
 <span data-ttu-id="aad91-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="aad91-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aad91-111">**ヘッダー:** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="aad91-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="aad91-112">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="aad91-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="aad91-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aad91-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aad91-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="aad91-114">See also</span></span>
- [<span data-ttu-id="aad91-115">ICorProfilerCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="aad91-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="aad91-116">ModuleUnloadFinished メソッド</span><span class="sxs-lookup"><span data-stu-id="aad91-116">ModuleUnloadFinished Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleunloadfinished-method.md)
