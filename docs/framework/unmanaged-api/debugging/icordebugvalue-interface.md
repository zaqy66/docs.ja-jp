---
title: ICorDebugValue Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue
helpviewer_keywords:
- ICorDebugValue interface [.NET Framework debugging]
ms.assetid: b2f7007f-c446-4b18-aed1-a25cff8aee31
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 41afc2e4305034340ad408e52ce08372bf8962dd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54507448"
---
# <a name="icordebugvalue-interface1"></a><span data-ttu-id="9187b-102">ICorDebugValue Interface1</span><span class="sxs-lookup"><span data-stu-id="9187b-102">ICorDebugValue Interface1</span></span>
<span data-ttu-id="9187b-103">デバッグ中のプロセスで値を表します。</span><span class="sxs-lookup"><span data-stu-id="9187b-103">Represents a value in the process being debugged.</span></span> <span data-ttu-id="9187b-104">値には、読み取り/書き込み値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="9187b-104">The value can be a read or a write value.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9187b-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="9187b-105">Methods</span></span>  
  
|<span data-ttu-id="9187b-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="9187b-106">Method</span></span>|<span data-ttu-id="9187b-107">説明</span><span class="sxs-lookup"><span data-stu-id="9187b-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9187b-108">CreateBreakpoint メソッド</span><span class="sxs-lookup"><span data-stu-id="9187b-108">CreateBreakpoint Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-createbreakpoint-method.md)|<span data-ttu-id="9187b-109">このメソッドは現在実装されていません。</span><span class="sxs-lookup"><span data-stu-id="9187b-109">This method is not currently implemented.</span></span>|  
|[<span data-ttu-id="9187b-110">GetAddress メソッド</span><span class="sxs-lookup"><span data-stu-id="9187b-110">GetAddress Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getaddress-method.md)|<span data-ttu-id="9187b-111">このアドレスを取得`ICorDebugValue`デバッグ中の処理中であるオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="9187b-111">Gets the address of this `ICorDebugValue` object, which is in the process of being debugged.</span></span>|  
|[<span data-ttu-id="9187b-112">GetSize メソッド</span><span class="sxs-lookup"><span data-stu-id="9187b-112">GetSize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getsize-method.md)|<span data-ttu-id="9187b-113">これのバイト単位のサイズを取得します。`ICorDebugValue`オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="9187b-113">Gets the size, in bytes, of this `ICorDebugValue` object.</span></span>|  
|[<span data-ttu-id="9187b-114">GetType メソッド</span><span class="sxs-lookup"><span data-stu-id="9187b-114">GetType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-gettype-method.md)|<span data-ttu-id="9187b-115">このプリミティブ型を取得`ICorDebugValue`オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="9187b-115">Gets the primitive type of this `ICorDebugValue` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9187b-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="9187b-116">Remarks</span></span>  
 <span data-ttu-id="9187b-117">一般に、返された場合、値オブジェクトの所有権が渡されます。</span><span class="sxs-lookup"><span data-stu-id="9187b-117">In general, ownership of a value object is passed when it is returned.</span></span> <span data-ttu-id="9187b-118">受信デバイスが、オブジェクトが完了したら、オブジェクトからの参照を削除する責任を負います。</span><span class="sxs-lookup"><span data-stu-id="9187b-118">The recipient is responsible for removing a reference from the object when it is finished with the object.</span></span>  
  
 <span data-ttu-id="9187b-119">ここから値を取得した、によって値削除される有効なプロセスが再開されます。</span><span class="sxs-lookup"><span data-stu-id="9187b-119">Depending on where the value was retrieved from, the value may not remain valid after the process is resumed.</span></span> <span data-ttu-id="9187b-120">そのため、一般にの値はありませんが保持呼び出しの間で、 [icordebugcontroller::continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="9187b-120">So, in general, the value shouldn't be held across a call of the [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9187b-121">このインターフェイスは、コンピューター間またはプロセス間でのリモート呼び出しをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="9187b-121">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9187b-122">必要条件</span><span class="sxs-lookup"><span data-stu-id="9187b-122">Requirements</span></span>  
 <span data-ttu-id="9187b-123">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9187b-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9187b-124">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9187b-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9187b-125">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9187b-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9187b-126">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9187b-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9187b-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="9187b-127">See also</span></span>




- [<span data-ttu-id="9187b-128">ICorDebugValue3 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9187b-128">ICorDebugValue3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md)
- [<span data-ttu-id="9187b-129">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9187b-129">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
