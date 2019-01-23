---
title: ICorDebugComObjectValue::GetCachedInterfaceTypes メソッド
ms.date: 03/30/2017
api_name:
- ICorDebugComObjectValue::GetCachedInterfaceTypes
api_location:
- mscordbi.dll
f1_keywords:
- ICorDebugComObjectValue::GetCachedInterfaceTypes
helpviewer_keywords:
- GetCachedInterface method, ICorDebugComObjectValue interface [.NET Framework debugging]
- ICorDebugComObjectValue::GetCachedInterface method [.NET Framework debugging]
ms.assetid: d492284f-d3c5-4614-adb8-d718d5042500
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6d0d2c4af79a7d5a7123c5fe0ba043c2dd6302f5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54525808"
---
# <a name="icordebugcomobjectvaluegetcachedinterfacetypes-method"></a><span data-ttu-id="c0b01-102">ICorDebugComObjectValue::GetCachedInterfaceTypes メソッド</span><span class="sxs-lookup"><span data-stu-id="c0b01-102">ICorDebugComObjectValue::GetCachedInterfaceTypes Method</span></span>
<span data-ttu-id="c0b01-103">現在のオブジェクトにキャストまたはとして使用されていることには、列挙子インターフェイス型を提供します。</span><span class="sxs-lookup"><span data-stu-id="c0b01-103">Provides an enumerator for the interface types that the current object has been cast to or used as.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0b01-104">構文</span><span class="sxs-lookup"><span data-stu-id="c0b01-104">Syntax</span></span>  
  
```  
HRESULT GetCachedInterfaceTypes(  
    [in] BOOL bIInspectableOnly,  
    [out] ICorDebugTypeEnum **ppInterfacesEnum);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c0b01-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c0b01-105">Parameters</span></span>  
 `bIInspectableOnly`  
 <span data-ttu-id="c0b01-106">[in]メソッドがのみ返すかどうかを示す値[!INCLUDE[wrt](../../../../includes/wrt-md.md)]インターフェイス (`IInspectable`インターフェイス) またはランタイム呼び出し可能ラッパー (RCW) によってキャッシュされたすべての COM インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="c0b01-106">[in] A value that indicates whether the method returns only [!INCLUDE[wrt](../../../../includes/wrt-md.md)] interfaces (`IInspectable` interfaces) or all COM interfaces cached by the runtime callable wrapper (RCW).</span></span>  
  
 `ppInterfacesEnum`  
 <span data-ttu-id="c0b01-107">[out]キャッシュされたインターフェイス型を表す ICorDebugType オブジェクトへのアクセスを提供する ICorDebugTypeEnum 列挙子のアドレスへのポインターがに従ってフィルター処理された`bIInspectableOnly`します。</span><span class="sxs-lookup"><span data-stu-id="c0b01-107">[out] A pointer to the address of an ICorDebugTypeEnum enumerator that provides access to ICorDebugType objects that represent cached interface types filtered according to `bIInspectableOnly`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c0b01-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="c0b01-108">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c0b01-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="c0b01-109">Requirements</span></span>  
 <span data-ttu-id="c0b01-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c0b01-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0b01-111">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c0b01-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c0b01-112">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c0b01-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c0b01-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c0b01-113">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0b01-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="c0b01-114">See also</span></span>
- [<span data-ttu-id="c0b01-115">ICorDebugComObjectValue のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="c0b01-115">ICorDebugComObjectValue Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcomobjectvalue-interface.md)
- [<span data-ttu-id="c0b01-116">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c0b01-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
