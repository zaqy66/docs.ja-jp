---
title: IMetaDataConverter::GetMetaDataFromTypeLib メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataConverter.GetMetaDataFromTypeLib
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataConverter::GetMetaDataFromTypeLib
helpviewer_keywords:
- IMetaDataConverter::GetMetaDataFromTypeLib method [.NET Framework metadata]
- GetMetaDataFromTypeLib method [.NET Framework metadata]
ms.assetid: 97dc3a56-adfa-431f-889e-06a35ac84d51
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d8d931b2f96045c53b895d7de5204e2d971b1c64
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54561037"
---
# <a name="imetadataconvertergetmetadatafromtypelib-method"></a><span data-ttu-id="b59bd-102">IMetaDataConverter::GetMetaDataFromTypeLib メソッド</span><span class="sxs-lookup"><span data-stu-id="b59bd-102">IMetaDataConverter::GetMetaDataFromTypeLib Method</span></span>
<span data-ttu-id="b59bd-103">インターフェイス ポインターを取得、 [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)インスタンスの指定によって表されるタイプ ライブラリのメタデータ署名を表す`ITypeLib`インスタンス。</span><span class="sxs-lookup"><span data-stu-id="b59bd-103">Gets an interface pointer to an [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) instance that represents the metadata signature of the type library represented by the specified `ITypeLib` instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b59bd-104">構文</span><span class="sxs-lookup"><span data-stu-id="b59bd-104">Syntax</span></span>  
  
```  
HRESULT GetMetaDataFromTypeLib (  
    [in]  ITypeLib        *pITL,   
    [out] IMetaDataImport **ppMDI  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b59bd-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b59bd-105">Parameters</span></span>  
 `pITL`  
 <span data-ttu-id="b59bd-106">[in]ポインター、`ITypeLib`タイプ ライブラリを表すオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="b59bd-106">[in] Pointer to an `ITypeLib` object that represents the type library.</span></span>  
  
 `ppMDI`  
 <span data-ttu-id="b59bd-107">[out]アドレスを受け取る場所へのポインター、`IMetaDataImport`メタデータ シグネチャを表すインスタンス。</span><span class="sxs-lookup"><span data-stu-id="b59bd-107">[out] Pointer to a location that receives the address of the `IMetaDataImport` instance that represents the metadata signature.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b59bd-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="b59bd-108">Requirements</span></span>  
 <span data-ttu-id="b59bd-109">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b59bd-109">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b59bd-110">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="b59bd-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b59bd-111">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="b59bd-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b59bd-112">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b59bd-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b59bd-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="b59bd-113">See also</span></span>
- [<span data-ttu-id="b59bd-114">IMetaDataEmit インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b59bd-114">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="b59bd-115">IMetaDataImport インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b59bd-115">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
