---
title: IMetaDataEmit::Merge メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.Merge
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::Merge
helpviewer_keywords:
- IMetaDataEmit::Merge method [.NET Framework metadata]
- Merge method [.NET Framework metadata]
ms.assetid: 7596220c-f699-4b6c-8ae7-c83220610650
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 899f2ca5ef1b987687f5c065ad3e1965e142d103
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44216107"
---
# <a name="imetadataemitmerge-method"></a><span data-ttu-id="99c8a-102">IMetaDataEmit::Merge メソッド</span><span class="sxs-lookup"><span data-stu-id="99c8a-102">IMetaDataEmit::Merge Method</span></span>
<span data-ttu-id="99c8a-103">指定されたインポートされたスコープをマージするスコープの一覧に追加します。</span><span class="sxs-lookup"><span data-stu-id="99c8a-103">Adds the specified imported scope to the list of scopes to be merged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="99c8a-104">構文</span><span class="sxs-lookup"><span data-stu-id="99c8a-104">Syntax</span></span>  
  
```  
HRESULT Merge (   
    [in]  IMetaDataImport  *pImport,   
    [in]  IMapToken        *pHostMapToken,   
    [in]  IUnknown         *pHandler   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="99c8a-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="99c8a-105">Parameters</span></span>  
 `pImport`  
 <span data-ttu-id="99c8a-106">[in]ポインター、 [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)マージするインポートされたスコープを識別するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="99c8a-106">[in] A pointer to an [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) object that identifies the imported scope to be merged.</span></span>  
  
 `pIMap`  
 <span data-ttu-id="99c8a-107">[in]ポインター、 [IMapToken](../../../../docs/framework/unmanaged-api/metadata/imaptoken-interface.md)トークンの再マップを指定するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="99c8a-107">[in] A pointer to an [IMapToken](../../../../docs/framework/unmanaged-api/metadata/imaptoken-interface.md) object that specifies the token re-map.</span></span>  
  
 `pHandleer`  
 <span data-ttu-id="99c8a-108">[in]ポインター、 [IUnknown](/cpp/atl/iunknown)エラーを指定するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="99c8a-108">[in] A pointer to an [IUnknown](/cpp/atl/iunknown) object that specifies the errors.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="99c8a-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="99c8a-109">Remarks</span></span>  
 <span data-ttu-id="99c8a-110">呼び出す[imetadataemit::mergeend](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-mergeend-method.md)を 1 つのスコープにメタデータの合併をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="99c8a-110">Call [IMetaDataEmit::MergeEnd](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-mergeend-method.md) to trigger the merger of metadata into a single scope.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="99c8a-111">要件</span><span class="sxs-lookup"><span data-stu-id="99c8a-111">Requirements</span></span>  
 <span data-ttu-id="99c8a-112">**:**「[システム要件](../../../../docs/framework/get-started/system-requirements.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99c8a-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="99c8a-113">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="99c8a-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="99c8a-114">**ライブラリ:** MSCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="99c8a-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="99c8a-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="99c8a-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99c8a-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="99c8a-116">See Also</span></span>  
 [<span data-ttu-id="99c8a-117">IMetaDataEmit インターフェイス</span><span class="sxs-lookup"><span data-stu-id="99c8a-117">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="99c8a-118">IMetaDataEmit2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="99c8a-118">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
