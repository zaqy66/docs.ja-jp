---
title: ISymUnmanagedVariable::GetSignature メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetSignature
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetSignature
helpviewer_keywords:
- GetSignature method, ISymUnmanagedVariable interface [.NET Framework debugging]
- ISymUnmanagedVariable::GetSignature method [.NET Framework debugging]
ms.assetid: 78c1ba28-a410-4360-805c-23a95408964a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 517a731815286130e2451ffdafc4c67181ec0d68
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54647284"
---
# <a name="isymunmanagedvariablegetsignature-method"></a><span data-ttu-id="6333a-102">ISymUnmanagedVariable::GetSignature メソッド</span><span class="sxs-lookup"><span data-stu-id="6333a-102">ISymUnmanagedVariable::GetSignature Method</span></span>
<span data-ttu-id="6333a-103">この変数のシグネチャを取得します。</span><span class="sxs-lookup"><span data-stu-id="6333a-103">Gets the signature of this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6333a-104">構文</span><span class="sxs-lookup"><span data-stu-id="6333a-104">Syntax</span></span>  
  
```  
HRESULT GetSignature(  
    [in]  ULONG32  cSig,  
    [out] ULONG32  *pcSig,  
    [out, size_is(cSig),  
        length_is(*pcSig)] BYTE sig[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6333a-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6333a-105">Parameters</span></span>  
 `cSig`  
 <span data-ttu-id="6333a-106">[in]によって示されるバッファーの長さ、`sig`パラメーター。</span><span class="sxs-lookup"><span data-stu-id="6333a-106">[in] The length of the buffer pointed to by the `sig` parameter.</span></span>  
  
 `pcSig`  
 <span data-ttu-id="6333a-107">[out]ポインター、`ULONG32`シグネチャの格納に必要なバッファーの文字のサイズを受け取る。</span><span class="sxs-lookup"><span data-stu-id="6333a-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the signature.</span></span>  
  
 `sig`  
 <span data-ttu-id="6333a-108">[out]シグネチャを格納するバッファー。</span><span class="sxs-lookup"><span data-stu-id="6333a-108">[out] The buffer that stores the signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6333a-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="6333a-109">Return Value</span></span>  
 <span data-ttu-id="6333a-110">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="6333a-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6333a-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="6333a-111">Requirements</span></span>  
 <span data-ttu-id="6333a-112">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="6333a-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6333a-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="6333a-113">See also</span></span>
- [<span data-ttu-id="6333a-114">ISymUnmanagedVariable インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6333a-114">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
