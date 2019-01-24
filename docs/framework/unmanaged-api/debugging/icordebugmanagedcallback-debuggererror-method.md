---
title: ICorDebugManagedCallback::DebuggerError メソッド
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.DebuggerError
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::DebuggerError
helpviewer_keywords:
- DebuggerError method [.NET Framework debugging]
- ICorDebugManagedCallback::DebuggerError method [.NET Framework debugging]
ms.assetid: 9e983d11-eaf3-4741-b936-29ec456384a3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 31a554fc57611f4abd5322fdc0c147e5dc110fb7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654946"
---
# <a name="icordebugmanagedcallbackdebuggererror-method"></a><span data-ttu-id="eb0ce-102">ICorDebugManagedCallback::DebuggerError メソッド</span><span class="sxs-lookup"><span data-stu-id="eb0ce-102">ICorDebugManagedCallback::DebuggerError Method</span></span>
<span data-ttu-id="eb0ce-103">共通言語ランタイム (CLR) からのイベントの処理を試行中にエラーが発生したことをデバッガーに通知します。</span><span class="sxs-lookup"><span data-stu-id="eb0ce-103">Notifies the debugger that an error has occurred while attempting to handle an event from the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eb0ce-104">構文</span><span class="sxs-lookup"><span data-stu-id="eb0ce-104">Syntax</span></span>  
  
```  
HRESULT DebuggerError (  
    [in] ICorDebugProcess *pProcess,  
    [in] HRESULT           errorHR,  
    [in] DWORD             errorCode  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="eb0ce-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="eb0ce-105">Parameters</span></span>  
 `pProcess`  
 <span data-ttu-id="eb0ce-106">[in]イベントが発生したプロセスを表す"ICorDebugProcess"オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="eb0ce-106">[in] A pointer to an "ICorDebugProcess" object that represents the process in which the event occurred.</span></span>  
  
 `errorHR`  
 <span data-ttu-id="eb0ce-107">[in]イベント ハンドラーから返された HRESULT 値。</span><span class="sxs-lookup"><span data-stu-id="eb0ce-107">[in] The HRESULT value that was returned from the event handler.</span></span>  
  
 `errorCode`  
 <span data-ttu-id="eb0ce-108">[in]CLR エラーを示す整数。</span><span class="sxs-lookup"><span data-stu-id="eb0ce-108">[in] An integer that specifies the CLR error.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="eb0ce-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="eb0ce-109">Remarks</span></span>  
 <span data-ttu-id="eb0ce-110">プロセスは、パススルー モードでは、エラーの性質によってに配置することがあります。</span><span class="sxs-lookup"><span data-stu-id="eb0ce-110">The process may be placed into pass-through mode, depending on the nature of the error.</span></span>  
  
 <span data-ttu-id="eb0ce-111">`DebugError`コールバックでは、デバッグ サービスが無効である、エラーのため、デバッガーは、エラー メッセージを使用できるように、ユーザーを示します。</span><span class="sxs-lookup"><span data-stu-id="eb0ce-111">The `DebugError` callback indicates that debugging services have been disabled due to an error, so debuggers should make the error message available to the user.</span></span> <span data-ttu-id="eb0ce-112">[Icordebugprocess::getid](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-getid-method.md)など、他のすべてのメソッド呼び出しになれる[icordebug::terminate](../../../../docs/framework/unmanaged-api/debugging/icordebug-terminate-method.md)、呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="eb0ce-112">[ICorDebugProcess::GetID](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess-getid-method.md) will be safe to call, but all other methods, including [ICorDebug::Terminate](../../../../docs/framework/unmanaged-api/debugging/icordebug-terminate-method.md), should not be called.</span></span> <span data-ttu-id="eb0ce-113">デバッガーは、プロセスを終了するためにオペレーティング システムの機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="eb0ce-113">The debugger should use operating-system facilities for terminating processes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eb0ce-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="eb0ce-114">Requirements</span></span>  
 <span data-ttu-id="eb0ce-115">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb0ce-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eb0ce-116">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="eb0ce-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="eb0ce-117">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eb0ce-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eb0ce-118">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eb0ce-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb0ce-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb0ce-119">See also</span></span>
- [<span data-ttu-id="eb0ce-120">ICorDebugManagedCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="eb0ce-120">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
