---
title: IMetaDataError::OnError メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataError.OnError
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataError::OnError
helpviewer_keywords:
- IMetaDataError::OnError method [.NET Framework metadata]
- OnError method, IMetaDataError interface [.NET Framework metadata]
ms.assetid: c1e744b8-a6fb-4d9c-a971-8babc875d8f0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7ebb7fdbcf8c17991928df2dc621ec651b9cd4f5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54678721"
---
# <a name="imetadataerroronerror-method"></a><span data-ttu-id="84cce-102">IMetaDataError::OnError メソッド</span><span class="sxs-lookup"><span data-stu-id="84cce-102">IMetaDataError::OnError Method</span></span>
<span data-ttu-id="84cce-103">メタデータのマージ中に発生したエラーの通知を提供します。</span><span class="sxs-lookup"><span data-stu-id="84cce-103">Provides notification of errors that occur during the metadata merge.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="84cce-104">構文</span><span class="sxs-lookup"><span data-stu-id="84cce-104">Syntax</span></span>  
  
```  
HRESULT OnError (  
    [in] HRESULT   hrError,   
    [in] mdToken   token  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="84cce-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84cce-105">Parameters</span></span>  
 `hrError`  
 <span data-ttu-id="84cce-106">[in]呼び出し元のメソッドに HRESULT エラー値が返されます。</span><span class="sxs-lookup"><span data-stu-id="84cce-106">[in] The HRESULT error value returned to the calling method.</span></span>  
  
 `token`  
 <span data-ttu-id="84cce-107">[in]エラーが発生したときをマージしているコード オブジェクトのメタデータ トークンです。</span><span class="sxs-lookup"><span data-stu-id="84cce-107">[in] The metadata token of the code object that was being merged when the error occurred.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="84cce-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="84cce-108">Requirements</span></span>  
 <span data-ttu-id="84cce-109">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="84cce-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="84cce-110">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="84cce-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="84cce-111">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="84cce-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="84cce-112">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="84cce-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84cce-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="84cce-113">See also</span></span>
- [<span data-ttu-id="84cce-114">IMetaDataError インターフェイス</span><span class="sxs-lookup"><span data-stu-id="84cce-114">IMetaDataError Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataerror-interface.md)
