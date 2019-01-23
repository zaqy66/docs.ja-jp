---
title: ISymUnmanagedDocument::HasEmbeddedSource メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.HasEmbeddedSource
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::HasEmbeddedSource
helpviewer_keywords:
- HasEmbeddedSource method [.NET Framework debugging]
- ISymUnmanagedDocument::HasEmbeddedSource method [.NET Framework debugging]
ms.assetid: 385fc4d3-365c-4645-b7b0-6c4c5344b79f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: acff919cbeb6b5d71197664139cdc9212961e314
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629515"
---
# <a name="isymunmanageddocumenthasembeddedsource-method"></a><span data-ttu-id="ddf0f-102">ISymUnmanagedDocument::HasEmbeddedSource メソッド</span><span class="sxs-lookup"><span data-stu-id="ddf0f-102">ISymUnmanagedDocument::HasEmbeddedSource Method</span></span>
<span data-ttu-id="ddf0f-103">返します`true`ドキュメントが、デバッグのシンボルに埋め込まれたソースを返しますそれ以外の場合、`false`します。</span><span class="sxs-lookup"><span data-stu-id="ddf0f-103">Returns `true` if the document has source embedded in the debugging symbols; otherwise, returns `false`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ddf0f-104">構文</span><span class="sxs-lookup"><span data-stu-id="ddf0f-104">Syntax</span></span>  
  
```  
HRESULT HasEmbeddedSource(  
   [out, retval]  BOOL  *pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ddf0f-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ddf0f-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="ddf0f-106">[out]デバッグのシンボルにドキュメントがソースになっているかどうかを示す変数へのポインターが埋め込まれます。</span><span class="sxs-lookup"><span data-stu-id="ddf0f-106">[out] A pointer to a variable that indicates whether the document has source embedded in the debugging symbols.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ddf0f-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="ddf0f-107">Return Value</span></span>  
 <span data-ttu-id="ddf0f-108">メソッドが成功した場合は s_ok を返します。</span><span class="sxs-lookup"><span data-stu-id="ddf0f-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ddf0f-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="ddf0f-109">See also</span></span>
- [<span data-ttu-id="ddf0f-110">ISymUnmanagedDocument インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ddf0f-110">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
