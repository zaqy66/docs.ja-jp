---
title: ICorDebugThread4 インターフェイス
ms.date: 03/30/2017
api_name:
- ICorDebugThread4
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread4
helpviewer_keywords:
- ICorDebugThread4 interface [.NET Framework debugging]
ms.assetid: a8c7719a-322b-4133-8566-4c27218dc104
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e583569e43ea58b37f33729bfa19eef1929fae3d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54517241"
---
# <a name="icordebugthread4-interface"></a><span data-ttu-id="dd434-102">ICorDebugThread4 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="dd434-102">ICorDebugThread4 Interface</span></span>
<span data-ttu-id="dd434-103">スレッドのブロック情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="dd434-103">Provides thread blocking information.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="dd434-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="dd434-104">Methods</span></span>  
  
|<span data-ttu-id="dd434-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="dd434-105">Method</span></span>|<span data-ttu-id="dd434-106">説明</span><span class="sxs-lookup"><span data-stu-id="dd434-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="dd434-107">GetBlockingObjects メソッド</span><span class="sxs-lookup"><span data-stu-id="dd434-107">GetBlockingObjects Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread4-getblockingobjects-method.md)|<span data-ttu-id="dd434-108">順序付けされた列挙体を提供[CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md)スレッドにブロックしている情報を提供する構造体。</span><span class="sxs-lookup"><span data-stu-id="dd434-108">Provides an ordered enumeration of [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structures that provide thread blocking information.</span></span>|  
|[<span data-ttu-id="dd434-109">HadUnhandledException メソッド</span><span class="sxs-lookup"><span data-stu-id="dd434-109">HadUnhandledException Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread4-hadunhandledexception-method.md)|<span data-ttu-id="dd434-110">スレッドが未処理の例外をしたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="dd434-110">Indicates whether the thread has ever had an unhandled exception.</span></span>|  
|[<span data-ttu-id="dd434-111">GetCurrentCustomDebuggerNotification メソッド</span><span class="sxs-lookup"><span data-stu-id="dd434-111">GetCurrentCustomDebuggerNotification Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread4-getcurrentcustomdebuggernotification-method.md)|<span data-ttu-id="dd434-112">現在の取得[icordebugmanagedcallback 3::customnotification](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback3-customnotification-method.md)現在のスレッド上のオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="dd434-112">Gets the current [ICorDebugManagedCallback3::CustomNotification](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback3-customnotification-method.md) object on the current thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dd434-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="dd434-113">Remarks</span></span>  
 <span data-ttu-id="dd434-114">このインターフェイスは ICorDebugThread、ICorDebugThread2 の論理拡張機能と[ICorDebugThread3](../../../../docs/framework/unmanaged-api/debugging/icordebugthread3-interface.md)インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="dd434-114">This interface is a logical extension of the ICorDebugThread, ICorDebugThread2, and [ICorDebugThread3](../../../../docs/framework/unmanaged-api/debugging/icordebugthread3-interface.md) interfaces.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="dd434-115">このインターフェイスは、コンピューター間またはプロセス間でのリモート呼び出しをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="dd434-115">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dd434-116">必要条件</span><span class="sxs-lookup"><span data-stu-id="dd434-116">Requirements</span></span>  
 <span data-ttu-id="dd434-117">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dd434-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dd434-118">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="dd434-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="dd434-119">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dd434-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dd434-120">**.NET Framework のバージョン:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dd434-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dd434-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="dd434-121">See also</span></span>
- [<span data-ttu-id="dd434-122">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="dd434-122">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="dd434-123">デバッグ</span><span class="sxs-lookup"><span data-stu-id="dd434-123">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
