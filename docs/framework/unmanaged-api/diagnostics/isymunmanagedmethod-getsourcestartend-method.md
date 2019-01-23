---
title: ISymUnmanagedMethod::GetSourceStartEnd メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetSourceStartEnd
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetSourceStartEnd
helpviewer_keywords:
- GetSourceStartEnd method [.NET Framework debugging]
- ISymUnmanagedMethod::GetSourceStartEnd method [.NET Framework debugging]
ms.assetid: 2a420900-01f1-4461-8777-3a34a6dc1426
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4ecb726f275a694fded2c486448a60b28fadb168
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54561869"
---
# <a name="isymunmanagedmethodgetsourcestartend-method"></a><span data-ttu-id="7fb2c-102">ISymUnmanagedMethod::GetSourceStartEnd メソッド</span><span class="sxs-lookup"><span data-stu-id="7fb2c-102">ISymUnmanagedMethod::GetSourceStartEnd Method</span></span>
<span data-ttu-id="7fb2c-103">このメソッドのソースの先頭と末尾のドキュメントの位置を取得します。</span><span class="sxs-lookup"><span data-stu-id="7fb2c-103">Gets the start and end document positions for the source of this method.</span></span> <span data-ttu-id="7fb2c-104">配列の最初の位置が、開始であり 2 番目の配列の位置は終わりです。</span><span class="sxs-lookup"><span data-stu-id="7fb2c-104">The first array position is the start, and the second array position is the end.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7fb2c-105">構文</span><span class="sxs-lookup"><span data-stu-id="7fb2c-105">Syntax</span></span>  
  
```  
HRESULT GetSourceStartEnd(  
    [in]  ISymUnmanagedDocument  *docs[2],  
    [in]  ULONG32                lines[2],  
    [in]  ULONG32                columns[2],  
    [out] BOOL                   *pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7fb2c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7fb2c-106">Parameters</span></span>  
 `docs`  
 <span data-ttu-id="7fb2c-107">[in]最初と最後のソース ドキュメント。</span><span class="sxs-lookup"><span data-stu-id="7fb2c-107">[in] The starting and ending source documents.</span></span>  
  
 `lines`  
 <span data-ttu-id="7fb2c-108">[in]ソース ドキュメントの開始と、対応する行を終了します。</span><span class="sxs-lookup"><span data-stu-id="7fb2c-108">[in] The starting and ending lines in the corresponding source documents.</span></span>  
  
 `columns`  
 <span data-ttu-id="7fb2c-109">[in]ソース ドキュメントの開始と、対応する列を終了します。</span><span class="sxs-lookup"><span data-stu-id="7fb2c-109">[in] The starting and ending columns in the corresponding source documents.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="7fb2c-110">[out]`true`位置が定義されている。 それ以外の場合`false`します。</span><span class="sxs-lookup"><span data-stu-id="7fb2c-110">[out] `true` if positions were defined; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7fb2c-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="7fb2c-111">Return Value</span></span>  
 <span data-ttu-id="7fb2c-112">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="7fb2c-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7fb2c-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="7fb2c-113">Requirements</span></span>  
 <span data-ttu-id="7fb2c-114">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="7fb2c-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7fb2c-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="7fb2c-115">See also</span></span>
- [<span data-ttu-id="7fb2c-116">ISymUnmanagedMethod インターフェイス</span><span class="sxs-lookup"><span data-stu-id="7fb2c-116">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
