---
title: ICorDebugCodeEnum::Next メソッド
ms.date: 03/30/2017
api_name:
- ICorDebugCodeEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCodeEnum::Next
helpviewer_keywords:
- ICorDebugCodeEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugEnum interface [.NET Framework debugging]
ms.assetid: 644ece86-384d-4c63-9fba-52c789616ff7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 45caad20ef7d2dbe35e0381fb8cd697fc526398f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54529805"
---
# <a name="icordebugcodeenumnext-method"></a><span data-ttu-id="35363-102">ICorDebugCodeEnum::Next メソッド</span><span class="sxs-lookup"><span data-stu-id="35363-102">ICorDebugCodeEnum::Next Method</span></span>
<span data-ttu-id="35363-103">列挙体の現在位置から指定された"ICorDebugCode"インスタンス数を取得します。</span><span class="sxs-lookup"><span data-stu-id="35363-103">Gets the specified number of "ICorDebugCode" instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35363-104">構文</span><span class="sxs-lookup"><span data-stu-id="35363-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugCode *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="35363-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="35363-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="35363-106">[in]数`ICorDebugCode`インスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="35363-106">[in] The number of `ICorDebugCode` instances to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="35363-107">[out]それぞれが指すポインターの配列、`ICorDebugCode`オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="35363-107">[out] An array of pointers, each of which points to an `ICorDebugCode` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="35363-108">[out]数へのポインター`ICorDebugCode`インスタンスが実際に返されます。</span><span class="sxs-lookup"><span data-stu-id="35363-108">[out] A pointer to the number of `ICorDebugCode` instances actually returned.</span></span> <span data-ttu-id="35363-109">この値は null になる場合`celt`は 1 つです。</span><span class="sxs-lookup"><span data-stu-id="35363-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="35363-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="35363-110">Requirements</span></span>  
 <span data-ttu-id="35363-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="35363-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="35363-112">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="35363-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="35363-113">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="35363-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="35363-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="35363-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="35363-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="35363-115">See also</span></span>


