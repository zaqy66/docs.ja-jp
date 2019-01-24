---
title: ISymUnmanagedENCUpdate::UpdateMethodLines メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate.UpdateMethodLines
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate::UpdateMethodLines
helpviewer_keywords:
- UpdateMethodLines method [.NET Framework debugging]
- ISymUnmanagedENCUpdate::UpdateMethodLines method [.NET Framework debugging]
ms.assetid: 275ef87b-0b53-49f9-af6b-58506335dc06
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f7905b3ee83378ed1a27501b082dbfca01d6436c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54688065"
---
# <a name="isymunmanagedencupdateupdatemethodlines-method"></a><span data-ttu-id="a2092-102">ISymUnmanagedENCUpdate::UpdateMethodLines メソッド</span><span class="sxs-lookup"><span data-stu-id="a2092-102">ISymUnmanagedENCUpdate::UpdateMethodLines Method</span></span>
<span data-ttu-id="a2092-103">再コンパイルされていない、その行が個別に移動されたメソッドの行情報の更新を許可します。</span><span class="sxs-lookup"><span data-stu-id="a2092-103">Allows updating the line information for a method that has not been recompiled, but whose lines have moved independently.</span></span> <span data-ttu-id="a2092-104">各ステートメントのデルタが許可されます。</span><span class="sxs-lookup"><span data-stu-id="a2092-104">A delta for each statement is allowed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a2092-105">構文</span><span class="sxs-lookup"><span data-stu-id="a2092-105">Syntax</span></span>  
  
```  
HRESULT UpdateMethodLines(  
    [in]  mdMethodDef  mdMethodToken,  
    [in, size_is(cDeltas)] INT32*  pDeltas,  
    [in]  ULONG        cDeltas);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a2092-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a2092-106">Parameters</span></span>  
 `mdMethodToken`  
 <span data-ttu-id="a2092-107">[in]メソッドのトークンのメタデータ。</span><span class="sxs-lookup"><span data-stu-id="a2092-107">[in] The metadata of the method token.</span></span>  
  
 `pDeltas`  
 <span data-ttu-id="a2092-108">[in]配列の`INT32`メソッドでは、各シーケンス ポイントのデルタを示す値。</span><span class="sxs-lookup"><span data-stu-id="a2092-108">[in] An array of `INT32` values that indicates deltas for each sequence point in the method.</span></span>  
  
 `cDeltas`  
 <span data-ttu-id="a2092-109">[in]A`ULONG`のサイズを含む、`pDeltas`パラメーター。</span><span class="sxs-lookup"><span data-stu-id="a2092-109">[in] A `ULONG` containing the size of the `pDeltas` parameter.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a2092-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="a2092-110">Return Value</span></span>  
 <span data-ttu-id="a2092-111">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="a2092-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a2092-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="a2092-112">Requirements</span></span>  
 <span data-ttu-id="a2092-113">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="a2092-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2092-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="a2092-114">See also</span></span>
- [<span data-ttu-id="a2092-115">ISymUnmanagedENCUpdate インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2092-115">ISymUnmanagedENCUpdate Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)
