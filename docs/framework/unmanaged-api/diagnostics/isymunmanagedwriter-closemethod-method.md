---
title: ISymUnmanagedWriter::CloseMethod メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.CloseMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::CloseMethod
helpviewer_keywords:
- ISymUnmanagedWriter::CloseMethod method [.NET Framework debugging]
- CloseMethod method [.NET Framework debugging]
ms.assetid: b8025e04-f0e5-40c8-849c-8cd51323420e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a6f8c8b522aabfce3b83b6b624bd0ca9757448ad
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54666021"
---
# <a name="isymunmanagedwriterclosemethod-method"></a><span data-ttu-id="2bbff-102">ISymUnmanagedWriter::CloseMethod メソッド</span><span class="sxs-lookup"><span data-stu-id="2bbff-102">ISymUnmanagedWriter::CloseMethod Method</span></span>
<span data-ttu-id="2bbff-103">現在のメソッドを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2bbff-103">Closes the current method.</span></span> <span data-ttu-id="2bbff-104">メソッドを終了すると、その中シンボルを定義できます。</span><span class="sxs-lookup"><span data-stu-id="2bbff-104">Once a method is closed, no more symbols can be defined within it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2bbff-105">構文</span><span class="sxs-lookup"><span data-stu-id="2bbff-105">Syntax</span></span>  
  
```  
HRESULT CloseMethod();  
```  
  
## <a name="return-value"></a><span data-ttu-id="2bbff-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="2bbff-106">Return Value</span></span>  
 <span data-ttu-id="2bbff-107">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="2bbff-107">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2bbff-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="2bbff-108">Requirements</span></span>  
 <span data-ttu-id="2bbff-109">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="2bbff-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2bbff-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="2bbff-110">See also</span></span>
- [<span data-ttu-id="2bbff-111">ISymUnmanagedWriter インターフェイス</span><span class="sxs-lookup"><span data-stu-id="2bbff-111">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [<span data-ttu-id="2bbff-112">OpenMethod メソッド</span><span class="sxs-lookup"><span data-stu-id="2bbff-112">OpenMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md)
