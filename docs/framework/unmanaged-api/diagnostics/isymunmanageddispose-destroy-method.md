---
title: ISymUnmanagedDispose::Destroy メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDispose.Destroy
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDispose::Destroy
helpviewer_keywords:
- ISymUnmanagedDispose::Destroy method [.NET Framework debugging]
- Destroy method [.NET Framework debugging]
ms.assetid: a854ab9f-d2ba-470e-867f-808c1e7bd07a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6a4a0bac056c7c88a491ac05a17b662ace833df1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54614459"
---
# <a name="isymunmanageddisposedestroy-method"></a><span data-ttu-id="86535-102">ISymUnmanagedDispose::Destroy メソッド</span><span class="sxs-lookup"><span data-stu-id="86535-102">ISymUnmanagedDispose::Destroy Method</span></span>
<span data-ttu-id="86535-103">基になるオブジェクトを内部参照をすべて解放し、後続のメソッド呼び出しでエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="86535-103">Causes the underlying object to release all internal references and return failure on any subsequent method calls.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86535-104">構文</span><span class="sxs-lookup"><span data-stu-id="86535-104">Syntax</span></span>  
  
```  
HRESULT Destroy();  
```  
  
## <a name="return-value"></a><span data-ttu-id="86535-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="86535-105">Return Value</span></span>  
 <span data-ttu-id="86535-106">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="86535-106">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="86535-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="86535-107">Requirements</span></span>  
 <span data-ttu-id="86535-108">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="86535-108">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86535-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="86535-109">See also</span></span>
- [<span data-ttu-id="86535-110">ISymUnmanagedDispose インターフェイス</span><span class="sxs-lookup"><span data-stu-id="86535-110">ISymUnmanagedDispose Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddispose-interface.md)
