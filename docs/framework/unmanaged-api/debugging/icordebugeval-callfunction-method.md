---
title: ICorDebugEval::CallFunction メソッド
ms.date: 03/30/2017
api_name:
- ICorDebugEval.CallFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::CallFunction
helpviewer_keywords:
- ICorDebugEval::CallFunction method [.NET Framework debugging]
- CallFunction method [.NET Framework debugging]
ms.assetid: 7f470c5c-e1c0-4d8d-aad8-830f113ae751
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 493b4850436b3724287210878992d1d8ce8fe168
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54589400"
---
# <a name="icordebugevalcallfunction-method"></a><span data-ttu-id="acc4d-102">ICorDebugEval::CallFunction メソッド</span><span class="sxs-lookup"><span data-stu-id="acc4d-102">ICorDebugEval::CallFunction Method</span></span>
<span data-ttu-id="acc4d-103">指定した関数の呼び出しを設定します。</span><span class="sxs-lookup"><span data-stu-id="acc4d-103">Sets up a call to the specified function.</span></span>  
  
 <span data-ttu-id="acc4d-104">このメソッドは、.NET Framework version 2.0 で廃止されています。</span><span class="sxs-lookup"><span data-stu-id="acc4d-104">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="acc4d-105">使用[icordebugeval 2::callparameterizedfunction](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-callparameterizedfunction-method.md)代わりにします。</span><span class="sxs-lookup"><span data-stu-id="acc4d-105">Use [ICorDebugEval2::CallParameterizedFunction](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-callparameterizedfunction-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="acc4d-106">構文</span><span class="sxs-lookup"><span data-stu-id="acc4d-106">Syntax</span></span>  
  
```  
HRESULT CallFunction (  
    [in] ICorDebugFunction  *pFunction,  
    [in] ULONG32            nArgs,  
    [in, size_is(nArgs)] ICorDebugValue *ppArgs[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="acc4d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="acc4d-107">Parameters</span></span>  
 `pFunction`  
 <span data-ttu-id="acc4d-108">[in]呼び出される関数を指定する ICorDebugFunction オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="acc4d-108">[in] Pointer to an ICorDebugFunction object that specifies the function to be called.</span></span>  
  
 `nArgs`  
 <span data-ttu-id="acc4d-109">[in]関数の引数の数。</span><span class="sxs-lookup"><span data-stu-id="acc4d-109">[in] The number of arguments for the function.</span></span>  
  
 `ppArgs`  
 <span data-ttu-id="acc4d-110">[in]関数に渡される引数を指定する ICorDebugValue オブジェクトを指す各ポインターの配列。</span><span class="sxs-lookup"><span data-stu-id="acc4d-110">[in] An array of pointers, each of which points to an ICorDebugValue object that specifies an argument to be passed to the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="acc4d-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="acc4d-111">Remarks</span></span>  
 <span data-ttu-id="acc4d-112">関数が仮想場合、`CallFunction`仮想ディスパッチを実行します。</span><span class="sxs-lookup"><span data-stu-id="acc4d-112">If the function is virtual, `CallFunction` will perform virtual dispatch.</span></span> <span data-ttu-id="acc4d-113">関数は、別のアプリケーション ドメインでは、すべての引数がそのアプリケーション ドメイン内にも限りの移行が発生します。</span><span class="sxs-lookup"><span data-stu-id="acc4d-113">If the function is in a different application domain, a transition will occur as long as all arguments are also in that application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="acc4d-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="acc4d-114">Requirements</span></span>  
 <span data-ttu-id="acc4d-115">**プラットフォーム:** WindowSee[システム要件](../../../../docs/framework/get-started/system-requirements.md)します。</span><span class="sxs-lookup"><span data-stu-id="acc4d-115">**Platforms:** WindowSee [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="acc4d-116">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="acc4d-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="acc4d-117">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="acc4d-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="acc4d-118">**.NET framework のバージョン:** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="acc4d-118">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="acc4d-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="acc4d-119">See also</span></span>
- [<span data-ttu-id="acc4d-120">CallParameterizedFunction メソッド</span><span class="sxs-lookup"><span data-stu-id="acc4d-120">CallParameterizedFunction Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-callparameterizedfunction-method.md)
