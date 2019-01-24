---
title: ISymUnmanagedWriter5::CloseMapTokensToSourceSpans メソッド
ms.date: 03/30/2017
ms.assetid: f8a0c0a2-a11d-436c-aa85-bc110215cfd6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ce4b41854d5d9324169b1873f431ef81c0a4c5be
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54677919"
---
# <a name="isymunmanagedwriter5closemaptokenstosourcespans-method"></a><span data-ttu-id="8a001-102">ISymUnmanagedWriter5::CloseMapTokensToSourceSpans メソッド</span><span class="sxs-lookup"><span data-stu-id="8a001-102">ISymUnmanagedWriter5::CloseMapTokensToSourceSpans Method</span></span>
<span data-ttu-id="8a001-103">マッピングの情報ソースへのトークンの範囲は、特別なカスタム データのセクションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8a001-103">Close the special custom data section for token-to-source span mapping information.</span></span> <span data-ttu-id="8a001-104">閉じられた後は、以上のマッピング情報を追加できます。</span><span class="sxs-lookup"><span data-stu-id="8a001-104">After it is closed, no more mapping information can be added.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a001-105">構文</span><span class="sxs-lookup"><span data-stu-id="8a001-105">Syntax</span></span>  
  
```idl  
HRESULT CloseMapTokensToSourceSpans();  
```  
  
## <a name="return-value"></a><span data-ttu-id="8a001-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="8a001-106">Return Value</span></span>  
 <span data-ttu-id="8a001-107">`HRESULT` を返します。</span><span class="sxs-lookup"><span data-stu-id="8a001-107">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a001-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="8a001-108">Requirements</span></span>  
 <span data-ttu-id="8a001-109">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="8a001-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8a001-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="8a001-110">See also</span></span>
- [<span data-ttu-id="8a001-111">ISymUnmanagedWriter5 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8a001-111">ISymUnmanagedWriter5 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)
