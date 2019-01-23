---
title: ICorDebugHeapValue Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue
helpviewer_keywords:
- ICorDebugHeapValue interface [.NET Framework debugging]
ms.assetid: 1bca66db-0359-4ae8-846e-e35f7e547e8b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a87790647ed8896f072aa8e943e31fa1980e3f62
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54622859"
---
# <a name="icordebugheapvalue-interface1"></a><span data-ttu-id="8944d-102">ICorDebugHeapValue Interface1</span><span class="sxs-lookup"><span data-stu-id="8944d-102">ICorDebugHeapValue Interface1</span></span>
<span data-ttu-id="8944d-103">共通言語ランタイム (CLR) のガベージ コレクターによって収集されたオブジェクトを表す"ICorDebugValue"のサブクラスです。</span><span class="sxs-lookup"><span data-stu-id="8944d-103">A subclass of "ICorDebugValue" that represents an object that has been collected by the common language runtime (CLR) garbage collector.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8944d-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="8944d-104">Methods</span></span>  
  
|<span data-ttu-id="8944d-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="8944d-105">Method</span></span>|<span data-ttu-id="8944d-106">説明</span><span class="sxs-lookup"><span data-stu-id="8944d-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8944d-107">CreateRelocBreakpoint メソッド</span><span class="sxs-lookup"><span data-stu-id="8944d-107">CreateRelocBreakpoint Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugheapvalue-createrelocbreakpoint-method.md)|<span data-ttu-id="8944d-108">実装されていません。</span><span class="sxs-lookup"><span data-stu-id="8944d-108">Not implemented.</span></span>|  
|[<span data-ttu-id="8944d-109">IsValid メソッド</span><span class="sxs-lookup"><span data-stu-id="8944d-109">IsValid Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugheapvalue-isvalid-method.md)|<span data-ttu-id="8944d-110">オブジェクトが、これによって表されるかどうかを示す値を取得します`ICorDebugHeapValue`有効ですが、またはガベージ コレクターによって解放されています。</span><span class="sxs-lookup"><span data-stu-id="8944d-110">Gets a value that indicates whether the object represented by this `ICorDebugHeapValue` is valid, or has been reclaimed by the garbage collector.</span></span> <span data-ttu-id="8944d-111">このメソッドは、.NET Framework version 2.0 で廃止されました。</span><span class="sxs-lookup"><span data-stu-id="8944d-111">This method has been deprecated in the .NET Framework version 2.0.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8944d-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="8944d-112">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8944d-113">このインターフェイスは、コンピューター間またはプロセス間でのリモート呼び出しをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="8944d-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8944d-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="8944d-114">Requirements</span></span>  
 <span data-ttu-id="8944d-115">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8944d-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8944d-116">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8944d-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8944d-117">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8944d-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8944d-118">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8944d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8944d-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="8944d-119">See also</span></span>



- [<span data-ttu-id="8944d-120">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8944d-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
