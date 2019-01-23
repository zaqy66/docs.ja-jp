---
title: COR_ACTIVE_FUNCTION 構造体
ms.date: 03/30/2017
api_name:
- COR_ACTIVE_FUNCTION
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_ACTIVE_FUNCTION
helpviewer_keywords:
- COR_ACTIVE_FUNCTION structure [.NET Framework debugging]
ms.assetid: ed86185f-2152-459c-961f-10c06d62e83f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5adf43bd68db449e465ffe3517c9eb9d41a5c18a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54502053"
---
# <a name="coractivefunction-structure"></a><span data-ttu-id="f9946-102">COR_ACTIVE_FUNCTION 構造体</span><span class="sxs-lookup"><span data-stu-id="f9946-102">COR_ACTIVE_FUNCTION Structure</span></span>
<span data-ttu-id="f9946-103">スレッドのフレームで現在アクティブな機能に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f9946-103">Contains information about the functions that are currently active in a thread's frames.</span></span> <span data-ttu-id="f9946-104">この構造が使用者、 [icordebugthread 2::getactivefunctions](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-getactivefunctions-method.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="f9946-104">This structure is used by the [ICorDebugThread2::GetActiveFunctions](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-getactivefunctions-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f9946-105">構文</span><span class="sxs-lookup"><span data-stu-id="f9946-105">Syntax</span></span>  
  
```  
typedef struct  _COR_ACTIVE_FUNCTION {  
    ICorDebugAppDomain   *pAppDomain;  
    ICorDebugModule      *pModule;  
    ICorDebugFunction2   *pFunction;  
    ULONG32              ilOffset;  
    ULONG32              flags;  
} COR_ACTIVE_FUNCTION;  
```  
  
## <a name="members"></a><span data-ttu-id="f9946-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="f9946-106">Members</span></span>  
  
|<span data-ttu-id="f9946-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="f9946-107">Member</span></span>|<span data-ttu-id="f9946-108">説明</span><span class="sxs-lookup"><span data-stu-id="f9946-108">Description</span></span>|  
|------------|-----------------|  
|`pAppDomain`|<span data-ttu-id="f9946-109">アプリケーション ドメインの所有者へのポインター、`ilOffset`フィールド。</span><span class="sxs-lookup"><span data-stu-id="f9946-109">Pointer to the application domain owner of the `ilOffset` field.</span></span>|  
|`pModule`|<span data-ttu-id="f9946-110">モジュールの所有者へのポインター、`ilOffset`フィールド。</span><span class="sxs-lookup"><span data-stu-id="f9946-110">Pointer to the module owner of the `ilOffset` field.</span></span>|  
|`pFunction`|<span data-ttu-id="f9946-111">関数の所有者へのポインター、`ilOffset`フィールド。</span><span class="sxs-lookup"><span data-stu-id="f9946-111">Pointer to the function owner of the `ilOffset` field.</span></span>|  
|`ilOffset`|<span data-ttu-id="f9946-112">フレームの Microsoft intermediate language (MSIL) オフセット。</span><span class="sxs-lookup"><span data-stu-id="f9946-112">The Microsoft intermediate language (MSIL) offset of the frame.</span></span>|  
|`flags`|<span data-ttu-id="f9946-113">将来の機能拡張予約されています。</span><span class="sxs-lookup"><span data-stu-id="f9946-113">Reserved for future extensibility.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f9946-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="f9946-114">Requirements</span></span>  
 <span data-ttu-id="f9946-115">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9946-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f9946-116">**ヘッダー:** CorDebug.idl</span><span class="sxs-lookup"><span data-stu-id="f9946-116">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="f9946-117">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f9946-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f9946-118">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f9946-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f9946-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="f9946-119">See also</span></span>
- [<span data-ttu-id="f9946-120">デバッグ構造体</span><span class="sxs-lookup"><span data-stu-id="f9946-120">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="f9946-121">デバッグ</span><span class="sxs-lookup"><span data-stu-id="f9946-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
