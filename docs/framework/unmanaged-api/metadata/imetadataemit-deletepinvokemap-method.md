---
title: IMetaDataEmit::DeletePinvokeMap メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DeletePinvokeMap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DeletePinvokeMap
helpviewer_keywords:
- IMetaDataEmit::DeletePinvokeMap method [.NET Framework metadata]
- DeletePinvokeMap method [.NET Framework metadata]
ms.assetid: 3c4f6b54-5ce7-4a2a-83e1-6dec16441f50
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c3b7c116410ce3309d970929580f4ec7f65bd657
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54558283"
---
# <a name="imetadataemitdeletepinvokemap-method"></a><span data-ttu-id="aa418-102">IMetaDataEmit::DeletePinvokeMap メソッド</span><span class="sxs-lookup"><span data-stu-id="aa418-102">IMetaDataEmit::DeletePinvokeMap Method</span></span>
<span data-ttu-id="aa418-103">指定したトークンによって参照されるオブジェクトの PInvoke マッピング メタデータを破棄します。</span><span class="sxs-lookup"><span data-stu-id="aa418-103">Destroys the PInvoke mapping metadata for the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aa418-104">構文</span><span class="sxs-lookup"><span data-stu-id="aa418-104">Syntax</span></span>  
  
```  
HRESULT DeletePinvokeMap (   
    [in]  mdToken     tk   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="aa418-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="aa418-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="aa418-106">[in]`mdFieldDef`または`mdMethodDef`PInvoke マッピングのメタデータを削除するオブジェクトを表すトークン。</span><span class="sxs-lookup"><span data-stu-id="aa418-106">[in] An `mdFieldDef` or `mdMethodDef` token that represents the object for which to delete the PInvoke mapping metadata.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aa418-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="aa418-107">Requirements</span></span>  
 <span data-ttu-id="aa418-108">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa418-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aa418-109">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="aa418-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="aa418-110">**ライブラリ:** MSCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="aa418-110">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="aa418-111">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aa418-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aa418-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa418-112">See also</span></span>
- [<span data-ttu-id="aa418-113">IMetaDataEmit インターフェイス</span><span class="sxs-lookup"><span data-stu-id="aa418-113">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="aa418-114">IMetaDataEmit2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="aa418-114">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
