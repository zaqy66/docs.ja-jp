---
title: ISymUnmanagedWriter::Abort メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.Abort
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::Abort
helpviewer_keywords:
- ISymUnmanagedWriter::Abort method [.NET Framework debugging]
- Abort method, ISymUnmanagedWriter interface [.NET Framework debugging]
ms.assetid: 416b220f-38d4-48e0-bb49-d2faa7366702
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b4c79cb3df37a9ed10e46567be63aad29fee37c4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54550189"
---
# <a name="isymunmanagedwriterabort-method"></a><span data-ttu-id="c750b-102">ISymUnmanagedWriter::Abort メソッド</span><span class="sxs-lookup"><span data-stu-id="c750b-102">ISymUnmanagedWriter::Abort Method</span></span>
<span data-ttu-id="c750b-103">シンボルをシンボル ストアにコミットせずには、シンボル ライターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c750b-103">Closes the symbol writer without committing the symbols to the symbol store.</span></span> <span data-ttu-id="c750b-104">この呼び出しの後、シンボルのライターが、以降の更新は無効になります。</span><span class="sxs-lookup"><span data-stu-id="c750b-104">After this call, the symbol writer becomes invalid for further updates.</span></span> <span data-ttu-id="c750b-105">コミットのシンボルをシンボル ライターを閉じるは、使用、 [isymunmanagedwriter::close](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-close-method.md)メソッド代わりにします。</span><span class="sxs-lookup"><span data-stu-id="c750b-105">To commit the symbols and close the symbol writer, use the [ISymUnmanagedWriter::Close](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-close-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c750b-106">構文</span><span class="sxs-lookup"><span data-stu-id="c750b-106">Syntax</span></span>  
  
```  
HRESULT Abort();  
```  
  
## <a name="return-value"></a><span data-ttu-id="c750b-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="c750b-107">Return Value</span></span>  
 <span data-ttu-id="c750b-108">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="c750b-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c750b-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="c750b-109">Requirements</span></span>  
 <span data-ttu-id="c750b-110">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="c750b-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c750b-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="c750b-111">See also</span></span>
- [<span data-ttu-id="c750b-112">ISymUnmanagedWriter インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c750b-112">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
