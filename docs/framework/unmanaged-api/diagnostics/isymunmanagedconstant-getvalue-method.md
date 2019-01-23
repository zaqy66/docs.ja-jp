---
title: ISymUnmanagedConstant::GetValue メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedConstant.GetValue
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedConstant::GetValue
helpviewer_keywords:
- GetValue method, ISymUnmanagedConstant interface [.NET Framework debugging]
- ISymUnmanagedConstant::GetValue method [.NET Framework debugging]
ms.assetid: 0036fc10-e768-47a8-b9cf-bf47faf8d194
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1043a7efe70798fbbc52ce6d1d0e16510e7c0503
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499146"
---
# <a name="isymunmanagedconstantgetvalue-method"></a><span data-ttu-id="0314a-102">ISymUnmanagedConstant::GetValue メソッド</span><span class="sxs-lookup"><span data-stu-id="0314a-102">ISymUnmanagedConstant::GetValue Method</span></span>
<span data-ttu-id="0314a-103">定数の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0314a-103">Gets the value of the constant.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0314a-104">構文</span><span class="sxs-lookup"><span data-stu-id="0314a-104">Syntax</span></span>  
  
```  
HRESULT GetValue(  
    [out]  VARIANT* pValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0314a-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0314a-105">Parameters</span></span>  
 `pValue`  
 <span data-ttu-id="0314a-106">[out]値を受け取る変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0314a-106">[out] A pointer to a variable that receives the value.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0314a-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="0314a-107">Return Value</span></span>  
 <span data-ttu-id="0314a-108">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="0314a-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0314a-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="0314a-109">Requirements</span></span>  
 <span data-ttu-id="0314a-110">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="0314a-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0314a-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="0314a-111">See also</span></span>
- [<span data-ttu-id="0314a-112">ISymUnmanagedConstant インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0314a-112">ISymUnmanagedConstant Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-interface.md)
- [<span data-ttu-id="0314a-113">GetName メソッド</span><span class="sxs-lookup"><span data-stu-id="0314a-113">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getname-method.md)
- [<span data-ttu-id="0314a-114">GetSignature メソッド</span><span class="sxs-lookup"><span data-stu-id="0314a-114">GetSignature Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getsignature-method.md)
