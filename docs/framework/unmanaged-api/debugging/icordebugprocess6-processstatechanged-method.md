---
title: ICorDebugProcess6::ProcessStateChanged メソッド
ms.date: 03/30/2017
ms.assetid: fb6d30d9-54f3-462b-8ebf-ce0440791ad5
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bb134b7d188c2fb966b53e4520a7fb825f11e428
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54612048"
---
# <a name="icordebugprocess6processstatechanged-method"></a><span data-ttu-id="274a9-102">ICorDebugProcess6::ProcessStateChanged メソッド</span><span class="sxs-lookup"><span data-stu-id="274a9-102">ICorDebugProcess6::ProcessStateChanged Method</span></span>
<span data-ttu-id="274a9-103">通知[ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)プロセスが実行されています。</span><span class="sxs-lookup"><span data-stu-id="274a9-103">Notifies [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) that the process is running.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="274a9-104">構文</span><span class="sxs-lookup"><span data-stu-id="274a9-104">Syntax</span></span>  
  
```  
HRESULT ProcessStateChanged(   [in] CorDebugStateChange change);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="274a9-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="274a9-105">Parameters</span></span>  
 `change`  
 <span data-ttu-id="274a9-106">[in]メンバー、 [ProcessStateChanged](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-processstatechanged-method.md)列挙型</span><span class="sxs-lookup"><span data-stu-id="274a9-106">[in] A member of the [ProcessStateChanged](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-processstatechanged-method.md) enumeration</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="274a9-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="274a9-107">Remarks</span></span>  
 <span data-ttu-id="274a9-108">デバッガーに通知するには、このメソッドを呼び出して[ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)プロセスが実行されています。</span><span class="sxs-lookup"><span data-stu-id="274a9-108">The debugger calls this method to notify [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) that the process is running.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="274a9-109">このメソッドは .NET ネイティブでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="274a9-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="274a9-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="274a9-110">Requirements</span></span>  
 <span data-ttu-id="274a9-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="274a9-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="274a9-112">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="274a9-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="274a9-113">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="274a9-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="274a9-114">**.NET Framework のバージョン:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="274a9-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="274a9-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="274a9-115">See also</span></span>
- [<span data-ttu-id="274a9-116">ICorDebugProcess6 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="274a9-116">ICorDebugProcess6 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-interface.md)
- [<span data-ttu-id="274a9-117">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="274a9-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
