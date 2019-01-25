---
title: ICorDebugLoadedModule::GetName メソッド
ms.date: 03/30/2017
ms.assetid: 88c304d5-edaa-4c0e-a8e1-144e8a76877e
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e97c7c793df389dd6a8f670e985a9c9384eab639
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54703745"
---
# <a name="icordebugloadedmodulegetname-method"></a><span data-ttu-id="5b8af-102">ICorDebugLoadedModule::GetName メソッド</span><span class="sxs-lookup"><span data-stu-id="5b8af-102">ICorDebugLoadedModule::GetName Method</span></span>
<span data-ttu-id="5b8af-103">読み込まれたモジュールの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="5b8af-103">Gets the name of the loaded module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5b8af-104">構文</span><span class="sxs-lookup"><span data-stu-id="5b8af-104">Syntax</span></span>  
  
```  
HRESULT GetName(  
   [in] ULONG32 cchName,  
   [out] ULONG32 *pcchName,  
   [out, size_is(cchName),  
   length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5b8af-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5b8af-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="5b8af-106">[in] `szName` バッファー内の文字数。</span><span class="sxs-lookup"><span data-stu-id="5b8af-106">[in] The number of characters in the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="5b8af-107">[out] `szName` バッファーに実際に書き込まれた文字数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5b8af-107">[out] A pointer to the number of characters actually written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="5b8af-108">[out] 読み込まれたモジュールの名前が含まれている文字配列。</span><span class="sxs-lookup"><span data-stu-id="5b8af-108">[out] An array of characters that contain the name of the loaded module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5b8af-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="5b8af-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5b8af-110">このメソッドは .NET ネイティブでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="5b8af-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5b8af-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="5b8af-111">Requirements</span></span>  
 <span data-ttu-id="5b8af-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b8af-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5b8af-113">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5b8af-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5b8af-114">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5b8af-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5b8af-115">**.NET Framework のバージョン:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5b8af-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5b8af-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="5b8af-116">See also</span></span>
- [<span data-ttu-id="5b8af-117">ICorDebugLoadedModule インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5b8af-117">ICorDebugLoadedModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-interface.md)
- [<span data-ttu-id="5b8af-118">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5b8af-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
