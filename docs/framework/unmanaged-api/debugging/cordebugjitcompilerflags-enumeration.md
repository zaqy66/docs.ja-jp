---
title: CorDebugJITCompilerFlags 列挙型
ms.date: 03/30/2017
api_name:
- CorDebugJITCompilerFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugJITCompilerFlags
helpviewer_keywords:
- CorDebugJITCompilerFlags enumeration [.NET Framework debugging]
ms.assetid: c0774f70-5bed-45e8-9922-fdad778c4c33
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 512122d264e0817b89e8a371f57f11d31f7c4380
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54639640"
---
# <a name="cordebugjitcompilerflags-enumeration"></a><span data-ttu-id="c3da2-102">CorDebugJITCompilerFlags 列挙型</span><span class="sxs-lookup"><span data-stu-id="c3da2-102">CorDebugJITCompilerFlags Enumeration</span></span>
<span data-ttu-id="c3da2-103">マネージド Just-In-Time (JIT) コンパイラの動作に影響を与える値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c3da2-103">Contains values that influence the behavior of the managed just-in-time (JIT) compiler.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c3da2-104">構文</span><span class="sxs-lookup"><span data-stu-id="c3da2-104">Syntax</span></span>  
  
```  
typedef enum CorDebugJITCompilerFlags {  
  
    CORDEBUG_JIT_DEFAULT = 0x1,  
    CORDEBUG_JIT_DISABLE_OPTIMIZATION = 0x3,  
    CORDEBUG_JIT_ENABLE_ENC = 0x7  
  
} CorDebugJITCompilerFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="c3da2-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="c3da2-105">Members</span></span>  
  
|<span data-ttu-id="c3da2-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="c3da2-106">Member</span></span>|<span data-ttu-id="c3da2-107">説明</span><span class="sxs-lookup"><span data-stu-id="c3da2-107">Description</span></span>|  
|------------|-----------------|  
|`CORDEBUG_JIT_DEFAULT`|<span data-ttu-id="c3da2-108">コンパイラがコンパイルのデータを追跡し、により、最適化を指定します。</span><span class="sxs-lookup"><span data-stu-id="c3da2-108">Specifies that the compiler should track compilation data, and allows optimizations.</span></span>|  
|`CORDEBUG_JIT_DISABLE_OPTIMIZATION`|<span data-ttu-id="c3da2-109">コンパイラが最適化を無効にしますが、コンパイルのデータを追跡する必要がありますを指定します。</span><span class="sxs-lookup"><span data-stu-id="c3da2-109">Specifies that the compiler should track compilation data, but disables optimizations.</span></span>|  
|`CORDEBUG_JIT_ENABLE_ENC`|<span data-ttu-id="c3da2-110">コンパイラを追跡するコンパイルのデータの最適化を無効にしてエディット コンティニュのテクノロジを有効に指定します。</span><span class="sxs-lookup"><span data-stu-id="c3da2-110">Specifies that the compiler should track compilation data, disables optimizations, and enables Edit and Continue technologies.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c3da2-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="c3da2-111">Requirements</span></span>  
 <span data-ttu-id="c3da2-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3da2-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c3da2-113">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c3da2-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c3da2-114">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c3da2-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c3da2-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c3da2-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c3da2-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="c3da2-116">See also</span></span>
- [<span data-ttu-id="c3da2-117">列挙型のデバッグ</span><span class="sxs-lookup"><span data-stu-id="c3da2-117">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
