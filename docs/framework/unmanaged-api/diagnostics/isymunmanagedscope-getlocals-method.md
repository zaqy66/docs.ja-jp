---
title: ISymUnmanagedScope::GetLocals メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetLocals
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetLocals
helpviewer_keywords:
- GetLocals method [.NET Framework debugging]
- ISymUnmanagedScope::GetLocals method [.NET Framework debugging]
ms.assetid: 17c45f15-8c44-44da-b070-f902077b36e4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8d0e1b764691fd2582e1225cb90003e2a644061f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54643690"
---
# <a name="isymunmanagedscopegetlocals-method"></a><span data-ttu-id="11ed4-102">ISymUnmanagedScope::GetLocals メソッド</span><span class="sxs-lookup"><span data-stu-id="11ed4-102">ISymUnmanagedScope::GetLocals Method</span></span>
<span data-ttu-id="11ed4-103">このスコープ内で定義されているローカル変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="11ed4-103">Gets the local variables defined within this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="11ed4-104">構文</span><span class="sxs-lookup"><span data-stu-id="11ed4-104">Syntax</span></span>  
  
```  
HRESULT GetLocals(  
    [in]  ULONG32  cLocals,  
    [out] ULONG32  *pcLocals,  
    [out, size_is(cLocals),  
        length_is(*pcLocals)] ISymUnmanagedVariable* locals[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="11ed4-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="11ed4-105">Parameters</span></span>  
 `cLocals`  
 <span data-ttu-id="11ed4-106">[in]A`ULONG32`のサイズを示す、`locals`配列。</span><span class="sxs-lookup"><span data-stu-id="11ed4-106">[in] A `ULONG32` that indicates the size of the `locals` array.</span></span>  
  
 `pcLocals`  
 <span data-ttu-id="11ed4-107">[out]ポインター、`ULONG32`ローカル変数の格納に必要なバッファーのサイズを受け取る。</span><span class="sxs-lookup"><span data-stu-id="11ed4-107">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the local variables.</span></span>  
  
 `locals`  
 <span data-ttu-id="11ed4-108">[out]ローカル変数を受け取る配列。</span><span class="sxs-lookup"><span data-stu-id="11ed4-108">[out] The array that receives the local variables.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="11ed4-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="11ed4-109">Return Value</span></span>  
 <span data-ttu-id="11ed4-110">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="11ed4-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="11ed4-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="11ed4-111">Requirements</span></span>  
 <span data-ttu-id="11ed4-112">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="11ed4-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="11ed4-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="11ed4-113">See also</span></span>
- [<span data-ttu-id="11ed4-114">ISymUnmanagedScope インターフェイス</span><span class="sxs-lookup"><span data-stu-id="11ed4-114">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
