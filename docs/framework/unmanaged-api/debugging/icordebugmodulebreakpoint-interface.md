---
title: ICorDebugModuleBreakpoint Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugModuleBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModuleBreakpoint
helpviewer_keywords:
- ICorDebugModuleBreakpoint interface [.NET Framework debugging]
ms.assetid: 34667162-f314-475f-ae1b-ce9cb0fcbb83
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c5ead45c6747cd69a76585c81b1ff6a4801cbb34
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631994"
---
# <a name="icordebugmodulebreakpoint-interface1"></a><span data-ttu-id="3a50d-102">ICorDebugModuleBreakpoint Interface1</span><span class="sxs-lookup"><span data-stu-id="3a50d-102">ICorDebugModuleBreakpoint Interface1</span></span>
<span data-ttu-id="3a50d-103">特定のモジュールへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="3a50d-103">Provides access to specific modules.</span></span> <span data-ttu-id="3a50d-104">このインターフェイスは、ICorDebugBreakpoint インターフェイスのサブクラスです。</span><span class="sxs-lookup"><span data-stu-id="3a50d-104">This interface is a subclass of the ICorDebugBreakpoint interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3a50d-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="3a50d-105">Methods</span></span>  
  
|<span data-ttu-id="3a50d-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="3a50d-106">Method</span></span>|<span data-ttu-id="3a50d-107">説明</span><span class="sxs-lookup"><span data-stu-id="3a50d-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3a50d-108">GetModule メソッド</span><span class="sxs-lookup"><span data-stu-id="3a50d-108">GetModule Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodulebreakpoint-getmodule-method.md)|<span data-ttu-id="3a50d-109">このブレークポイントが設定されているモジュールを参照する、ICorDebugModule にインターフェイス ポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="3a50d-109">Gets an interface pointer to an ICorDebugModule that references the module where this breakpoint is set.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3a50d-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="3a50d-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3a50d-111">このインターフェイスは、コンピューター間またはプロセス間でのリモート呼び出しをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="3a50d-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a50d-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="3a50d-112">Requirements</span></span>  
 <span data-ttu-id="3a50d-113">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3a50d-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3a50d-114">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3a50d-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3a50d-115">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3a50d-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3a50d-116">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3a50d-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a50d-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="3a50d-117">See also</span></span>
- [<span data-ttu-id="3a50d-118">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="3a50d-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
