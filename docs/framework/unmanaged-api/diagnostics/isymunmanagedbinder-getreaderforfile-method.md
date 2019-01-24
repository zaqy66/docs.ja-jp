---
title: ISymUnmanagedBinder::GetReaderForFile メソッド
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder.GetReaderForFile
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder::GetReaderForFile
helpviewer_keywords:
- ISymUnmanagedBinder::GetReaderForFile method [.NET Framework debugging]
- GetReaderForFile method [.NET Framework debugging]
ms.assetid: 46c06258-831e-47c8-a50a-8650af6b637e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 53558e1b76d5bb22ff2af3b8d7d9e4006072775b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54734285"
---
# <a name="isymunmanagedbindergetreaderforfile-method"></a><span data-ttu-id="5c8ba-102">ISymUnmanagedBinder::GetReaderForFile メソッド</span><span class="sxs-lookup"><span data-stu-id="5c8ba-102">ISymUnmanagedBinder::GetReaderForFile Method</span></span>
<span data-ttu-id="5c8ba-103">メタデータ インターフェイスおよびファイル名を指定されたを返します、正しい[ISymUnmanagedReader](isymunmanagedreader-interface.md)をモジュールに関連付けられているデバッグ シンボルを読み取る。</span><span class="sxs-lookup"><span data-stu-id="5c8ba-103">Given a metadata interface and a file name, returns the correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface that will read the debugging symbols associated with the module.</span></span>  
  
 <span data-ttu-id="5c8ba-104">実行可能ファイルの横にある場合にのみ、このメソッドは、プログラム データベース (PDB) ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="5c8ba-104">This method will open the program database (PDB) file only if it is next to the executable file.</span></span> <span data-ttu-id="5c8ba-105">セキュリティのために変更されています。</span><span class="sxs-lookup"><span data-stu-id="5c8ba-105">This change has been made for security purposes.</span></span> <span data-ttu-id="5c8ba-106">PDB ファイルをより広範な検索が必要な場合は、使用、 [isymunmanagedbinder 2::getreaderforfile2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-getreaderforfile2-method.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="5c8ba-106">If you need a more extensive search for the PDB file, use the [ISymUnmanagedBinder2::GetReaderForFile2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-getreaderforfile2-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5c8ba-107">構文</span><span class="sxs-lookup"><span data-stu-id="5c8ba-107">Syntax</span></span>  
  
```  
HRESULT GetReaderForFile(  
    [in]  IUnknown     *importer,  
    [in]  const WCHAR  *fileName,  
    [in]  const WCHAR  *searchPath,  
    [out, retval] ISymUnmanagedReader  **pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5c8ba-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5c8ba-108">Parameters</span></span>  
 `importer`  
 <span data-ttu-id="5c8ba-109">[in]メタデータ インポート インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5c8ba-109">[in] A pointer to the metadata import interface.</span></span>  
  
 `fileName`  
 <span data-ttu-id="5c8ba-110">[in]ファイル名へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5c8ba-110">[in] A pointer to the file name.</span></span>  
  
 `searchPath`  
 <span data-ttu-id="5c8ba-111">[in]検索パスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5c8ba-111">[in] A pointer to the search path.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="5c8ba-112">[out]設定されているポインターに返された[ISymUnmanagedReader](isymunmanagedreader-interface.md)インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="5c8ba-112">[out] A pointer that is set to the returned [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5c8ba-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="5c8ba-113">Return Value</span></span>  
 <span data-ttu-id="5c8ba-114">メソッドが成功した場合は s_ok を返します。それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="5c8ba-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5c8ba-115">必要条件</span><span class="sxs-lookup"><span data-stu-id="5c8ba-115">Requirements</span></span>  
 <span data-ttu-id="5c8ba-116">**ヘッダー:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="5c8ba-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5c8ba-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c8ba-117">See also</span></span>
- [<span data-ttu-id="5c8ba-118">ISymUnmanagedBinder インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5c8ba-118">ISymUnmanagedBinder Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md)
- [<span data-ttu-id="5c8ba-119">GetReaderForFile2 メソッド</span><span class="sxs-lookup"><span data-stu-id="5c8ba-119">GetReaderForFile2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-getreaderforfile2-method.md)
