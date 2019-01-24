---
title: ICorDebugValueBreakpoint Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugValueBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValueBreakpoint
helpviewer_keywords:
- ICorDebugValueBreakpoint interface [.NET Framework debugging]
ms.assetid: c02338fe-da6c-467f-9567-70ebb387e901
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 58e6807b0546eadc4baacc276fa1ba7bda4e3aba
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54557761"
---
# <a name="icordebugvaluebreakpoint-interface1"></a><span data-ttu-id="8ca92-102">ICorDebugValueBreakpoint Interface1</span><span class="sxs-lookup"><span data-stu-id="8ca92-102">ICorDebugValueBreakpoint Interface1</span></span>
<span data-ttu-id="8ca92-103">特定の値へのアクセスを提供する ICorDebugBreakpoint インターフェイスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="8ca92-103">Extends the ICorDebugBreakpoint interface to provide access to specific values.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8ca92-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="8ca92-104">Methods</span></span>  
  
|<span data-ttu-id="8ca92-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="8ca92-105">Method</span></span>|<span data-ttu-id="8ca92-106">説明</span><span class="sxs-lookup"><span data-stu-id="8ca92-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8ca92-107">GetValue メソッド</span><span class="sxs-lookup"><span data-stu-id="8ca92-107">GetValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvaluebreakpoint-getvalue-method.md)|<span data-ttu-id="8ca92-108">ブレークポイントが設定されているオブジェクトの値を表す ICorDebugValue オブジェクトへのインターフェイス ポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="8ca92-108">Gets an interface pointer to an ICorDebugValue object that represents the value of the object upon which the breakpoint is set.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8ca92-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="8ca92-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8ca92-110">このインターフェイスは、コンピューター間またはプロセス間でのリモート呼び出しをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="8ca92-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8ca92-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="8ca92-111">Requirements</span></span>  
 <span data-ttu-id="8ca92-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ca92-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8ca92-113">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8ca92-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8ca92-114">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8ca92-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8ca92-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8ca92-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ca92-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="8ca92-116">See also</span></span>
- [<span data-ttu-id="8ca92-117">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8ca92-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
