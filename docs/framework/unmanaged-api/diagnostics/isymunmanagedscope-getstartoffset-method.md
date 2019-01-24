---
title: ISymUnmanagedScope::GetStartOffset メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetStartOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetStartOffset
helpviewer_keywords:
- GetStartOffset method, ISymUnmanagedScope interface [.NET Framework debugging]
- ISymUnmanagedScope::GetStartOffset method [.NET Framework debugging]
ms.assetid: da6bbc75-94d1-4354-9722-0d455b4428fb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2b81ac93c67d59c294f22eb825527fa9982d9124
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54721098"
---
# <a name="isymunmanagedscopegetstartoffset-method"></a><span data-ttu-id="8462f-102">ISymUnmanagedScope::GetStartOffset メソッド</span><span class="sxs-lookup"><span data-stu-id="8462f-102">ISymUnmanagedScope::GetStartOffset Method</span></span>
<span data-ttu-id="8462f-103">このスコープの開始オフセットを取得します。</span><span class="sxs-lookup"><span data-stu-id="8462f-103">Gets the start offset for this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8462f-104">構文</span><span class="sxs-lookup"><span data-stu-id="8462f-104">Syntax</span></span>  
  
```  
HRESULT GetStartOffset(  
    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8462f-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8462f-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="8462f-106">[out]ポインターを`ULONG32`開始オフセットを格納しています。</span><span class="sxs-lookup"><span data-stu-id="8462f-106">[out] A pointer to a `ULONG32` that contains the starting offset.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8462f-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="8462f-107">Return Value</span></span>  
 <span data-ttu-id="8462f-108">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="8462f-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8462f-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="8462f-109">Requirements</span></span>  
 <span data-ttu-id="8462f-110">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="8462f-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8462f-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="8462f-111">See also</span></span>
- [<span data-ttu-id="8462f-112">ISymUnmanagedScope インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8462f-112">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
- [<span data-ttu-id="8462f-113">GetEndOffSet メソッド</span><span class="sxs-lookup"><span data-stu-id="8462f-113">GetEndOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getendoffset-method.md)
