---
title: ICLRDataEnumMemoryRegionsCallback インターフェイス
ms.date: 03/30/2017
api_name:
- ICLRDataEnumMemoryRegionsCallback
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataEnumMemoryRegionsCallback
helpviewer_keywords:
- ICLRDataEnumMemoryRegionsCallback interface [.NET Framework debugging]
ms.assetid: 3f1af8b0-8478-48e0-a7ec-3e90e0b97649
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b0e7ce243658a8c8a8404ff9079ed1395e56486f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54604152"
---
# <a name="iclrdataenummemoryregionscallback-interface"></a><span data-ttu-id="e65a2-102">ICLRDataEnumMemoryRegionsCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e65a2-102">ICLRDataEnumMemoryRegionsCallback Interface</span></span>
<span data-ttu-id="e65a2-103">コールバック メソッドを提供します[iclrdataenummemoryregions::enummemoryregions](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregions-enummemoryregions-method.md)メモリの指定した領域の列挙の試行の結果をデバッガーに報告します。</span><span class="sxs-lookup"><span data-stu-id="e65a2-103">Provides a callback method for [ICLRDataEnumMemoryRegions::EnumMemoryRegions](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregions-enummemoryregions-method.md) to report to the debugger the result of an attempt to enumerate a specified region of memory.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e65a2-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="e65a2-104">Methods</span></span>  
  
|<span data-ttu-id="e65a2-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="e65a2-105">Method</span></span>|<span data-ttu-id="e65a2-106">説明</span><span class="sxs-lookup"><span data-stu-id="e65a2-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e65a2-107">EnumMemoryRegion メソッド</span><span class="sxs-lookup"><span data-stu-id="e65a2-107">EnumMemoryRegion Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregionscallback-enummemoryregion-method.md)|<span data-ttu-id="e65a2-108">によって呼び出される`ICLRDataEnumMemoryRegions::EnumMemoryRegions`メモリの指定した領域の列挙の試行の結果をデバッガーに報告します。</span><span class="sxs-lookup"><span data-stu-id="e65a2-108">Called by `ICLRDataEnumMemoryRegions::EnumMemoryRegions` to report to the debugger the result of an attempt to enumerate a specified region of memory.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e65a2-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="e65a2-109">Requirements</span></span>  
 <span data-ttu-id="e65a2-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e65a2-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e65a2-111">**ヘッダー:** ClrData.idl、ClrData.h</span><span class="sxs-lookup"><span data-stu-id="e65a2-111">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="e65a2-112">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e65a2-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e65a2-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e65a2-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e65a2-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="e65a2-114">See also</span></span>
- [<span data-ttu-id="e65a2-115">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e65a2-115">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
