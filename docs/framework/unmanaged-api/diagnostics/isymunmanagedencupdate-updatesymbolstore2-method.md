---
title: ISymUnmanagedENCUpdate::UpdateSymbolStore2 メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate.UpdateSymbolStore2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate::UpdateSymbolStore2
helpviewer_keywords:
- ISymUnmanagedENCUpdate::UpdateSymbolStore2 method [.NET Framework debugging]
- UpdateSymbolStore2 method [.NET Framework debugging]
ms.assetid: 35588317-6184-485c-ab41-4b15fc1765d9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 78d9e27299c9d7ed7d6cb9b09dd659ba081c5fde
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47204970"
---
# <a name="isymunmanagedencupdateupdatesymbolstore2-method"></a><span data-ttu-id="b0881-102">ISymUnmanagedENCUpdate::UpdateSymbolStore2 メソッド</span><span class="sxs-lookup"><span data-stu-id="b0881-102">ISymUnmanagedENCUpdate::UpdateSymbolStore2 Method</span></span>
<span data-ttu-id="b0881-103">コンパイラが行情報が要件を満たしている限り、プログラム データベース (PDB) のストリームから変更されていない関数を省略できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b0881-103">Allows a compiler to omit functions that have not been modified from the program database (PDB) stream, provided the line information meets the requirements.</span></span> <span data-ttu-id="b0881-104">PDB の行の古い情報と、関数のすべての行の 1 つのデルタは正しい行情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="b0881-104">The correct line information can be determined with the old PDB line information and one delta for all lines in the function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b0881-105">構文</span><span class="sxs-lookup"><span data-stu-id="b0881-105">Syntax</span></span>  
  
```  
HRESULT UpdateSymbolStore2(  
    [in]  IStream      *pIStream,  
    [in]  SYMLINEDELTA* pDeltaLines,  
    [in]  ULONG         cDeltaLines);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b0881-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0881-106">Parameters</span></span>  
 `pIStream`  
 <span data-ttu-id="b0881-107">[in]ポインター、 [IStream](/windows/desktop/api/objidl/nn-objidl-istream)行情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="b0881-107">[in] A pointer to an [IStream](/windows/desktop/api/objidl/nn-objidl-istream) that contains the line information.</span></span>  
  
 `pDeltaLines`  
 <span data-ttu-id="b0881-108">[in]ポインターを[SYMLINEDELTA](../../../../docs/framework/unmanaged-api/diagnostics/symlinedelta-structure.md)が変更された行を含む構造体。</span><span class="sxs-lookup"><span data-stu-id="b0881-108">[in] A pointer to a [SYMLINEDELTA](../../../../docs/framework/unmanaged-api/diagnostics/symlinedelta-structure.md) structure that contains the lines that have changed.</span></span>  
  
 `cDeltaLines`  
 <span data-ttu-id="b0881-109">[in]A`ULONG`が変更された行の数を表します。</span><span class="sxs-lookup"><span data-stu-id="b0881-109">[in] A `ULONG` that represents the number of lines that have changed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b0881-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="b0881-110">Return Value</span></span>  
 <span data-ttu-id="b0881-111">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="b0881-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b0881-112">要件</span><span class="sxs-lookup"><span data-stu-id="b0881-112">Requirements</span></span>  
 <span data-ttu-id="b0881-113">**ヘッダー:** CorSym.idl、CorSym.h</span><span class="sxs-lookup"><span data-stu-id="b0881-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0881-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="b0881-114">See Also</span></span>  
 [<span data-ttu-id="b0881-115">ISymUnmanagedENCUpdate インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b0881-115">ISymUnmanagedENCUpdate Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)
