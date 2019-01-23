---
title: IMetaDataEmit2::GetDeltaSaveSize メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.GetDeltaSaveSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::GetDeltaSaveSize
helpviewer_keywords:
- IMetaDataEmit2::GetDeltaSaveSize method [.NET Framework metadata]
- GetDeltaSaveSize method [.NET Framework metadata]
ms.assetid: 036db5e7-8211-4645-9a34-03d1a89be955
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: cb59fdb2249d798c70b1990a6bca41c5c14b80c0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54610566"
---
# <a name="imetadataemit2getdeltasavesize-method"></a><span data-ttu-id="a0671-102">IMetaDataEmit2::GetDeltaSaveSize メソッド</span><span class="sxs-lookup"><span data-stu-id="a0671-102">IMetaDataEmit2::GetDeltaSaveSize Method</span></span>
<span data-ttu-id="a0671-103">エディット コンティニュの現在のセッションから生成されるメタデータのサイズ変更を示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="a0671-103">Gets a value indicating any change in metadata size that results from the current edit-and-continue session.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a0671-104">構文</span><span class="sxs-lookup"><span data-stu-id="a0671-104">Syntax</span></span>  
  
```  
HRESULT GetDeltaSaveSize (  
    [in]  CorSaveSize  fSave,  
    [out] DWORD        *pdwSaveSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a0671-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a0671-105">Parameters</span></span>  
 `fSave`  
 <span data-ttu-id="a0671-106">[in]1 つ、 [CorSaveSize](../../../../docs/framework/unmanaged-api/metadata/corsavesize-enumeration.md)必要に応じて有効桁数のレベルを示す値。</span><span class="sxs-lookup"><span data-stu-id="a0671-106">[in] One of the [CorSaveSize](../../../../docs/framework/unmanaged-api/metadata/corsavesize-enumeration.md) values, indicating the level of precision desired.</span></span> <span data-ttu-id="a0671-107">.NET Framework version 2.0 では、このパラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a0671-107">For the .NET Framework version 2.0, this parameter is ignored.</span></span>  
  
 `pdwSaveSize`  
 <span data-ttu-id="a0671-108">[out]メタデータのサイズに変更します。</span><span class="sxs-lookup"><span data-stu-id="a0671-108">[out] The change in the size of the metadata.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a0671-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="a0671-109">Requirements</span></span>  
 <span data-ttu-id="a0671-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0671-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a0671-111">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a0671-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a0671-112">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="a0671-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a0671-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a0671-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0671-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0671-114">See also</span></span>
- [<span data-ttu-id="a0671-115">IMetaDataEmit2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a0671-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
- [<span data-ttu-id="a0671-116">IMetaDataEmit インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a0671-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
