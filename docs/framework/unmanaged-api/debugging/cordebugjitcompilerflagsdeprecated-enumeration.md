---
title: CorDebugJITCompilerFlagsDeprecated 列挙型
ms.date: 03/30/2017
api_name:
- CorDebugJITCompilerFlagsDeprecated
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugJITCompilerFlagsDeprecated
helpviewer_keywords:
- CorDebugJITCompilerFlagsDeprecated enumeration [.NET Framework debugging]
ms.assetid: af15e2ca-6be1-472b-bd36-03644a1e3ddd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4ef262fcae117b27f06d4dba3b2087028b5cfa65
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54743258"
---
# <a name="cordebugjitcompilerflagsdeprecated-enumeration"></a><span data-ttu-id="7169d-102">CorDebugJITCompilerFlagsDeprecated 列挙型</span><span class="sxs-lookup"><span data-stu-id="7169d-102">CorDebugJITCompilerFlagsDeprecated Enumeration</span></span>
<span data-ttu-id="7169d-103">この列挙体は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="7169d-103">This enumeration is obsolete.</span></span> <span data-ttu-id="7169d-104">使用して、`CORDEBUG_JIT_DEFAULT`のメンバー、 [CorDebugJITCompilerFlags](../../../../docs/framework/unmanaged-api/debugging/cordebugjitcompilerflags-enumeration.md)列挙代わりにします。</span><span class="sxs-lookup"><span data-stu-id="7169d-104">Use the `CORDEBUG_JIT_DEFAULT` member of the [CorDebugJITCompilerFlags](../../../../docs/framework/unmanaged-api/debugging/cordebugjitcompilerflags-enumeration.md) enumeration instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7169d-105">構文</span><span class="sxs-lookup"><span data-stu-id="7169d-105">Syntax</span></span>  
  
```  
typedef enum CorDebugJITCompilerFlagsDeprecated {  
    CORDEBUG_JIT_TRACK_DEBUG_INFO  = 0x1  
} CorDebugJITCompilerFlagsDeprecated;  
```  
  
## <a name="members"></a><span data-ttu-id="7169d-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="7169d-106">Members</span></span>  
  
|<span data-ttu-id="7169d-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="7169d-107">Member</span></span>|<span data-ttu-id="7169d-108">説明</span><span class="sxs-lookup"><span data-stu-id="7169d-108">Description</span></span>|  
|------------|-----------------|  
|`CORDEBUG_JIT_TRACK_DEBUG_INFO`|<span data-ttu-id="7169d-109">代わりに、`CORDEBUG_JIT_DEFAULT` を使用してください。</span><span class="sxs-lookup"><span data-stu-id="7169d-109">Use `CORDEBUG_JIT_DEFAULT` instead.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="7169d-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="7169d-110">Requirements</span></span>  
 <span data-ttu-id="7169d-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7169d-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7169d-112">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7169d-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7169d-113">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7169d-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7169d-114">**.NET framework のバージョン:** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="7169d-114">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7169d-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="7169d-115">See also</span></span>
- [<span data-ttu-id="7169d-116">列挙型のデバッグ</span><span class="sxs-lookup"><span data-stu-id="7169d-116">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
