---
title: ICorDebugController::Detach メソッド
ms.date: 03/30/2017
api_name:
- ICorDebugController.Detach
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::Detach
helpviewer_keywords:
- Detach method, ICorDebugController interface [.NET Framework debugging]
- ICorDebugController::Detach method [.NET Framework debugging]
ms.assetid: 06fae364-f2c6-4a50-aa7e-3da9f2684dc3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4f2dae147f8667a73036dbcf873e2082996b2755
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54666986"
---
# <a name="icordebugcontrollerdetach-method"></a><span data-ttu-id="eb083-102">ICorDebugController::Detach メソッド</span><span class="sxs-lookup"><span data-stu-id="eb083-102">ICorDebugController::Detach Method</span></span>
<span data-ttu-id="eb083-103">プロセスまたはアプリケーション ドメインからデバッガーをデタッチします。</span><span class="sxs-lookup"><span data-stu-id="eb083-103">Detaches the debugger from the process or application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eb083-104">構文</span><span class="sxs-lookup"><span data-stu-id="eb083-104">Syntax</span></span>  
  
```  
HRESULT Detach ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="eb083-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="eb083-105">Remarks</span></span>  
 <span data-ttu-id="eb083-106">プロセスまたはアプリケーション ドメインは通常、実行を継続し、"ICorDebugProcess"または"ICorDebugAppDomain"オブジェクトが無効になってがさらにコールバックが行われません。</span><span class="sxs-lookup"><span data-stu-id="eb083-106">The process or application domain continues execution normally, but the "ICorDebugProcess" or "ICorDebugAppDomain" object is no longer valid and no further callbacks will occur.</span></span>  
  
 <span data-ttu-id="eb083-107">.NET framework version 2.0 では、アンマネージ デバッグが有効になっている場合は、このメソッドはオペレーティング システムの制限により失敗します。</span><span class="sxs-lookup"><span data-stu-id="eb083-107">In the .NET Framework version 2.0, if unmanaged debugging is enabled, this method will fail due to operating system limitations.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eb083-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="eb083-108">Requirements</span></span>  
 <span data-ttu-id="eb083-109">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb083-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eb083-110">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="eb083-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="eb083-111">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eb083-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eb083-112">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eb083-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb083-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb083-113">See also</span></span>

