---
title: IMetaDataEmit2::DefineGenericParam メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.DefineGenericParam
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::DefineGenericParam
helpviewer_keywords:
- IMetaDataEmit2::DefineGenericParam method [.NET Framework metadata]
- DefineGenericParam method [.NET Framework metadata]
ms.assetid: 47b2a3b6-907d-43dc-858d-1ae7dca1316a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b54f5bb47135bcf56c91cd07b916c959e75b9fb5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745313"
---
# <a name="imetadataemit2definegenericparam-method"></a><span data-ttu-id="db210-102">IMetaDataEmit2::DefineGenericParam メソッド</span><span class="sxs-lookup"><span data-stu-id="db210-102">IMetaDataEmit2::DefineGenericParam Method</span></span>
<span data-ttu-id="db210-103">ジェネリック型パラメーターの定義を作成し、そのジェネリック型パラメーターのトークンを取得します。</span><span class="sxs-lookup"><span data-stu-id="db210-103">Creates a definition for a generic type parameter, and gets a token to that generic type parameter.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db210-104">構文</span><span class="sxs-lookup"><span data-stu-id="db210-104">Syntax</span></span>  
  
```  
HRESULT DefineGenericParam (   
    [in]  mdToken         tk,   
    [in]  ULONG           ulParamSeq,   
    [in]  DWORD           dwParamFlags,   
    [in]  LPCWSTR         szname,   
    [in]  DWORD           reserved,   
    [in]  mdToken         rtkConstraints[],   
    [out] mdGenericParam  *pgp  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="db210-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="db210-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="db210-106">[in]`mdTypeDef`または`mdMethodDef`メソッドまたはジェネリック パラメーターを定義する対象のコンス トラクターを表すトークン。</span><span class="sxs-lookup"><span data-stu-id="db210-106">[in] An `mdTypeDef` or `mdMethodDef` token that represents the method or constructor for which to define a generic parameter.</span></span>  
  
 `ulParamSeq`  
 <span data-ttu-id="db210-107">[in]ジェネリック パラメーターのインデックス。</span><span class="sxs-lookup"><span data-stu-id="db210-107">[in] The index of the generic parameter.</span></span>  
  
 `dwParamFlags`  
 <span data-ttu-id="db210-108">[in]値、 [CorGenericParamAttr](../../../../docs/framework/unmanaged-api/metadata/corgenericparamattr-enumeration.md)ジェネリック パラメーターの型を表す列挙体。</span><span class="sxs-lookup"><span data-stu-id="db210-108">[in] A value of the [CorGenericParamAttr](../../../../docs/framework/unmanaged-api/metadata/corgenericparamattr-enumeration.md) enumeration that describes the type for the generic parameter.</span></span>  
  
 `szname`  
 <span data-ttu-id="db210-109">[in]パラメーターの名前。</span><span class="sxs-lookup"><span data-stu-id="db210-109">[in] The name of the parameter.</span></span>  
  
 `reserved`  
 <span data-ttu-id="db210-110">[in]このパラメーターは、将来の機能拡張予約されています。</span><span class="sxs-lookup"><span data-stu-id="db210-110">[in] This parameter is reserved for future extensibility.</span></span>  
  
 `rtkConstraints`  
 <span data-ttu-id="db210-111">[in]型の制約の 0 で終わる配列。</span><span class="sxs-lookup"><span data-stu-id="db210-111">[in] A zero-terminated array of type constraints.</span></span> <span data-ttu-id="db210-112">配列のメンバーである必要があります、 `mdTypeDef`、 `mdTypeRef`、または`mdTypeSpec`メタデータ トークン。</span><span class="sxs-lookup"><span data-stu-id="db210-112">Array members must be an `mdTypeDef`, `mdTypeRef`, or `mdTypeSpec` metadata token.</span></span>  
  
 `pgp`  
 <span data-ttu-id="db210-113">[out]ジェネリック パラメーターを表すトークン。</span><span class="sxs-lookup"><span data-stu-id="db210-113">[out] A token that represents the generic parameter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="db210-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="db210-114">Requirements</span></span>  
 <span data-ttu-id="db210-115">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="db210-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="db210-116">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="db210-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="db210-117">**ライブラリ:** MsCorEE.dll にリソースとして使用</span><span class="sxs-lookup"><span data-stu-id="db210-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="db210-118">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="db210-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="db210-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="db210-119">See also</span></span>
- [<span data-ttu-id="db210-120">IMetaDataEmit2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="db210-120">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
- [<span data-ttu-id="db210-121">IMetaDataEmit インターフェイス</span><span class="sxs-lookup"><span data-stu-id="db210-121">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
