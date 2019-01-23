---
title: ISymUnmanagedSymbolSearchInfo::GetHRESULT メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSymbolSearchInfo.GetHRESULT
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSymbolSearchInfo::GetHRESULT
helpviewer_keywords:
- ISymUnmanagedSymbolSearchInfo::GetHRESULT method [.NET Framework debugging]
- GetHRESULT method [.NET Framework debugging]
ms.assetid: 6999dc3d-65d7-4bf6-bb0a-6efc0fc72588
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 15f85a6f5ab418692d747cc9ad415c637d7b96e2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54614368"
---
# <a name="isymunmanagedsymbolsearchinfogethresult-method"></a><span data-ttu-id="c810a-102">ISymUnmanagedSymbolSearchInfo::GetHRESULT メソッド</span><span class="sxs-lookup"><span data-stu-id="c810a-102">ISymUnmanagedSymbolSearchInfo::GetHRESULT Method</span></span>
<span data-ttu-id="c810a-103">HRESULT を取得します。</span><span class="sxs-lookup"><span data-stu-id="c810a-103">Gets the HRESULT.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c810a-104">構文</span><span class="sxs-lookup"><span data-stu-id="c810a-104">Syntax</span></span>  
  
```  
HRESULT GetHRESULT(  
    [out] HRESULT *phr);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c810a-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c810a-105">Parameters</span></span>  
 `phr`  
 <span data-ttu-id="c810a-106">[out]HRESULT へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c810a-106">[out] A pointer to the HRESULT.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c810a-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="c810a-107">Return Value</span></span>  
 <span data-ttu-id="c810a-108">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="c810a-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c810a-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="c810a-109">Requirements</span></span>  
 <span data-ttu-id="c810a-110">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="c810a-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c810a-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="c810a-111">See also</span></span>
- [<span data-ttu-id="c810a-112">ISymUnmanagedSymbolSearchInfo インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c810a-112">ISymUnmanagedSymbolSearchInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-interface.md)
