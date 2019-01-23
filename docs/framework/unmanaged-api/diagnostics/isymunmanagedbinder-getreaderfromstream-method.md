---
title: ISymUnmanagedBinder::GetReaderFromStream メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder.GetReaderFromStream
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder::GetReaderFromStream
helpviewer_keywords:
- ISymUnmanagedBinder::GetReaderFromStream method [.NET Framework debugging]
- GetReaderFromStream method [.NET Framework debugging]
ms.assetid: aa38efd4-de7e-4482-a5d3-adc152093460
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: af4e9124140c2b311fb2c10800200f5d4d8dc679
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54545765"
---
# <a name="isymunmanagedbindergetreaderfromstream-method"></a><span data-ttu-id="6f686-102">ISymUnmanagedBinder::GetReaderFromStream メソッド</span><span class="sxs-lookup"><span data-stu-id="6f686-102">ISymUnmanagedBinder::GetReaderFromStream Method</span></span>
<span data-ttu-id="6f686-103">メタデータ インターフェイスとシンボル ストアを格納しているストリームでは、指定されたを返します、正しい[ISymUnmanagedReader](isymunmanagedreader-interface.md)構造は、デバッグを読み取ることが特定のシンボル ストアからシンボルします。</span><span class="sxs-lookup"><span data-stu-id="6f686-103">Given a metadata interface and a stream that contains the symbol store, returns the correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) structure that will read the debugging symbols from the given symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6f686-104">構文</span><span class="sxs-lookup"><span data-stu-id="6f686-104">Syntax</span></span>  
  
```  
HRESULT GetReaderFromStream(  
    [in]  IUnknown  *importer,  
    [in]  IStream   *pstream,  
    [out,retval] ISymUnmanagedReader **pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6f686-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6f686-105">Parameters</span></span>  
 `importer`  
 <span data-ttu-id="6f686-106">[in]メタデータ インポート インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6f686-106">[in] A pointer to the metadata import interface.</span></span>  
  
 `pstream`  
 <span data-ttu-id="6f686-107">[in]シンボル ストアを格納しているストリームへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6f686-107">[in] A pointer to the stream that contains the symbol store.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="6f686-108">[out]設定されているポインターに返された[ISymUnmanagedReader](isymunmanagedreader-interface.md)インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="6f686-108">[out] A pointer that is set to the returned [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6f686-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="6f686-109">Return Value</span></span>  
 <span data-ttu-id="6f686-110">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="6f686-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6f686-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="6f686-111">Requirements</span></span>  
 <span data-ttu-id="6f686-112">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="6f686-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6f686-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f686-113">See also</span></span>
- [<span data-ttu-id="6f686-114">ISymUnmanagedBinder インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6f686-114">ISymUnmanagedBinder Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md)
