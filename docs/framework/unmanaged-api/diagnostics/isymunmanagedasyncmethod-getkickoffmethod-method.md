---
title: ISymUnmanagedAsyncMethod::GetKickoffMethod メソッド
ms.date: 03/30/2017
ms.assetid: ba084444-9e68-4cde-9388-54b950670987
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f20039318d6e1230ccc0fbd203fc44686806bb2e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54604471"
---
# <a name="isymunmanagedasyncmethodgetkickoffmethod-method"></a><span data-ttu-id="cd0e5-102">ISymUnmanagedAsyncMethod::GetKickoffMethod メソッド</span><span class="sxs-lookup"><span data-stu-id="cd0e5-102">ISymUnmanagedAsyncMethod::GetKickoffMethod Method</span></span>
<span data-ttu-id="cd0e5-103">参照してください[DefineKickoffMethod メソッド](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md)します。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-103">See [DefineKickoffMethod Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd0e5-104">構文</span><span class="sxs-lookup"><span data-stu-id="cd0e5-104">Syntax</span></span>  
  
```idl  
HRESULT GetKickoffMethod(    [out, retval] mdToken* kickoffMethod);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cd0e5-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cd0e5-105">Parameters</span></span>  
  
|<span data-ttu-id="cd0e5-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cd0e5-106">Parameter</span></span>|<span data-ttu-id="cd0e5-107">説明</span><span class="sxs-lookup"><span data-stu-id="cd0e5-107">Description</span></span>|  
|---------------|-----------------|  
|`kickoffMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="cd0e5-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="cd0e5-108">Return Value</span></span>  
 <span data-ttu-id="cd0e5-109">`HRESULT` を返します。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cd0e5-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="cd0e5-110">Requirements</span></span>  
 <span data-ttu-id="cd0e5-111">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="cd0e5-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cd0e5-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="cd0e5-112">See also</span></span>
- [<span data-ttu-id="cd0e5-113">ISymUnmanagedAsyncMethod インターフェイス</span><span class="sxs-lookup"><span data-stu-id="cd0e5-113">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
