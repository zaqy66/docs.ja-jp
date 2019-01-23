---
title: IMetaDataImport::GetModuleRefProps メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetModuleRefProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetModuleRefProps
helpviewer_keywords:
- GetModuleRefProps method [.NET Framework metadata]
- IMetaDataImport::GetModuleRefProps method [.NET Framework metadata]
ms.assetid: b558e766-4c11-4628-ae47-b4e0a1800168
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 501c554f6e2e4ddd8abd21fe81b81d1898ea070b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54583618"
---
# <a name="imetadataimportgetmodulerefprops-method"></a><span data-ttu-id="e2bfd-102">IMetaDataImport::GetModuleRefProps メソッド</span><span class="sxs-lookup"><span data-stu-id="e2bfd-102">IMetaDataImport::GetModuleRefProps Method</span></span>
<span data-ttu-id="e2bfd-103">指定したメタデータ トークンによって参照されるモジュールの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="e2bfd-103">Gets the name of the module referenced by the specified metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e2bfd-104">構文</span><span class="sxs-lookup"><span data-stu-id="e2bfd-104">Syntax</span></span>  
  
```  
HRESULT GetModuleRefProps (  
   [in]  mdModuleRef         mur,  
   [out] LPWSTR              szName,   
   [in]  ULONG               cchName,   
   [out] ULONG               *pchName   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e2bfd-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e2bfd-105">Parameters</span></span>  
 `mur`  
 <span data-ttu-id="e2bfd-106">[in]メタデータ情報を取得するモジュールを参照する ModuleRef メタデータ トークンです。</span><span class="sxs-lookup"><span data-stu-id="e2bfd-106">[in] The ModuleRef metadata token that references the module to get metadata information for.</span></span>  
  
 `szName`  
 <span data-ttu-id="e2bfd-107">[out]モジュール名を保持するバッファー。</span><span class="sxs-lookup"><span data-stu-id="e2bfd-107">[out] A buffer to hold the module name.</span></span>  
  
 `cchName`  
 <span data-ttu-id="e2bfd-108">[in]要求されたサイズの`szName`ワイド文字。</span><span class="sxs-lookup"><span data-stu-id="e2bfd-108">[in] The requested size of `szName` in wide characters.</span></span>  
  
 `pchName`  
 <span data-ttu-id="e2bfd-109">[out]サイズが返される`szName`ワイド文字。</span><span class="sxs-lookup"><span data-stu-id="e2bfd-109">[out] The returned size of `szName` in wide characters.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e2bfd-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="e2bfd-110">Requirements</span></span>  
 <span data-ttu-id="e2bfd-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2bfd-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e2bfd-112">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e2bfd-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e2bfd-113">**ライブラリ:** MsCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="e2bfd-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e2bfd-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e2bfd-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e2bfd-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2bfd-115">See also</span></span>
- [<span data-ttu-id="e2bfd-116">IMetaDataImport インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e2bfd-116">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="e2bfd-117">IMetaDataImport2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e2bfd-117">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
