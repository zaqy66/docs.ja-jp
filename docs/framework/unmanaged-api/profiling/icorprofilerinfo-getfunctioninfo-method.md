---
title: ICorProfilerInfo::GetFunctionInfo メソッド
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetFunctionInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetFunctionInfo
helpviewer_keywords:
- ICorProfilerInfo::GetFunctionInfo method [.NET Framework profiling]
- GetFunctionInfo method [.NET Framework profiling]
ms.assetid: c42b5891-019d-46b3-b551-4606295b75b8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 00b20134c0134aa30d2056b634c8525f66ed8cf5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54602457"
---
# <a name="icorprofilerinfogetfunctioninfo-method"></a><span data-ttu-id="e7781-102">ICorProfilerInfo::GetFunctionInfo メソッド</span><span class="sxs-lookup"><span data-stu-id="e7781-102">ICorProfilerInfo::GetFunctionInfo Method</span></span>
<span data-ttu-id="e7781-103">指定された関数の親クラスとメタデータ トークンを取得します。</span><span class="sxs-lookup"><span data-stu-id="e7781-103">Gets the parent class and metadata token for the specified function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e7781-104">構文</span><span class="sxs-lookup"><span data-stu-id="e7781-104">Syntax</span></span>  
  
```  
HRESULT GetFunctionInfo(  
    [in]  FunctionID functionId,  
    [out] ClassID    *pClassId,  
    [out] ModuleID   *pModuleId,  
    [out] mdToken    *pToken);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e7781-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e7781-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="e7781-106">[in]親クラスとメタデータ トークンを取得する対象の関数の ID。</span><span class="sxs-lookup"><span data-stu-id="e7781-106">[in] The ID of the function for which to get the parent class and metadata token.</span></span>  
  
 `pClassId`  
 <span data-ttu-id="e7781-107">[out] 関数の親クラスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e7781-107">[out] A pointer to the parent class of the function.</span></span>  
  
 `pModuleId`  
 <span data-ttu-id="e7781-108">[out] 関数の親クラスが定義されているモジュールへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e7781-108">[out] A pointer to the module in which the function's parent class is defined.</span></span>  
  
 `pToken`  
 <span data-ttu-id="e7781-109">[out] 関数のメタデータ トークンへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e7781-109">[out] A pointer to the metadata token for the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e7781-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="e7781-110">Remarks</span></span>  
 <span data-ttu-id="e7781-111">プロファイラー コードを呼び出すことができます[icorprofilerinfo::getmodulemetadata](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getmodulemetadata-method.md)指定したモジュールのメタデータ インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="e7781-111">The profiler code can call [ICorProfilerInfo::GetModuleMetaData](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getmodulemetadata-method.md) to obtain a metadata interface for a given module.</span></span> <span data-ttu-id="e7781-112">`pToken` が参照している場所に返されるメタデータ トークンを使用すると、関数のメタデータにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e7781-112">The metadata token that is returned to the location referenced by `pToken` can then be used to access the metadata for the function.</span></span>  
  
 <span data-ttu-id="e7781-113">`ClassID`ジェネリック クラスの関数のできない可能性があります、関数の使用に関する詳細なコンテキスト情報なしで取得できます。</span><span class="sxs-lookup"><span data-stu-id="e7781-113">The `ClassID` of a function on a generic class might not be obtainable without more contextual information about the use of the function.</span></span> <span data-ttu-id="e7781-114">この場合、`pClassId`は 0 になります。</span><span class="sxs-lookup"><span data-stu-id="e7781-114">In this case, `pClassId` will be 0.</span></span> <span data-ttu-id="e7781-115">Profiler のコードを使用する必要があります[icorprofilerinfo 2::getfunctioninfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getfunctioninfo2-method.md) COR_PRF_FRAME_INFO の値に詳細なコンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="e7781-115">Profiler code should use [ICorProfilerInfo2::GetFunctionInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getfunctioninfo2-method.md) with a COR_PRF_FRAME_INFO value to provide more context.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e7781-116">必要条件</span><span class="sxs-lookup"><span data-stu-id="e7781-116">Requirements</span></span>  
 <span data-ttu-id="e7781-117">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7781-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e7781-118">**ヘッダー:** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e7781-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e7781-119">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e7781-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e7781-120">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e7781-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7781-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7781-121">See also</span></span>
- [<span data-ttu-id="e7781-122">ICorProfilerInfo インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e7781-122">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
