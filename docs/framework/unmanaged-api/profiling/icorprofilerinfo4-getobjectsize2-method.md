---
title: ICorProfilerInfo4::GetObjectSize2 メソッド
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo4.GetObjectSize2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo4::GetObjectSize2
helpviewer_keywords:
- GetObjectSize2 method, ICorProfilerInfo4 interface [.NET Framework profiling]
- ICorProfilerInfo4::GetObjectSize2 method [.NET Framework profiling]
ms.assetid: 4a3e43ed-3ee3-4395-ab14-f78b903be13e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9a3b0ddc804e8eefdf90b3b0f17f4575b4d92bf3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54502651"
---
# <a name="icorprofilerinfo4getobjectsize2-method"></a><span data-ttu-id="e6288-102">ICorProfilerInfo4::GetObjectSize2 メソッド</span><span class="sxs-lookup"><span data-stu-id="e6288-102">ICorProfilerInfo4::GetObjectSize2 Method</span></span>
<span data-ttu-id="e6288-103">指定したオブジェクトのサイズを返します。</span><span class="sxs-lookup"><span data-stu-id="e6288-103">Returns the size of a specified object.</span></span> <span data-ttu-id="e6288-104">置換、 [icorprofilerinfo::getobjectsize](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getobjectsize-method.md)メソッドで表現できる内容よりも大きいオブジェクトのサイズを報告することによって、`ULONG`します。</span><span class="sxs-lookup"><span data-stu-id="e6288-104">Replaces the [ICorProfilerInfo::GetObjectSize](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getobjectsize-method.md) method by reporting sizes of objects that are larger than what can be expressed in a `ULONG`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e6288-105">構文</span><span class="sxs-lookup"><span data-stu-id="e6288-105">Syntax</span></span>  
  
```  
HRESULT GetObjectSize2(  
    [in]  ObjectID objectId,  
    [out] SIZE_T *pcSize);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e6288-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e6288-106">Parameters</span></span>  
 `objectId`  
 <span data-ttu-id="e6288-107">[in]オブジェクトの ID。</span><span class="sxs-lookup"><span data-stu-id="e6288-107">[in] The ID of the object.</span></span>  
  
 `pcSize`  
 <span data-ttu-id="e6288-108">[out]オブジェクトのサイズ (バイト) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6288-108">[out] A pointer to the object's size, in bytes.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e6288-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="e6288-109">Remarks</span></span>  
 <span data-ttu-id="e6288-110">多くの場合、同じ種類の異なるオブジェクトと同じサイズである場合します。</span><span class="sxs-lookup"><span data-stu-id="e6288-110">Different objects of the same types often have the same size.</span></span> <span data-ttu-id="e6288-111">ただし、配列や文字列など、一部の種類には、オブジェクトごとに別のサイズがあります。</span><span class="sxs-lookup"><span data-stu-id="e6288-111">However, some types, such as arrays or strings, may have a different size for each object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e6288-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="e6288-112">Requirements</span></span>  
 <span data-ttu-id="e6288-113">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e6288-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e6288-114">**ヘッダー:** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e6288-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e6288-115">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e6288-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e6288-116">**.NET Framework のバージョン:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e6288-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e6288-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="e6288-117">See also</span></span>
- [<span data-ttu-id="e6288-118">ICorProfilerInfo4 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e6288-118">ICorProfilerInfo4 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md)
