---
title: ICorDebugManagedCallback::CreateProcess メソッド
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.CreateProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::CreateProcess
helpviewer_keywords:
- ICorDebugManagedCallback::CreateProcess method [.NET Framework debugging]
- CreateProcess method, ICorDebugManagedCallback interface [.NET Framework debugging]
ms.assetid: 8e89d5ee-e4e3-4738-8302-0b7d1cf4846e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7693111427f3181adcd2127ad5ecb2a317e30921
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54515616"
---
# <a name="icordebugmanagedcallbackcreateprocess-method"></a><span data-ttu-id="597f6-102">ICorDebugManagedCallback::CreateProcess メソッド</span><span class="sxs-lookup"><span data-stu-id="597f6-102">ICorDebugManagedCallback::CreateProcess Method</span></span>
<span data-ttu-id="597f6-103">プロセスにアタッチまたは最初に起動された場合に、デバッガーに通知します。</span><span class="sxs-lookup"><span data-stu-id="597f6-103">Notifies the debugger when a process has been attached or started for the first time.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="597f6-104">構文</span><span class="sxs-lookup"><span data-stu-id="597f6-104">Syntax</span></span>  
  
```  
HRESULT CreateProcess (  
    [in] ICorDebugProcess *pProcess  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="597f6-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="597f6-105">Parameters</span></span>  
 `pProcess`  
 <span data-ttu-id="597f6-106">[in]ICorDebugProcess を表すオブジェクトをアタッチまたは開始されたプロセスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="597f6-106">[in] A pointer to an ICorDebugProcess object that represents the process that has been attached or started.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="597f6-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="597f6-107">Remarks</span></span>  
 <span data-ttu-id="597f6-108">共通言語ランタイムが初期化されるまで、このメソッドは呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="597f6-108">This method is not called until the common language runtime is initialized.</span></span> <span data-ttu-id="597f6-109">ほとんどの[ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)メソッドでは、前に CORDBG_E_NOTREADY を返します、`CreateProcess`コールバック。</span><span class="sxs-lookup"><span data-stu-id="597f6-109">Most of the [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) methods will return CORDBG_E_NOTREADY before the `CreateProcess` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="597f6-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="597f6-110">Requirements</span></span>  
 <span data-ttu-id="597f6-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="597f6-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="597f6-112">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="597f6-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="597f6-113">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="597f6-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="597f6-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="597f6-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="597f6-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="597f6-115">See also</span></span>
- [<span data-ttu-id="597f6-116">ICorDebugManagedCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="597f6-116">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
