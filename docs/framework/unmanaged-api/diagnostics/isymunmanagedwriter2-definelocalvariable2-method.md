---
title: ISymUnmanagedWriter2::DefineLocalVariable2 メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter2.DefineLocalVariable2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter2::DefineLocalVariable2
helpviewer_keywords:
- ISymUnmanagedWriter2::DefineLocalVariable2 method [.NET Framework debugging]
- DefineLocalVariable2 method [.NET Framework debugging]
ms.assetid: e774eefe-858c-4362-8d2d-28ebf2ba1a24
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e0ce6a207f2a7862b0b49f1e68cda9528aa03ca7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54667532"
---
# <a name="isymunmanagedwriter2definelocalvariable2-method"></a><span data-ttu-id="0fb57-102">ISymUnmanagedWriter2::DefineLocalVariable2 メソッド</span><span class="sxs-lookup"><span data-stu-id="0fb57-102">ISymUnmanagedWriter2::DefineLocalVariable2 Method</span></span>
<span data-ttu-id="0fb57-103">現在の構文のスコープの変数を 1 つ定義します。</span><span class="sxs-lookup"><span data-stu-id="0fb57-103">Defines a single variable in the current lexical scope.</span></span> <span data-ttu-id="0fb57-104">このメソッドをスコープ全体で複数のホームのある同じ名前の変数を複数回呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="0fb57-104">This method can be called multiple times for a variable of the same name that has multiple homes throughout a scope.</span></span> <span data-ttu-id="0fb57-105">この場合、ただしの値、`startOffset`と`endOffset`パラメーターが重複しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fb57-105">In this case, however, the values of the `startOffset` and `endOffset` parameters must not overlap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0fb57-106">構文</span><span class="sxs-lookup"><span data-stu-id="0fb57-106">Syntax</span></span>  
  
```  
HRESULT DefineLocalVariable2(  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] mdSignature  sigToken,  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3,  
    [in] ULONG32      startOffset,  
    [in] ULONG32      endOffset);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0fb57-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0fb57-107">Parameters</span></span>  
 `name`  
 <span data-ttu-id="0fb57-108">[in]ローカル変数の名前。</span><span class="sxs-lookup"><span data-stu-id="0fb57-108">[in] The local variable name.</span></span>  
  
 `attributes`  
 <span data-ttu-id="0fb57-109">[in]ローカル変数の属性。</span><span class="sxs-lookup"><span data-stu-id="0fb57-109">[in] The local variable attributes.</span></span>  
  
 `sigToken`  
 <span data-ttu-id="0fb57-110">[in]シグネチャのメタデータ トークンです。</span><span class="sxs-lookup"><span data-stu-id="0fb57-110">[in] The metadata token of the signature.</span></span>  
  
 `addrKind`  
 <span data-ttu-id="0fb57-111">[in]アドレスの種類。</span><span class="sxs-lookup"><span data-stu-id="0fb57-111">[in] The address type.</span></span>  
  
 `addr1`  
 <span data-ttu-id="0fb57-112">[in]パラメーター指定の最初のアドレス。</span><span class="sxs-lookup"><span data-stu-id="0fb57-112">[in] The first address for the parameter specification.</span></span>  
  
 `addr2`  
 <span data-ttu-id="0fb57-113">[in]パラメーター指定の 2 番目のアドレス。</span><span class="sxs-lookup"><span data-stu-id="0fb57-113">[in] The second address for the parameter specification.</span></span>  
  
 `addr3`  
 <span data-ttu-id="0fb57-114">[in]パラメーター指定の 3 番目のアドレス。</span><span class="sxs-lookup"><span data-stu-id="0fb57-114">[in] The third address for the parameter specification.</span></span>  
  
 `startOffset`  
 <span data-ttu-id="0fb57-115">[in]変数の開始オフセット。</span><span class="sxs-lookup"><span data-stu-id="0fb57-115">[in] The start offset for the variable.</span></span> <span data-ttu-id="0fb57-116">このパラメーターは省略できます。</span><span class="sxs-lookup"><span data-stu-id="0fb57-116">This parameter is optional.</span></span> <span data-ttu-id="0fb57-117">0 の場合は、このパラメーターは無視され、スコープ全体で変数が定義されています。</span><span class="sxs-lookup"><span data-stu-id="0fb57-117">If it is 0, this parameter is ignored and the variable is defined throughout the entire scope.</span></span> <span data-ttu-id="0fb57-118">0 以外の値の場合は、現在のスコープのオフセット内、変数となります。</span><span class="sxs-lookup"><span data-stu-id="0fb57-118">If it is a nonzero value, the variable falls within the offsets of the current scope.</span></span>  
  
 `endOffset`  
 <span data-ttu-id="0fb57-119">[in]変数の終了オフセット。</span><span class="sxs-lookup"><span data-stu-id="0fb57-119">[in] The end offset for the variable.</span></span> <span data-ttu-id="0fb57-120">このパラメーターは省略できます。</span><span class="sxs-lookup"><span data-stu-id="0fb57-120">This parameter is optional.</span></span> <span data-ttu-id="0fb57-121">0 の場合は、このパラメーターは無視され、スコープ全体で変数が定義されています。</span><span class="sxs-lookup"><span data-stu-id="0fb57-121">If it is 0, this parameter is ignored and the variable is defined throughout the entire scope.</span></span> <span data-ttu-id="0fb57-122">0 以外の値の場合は、現在のスコープのオフセット内、変数となります。</span><span class="sxs-lookup"><span data-stu-id="0fb57-122">If it is a nonzero value, the variable falls within the offsets of the current scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0fb57-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="0fb57-123">Return Value</span></span>  
 <span data-ttu-id="0fb57-124">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="0fb57-124">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0fb57-125">必要条件</span><span class="sxs-lookup"><span data-stu-id="0fb57-125">Requirements</span></span>  
 <span data-ttu-id="0fb57-126">**ヘッダー:** CorSym.idl</span><span class="sxs-lookup"><span data-stu-id="0fb57-126">**Header:** CorSym.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0fb57-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="0fb57-127">See also</span></span>
- [<span data-ttu-id="0fb57-128">ISymUnmanagedWriter2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0fb57-128">ISymUnmanagedWriter2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-interface.md)
- [<span data-ttu-id="0fb57-129">DefineLocalVariable メソッド</span><span class="sxs-lookup"><span data-stu-id="0fb57-129">DefineLocalVariable Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-definelocalvariable-method.md)
