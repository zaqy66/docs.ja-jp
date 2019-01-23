---
title: ICorDebugFunction3 インターフェイス
ms.date: 03/30/2017
api_name:
- ICorDebugFunction3
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: b22717b9-ead5-4eea-887e-789b52d613dc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e564ce63f7bf9e04ebf9a0bdcfc819ea23b3b2ff
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54515561"
---
# <a name="icordebugfunction3-interface"></a><span data-ttu-id="4b303-102">ICorDebugFunction3 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="4b303-102">ICorDebugFunction3 Interface</span></span>
<span data-ttu-id="4b303-103">[.NET Framework 4.5.2 以降のバージョンでのみでサポート]</span><span class="sxs-lookup"><span data-stu-id="4b303-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="4b303-104">ReJIT 要求からコードへのアクセスを提供する ICorDebugFunction インターフェイスを論理的に拡張します。</span><span class="sxs-lookup"><span data-stu-id="4b303-104">Logically extends the ICorDebugFunction interface to provide access to code from a ReJIT request.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4b303-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="4b303-105">Methods</span></span>  
  
|<span data-ttu-id="4b303-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="4b303-106">Method</span></span>|<span data-ttu-id="4b303-107">説明</span><span class="sxs-lookup"><span data-stu-id="4b303-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4b303-108">GetActiveReJitRequestILCode メソッド</span><span class="sxs-lookup"><span data-stu-id="4b303-108">GetActiveReJitRequestILCode Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction3-getactiverejitrequestilcode-method.md)|<span data-ttu-id="4b303-109">インターフェイス ポインターを取得、 [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md)アクティブな ReJIT 要求から IL を格納しています。</span><span class="sxs-lookup"><span data-stu-id="4b303-109">Gets an interface pointer to an [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md) that contains the IL from an active ReJIT request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4b303-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="4b303-110">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4b303-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="4b303-111">Requirements</span></span>  
 <span data-ttu-id="4b303-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b303-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4b303-113">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4b303-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4b303-114">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4b303-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4b303-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4b303-115">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b303-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b303-116">See also</span></span>
- [<span data-ttu-id="4b303-117">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="4b303-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="4b303-118">デバッグ</span><span class="sxs-lookup"><span data-stu-id="4b303-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="4b303-119">ReJIT:ハウツー ガイド</span><span class="sxs-lookup"><span data-stu-id="4b303-119">ReJIT: A How-To Guide</span></span>](https://blogs.msdn.com/b/davbr/archive/2011/10/12/rejit-a-how-to-guide.aspx)
