---
title: ISymUnmanagedDocument::GetCheckSum メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetCheckSum
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetCheckSum
helpviewer_keywords:
- ISymUnmanagedDocument::GetCheckSum method [.NET Framework debugging]
- GetCheckSum method [.NET Framework debugging]
ms.assetid: 9bc881b3-e2ce-48a7-ad69-17eaaa304120
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 406fdfcfc0b6db988b317245aaaa4f4a643b2079
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54561401"
---
# <a name="isymunmanageddocumentgetchecksum-method"></a><span data-ttu-id="39f61-102">ISymUnmanagedDocument::GetCheckSum メソッド</span><span class="sxs-lookup"><span data-stu-id="39f61-102">ISymUnmanagedDocument::GetCheckSum Method</span></span>
<span data-ttu-id="39f61-103">チェックサムを取得します。</span><span class="sxs-lookup"><span data-stu-id="39f61-103">Gets the checksum.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="39f61-104">構文</span><span class="sxs-lookup"><span data-stu-id="39f61-104">Syntax</span></span>  
  
```  
HRESULT GetCheckSum(  
    [in]  ULONG32  cData,  
    [out] ULONG32  *pcData,  
    [out, size_is(cData), length_is(*pcData)] BYTE data[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="39f61-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="39f61-105">Parameters</span></span>  
 `cData`  
 <span data-ttu-id="39f61-106">[in]によって提供されるバッファーの長さ、`data`パラメーター</span><span class="sxs-lookup"><span data-stu-id="39f61-106">[in] The length of the buffer provided by the `data` parameter</span></span>  
  
 `pcData`  
 <span data-ttu-id="39f61-107">[out]サイズとチェックサムをバイト単位の長さ。</span><span class="sxs-lookup"><span data-stu-id="39f61-107">[out] The size and length of the checksum, in bytes.</span></span>  
  
 `data`  
 <span data-ttu-id="39f61-108">[out]チェックサムを受け取るバッファー。</span><span class="sxs-lookup"><span data-stu-id="39f61-108">[out] The buffer that receives the checksum.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="39f61-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="39f61-109">Return Value</span></span>  
 <span data-ttu-id="39f61-110">メソッドが成功した場合は s_ok を返します。それ以外の場合、エラー コード。</span><span class="sxs-lookup"><span data-stu-id="39f61-110">S_OK if the method succeeds; otherwise, an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="39f61-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="39f61-111">See also</span></span>
- [<span data-ttu-id="39f61-112">ISymUnmanagedDocument インターフェイス</span><span class="sxs-lookup"><span data-stu-id="39f61-112">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
