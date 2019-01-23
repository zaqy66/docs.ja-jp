---
title: ICorDebugCode2 Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugCode2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode2
helpviewer_keywords:
- ICorDebugCode2 interface [.NET Framework debugging]
ms.assetid: 9321903b-7dea-40d8-ba32-99016c00cc46
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8a5c28ec6c447f3fc3305e0faf51aa868d5a4c17
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499974"
---
# <a name="icordebugcode2-interface1"></a><span data-ttu-id="fe7ed-102">ICorDebugCode2 Interface1</span><span class="sxs-lookup"><span data-stu-id="fe7ed-102">ICorDebugCode2 Interface1</span></span>
<span data-ttu-id="fe7ed-103">"ICorDebugCode"の機能を拡張するメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="fe7ed-103">Provides methods that extend the capabilities of "ICorDebugCode".</span></span>  
  
## <a name="methods"></a><span data-ttu-id="fe7ed-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="fe7ed-104">Methods</span></span>  
  
|<span data-ttu-id="fe7ed-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="fe7ed-105">Method</span></span>|<span data-ttu-id="fe7ed-106">説明</span><span class="sxs-lookup"><span data-stu-id="fe7ed-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="fe7ed-107">GetCodeChunks メソッド</span><span class="sxs-lookup"><span data-stu-id="fe7ed-107">GetCodeChunks Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md)|<span data-ttu-id="fe7ed-108">このコード オブジェクトを構成しているコード チャンクを取得します。</span><span class="sxs-lookup"><span data-stu-id="fe7ed-108">Gets the chunks of code that this code object is composed of.</span></span>|  
|[<span data-ttu-id="fe7ed-109">GetCompilerFlags メソッド</span><span class="sxs-lookup"><span data-stu-id="fe7ed-109">GetCompilerFlags Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcompilerflags-method.md)|<span data-ttu-id="fe7ed-110">このコード オブジェクトが Just-In-Time (JIT) コンパイルされたとき、またはネイティブ イメージ ジェネレーター (Ngen.exe) を使用して生成されたときの条件を指定するフラグを取得します。</span><span class="sxs-lookup"><span data-stu-id="fe7ed-110">Gets the flags that specify the conditions under which this code object was either just-in-time (JIT) compiled or generated using the native image generator (Ngen.exe).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fe7ed-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="fe7ed-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fe7ed-112">このインターフェイスは、コンピューター間またはプロセス間でのリモート呼び出しをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="fe7ed-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe7ed-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="fe7ed-113">Requirements</span></span>  
 <span data-ttu-id="fe7ed-114">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe7ed-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fe7ed-115">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fe7ed-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fe7ed-116">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fe7ed-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fe7ed-117">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fe7ed-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe7ed-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="fe7ed-118">See also</span></span>

- [<span data-ttu-id="fe7ed-119">ICorDebugCode3 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fe7ed-119">ICorDebugCode3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode3-interface.md)
- [<span data-ttu-id="fe7ed-120">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fe7ed-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
