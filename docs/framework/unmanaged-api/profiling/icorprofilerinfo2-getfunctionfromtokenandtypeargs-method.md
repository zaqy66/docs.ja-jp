---
title: ICorProfilerInfo2::GetFunctionFromTokenAndTypeArgs メソッド
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetFunctionFromTokenAndTypeArgs
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetFunctionFromTokenAndTypeArgs
helpviewer_keywords:
- ICorProfilerInfo2::GetFunctionFromTokenAndTypeArgs method [.NET Framework profiling]
- GetFunctionFromTokenAndTypeArgs method [.NET Framework profiling]
ms.assetid: ce8f6aa6-4ebf-4a86-b429-4bbc8af41a8f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 60a9ba78211cd02300cccc7d150bb08fa68b0604
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54556182"
---
# <a name="icorprofilerinfo2getfunctionfromtokenandtypeargs-method"></a><span data-ttu-id="45daf-102">ICorProfilerInfo2::GetFunctionFromTokenAndTypeArgs メソッド</span><span class="sxs-lookup"><span data-stu-id="45daf-102">ICorProfilerInfo2::GetFunctionFromTokenAndTypeArgs Method</span></span>
<span data-ttu-id="45daf-103">取得、`FunctionID`クラスを格納している、指定したメタデータ トークンを使用して関数のおよび`ClassID`のいずれかの値が引数を入力します。</span><span class="sxs-lookup"><span data-stu-id="45daf-103">Gets the `FunctionID` of a function by using the specified metadata token, containing class, and `ClassID` values of any type arguments.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="45daf-104">構文</span><span class="sxs-lookup"><span data-stu-id="45daf-104">Syntax</span></span>  
  
```  
HRESULT GetFunctionFromTokenAndTypeArgs(  
    [in] ModuleID moduleID,  
    [in] mdMethodDef funcDef,  
    [in] ClassID classId,  
    [in] ULONG32 cTypeArgs,  
    [in, size_is(cTypeArgs)] ClassID typeArgs[],  
    [out] FunctionID* pFunctionID);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="45daf-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="45daf-105">Parameters</span></span>  
 `moduleID`  
 <span data-ttu-id="45daf-106">[in]関数が存在するモジュールの ID。</span><span class="sxs-lookup"><span data-stu-id="45daf-106">[in] The ID of the module in which the function resides.</span></span>  
  
 `funcDef`  
 <span data-ttu-id="45daf-107">[in]`mdMethodDef`関数を参照するメタデータ トークン。</span><span class="sxs-lookup"><span data-stu-id="45daf-107">[in] An `mdMethodDef` metadata token that references the function.</span></span>  
  
 `classId`  
 <span data-ttu-id="45daf-108">[in]関数の外側のクラスの ID。</span><span class="sxs-lookup"><span data-stu-id="45daf-108">[in] The ID of the function's containing class.</span></span>  
  
 `cTypeArgs`  
 <span data-ttu-id="45daf-109">[in]指定された関数の型パラメーターの数。</span><span class="sxs-lookup"><span data-stu-id="45daf-109">[in] The number of type parameters for the given function.</span></span> <span data-ttu-id="45daf-110">この値は、非ジェネリック関数に 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="45daf-110">This value must be zero for non-generic functions.</span></span>  
  
 `typeArgs`  
 <span data-ttu-id="45daf-111">[in]配列の`ClassID`関数の引数は、それぞれの値。</span><span class="sxs-lookup"><span data-stu-id="45daf-111">[in] An array of `ClassID` values, each of which is an argument of the function.</span></span> <span data-ttu-id="45daf-112">値`typeArgs`場合に NULL が`cTypeArgs`0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="45daf-112">The value of `typeArgs` can be NULL if `cTypeArgs` is set to zero.</span></span>  
  
 `pFunctionID`  
 <span data-ttu-id="45daf-113">[out]ポインター、`FunctionID`指定された関数。</span><span class="sxs-lookup"><span data-stu-id="45daf-113">[out] A pointer to the `FunctionID` of the specified function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="45daf-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="45daf-114">Remarks</span></span>  
 <span data-ttu-id="45daf-115">呼び出す、`GetFunctionFromTokenAndTypeArgs`メソッドを`mdMethodRef`メタデータの代わりに、`mdMethodDef`メタデータ トークンが予期しない結果を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="45daf-115">Calling the `GetFunctionFromTokenAndTypeArgs` method with an `mdMethodRef` metadata instead of an `mdMethodDef` metadata token can have unpredictable results.</span></span> <span data-ttu-id="45daf-116">呼び出し元を解決する必要があります、`mdMethodRef`を`mdMethodDef`渡すとき。</span><span class="sxs-lookup"><span data-stu-id="45daf-116">Callers should resolve the `mdMethodRef` to an `mdMethodDef` when passing it.</span></span>  
  
 <span data-ttu-id="45daf-117">関数が既に読み込まれていない場合は、呼び出す`GetFunctionFromTokenAndTypeArgs`これはさまざまなコンテキストで危険な操作が発生する読み込みが発生します。</span><span class="sxs-lookup"><span data-stu-id="45daf-117">If the function is not already loaded, calling `GetFunctionFromTokenAndTypeArgs` will cause loading to occur, which is a dangerous operation in many contexts.</span></span> <span data-ttu-id="45daf-118">たとえば、モジュールまたは型の読み込み中にこのメソッドを呼び出すと、ランタイムが循環的に読み込みしよう無限ループが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="45daf-118">For example, calling this method during loading of modules or types could lead to an infinite loop as the runtime attempts to circularly load things.</span></span>  
  
 <span data-ttu-id="45daf-119">一般の使用`GetFunctionFromTokenAndTypeArgs`をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="45daf-119">In general, use of `GetFunctionFromTokenAndTypeArgs` is discouraged.</span></span> <span data-ttu-id="45daf-120">プロファイラー イベントを特定の関数の場合、保存する必要があります、`ModuleID`と`mdMethodDef`その関数、および使用の[icorprofilerinfo 2::getfunctioninfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getfunctioninfo2-method.md)を確認するかどうかを指定した`FunctionID`は必要な関数です。</span><span class="sxs-lookup"><span data-stu-id="45daf-120">If profilers are interested in events for a particular function, they should store the `ModuleID` and `mdMethodDef` of that function, and use [ICorProfilerInfo2::GetFunctionInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getfunctioninfo2-method.md) to check whether a given `FunctionID` is that of the desired function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="45daf-121">必要条件</span><span class="sxs-lookup"><span data-stu-id="45daf-121">Requirements</span></span>  
 <span data-ttu-id="45daf-122">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="45daf-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="45daf-123">**ヘッダー:** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="45daf-123">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="45daf-124">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="45daf-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="45daf-125">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="45daf-125">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="45daf-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="45daf-126">See also</span></span>
- [<span data-ttu-id="45daf-127">ICorProfilerInfo インターフェイス</span><span class="sxs-lookup"><span data-stu-id="45daf-127">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [<span data-ttu-id="45daf-128">ICorProfilerInfo2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="45daf-128">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
