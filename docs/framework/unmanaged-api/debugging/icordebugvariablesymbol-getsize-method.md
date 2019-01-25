---
title: ICorDebugVariableSymbol::GetSize メソッド
ms.date: 03/30/2017
ms.assetid: add0cd9d-9a29-49b1-ae07-d9d3786b4ccd
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8a41ec4a556ca26404b5f76ddb35d9f73d7307a7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54659057"
---
# <a name="icordebugvariablesymbolgetsize-method"></a><span data-ttu-id="c9f40-102">ICorDebugVariableSymbol::GetSize メソッド</span><span class="sxs-lookup"><span data-stu-id="c9f40-102">ICorDebugVariableSymbol::GetSize Method</span></span>
<span data-ttu-id="c9f40-103">変数のサイズ (バイト単位) を取得します。</span><span class="sxs-lookup"><span data-stu-id="c9f40-103">Gets the size of a variable in bytes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c9f40-104">構文</span><span class="sxs-lookup"><span data-stu-id="c9f40-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcbValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c9f40-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c9f40-105">Parameters</span></span>  
 `pcbValue`  
 <span data-ttu-id="c9f40-106">変数のサイズが格納されている 32 ビットの符号なし整数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c9f40-106">A pointer to a 32-bit unsigned integer containing the size of the variable.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c9f40-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="c9f40-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c9f40-108">このメソッドは .NET ネイティブでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="c9f40-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c9f40-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="c9f40-109">Requirements</span></span>  
 <span data-ttu-id="c9f40-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9f40-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c9f40-111">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c9f40-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c9f40-112">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c9f40-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c9f40-113">**.NET Framework のバージョン:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c9f40-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c9f40-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="c9f40-114">See also</span></span>
- [<span data-ttu-id="c9f40-115">ICorDebugVariableSymbol インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c9f40-115">ICorDebugVariableSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="c9f40-116">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c9f40-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
