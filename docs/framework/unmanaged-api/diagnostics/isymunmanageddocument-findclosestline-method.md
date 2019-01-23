---
title: ISymUnmanagedDocument::FindClosestLine メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.FindClosestLine
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::FindClosestLine
helpviewer_keywords:
- FindClosestLine method [.NET Framework debugging]
- ISymUnmanagedDocument::FindClosestLine method [.NET Framework debugging]
ms.assetid: 628f2a04-e529-407d-841e-3b3da219a9cb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 96ad0e34bf638c378f37e317f790696c2ac7cb25
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54519698"
---
# <a name="isymunmanageddocumentfindclosestline-method"></a><span data-ttu-id="35a16-102">ISymUnmanagedDocument::FindClosestLine メソッド</span><span class="sxs-lookup"><span data-stu-id="35a16-102">ISymUnmanagedDocument::FindClosestLine Method</span></span>
<span data-ttu-id="35a16-103">行を指定したシーケンス ポイントができない可能性がありますが、このドキュメントでは、シーケンス ポイントである最も近い行を返します。</span><span class="sxs-lookup"><span data-stu-id="35a16-103">Returns the closest line that is a sequence point, given a line in this document that may or may not be a sequence point.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35a16-104">構文</span><span class="sxs-lookup"><span data-stu-id="35a16-104">Syntax</span></span>  
  
```  
HRESULT FindClosestLine(  
    [in]  ULONG32  line,  
    [out, retval] ULONG32*  pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="35a16-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="35a16-105">Parameters</span></span>  
 `line`  
 <span data-ttu-id="35a16-106">[in]このドキュメント内の行。</span><span class="sxs-lookup"><span data-stu-id="35a16-106">[in] A line in this document.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="35a16-107">[out]行を受け取る変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="35a16-107">[out] A pointer to a variable that receives the line.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="35a16-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="35a16-108">Return Value</span></span>  
 <span data-ttu-id="35a16-109">メソッドが成功した場合は s_ok を返します。それ以外の場合、エラー コード。</span><span class="sxs-lookup"><span data-stu-id="35a16-109">S_OK if the method succeeds; otherwise, an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="35a16-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="35a16-110">See also</span></span>
- [<span data-ttu-id="35a16-111">ISymUnmanagedDocument インターフェイス</span><span class="sxs-lookup"><span data-stu-id="35a16-111">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
