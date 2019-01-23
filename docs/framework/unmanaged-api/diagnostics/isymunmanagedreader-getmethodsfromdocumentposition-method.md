---
title: ISymUnmanagedReader::GetMethodsFromDocumentPosition メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetMethodsFromDocumentPosition
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetMethodsFromDocumentPosition
helpviewer_keywords:
- GetMethodsFromDocumentPosition method [.NET Framework debugging]
- ISymUnmanagedReader::GetMethodsFromDocumentPosition method [.NET Framework debugging]
ms.assetid: 83605f1e-e4f3-49e6-859b-f13cad68bb54
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f55c8986d2efc78b6fcd2840bad588af84228017
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54561779"
---
# <a name="isymunmanagedreadergetmethodsfromdocumentposition-method"></a><span data-ttu-id="444cc-102">ISymUnmanagedReader::GetMethodsFromDocumentPosition メソッド</span><span class="sxs-lookup"><span data-stu-id="444cc-102">ISymUnmanagedReader::GetMethodsFromDocumentPosition Method</span></span>
<span data-ttu-id="444cc-103">メソッドのドキュメントで指定された位置にブレークポイントを含む配列を返します。</span><span class="sxs-lookup"><span data-stu-id="444cc-103">Returns an array of methods, each of which contains the breakpoint at the given position in a document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="444cc-104">構文</span><span class="sxs-lookup"><span data-stu-id="444cc-104">Syntax</span></span>  
  
```  
HRESULT GetMethodsFromDocumentPosition (  
    [in]  ISymUnmanagedDocument* document,  
    [in]  ULONG32 line,  
    [in]  ULONG32 column,  
    [in]  ULONG32 cMethod,  
    [out] ULONG32* pcMethod,  
    [out, size_is (cMethod),  
        length_is (*pcMethod)] ISymUnmanagedMethod* pRetVal[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="444cc-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="444cc-105">Parameters</span></span>  
 `document`  
 <span data-ttu-id="444cc-106">[in]指定されたドキュメントです。</span><span class="sxs-lookup"><span data-stu-id="444cc-106">[in] The specified document.</span></span>  
  
 `line`  
 <span data-ttu-id="444cc-107">[in]指定されたドキュメントの行。</span><span class="sxs-lookup"><span data-stu-id="444cc-107">[in] The line of the specified document.</span></span>  
  
 `column`  
 <span data-ttu-id="444cc-108">[in]指定されたドキュメントの列です。</span><span class="sxs-lookup"><span data-stu-id="444cc-108">[in] The column of the specified document.</span></span>  
  
 `cMethod`  
 <span data-ttu-id="444cc-109">[in] `pRetVal` 配列のサイズ。</span><span class="sxs-lookup"><span data-stu-id="444cc-109">[in] The size of the `pRetVal` array.</span></span>  
  
 `pcMethod`  
 <span data-ttu-id="444cc-110">[out]返される要素の数を受け取る変数へのポインター、`pRetVal`配列。</span><span class="sxs-lookup"><span data-stu-id="444cc-110">[out] A pointer to a variable that receives the number of elements returned in the `pRetVal` array.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="444cc-111">[out]それぞれが指すポインターの配列、 [ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)ブレークポイントを含むメソッドを表すオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="444cc-111">[out] An array of pointers, each of which points to an [ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) object that represents a method containing the breakpoint.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="444cc-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="444cc-112">Return Value</span></span>  
 <span data-ttu-id="444cc-113">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="444cc-113">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="444cc-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="444cc-114">Requirements</span></span>  
 <span data-ttu-id="444cc-115">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="444cc-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="444cc-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="444cc-116">See also</span></span>
- [<span data-ttu-id="444cc-117">ISymUnmanagedReader インターフェイス</span><span class="sxs-lookup"><span data-stu-id="444cc-117">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
