---
title: ICorProfilerCallback2::HandleCreated メソッド
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.HandleCreated
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::HandleCreated
helpviewer_keywords:
- HandleCreated method [.NET Framework profiling]
- ICorProfilerCallback2::HandleCreated method [.NET Framework profiling]
ms.assetid: 6bbb7786-7c38-490f-9834-91aa2795c355
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fd80c598401d7c72b1b67445b474470ae14736cd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54501910"
---
# <a name="icorprofilercallback2handlecreated-method"></a><span data-ttu-id="96c40-102">ICorProfilerCallback2::HandleCreated メソッド</span><span class="sxs-lookup"><span data-stu-id="96c40-102">ICorProfilerCallback2::HandleCreated Method</span></span>
<span data-ttu-id="96c40-103">ガベージ コレクション ハンドルが作成されているコード プロファイラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="96c40-103">Notifies the code profiler that a garbage collection handle has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="96c40-104">構文</span><span class="sxs-lookup"><span data-stu-id="96c40-104">Syntax</span></span>  
  
```  
HRESULT HandleCreated(  
    [in] GCHandleID handleId,  
    [in] ObjectID initialObjectId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="96c40-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="96c40-105">Parameters</span></span>  
 `handleId`  
 <span data-ttu-id="96c40-106">[in]ガベージ コレクション ハンドルの ID。</span><span class="sxs-lookup"><span data-stu-id="96c40-106">[in] The ID of the handle for the garbage collection.</span></span>  
  
 `initialObjectId`  
 <span data-ttu-id="96c40-107">[in]ガベージ コレクション ハンドルが作成されたオブジェクトの ID。</span><span class="sxs-lookup"><span data-stu-id="96c40-107">[in] The ID of the object for which the garbage collection handle was created.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="96c40-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="96c40-108">Requirements</span></span>  
 <span data-ttu-id="96c40-109">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="96c40-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="96c40-110">**ヘッダー:** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="96c40-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="96c40-111">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="96c40-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="96c40-112">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="96c40-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="96c40-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="96c40-113">See also</span></span>
- [<span data-ttu-id="96c40-114">ICorProfilerCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="96c40-114">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="96c40-115">ICorProfilerCallback2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="96c40-115">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
