---
title: ISymUnmanagedScope::GetLocalCount メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetLocalCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetLocalCount
helpviewer_keywords:
- GetLocalCount method [.NET Framework debugging]
- ISymUnmanagedScope::GetLocalCount method [.NET Framework debugging]
ms.assetid: 3ede8fb5-f655-4088-8e19-9c53812588a8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 809b9033c784954374065a901f34f7542f41e7ab
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54549942"
---
# <a name="isymunmanagedscopegetlocalcount-method"></a><span data-ttu-id="99c09-102">ISymUnmanagedScope::GetLocalCount メソッド</span><span class="sxs-lookup"><span data-stu-id="99c09-102">ISymUnmanagedScope::GetLocalCount Method</span></span>
<span data-ttu-id="99c09-103">このスコープ内で定義されているローカル変数の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="99c09-103">Gets a count of the local variables defined within this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="99c09-104">構文</span><span class="sxs-lookup"><span data-stu-id="99c09-104">Syntax</span></span>  
  
```  
HRESULT GetLocalCount(  
    [out, retval] ULONG32 *pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="99c09-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="99c09-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="99c09-106">[out]ポインター、`ULONG32`ローカル変数の数を受け取る。</span><span class="sxs-lookup"><span data-stu-id="99c09-106">[out] A pointer to a `ULONG32` that receives the count of local variables.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="99c09-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="99c09-107">Return Value</span></span>  
 <span data-ttu-id="99c09-108">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="99c09-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="99c09-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="99c09-109">Requirements</span></span>  
 <span data-ttu-id="99c09-110">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="99c09-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99c09-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="99c09-111">See also</span></span>
- [<span data-ttu-id="99c09-112">ISymUnmanagedScope インターフェイス</span><span class="sxs-lookup"><span data-stu-id="99c09-112">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
