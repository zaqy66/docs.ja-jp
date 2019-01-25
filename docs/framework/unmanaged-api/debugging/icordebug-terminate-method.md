---
title: ICorDebug::Terminate メソッド
ms.date: 03/30/2017
api_name:
- ICorDebug.Terminate
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::Terminate
helpviewer_keywords:
- Terminate method, ICorDebug interface [.NET Framework debugging]
- ICorDebug::Terminate method [.NET Framework debugging]
ms.assetid: fffe5616-0896-4426-ab5e-21869b514883
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 057ee7a323a8a725ebf82ee9dbaea61a43c061ca
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54674610"
---
# <a name="icordebugterminate-method"></a><span data-ttu-id="312f7-102">ICorDebug::Terminate メソッド</span><span class="sxs-lookup"><span data-stu-id="312f7-102">ICorDebug::Terminate Method</span></span>
<span data-ttu-id="312f7-103">終了、`ICorDebug`オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="312f7-103">Terminates the `ICorDebug` object.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="312f7-104">`Terminate` まで呼び出すことはできません、 [icordebugmanagedcallback::exitprocess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md)デバッグ中のすべてのプロセスのコールバックを受け取りました。</span><span class="sxs-lookup"><span data-stu-id="312f7-104">`Terminate` should not be called until an [ICorDebugManagedCallback::ExitProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md) callback has been received for all processes being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="312f7-105">構文</span><span class="sxs-lookup"><span data-stu-id="312f7-105">Syntax</span></span>  
  
```  
HRESULT Terminate ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="312f7-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="312f7-106">Remarks</span></span>  
 <span data-ttu-id="312f7-107">`Terminate` ときに呼び出す必要があります、`ICorDebug`オブジェクトが不要です。</span><span class="sxs-lookup"><span data-stu-id="312f7-107">`Terminate` must be called when the `ICorDebug` object is no longer needed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="312f7-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="312f7-108">Requirements</span></span>  
 <span data-ttu-id="312f7-109">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="312f7-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="312f7-110">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="312f7-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="312f7-111">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="312f7-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="312f7-112">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="312f7-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="312f7-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="312f7-113">See also</span></span>
- [<span data-ttu-id="312f7-114">ICorDebug インターフェイス</span><span class="sxs-lookup"><span data-stu-id="312f7-114">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
