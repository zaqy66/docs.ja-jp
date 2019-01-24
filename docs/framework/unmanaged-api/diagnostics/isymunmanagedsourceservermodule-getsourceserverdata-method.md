---
title: ISymUnmanagedSourceServerModule::GetSourceServerData メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSourceServerModule.GetSourceServerData
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSourceServerModule::GetSourceServerData
helpviewer_keywords:
- ISymUnmanagedSourceServerModule::GetSourceServerData method [.NET Framework debugging]
- GetSourceServerData method [.NET Framework debugging]
ms.assetid: 20bdf8ff-2d15-4c64-8950-6888f642d6c0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 71251af116fc8d634b822e1daa49d90e91fec6f1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54648824"
---
# <a name="isymunmanagedsourceservermodulegetsourceserverdata-method"></a><span data-ttu-id="4fc58-102">ISymUnmanagedSourceServerModule::GetSourceServerData メソッド</span><span class="sxs-lookup"><span data-stu-id="4fc58-102">ISymUnmanagedSourceServerModule::GetSourceServerData Method</span></span>
<span data-ttu-id="4fc58-103">モジュールのソース サーバーのデータを返します。</span><span class="sxs-lookup"><span data-stu-id="4fc58-103">Returns the source server data for the module.</span></span> <span data-ttu-id="4fc58-104">使用して、呼び出し元がリソースを解放する必要があります`CoTaskMemFree`します。</span><span class="sxs-lookup"><span data-stu-id="4fc58-104">The caller must free resources by using `CoTaskMemFree`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4fc58-105">構文</span><span class="sxs-lookup"><span data-stu-id="4fc58-105">Syntax</span></span>  
  
```  
HRESULT GetSourceServerData(  
    [out] ULONG* pDataByteCount,   
    [out, size_is (, *pDataByteCount)] BYTE** ppData);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4fc58-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4fc58-106">Parameters</span></span>  
 `pDataByteCount`  
 <span data-ttu-id="4fc58-107">[out]ポインター、`ULONG32`ソース サーバーのデータのバイト単位のサイズを受け取る。</span><span class="sxs-lookup"><span data-stu-id="4fc58-107">[out] A pointer to a `ULONG32` that receives the size, in bytes, of the source server data.</span></span>  
  
 `ppData`  
 <span data-ttu-id="4fc58-108">[out]返されたポインター`pDataByteCount`値。</span><span class="sxs-lookup"><span data-stu-id="4fc58-108">[out] A pointer to the returned `pDataByteCount` value.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4fc58-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="4fc58-109">Return Value</span></span>  
 <span data-ttu-id="4fc58-110">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="4fc58-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4fc58-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="4fc58-111">Requirements</span></span>  
 <span data-ttu-id="4fc58-112">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="4fc58-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4fc58-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="4fc58-113">See also</span></span>
- [<span data-ttu-id="4fc58-114">ISymUnmanagedSourceServerModule インターフェイス</span><span class="sxs-lookup"><span data-stu-id="4fc58-114">ISymUnmanagedSourceServerModule Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsourceservermodule-interface.md)
