---
title: CorDebugHandleType 列挙型
ms.date: 03/30/2017
api_name:
- CorDebugHandleType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugHandleType
helpviewer_keywords:
- CorDebugHandleType enumeration [.NET Framework debugging]
ms.assetid: 84296b55-c2c5-424c-ac9c-8e28e2895945
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5ca7508c675ccc4c4ee0c07a2d7790bb5de7a668
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54594591"
---
# <a name="cordebughandletype-enumeration"></a><span data-ttu-id="4223f-102">CorDebugHandleType 列挙型</span><span class="sxs-lookup"><span data-stu-id="4223f-102">CorDebugHandleType Enumeration</span></span>
<span data-ttu-id="4223f-103">ハンドル型を示します。</span><span class="sxs-lookup"><span data-stu-id="4223f-103">Indicates the handle type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4223f-104">構文</span><span class="sxs-lookup"><span data-stu-id="4223f-104">Syntax</span></span>  
  
```  
typedef enum CorDebugHandleType {  
    HANDLE_STRONG                  = 1,  
    HANDLE_WEAK_TRACK_RESURRECTION = 2  
} CorDebugHandleType;  
```  
  
## <a name="members"></a><span data-ttu-id="4223f-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="4223f-105">Members</span></span>  
  
|<span data-ttu-id="4223f-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="4223f-106">Member</span></span>|<span data-ttu-id="4223f-107">説明</span><span class="sxs-lookup"><span data-stu-id="4223f-107">Description</span></span>|  
|------------|-----------------|  
|`HANDLE_STRONG`|<span data-ttu-id="4223f-108">ハンドルは、ガベージ コレクションで回収されてからオブジェクトを防ぐことが、強力なです。</span><span class="sxs-lookup"><span data-stu-id="4223f-108">The handle is strong, which prevents an object from being reclaimed by garbage collection.</span></span>|  
|`HANDLE_WEAK_TRACK_RESURRECTION`|<span data-ttu-id="4223f-109">ハンドルは、ガベージ コレクションで回収されてからオブジェクトを回避することできませんが、脆弱です。</span><span class="sxs-lookup"><span data-stu-id="4223f-109">The handle is weak, which does not prevent an object from being reclaimed by garbage collection.</span></span><br /><br /> <span data-ttu-id="4223f-110">オブジェクトを収集するときに、ハンドルは無効になります。</span><span class="sxs-lookup"><span data-stu-id="4223f-110">The handle becomes invalid when the object is collected.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="4223f-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="4223f-111">Requirements</span></span>  
 <span data-ttu-id="4223f-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4223f-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4223f-113">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4223f-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4223f-114">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4223f-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4223f-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4223f-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4223f-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="4223f-116">See also</span></span>
- [<span data-ttu-id="4223f-117">列挙型のデバッグ</span><span class="sxs-lookup"><span data-stu-id="4223f-117">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
