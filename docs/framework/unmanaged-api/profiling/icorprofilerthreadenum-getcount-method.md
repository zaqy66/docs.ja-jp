---
title: ICorProfilerThreadEnum::GetCount メソッド
ms.date: 03/30/2017
api_name:
- ICorProfilerThreadEnum.GetCount
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerThreadEnum::GetCount
helpviewer_keywords:
- ICorProfilerThreadEnum::GetCount method [.NET Framework profiling]
- GetCount method, ICorProfilerThreadEnum interface [.NET Framework profiling]
ms.assetid: d6dbdc4a-6115-455d-a3f3-704a81d3646b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c96c0a9819012c680a67a22d10d173c83d2f6da3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54536230"
---
# <a name="icorprofilerthreadenumgetcount-method"></a><span data-ttu-id="209f8-102">ICorProfilerThreadEnum::GetCount メソッド</span><span class="sxs-lookup"><span data-stu-id="209f8-102">ICorProfilerThreadEnum::GetCount Method</span></span>
<span data-ttu-id="209f8-103">アプリケーションで使用されるスレッドの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="209f8-103">Gets the number of threads that are used by the application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="209f8-104">構文</span><span class="sxs-lookup"><span data-stu-id="209f8-104">Syntax</span></span>  
  
```  
HRESULT GetCount (    [out] ULONG * pcelt  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="209f8-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="209f8-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="209f8-106">[out]アプリケーションで使用されるスレッドの数。</span><span class="sxs-lookup"><span data-stu-id="209f8-106">[out] The number of threads used by the application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="209f8-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="209f8-107">Requirements</span></span>  
 <span data-ttu-id="209f8-108">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="209f8-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="209f8-109">**ヘッダー:** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="209f8-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="209f8-110">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="209f8-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="209f8-111">**.NET Framework のバージョン:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="209f8-111">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="209f8-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="209f8-112">See also</span></span>
- [<span data-ttu-id="209f8-113">ICorProfilerThreadEnum インターフェイス</span><span class="sxs-lookup"><span data-stu-id="209f8-113">ICorProfilerThreadEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerthreadenum-interface.md)
- [<span data-ttu-id="209f8-114">プロファイリングのインターフェイス</span><span class="sxs-lookup"><span data-stu-id="209f8-114">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
