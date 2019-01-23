---
title: ICorProfilerCallback::ExceptionSearchFunctionEnter メソッド
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionSearchFunctionEnter
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionSearchFunctionEnter
helpviewer_keywords:
- ExceptionSearchFunctionEnter method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionSearchFunctionEnter method [.NET Framework profiling]
ms.assetid: bfd54573-b7e6-4bd1-a184-7f08a8b39fae
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c2f27eccc506ce7145b383132260ad4e470f8906
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54519230"
---
# <a name="icorprofilercallbackexceptionsearchfunctionenter-method"></a><span data-ttu-id="b7851-102">ICorProfilerCallback::ExceptionSearchFunctionEnter メソッド</span><span class="sxs-lookup"><span data-stu-id="b7851-102">ICorProfilerCallback::ExceptionSearchFunctionEnter Method</span></span>
<span data-ttu-id="b7851-103">例外処理の検索フェーズで、現在の例外のハンドラーを検索する関数の検索が開始されたことをプロファイラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="b7851-103">Notifies the profiler that the search phase of exception handling has begun searching a function to find a handler for the current exception.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7851-104">構文</span><span class="sxs-lookup"><span data-stu-id="b7851-104">Syntax</span></span>  
  
```  
HRESULT ExceptionSearchFunctionEnter(  
    [in] FunctionID functionId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b7851-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b7851-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="b7851-106">[in]入力されている関数の ID。</span><span class="sxs-lookup"><span data-stu-id="b7851-106">[in] The ID of the function that has been entered.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7851-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="b7851-107">Requirements</span></span>  
 <span data-ttu-id="b7851-108">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7851-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7851-109">**ヘッダー:** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b7851-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b7851-110">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b7851-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b7851-111">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b7851-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7851-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7851-112">See also</span></span>
- [<span data-ttu-id="b7851-113">ICorProfilerCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b7851-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="b7851-114">ExceptionSearchFunctionLeave メソッド</span><span class="sxs-lookup"><span data-stu-id="b7851-114">ExceptionSearchFunctionLeave Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionsearchfunctionleave-method.md)
