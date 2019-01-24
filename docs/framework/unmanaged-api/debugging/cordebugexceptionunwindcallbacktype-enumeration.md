---
title: CorDebugExceptionUnwindCallbackType 列挙型
ms.date: 03/30/2017
api_name:
- CorDebugExceptionUnwindCallbackType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugExceptionUnwindCallbackType
helpviewer_keywords:
- CorDebugExceptionUnwindCallbackType enumeration [.NET Framework debugging]
ms.assetid: 783dce92-8a98-43db-8f78-888d943dd5b2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 31b302977950b3daeab6ac2be117c7f8db51eb2e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654764"
---
# <a name="cordebugexceptionunwindcallbacktype-enumeration"></a><span data-ttu-id="4ce78-102">CorDebugExceptionUnwindCallbackType 列挙型</span><span class="sxs-lookup"><span data-stu-id="4ce78-102">CorDebugExceptionUnwindCallbackType Enumeration</span></span>
<span data-ttu-id="4ce78-103">アンワインド フェーズ中にコールバックによって通知されるイベントを示します。</span><span class="sxs-lookup"><span data-stu-id="4ce78-103">Indicates the event that is being signaled by the callback during the unwind phase.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4ce78-104">構文</span><span class="sxs-lookup"><span data-stu-id="4ce78-104">Syntax</span></span>  
  
```  
typedef enum CorDebugExceptionUnwindCallbackType {  
    DEBUG_EXCEPTION_UNWIND_BEGIN = 1,  
    DEBUG_EXCEPTION_INTERCEPTED  = 2  
} CorDebugExceptionUnwindCallbackType;  
```  
  
## <a name="members"></a><span data-ttu-id="4ce78-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="4ce78-105">Members</span></span>  
  
|<span data-ttu-id="4ce78-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="4ce78-106">Member</span></span>|<span data-ttu-id="4ce78-107">説明</span><span class="sxs-lookup"><span data-stu-id="4ce78-107">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_EXCEPTION_UNWIND_BEGIN`|<span data-ttu-id="4ce78-108">アンワインド プロセスの開始。</span><span class="sxs-lookup"><span data-stu-id="4ce78-108">The beginning of the unwind process.</span></span>|  
|`DEBUG_EXCEPTION_INTERCEPTED`|<span data-ttu-id="4ce78-109">例外を受け取りました。</span><span class="sxs-lookup"><span data-stu-id="4ce78-109">The exception was intercepted.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="4ce78-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="4ce78-110">Requirements</span></span>  
 <span data-ttu-id="4ce78-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ce78-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4ce78-112">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4ce78-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4ce78-113">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4ce78-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4ce78-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4ce78-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4ce78-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="4ce78-115">See also</span></span>
- [<span data-ttu-id="4ce78-116">列挙型のデバッグ</span><span class="sxs-lookup"><span data-stu-id="4ce78-116">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
