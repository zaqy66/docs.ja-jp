---
title: ICorProfilerCallback::ExceptionUnwindFunctionEnter メソッド
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionUnwindFunctionEnter
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionUnwindFunctionEnter
helpviewer_keywords:
- ICorProfilerCallback::ExceptionUnwindFunctionEnter method [.NET Framework profiling]
- ExceptionUnwindFunctionEnter method [.NET Framework profiling]
ms.assetid: ea3dc625-5650-4bf4-8e67-01e42be065b1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3184b0b3bc03aa300832211b52e40f2f2f2988a4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54678643"
---
# <a name="icorprofilercallbackexceptionunwindfunctionenter-method"></a><span data-ttu-id="6433f-102">ICorProfilerCallback::ExceptionUnwindFunctionEnter メソッド</span><span class="sxs-lookup"><span data-stu-id="6433f-102">ICorProfilerCallback::ExceptionUnwindFunctionEnter Method</span></span>
<span data-ttu-id="6433f-103">関数をアンワインドする例外処理のアンワインド フェーズが開始されたことをプロファイラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="6433f-103">Notifies the profiler that the unwind phase of exception handling has begun to unwind a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6433f-104">構文</span><span class="sxs-lookup"><span data-stu-id="6433f-104">Syntax</span></span>  
  
```  
HRESULT ExceptionUnwindFunctionEnter(  
    [in] FunctionID functionId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6433f-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6433f-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="6433f-106">[in]展開される関数の ID。</span><span class="sxs-lookup"><span data-stu-id="6433f-106">[in] The ID of the function that is being unwound.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6433f-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="6433f-107">Remarks</span></span>  
 <span data-ttu-id="6433f-108">プロファイラーでは、スタックはガベージ コレクションを許可する状態にできない可能性がありますので、このメソッドの実装でブロックしないでくださいし、そのため、プリエンプティブなガベージ コレクションを有効にできません。</span><span class="sxs-lookup"><span data-stu-id="6433f-108">The profiler should not block in its implementation of this method because the stack may not be in a state that allows garbage collection, and therefore preemptive garbage collection cannot be enabled.</span></span> <span data-ttu-id="6433f-109">ここで、プロファイラーをブロックする場合とは、ガベージ コレクションが試行されると、ランタイムがこのコールバックが戻るまでブロックされます。</span><span class="sxs-lookup"><span data-stu-id="6433f-109">If the profiler blocks here and garbage collection is attempted, the runtime will block until this callback returns.</span></span>  
  
 <span data-ttu-id="6433f-110">このメソッドのプロファイラーの実装には、任意の方法で管理されているメモリの割り当てが発生またはマネージ コードを呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="6433f-110">The profiler's implementation of this method should not call into managed code or in any way cause a managed-memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6433f-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="6433f-111">Requirements</span></span>  
 <span data-ttu-id="6433f-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6433f-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6433f-113">**ヘッダー:** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="6433f-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="6433f-114">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6433f-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6433f-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6433f-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6433f-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="6433f-116">See also</span></span>
- [<span data-ttu-id="6433f-117">ICorProfilerCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6433f-117">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="6433f-118">ExceptionUnwindFunctionLeave メソッド</span><span class="sxs-lookup"><span data-stu-id="6433f-118">ExceptionUnwindFunctionLeave Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionunwindfunctionleave-method.md)
