---
title: ICorDebugRuntimeUnwindableFrame インターフェイス
ms.date: 03/30/2017
api_name:
- ICorDebugUnwindableFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugUnwindableFrame
helpviewer_keywords:
- ICorDebugUnwindableFrame interface [.NET Framework debugging]
ms.assetid: cd6a3982-6ed3-4909-808d-a66055e813e0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f006085aba140264e2a2605adce39924dbe082e4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54568115"
---
# <a name="icordebugruntimeunwindableframe-interface"></a><span data-ttu-id="48f52-102">ICorDebugRuntimeUnwindableFrame インターフェイス</span><span class="sxs-lookup"><span data-stu-id="48f52-102">ICorDebugRuntimeUnwindableFrame Interface</span></span>
<span data-ttu-id="48f52-103">共通言語ランタイム (CLR: Common Language Runtime) でフレームをアンワインドする必要のあるアンマネージ メソッドに対してサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="48f52-103">Provides support for unmanaged methods that require the common language runtime (CLR) to unwind a frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="48f52-104">Remarks</span><span class="sxs-lookup"><span data-stu-id="48f52-104">Remarks</span></span>  
 <span data-ttu-id="48f52-105">`ICorDebugRuntimeUnwindableFrame` ICorDebugFrame インターフェイスの特殊化されたバージョンです。</span><span class="sxs-lookup"><span data-stu-id="48f52-105">`ICorDebugRuntimeUnwindableFrame` is a specialized version of the ICorDebugFrame interface.</span></span> <span data-ttu-id="48f52-106">現在のスタックのフレームをアンワインドするランタイムを必要とする非管理対象のメソッドによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="48f52-106">It is used by unmanaged methods that require the runtime to unwind a frame on the current stack.</span></span> <span data-ttu-id="48f52-107">既存のアンワインド規則は機能せず、JIT コンパイル コードを使用しないためです。</span><span class="sxs-lookup"><span data-stu-id="48f52-107">Existing unwinding conventions do not work, because they do not use JIT-compiled code.</span></span> <span data-ttu-id="48f52-108">デバッガーでは、アンワインド可能のフレームを見てを使用する、 [icordebugstackwalk::next](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-next-method.md)メソッドが、アンワインドは自体検査を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48f52-108">When the debugger sees an unwindable frame, it should use the [ICorDebugStackWalk::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-next-method.md) method to unwind it, but it should perform inspection itself.</span></span> <span data-ttu-id="48f52-109">デバッガーを受信すると、 `ICorDebugRuntimeUnwindableFrame`、呼び出すことができます、 [icordebugstackwalk::getcontext](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-getcontext-method.md)フレームのコンテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="48f52-109">When the debugger receives an `ICorDebugRuntimeUnwindableFrame`, it can call the [ICorDebugStackWalk::GetContext](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-getcontext-method.md) method to retrieve the context of the frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="48f52-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="48f52-110">Requirements</span></span>  
 <span data-ttu-id="48f52-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="48f52-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="48f52-112">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="48f52-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="48f52-113">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="48f52-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="48f52-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="48f52-114">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48f52-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="48f52-115">See also</span></span>
- [<span data-ttu-id="48f52-116">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="48f52-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="48f52-117">デバッグ</span><span class="sxs-lookup"><span data-stu-id="48f52-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
