---
title: ISymUnmanagedDocument::GetSourceRange メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetSourceRange
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetSourceRange
helpviewer_keywords:
- ISymUnmanagedDocument::GetSourceRange method [.NET Framework debugging]
- GetSourceRange method [.NET Framework debugging]
ms.assetid: 20fefee7-1040-41ba-93dc-bd42f68b90c2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a89c706ece0949ffa3c182d53b57221acf81b18d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54515072"
---
# <a name="isymunmanageddocumentgetsourcerange-method"></a><span data-ttu-id="260ee-102">ISymUnmanagedDocument::GetSourceRange メソッド</span><span class="sxs-lookup"><span data-stu-id="260ee-102">ISymUnmanagedDocument::GetSourceRange Method</span></span>
<span data-ttu-id="260ee-103">指定されたバッファーに埋め込みのソースの指定した範囲を返します。</span><span class="sxs-lookup"><span data-stu-id="260ee-103">Returns the specified range of the embedded source into the given buffer.</span></span> <span data-ttu-id="260ee-104">バッファーは、ソースを保持するために十分な大きさである必要があります。</span><span class="sxs-lookup"><span data-stu-id="260ee-104">The buffer must be large enough to hold the source.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="260ee-105">構文</span><span class="sxs-lookup"><span data-stu-id="260ee-105">Syntax</span></span>  
  
```  
HRESULT GetSourceRange(  
    [in]  ULONG32  startLine,  
    [in]  ULONG32  startColumn,  
    [in]  ULONG32  endLine,  
    [in]  ULONG32  endColumn,  
    [in]  ULONG32  cSourceBytes,  
    [out] ULONG32  *pcSourceBytes,  
    [out, size_is(cSourceBytes),  
        length_is(*pcSourceBytes)] BYTE source[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="260ee-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="260ee-106">Parameters</span></span>  
 `startLine`  
 <span data-ttu-id="260ee-107">[in]現在のドキュメント内の開始行。</span><span class="sxs-lookup"><span data-stu-id="260ee-107">[in] The starting line in the current document.</span></span>  
  
 `startColumn`  
 <span data-ttu-id="260ee-108">[in]現在のドキュメント内の開始列。</span><span class="sxs-lookup"><span data-stu-id="260ee-108">[in] The starting column in the current document.</span></span>  
  
 `endLine`  
 <span data-ttu-id="260ee-109">[in]現在のドキュメントの最後の行。</span><span class="sxs-lookup"><span data-stu-id="260ee-109">[in] The final line in the current document.</span></span>  
  
 `endColumn`  
 <span data-ttu-id="260ee-110">[in]現在のドキュメントの最後の列。</span><span class="sxs-lookup"><span data-stu-id="260ee-110">[in] The final column in the current document.</span></span>  
  
 `cSourceBytes`  
 <span data-ttu-id="260ee-111">[in] \(バイト単位)、ソースのサイズ。</span><span class="sxs-lookup"><span data-stu-id="260ee-111">[in] The size of the source, in bytes.</span></span>  
  
 `pcSourceBytes`  
 <span data-ttu-id="260ee-112">[out]ソースのサイズを受け取る変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="260ee-112">[out] A pointer to a variable that receives the source size.</span></span>  
  
 `source`  
 <span data-ttu-id="260ee-113">[out]サイズと指定されたバイト数で、ソース ドキュメントの範囲の長さ。</span><span class="sxs-lookup"><span data-stu-id="260ee-113">[out] The size and length of the specified range of the source document, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="260ee-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="260ee-114">Return Value</span></span>  
 <span data-ttu-id="260ee-115">メソッドが成功した場合は s_ok を返します。</span><span class="sxs-lookup"><span data-stu-id="260ee-115">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="260ee-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="260ee-116">See also</span></span>
- [<span data-ttu-id="260ee-117">ISymUnmanagedDocument インターフェイス</span><span class="sxs-lookup"><span data-stu-id="260ee-117">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
