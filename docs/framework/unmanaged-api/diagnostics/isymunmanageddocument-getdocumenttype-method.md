---
title: ISymUnmanagedDocument::GetDocumentType メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetDocumentType
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetDocumentType
helpviewer_keywords:
- ISymUnmanagedDocument::GetDocumentType method [.NET Framework debugging]
- GetDocumentType method [.NET Framework debugging]
ms.assetid: 2d381ab1-7e7c-4281-af2b-e54d879b3ef8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: adad8854052d76476076e5e1357f6d3e2dec1052
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629476"
---
# <a name="isymunmanageddocumentgetdocumenttype-method"></a><span data-ttu-id="4bca6-102">ISymUnmanagedDocument::GetDocumentType メソッド</span><span class="sxs-lookup"><span data-stu-id="4bca6-102">ISymUnmanagedDocument::GetDocumentType Method</span></span>
<span data-ttu-id="4bca6-103">このドキュメントのドキュメントの種類を取得します。</span><span class="sxs-lookup"><span data-stu-id="4bca6-103">Gets the document type of this document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4bca6-104">構文</span><span class="sxs-lookup"><span data-stu-id="4bca6-104">Syntax</span></span>  
  
```  
HRESULT GetDocumentType(  
    [out, retval] GUID*  pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4bca6-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4bca6-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="4bca6-106">[out]ドキュメントの種類を受け取る変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4bca6-106">[out] Pointer to a variable that receives the document type.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4bca6-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="4bca6-107">Return Value</span></span>  
 <span data-ttu-id="4bca6-108">メソッドが成功した場合は s_ok を返します。</span><span class="sxs-lookup"><span data-stu-id="4bca6-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4bca6-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="4bca6-109">See also</span></span>
- [<span data-ttu-id="4bca6-110">ISymUnmanagedDocument インターフェイス</span><span class="sxs-lookup"><span data-stu-id="4bca6-110">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
