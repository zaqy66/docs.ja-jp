---
title: ICorProfilerFunctionControl インターフェイス
ms.date: 03/30/2017
api_name:
- ICorProfilerFunctionControl
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerFunctionControl
helpviewer_keywords:
- ICorProfilerFunctionControl interface [.NET Framework profiling]
ms.assetid: 4e3d3141-4662-4166-8f05-bc857c1b4216
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 37e0c9dcbd8975338e7c64dbd9c44dd54508b4d6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54649714"
---
# <a name="icorprofilerfunctioncontrol-interface"></a><span data-ttu-id="e3dd0-102">ICorProfilerFunctionControl インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3dd0-102">ICorProfilerFunctionControl Interface</span></span>
<span data-ttu-id="e3dd0-103">特定のメソッドを再コンパイルする時に JIT コンパイラーがコードをどのように生成するかを制御するために、コード プロファイラーが共通言語ランタイム (CLR) と通信できるようにするメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="e3dd0-103">Provides methods that allow a code profiler to communicate with the common language runtime (CLR) to control how the JIT compiler should generate code when recompiling a specific method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e3dd0-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="e3dd0-104">Methods</span></span>  
  
|<span data-ttu-id="e3dd0-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="e3dd0-105">Method</span></span>|<span data-ttu-id="e3dd0-106">説明</span><span class="sxs-lookup"><span data-stu-id="e3dd0-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e3dd0-107">SetCodegenFlags メソッド</span><span class="sxs-lookup"><span data-stu-id="e3dd0-107">SetCodegenFlags Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md)|<span data-ttu-id="e3dd0-108">1 つまたは複数のフラグを設定、 [COR_PRF_CODEGEN_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-codegen-flags-enumeration.md)を - just-in-time (JIT) のコード生成を制御する列挙型の再コンパイルされた関数。</span><span class="sxs-lookup"><span data-stu-id="e3dd0-108">Sets one or more flags from the [COR_PRF_CODEGEN_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-codegen-flags-enumeration.md) enumeration to control code generation for a just-in-time (JIT) recompiled function.</span></span>|  
|[<span data-ttu-id="e3dd0-109">SetILFunctionBody メソッド</span><span class="sxs-lookup"><span data-stu-id="e3dd0-109">SetILFunctionBody Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setilfunctionbody-method.md)|<span data-ttu-id="e3dd0-110">メソッドの中間共通言語 (CIL) 本体を置換します。</span><span class="sxs-lookup"><span data-stu-id="e3dd0-110">Replaces the Common Intermediate Language (CIL) body of the method.</span></span>|  
|[<span data-ttu-id="e3dd0-111">SetILInstrumentedCodeMap メソッド</span><span class="sxs-lookup"><span data-stu-id="e3dd0-111">SetILInstrumentedCodeMap Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setilinstrumentedcodemap-method.md)|<span data-ttu-id="e3dd0-112">指定した共通中間言語 (CIL) マップ エントリを使用して、指定される関数のコード マップを設定します。</span><span class="sxs-lookup"><span data-stu-id="e3dd0-112">Sets a code map for the specified function by using the specified Common Intermediate Language (CIL) map entries.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e3dd0-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="e3dd0-113">Remarks</span></span>  
 <span data-ttu-id="e3dd0-114">`ICorProfilerFunctionControl` インターフェイスは、単一の再コンパイルされた関数に対してコード生成を制御するためにメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="e3dd0-114">The `ICorProfilerFunctionControl` interface provides methods for controlling code generation for a single recompiled function.</span></span> <span data-ttu-id="e3dd0-115">プロファイラーは、使用して、このインターフェイスのインスタンスを取得、 [icorprofilercallback 4::getrejitparameters](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-getrejitparameters-method.md)コールバック。</span><span class="sxs-lookup"><span data-stu-id="e3dd0-115">The profiler obtains an instance of this interface through the [ICorProfilerCallback4::GetReJITParameters](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-getrejitparameters-method.md) callback.</span></span> <span data-ttu-id="e3dd0-116">`ICorProfilerFunctionControl` の各インスタンスは一つの関数の全てのインスタンスを制御します。</span><span class="sxs-lookup"><span data-stu-id="e3dd0-116">Each instance of `ICorProfilerFunctionControl` controls all instances of one function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e3dd0-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="e3dd0-117">Requirements</span></span>  
 <span data-ttu-id="e3dd0-118">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e3dd0-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e3dd0-119">**ヘッダー:** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e3dd0-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e3dd0-120">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e3dd0-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e3dd0-121">**.NET Framework のバージョン:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e3dd0-121">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3dd0-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="e3dd0-122">See also</span></span>
- [<span data-ttu-id="e3dd0-123">ICorProfilerInfo4 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3dd0-123">ICorProfilerInfo4 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md)
- [<span data-ttu-id="e3dd0-124">プロファイリングのインターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3dd0-124">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="e3dd0-125">EnumJITedFunctions2 メソッド</span><span class="sxs-lookup"><span data-stu-id="e3dd0-125">EnumJITedFunctions2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-enumjitedfunctions2-method.md)
