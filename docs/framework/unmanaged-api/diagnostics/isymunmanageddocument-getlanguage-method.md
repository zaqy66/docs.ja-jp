---
title: ISymUnmanagedDocument::GetLanguage メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetLanguage
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetLanguage
helpviewer_keywords:
- ISymUnmanagedDocument::GetLanguage method [.NET Framework debugging]
- GetLanguage method [.NET Framework debugging]
ms.assetid: c6639418-e9f2-4a99-8ce2-ec9876e0bc79
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 186ea5fd46ca5c6205ff1f98d8964e656655a2ad
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54666034"
---
# <a name="isymunmanageddocumentgetlanguage-method"></a><span data-ttu-id="dc816-102">ISymUnmanagedDocument::GetLanguage メソッド</span><span class="sxs-lookup"><span data-stu-id="dc816-102">ISymUnmanagedDocument::GetLanguage Method</span></span>
<span data-ttu-id="dc816-103">このドキュメントの言語識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="dc816-103">Gets the language identifier of this document</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dc816-104">構文</span><span class="sxs-lookup"><span data-stu-id="dc816-104">Syntax</span></span>  
  
```  
HRESULT GetLanguage(  
    [out, retval]  GUID*  pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="dc816-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dc816-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="dc816-106">[out]言語識別子を受け取る変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dc816-106">[out] A pointer to a variable that receives the language identifier.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="dc816-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="dc816-107">Return Value</span></span>  
 <span data-ttu-id="dc816-108">メソッドが成功した場合は s_ok を返します。</span><span class="sxs-lookup"><span data-stu-id="dc816-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc816-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="dc816-109">See also</span></span>
- [<span data-ttu-id="dc816-110">ISymUnmanagedDocument インターフェイス</span><span class="sxs-lookup"><span data-stu-id="dc816-110">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
