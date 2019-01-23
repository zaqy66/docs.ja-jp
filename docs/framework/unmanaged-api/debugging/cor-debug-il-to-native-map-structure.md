---
title: COR_DEBUG_IL_TO_NATIVE_MAP 構造体
ms.date: 03/30/2017
api_name:
- COR_DEBUG_IL_TO_NATIVE_MAP
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_DEBUG_IL_TO_NATIVE_MAP
helpviewer_keywords:
- COR_DEBUG_IL_TO_NATIVE_MAP structure [.NET Framework debugging]
ms.assetid: 06f3b504-085f-4142-934a-25381fe23d4c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 56d4255b06f1317c87685737e4ee4021c37a77f5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54555012"
---
# <a name="cordebugiltonativemap-structure"></a><span data-ttu-id="d4919-102">COR_DEBUG_IL_TO_NATIVE_MAP 構造体</span><span class="sxs-lookup"><span data-stu-id="d4919-102">COR_DEBUG_IL_TO_NATIVE_MAP Structure</span></span>
<span data-ttu-id="d4919-103">Microsoft intermediate language (MSIL) コードをネイティブ コードにマップするために使用するオフセットが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d4919-103">Contains the offsets that are used to map Microsoft intermediate language (MSIL) code to native code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d4919-104">構文</span><span class="sxs-lookup"><span data-stu-id="d4919-104">Syntax</span></span>  
  
```  
typedef struct COR_DEBUG_IL_TO_NATIVE_MAP {  
    ULONG32  ilOffset;  
    ULONG32  nativeStartOffset;  
    ULONG32  nativeEndOffset;  
} COR_DEBUG_IL_TO_NATIVE_MAP;  
```  
  
## <a name="members"></a><span data-ttu-id="d4919-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="d4919-105">Members</span></span>  
  
|<span data-ttu-id="d4919-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="d4919-106">Member</span></span>|<span data-ttu-id="d4919-107">説明</span><span class="sxs-lookup"><span data-stu-id="d4919-107">Description</span></span>|  
|------------|-----------------|  
|`ilOffset`|<span data-ttu-id="d4919-108">MSIL コードのオフセット。</span><span class="sxs-lookup"><span data-stu-id="d4919-108">The offset of the MSIL code.</span></span>|  
|`nativeStartOffset`|<span data-ttu-id="d4919-109">ネイティブ コードの開始のオフセット。</span><span class="sxs-lookup"><span data-stu-id="d4919-109">The offset of the start of the native code.</span></span>|  
|`nativeEndOffset`|<span data-ttu-id="d4919-110">ネイティブ コードの最後のオフセット。</span><span class="sxs-lookup"><span data-stu-id="d4919-110">The offset of the end of the native code.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d4919-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="d4919-111">Requirements</span></span>  
 <span data-ttu-id="d4919-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4919-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d4919-113">**ヘッダー:** CorProf.idl, CorDebug.idl</span><span class="sxs-lookup"><span data-stu-id="d4919-113">**Header:** CorProf.idl, CorDebug.idl</span></span>  
  
 <span data-ttu-id="d4919-114">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d4919-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d4919-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d4919-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d4919-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="d4919-116">See also</span></span>
- [<span data-ttu-id="d4919-117">GetILToNativeMapping メソッド</span><span class="sxs-lookup"><span data-stu-id="d4919-117">GetILToNativeMapping Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getiltonativemapping-method.md)
- [<span data-ttu-id="d4919-118">GetILToNativeMapping メソッド</span><span class="sxs-lookup"><span data-stu-id="d4919-118">GetILToNativeMapping Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode-getiltonativemapping-method.md)
- [<span data-ttu-id="d4919-119">デバッグ構造体</span><span class="sxs-lookup"><span data-stu-id="d4919-119">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="d4919-120">デバッグ</span><span class="sxs-lookup"><span data-stu-id="d4919-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
