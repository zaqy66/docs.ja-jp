---
title: ICorDebugVariableSymbol::GetName メソッド
ms.date: 03/30/2017
ms.assetid: c922b7d4-44e5-45e4-aef3-cc9c35a0be80
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c5b414e1fa035a50cdcfd317592f69abdc40fb0c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54684112"
---
# <a name="icordebugvariablesymbolgetname-method"></a><span data-ttu-id="cf435-102">ICorDebugVariableSymbol::GetName メソッド</span><span class="sxs-lookup"><span data-stu-id="cf435-102">ICorDebugVariableSymbol::GetName Method</span></span>
<span data-ttu-id="cf435-103">変数の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="cf435-103">Gets the name of a variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cf435-104">構文</span><span class="sxs-lookup"><span data-stu-id="cf435-104">Syntax</span></span>  
  
```  
HRESULT GetName(  
   [in] ULONG32 cchName,   
   [out] ULONG32 *pcchName,   
   [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cf435-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cf435-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="cf435-106">[in] `szName` バッファー内の文字数。</span><span class="sxs-lookup"><span data-stu-id="cf435-106">[in] The number of characters in the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="cf435-107">[out] `szName` バッファーに実際に書き込まれた文字数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf435-107">[out] A pointer to the number of characters actually written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="cf435-108">変数名が格納されている文字配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf435-108">A pointer to a character array that contains the variable name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cf435-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="cf435-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cf435-110">このメソッドは .NET ネイティブでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="cf435-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cf435-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="cf435-111">Requirements</span></span>  
 <span data-ttu-id="cf435-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cf435-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cf435-113">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cf435-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cf435-114">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cf435-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cf435-115">**.NET Framework のバージョン:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cf435-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cf435-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf435-116">See also</span></span>
- [<span data-ttu-id="cf435-117">ICorDebugVariableSymbol インターフェイス</span><span class="sxs-lookup"><span data-stu-id="cf435-117">ICorDebugVariableSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="cf435-118">デバッグ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="cf435-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
