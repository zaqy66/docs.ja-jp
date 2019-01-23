---
title: ICorDebugILCode2 インターフェイス
ms.date: 03/30/2017
api_name:
- ICorDebugILCode2
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: f9dc2afd-df8a-464d-bdbf-5af0a1d4bf85
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d511999cac312c785e528cda24c215555a62ae76
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491169"
---
# <a name="icordebugilcode2-interface"></a><span data-ttu-id="18f6f-102">ICorDebugILCode2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="18f6f-102">ICorDebugILCode2 Interface</span></span>
<span data-ttu-id="18f6f-103">[.NET Framework 4.5.2 以降のバージョンでのみでサポート]</span><span class="sxs-lookup"><span data-stu-id="18f6f-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="18f6f-104">論理的に拡張し、 [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md)に元のメソッド IL オフセットを関数のローカル変数シグネチャのトークンを返すし、プロファイラーのインストルメント化された中間言語 (IL) をマップする方法を提供するインターフェイスオフセットします。</span><span class="sxs-lookup"><span data-stu-id="18f6f-104">Logically extends the [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md) interface to provide methods that return the token for a function's local variable signature, and that map a profiler's instrumented intermediate language (IL) offsets to original method IL offsets.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="18f6f-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="18f6f-105">Methods</span></span>  
  
|<span data-ttu-id="18f6f-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="18f6f-106">Method</span></span>|<span data-ttu-id="18f6f-107">説明</span><span class="sxs-lookup"><span data-stu-id="18f6f-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="18f6f-108">GetInstrumentedILMap メソッド</span><span class="sxs-lookup"><span data-stu-id="18f6f-108">GetInstrumentedILMap Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode2-getinstrumentedilmap-method.md)|<span data-ttu-id="18f6f-109">プロファイラーのインストルメント化された IL オフセットから、このインスタンスに対する元のメソッドの IL オフセットへのマップを返します。</span><span class="sxs-lookup"><span data-stu-id="18f6f-109">Returns a map from profiler instrumented IL offsets to original method IL offsets for this instance.</span></span>|  
|[<span data-ttu-id="18f6f-110">GetLocalVarSigToken メソッド</span><span class="sxs-lookup"><span data-stu-id="18f6f-110">GetLocalVarSigToken Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode2-getlocalvarsigtoken-method.md)|<span data-ttu-id="18f6f-111">このインスタンスで示される関数について、ローカル変数のシグネチャのメタデータ トークンを取得します。</span><span class="sxs-lookup"><span data-stu-id="18f6f-111">Gets the metadata token for the local variable signature for the function that is represented by this instance.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="18f6f-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="18f6f-112">Requirements</span></span>  
 <span data-ttu-id="18f6f-113">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="18f6f-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="18f6f-114">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="18f6f-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="18f6f-115">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="18f6f-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="18f6f-116">**.NET Framework のバージョン:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="18f6f-116">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="18f6f-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="18f6f-117">See also</span></span>
- [<span data-ttu-id="18f6f-118">ICorDebugILCode インターフェイス</span><span class="sxs-lookup"><span data-stu-id="18f6f-118">ICorDebugILCode Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md)
- [<span data-ttu-id="18f6f-119">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="18f6f-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="18f6f-120">デバッグ</span><span class="sxs-lookup"><span data-stu-id="18f6f-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
