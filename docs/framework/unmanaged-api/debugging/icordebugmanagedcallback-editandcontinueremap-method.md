---
title: ICorDebugManagedCallback::EditAndContinueRemap メソッド
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.EditAndContinueRemap
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::EditAndContinueRemap
helpviewer_keywords:
- EditAndContinueRemap method [.NET Framework debugging]
- ICorDebugManagedCallback::EditAndContinueRemap method [.NET Framework debugging]
ms.assetid: 24a8fcce-317e-48ff-aefc-d86123ada935
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e1e97b8df2ad81f91cd7250afbe4c5cc544ca6be
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702250"
---
# <a name="icordebugmanagedcallbackeditandcontinueremap-method"></a><span data-ttu-id="81bb2-102">ICorDebugManagedCallback::EditAndContinueRemap メソッド</span><span class="sxs-lookup"><span data-stu-id="81bb2-102">ICorDebugManagedCallback::EditAndContinueRemap Method</span></span>
<span data-ttu-id="81bb2-103">このメソッドの使用は非推奨とされました。</span><span class="sxs-lookup"><span data-stu-id="81bb2-103">This method has been deprecated.</span></span> <span data-ttu-id="81bb2-104">統合開発環境 (IDE) に再割り当てイベントが送信されたことに、デバッガーに通知します。</span><span class="sxs-lookup"><span data-stu-id="81bb2-104">It notifies the debugger that a remap event has been sent to the integrated development environment (IDE).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="81bb2-105">構文</span><span class="sxs-lookup"><span data-stu-id="81bb2-105">Syntax</span></span>  
  
```  
HRESULT EditAndContinueRemap (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread *pThread,  
    [in] ICorDebugFunction *pFunction,  
    [in] BOOL fAccurate  
);  
```  
  
## <a name="remarks"></a><span data-ttu-id="81bb2-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="81bb2-106">Remarks</span></span>  
 <span data-ttu-id="81bb2-107">`EditAndContinueRemap`更新済みの関数の古いバージョンのコードの実行が試行されたときに、メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="81bb2-107">The `EditAndContinueRemap` method is called when the execution of the code in an old version of an updated function has been attempted.</span></span> <span data-ttu-id="81bb2-108">共通言語ランタイムの呼び出し、 `EditAndContinueRemap` IDE に再割り当てイベントを送信する方法。</span><span class="sxs-lookup"><span data-stu-id="81bb2-108">The common language runtime calls the `EditAndContinueRemap` method to send a remap event to the IDE.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="81bb2-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="81bb2-109">Requirements</span></span>  
 <span data-ttu-id="81bb2-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="81bb2-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="81bb2-111">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="81bb2-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="81bb2-112">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="81bb2-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="81bb2-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="81bb2-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="81bb2-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="81bb2-114">See also</span></span>
- [<span data-ttu-id="81bb2-115">ICorDebugManagedCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="81bb2-115">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
