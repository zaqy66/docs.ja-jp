---
title: CorDebugGuidToTypeMapping 構造体
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- CorDebugGuidToTypeMapping
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugGuidToTypeMapping
helpviewer_keywords:
- CorDebugGuidToTypeMapping structure [.NET Framework debugging]
ms.assetid: 57dbccd9-b16d-4da3-ae25-7a2cf9adf679
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 49290a37ca7ea101e3c8b458a5daa4995cb3beee
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54610046"
---
# <a name="cordebugguidtotypemapping-structure"></a><span data-ttu-id="9340a-102">CorDebugGuidToTypeMapping 構造体</span><span class="sxs-lookup"><span data-stu-id="9340a-102">CorDebugGuidToTypeMapping Structure</span></span>
<span data-ttu-id="9340a-103">マップを[!INCLUDE[wrt](../../../../includes/wrt-md.md)]を対応する ICorDebugType オブジェクトの GUID。</span><span class="sxs-lookup"><span data-stu-id="9340a-103">Maps a [!INCLUDE[wrt](../../../../includes/wrt-md.md)] GUID to its corresponding ICorDebugType object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9340a-104">構文</span><span class="sxs-lookup"><span data-stu-id="9340a-104">Syntax</span></span>  
  
```cpp
typedef struct CorDebugGuidToTypeMapping {  
    GUID iid;  
    ICorDebugType *pType;  
} CorDebugGuidToTypeMapping;  
```  
  
## <a name="members"></a><span data-ttu-id="9340a-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="9340a-105">Members</span></span>  
  
|<span data-ttu-id="9340a-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="9340a-106">Member</span></span>|<span data-ttu-id="9340a-107">説明</span><span class="sxs-lookup"><span data-stu-id="9340a-107">Description</span></span>|  
|------------|-----------------|  
|`iid`|<span data-ttu-id="9340a-108">キャッシュされた GUID[!INCLUDE[wrt](../../../../includes/wrt-md.md)]型。</span><span class="sxs-lookup"><span data-stu-id="9340a-108">The GUID of the cached [!INCLUDE[wrt](../../../../includes/wrt-md.md)] type.</span></span>|  
|`pType`|<span data-ttu-id="9340a-109">キャッシュされている型に関する情報を提供する ICorDebugType オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9340a-109">A pointer to an ICorDebugType object that provides information about the cached type.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9340a-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="9340a-110">Requirements</span></span>  
 <span data-ttu-id="9340a-111">**プラットフォーム:** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]します。</span><span class="sxs-lookup"><span data-stu-id="9340a-111">**Platforms:** [!INCLUDE[wrt](../../../../includes/wrt-md.md)].</span></span>  
  
 <span data-ttu-id="9340a-112">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9340a-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9340a-113">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9340a-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9340a-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9340a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9340a-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="9340a-115">See also</span></span>
- [<span data-ttu-id="9340a-116">デバッグ構造体</span><span class="sxs-lookup"><span data-stu-id="9340a-116">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="9340a-117">デバッグ</span><span class="sxs-lookup"><span data-stu-id="9340a-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
