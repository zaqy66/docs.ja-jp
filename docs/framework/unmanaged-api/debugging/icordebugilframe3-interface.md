---
title: ICorDebugILFrame3 インターフェイス
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame3
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 15212cb5-93d4-4025-bec9-d4b9919eb1fe
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9c87578c3a5e2bec9bbd754929308645f7862ee5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54701678"
---
# <a name="icordebugilframe3-interface"></a><span data-ttu-id="b5173-102">ICorDebugILFrame3 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b5173-102">ICorDebugILFrame3 Interface</span></span>
<span data-ttu-id="b5173-103">関数の戻り値をカプセル化するメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="b5173-103">Provides a method that encapsulates the return value of a function.</span></span> <span data-ttu-id="b5173-104">`ICorDebugILFrame3` ICorDebugILFrame および ICorDebugILFrame2 インターフェイスの論理的な拡張です。</span><span class="sxs-lookup"><span data-stu-id="b5173-104">`ICorDebugILFrame3` is a logical extension of the ICorDebugILFrame and ICorDebugILFrame2 interfaces.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b5173-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="b5173-105">Methods</span></span>  
  
|<span data-ttu-id="b5173-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="b5173-106">Method</span></span>|<span data-ttu-id="b5173-107">説明</span><span class="sxs-lookup"><span data-stu-id="b5173-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b5173-108">GetReturnValueForILOffSet メソッド</span><span class="sxs-lookup"><span data-stu-id="b5173-108">GetReturnValueForILOffset Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe3-getreturnvalueforiloffset-method.md)|<span data-ttu-id="b5173-109">関数の戻り値をカプセル化する ICorDebugValue オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="b5173-109">Gets an ICorDebugValue object that encapsulates the return value of a function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b5173-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="b5173-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b5173-111">このインターフェイスは、コンピューター間またはプロセス間でのリモート呼び出しをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="b5173-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b5173-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="b5173-112">Requirements</span></span>  
 <span data-ttu-id="b5173-113">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5173-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b5173-114">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b5173-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b5173-115">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b5173-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b5173-116">**.NET Framework のバージョン:** [!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b5173-116">**.NET Framework Versions:** [!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b5173-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="b5173-117">See also</span></span>
- [<span data-ttu-id="b5173-118">ICorDebugCode3 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b5173-118">ICorDebugCode3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode3-interface.md)
- [<span data-ttu-id="b5173-119">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b5173-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
