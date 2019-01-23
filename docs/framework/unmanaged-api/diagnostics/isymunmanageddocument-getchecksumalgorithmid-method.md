---
title: ISymUnmanagedDocument::GetCheckSumAlgorithmId メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetCheckSumAlgorithmId
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetCheckSumAlgorithmId
helpviewer_keywords:
- ISymUnmanagedDocument::GetCheckSumAlgorithmId method [.NET Framework debugging]
- GetCheckSumAlgorithmId method [.NET Framework debugging]
ms.assetid: c7f941cd-e25b-4b85-b1ce-5f77c9208fa9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6c5861f598a653f433ffaa611d6f1be3ba6f69a2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54585605"
---
# <a name="isymunmanageddocumentgetchecksumalgorithmid-method"></a><span data-ttu-id="afff1-102">ISymUnmanagedDocument::GetCheckSumAlgorithmId メソッド</span><span class="sxs-lookup"><span data-stu-id="afff1-102">ISymUnmanagedDocument::GetCheckSumAlgorithmId Method</span></span>
<span data-ttu-id="afff1-103">チェックサム アルゴリズム識別子を取得またはチェックサムがない場合は、すべてゼロの GUID を返します。</span><span class="sxs-lookup"><span data-stu-id="afff1-103">Gets the checksum algorithm identifier, or returns a GUID of all zeros if there is no checksum.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="afff1-104">構文</span><span class="sxs-lookup"><span data-stu-id="afff1-104">Syntax</span></span>  
  
```  
HRESULT GetCheckSumAlgorithmId(  
    [out, retval] GUID*  pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="afff1-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="afff1-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="afff1-106">[out]チェックサム アルゴリズム識別子を受け取る変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="afff1-106">[out] A pointer to a variable that receives the checksum algorithm identifier.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="afff1-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="afff1-107">Return Value</span></span>  
 <span data-ttu-id="afff1-108">メソッドが成功した場合は s_ok を返します。</span><span class="sxs-lookup"><span data-stu-id="afff1-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="afff1-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="afff1-109">See also</span></span>
- [<span data-ttu-id="afff1-110">ISymUnmanagedDocument インターフェイス</span><span class="sxs-lookup"><span data-stu-id="afff1-110">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
