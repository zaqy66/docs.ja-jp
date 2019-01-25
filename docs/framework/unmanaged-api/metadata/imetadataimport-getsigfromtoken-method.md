---
title: IMetaDataImport::GetSigFromToken メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetSigFromToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetSigFromToken
helpviewer_keywords:
- IMetaDataImport::GetSigFromToken method [.NET Framework metadata]
- GetSigFromToken method [.NET Framework metadata]
ms.assetid: ab894dc4-f7b6-4afc-bfcb-582a4b7e53a2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b25eb71d78797b5f764cfe4de7abd45f0143fde4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54717637"
---
# <a name="imetadataimportgetsigfromtoken-method"></a><span data-ttu-id="82382-102">IMetaDataImport::GetSigFromToken メソッド</span><span class="sxs-lookup"><span data-stu-id="82382-102">IMetaDataImport::GetSigFromToken Method</span></span>
<span data-ttu-id="82382-103">指定したトークンに関連付けられているバイナリ メタデータ シグネチャを取得します。</span><span class="sxs-lookup"><span data-stu-id="82382-103">Gets the binary metadata signature associated with the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="82382-104">構文</span><span class="sxs-lookup"><span data-stu-id="82382-104">Syntax</span></span>  
  
```  
HRESULT GetSigFromToken (   
   [in]   mdSignature        mdSig,   
   [out]  PCCOR_SIGNATURE    *ppvSig,   
   [out]  ULONG              *pcbSig   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="82382-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="82382-105">Parameters</span></span>  
 `mdSig`  
 <span data-ttu-id="82382-106">[in]バイナリ メタデータ シグネチャを返すトークンです。</span><span class="sxs-lookup"><span data-stu-id="82382-106">[in] The token to return the binary metadata signature for.</span></span>  
  
 `ppvSig`  
 <span data-ttu-id="82382-107">[out]返されたメタデータ署名へのポインター。</span><span class="sxs-lookup"><span data-stu-id="82382-107">[out] A pointer to the returned metadata signature.</span></span>  
  
 `pcbSig`  
 <span data-ttu-id="82382-108">[out]バイナリ メタデータ シグネチャのバイト単位のサイズ。</span><span class="sxs-lookup"><span data-stu-id="82382-108">[out] The size in bytes of the binary metadata signature.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="82382-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="82382-109">Requirements</span></span>  
 <span data-ttu-id="82382-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="82382-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="82382-111">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="82382-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="82382-112">**ライブラリ:** MsCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="82382-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="82382-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="82382-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="82382-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="82382-114">See also</span></span>
- [<span data-ttu-id="82382-115">IMetaDataImport インターフェイス</span><span class="sxs-lookup"><span data-stu-id="82382-115">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="82382-116">IMetaDataImport2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="82382-116">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
