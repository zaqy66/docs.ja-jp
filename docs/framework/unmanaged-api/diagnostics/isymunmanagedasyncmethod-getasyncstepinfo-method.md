---
title: ISymUnmanagedAsyncMethod::GetAsyncStepInfo メソッド
ms.date: 03/30/2017
ms.assetid: 3ef5b4b8-4ac7-4906-849b-f932c5e3db07
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fa87188765450e84fc2417be8530ff43c88c237c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54666229"
---
# <a name="isymunmanagedasyncmethodgetasyncstepinfo-method"></a><span data-ttu-id="6e6ef-102">ISymUnmanagedAsyncMethod::GetAsyncStepInfo メソッド</span><span class="sxs-lookup"><span data-stu-id="6e6ef-102">ISymUnmanagedAsyncMethod::GetAsyncStepInfo Method</span></span>
<span data-ttu-id="6e6ef-103">参照してください[DefineAsyncStepInfo メソッド](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md)します。</span><span class="sxs-lookup"><span data-stu-id="6e6ef-103">See [DefineAsyncStepInfo Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e6ef-104">構文</span><span class="sxs-lookup"><span data-stu-id="6e6ef-104">Syntax</span></span>  
  
```idl  
HRESULT GetAsyncStepInfo(    [in] ULONG32 cStepInfo,    [out] ULONG32 *pcStepInfo,    [in, size_is(cStepInfo)] ULONG32 yieldOffsets[],    [in, size_is(cStepInfo)] ULONG32 breakpointOffset[],    [in, size_is(cStepInfo)] mdToken breakpointMethod[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6e6ef-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6e6ef-105">Parameters</span></span>  
  
|<span data-ttu-id="6e6ef-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6e6ef-106">Parameter</span></span>|<span data-ttu-id="6e6ef-107">説明</span><span class="sxs-lookup"><span data-stu-id="6e6ef-107">Description</span></span>|  
|---------------|-----------------|  
|`cStepInfo`||  
|`pcStepInfo`||  
|`yieldOffsets`||  
|`breakpointOffset`||  
|`breakpointMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="6e6ef-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="6e6ef-108">Return Value</span></span>  
 <span data-ttu-id="6e6ef-109">`HRESULT` を返します。</span><span class="sxs-lookup"><span data-stu-id="6e6ef-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6e6ef-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="6e6ef-110">Requirements</span></span>  
 <span data-ttu-id="6e6ef-111">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="6e6ef-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e6ef-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="6e6ef-112">See also</span></span>
- [<span data-ttu-id="6e6ef-113">ISymUnmanagedAsyncMethod インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6e6ef-113">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
