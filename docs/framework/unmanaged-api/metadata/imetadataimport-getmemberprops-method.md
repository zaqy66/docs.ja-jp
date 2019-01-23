---
title: IMetaDataImport::GetMemberProps メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetMemberProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetMemberProps
helpviewer_keywords:
- IMetaDataImport::GetMemberProps method [.NET Framework metadata]
- GetMemberProps method [.NET Framework metadata]
ms.assetid: 42790918-4142-4938-b8f4-a56979a55846
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 98d7be5adc81cff09b121265e7d5b5f712122607
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54611411"
---
# <a name="imetadataimportgetmemberprops-method"></a><span data-ttu-id="d947c-102">IMetaDataImport::GetMemberProps メソッド</span><span class="sxs-lookup"><span data-stu-id="d947c-102">IMetaDataImport::GetMemberProps Method</span></span>
<span data-ttu-id="d947c-103">名前、バイナリ シグネチャ、相対仮想アドレスをなどのメタデータ情報を取得、<xref:System.Type>指定したメタデータ トークンによって参照されるメンバー。</span><span class="sxs-lookup"><span data-stu-id="d947c-103">Gets metadata information, including the name, binary signature, and relative virtual address, of the <xref:System.Type> member referenced by the specified metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d947c-104">構文</span><span class="sxs-lookup"><span data-stu-id="d947c-104">Syntax</span></span>  
  
```  
HRESULT GetMemberProps (  
   [in]  mdToken           mb,   
   [out] mdTypeDef         *pClass,  
   [out] LPWSTR            szMember,   
   [in]  ULONG             cchMember,   
   [out] ULONG             *pchMember,   
   [out] DWORD             *pdwAttr,  
   [out] PCCOR_SIGNATURE   *ppvSigBlob,   
   [out] ULONG             *pcbSigBlob,   
   [out] ULONG             *pulCodeRVA,   
   [out] DWORD             *pdwImplFlags,   
   [out] DWORD             *pdwCPlusTypeFlag,   
   [out] UVCP_CONSTANT     *ppValue,  
   [out] ULONG             *pcchValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d947c-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d947c-105">Parameters</span></span>  
 `mb`  
 <span data-ttu-id="d947c-106">[in]関連付けられているメタデータを取得するメンバーを参照するトークンです。</span><span class="sxs-lookup"><span data-stu-id="d947c-106">[in] The token that references the member to get the associated metadata for.</span></span>  
  
 `pClass`  
 <span data-ttu-id="d947c-107">[out]メンバーのクラスを表すメタデータ トークンへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d947c-107">[out] A pointer to the metadata token that represents the class of the member.</span></span>  
  
 `szMember`  
 <span data-ttu-id="d947c-108">[out]メンバーの名前。</span><span class="sxs-lookup"><span data-stu-id="d947c-108">[out] The name of the member.</span></span>  
  
 `cchMember`  
 <span data-ttu-id="d947c-109">[in]ワイド文字のサイズ、`szMember`バッファー。</span><span class="sxs-lookup"><span data-stu-id="d947c-109">[in] The size in wide characters of the `szMember` buffer.</span></span>  
  
 `pchMember`  
 <span data-ttu-id="d947c-110">[out]返される名前のワイド文字単位のサイズ。</span><span class="sxs-lookup"><span data-stu-id="d947c-110">[out] The size in wide characters of the returned name.</span></span>  
  
 `pdwAttr`  
 <span data-ttu-id="d947c-111">[out]いずれかのフラグ値がメンバーに適用します。</span><span class="sxs-lookup"><span data-stu-id="d947c-111">[out] Any flag values applied to the member.</span></span>  
  
 `ppvSigBlob`  
 <span data-ttu-id="d947c-112">[out]メンバーのバイナリ メタデータ シグネチャへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d947c-112">[out] A pointer to the binary metadata signature of the member.</span></span>  
  
 `pcbSigBlob`  
 <span data-ttu-id="d947c-113">[out]バイト サイズ`ppvSigBlob`します。</span><span class="sxs-lookup"><span data-stu-id="d947c-113">[out] The size in bytes of `ppvSigBlob`.</span></span>  
  
 `pulCodeRVA`  
 <span data-ttu-id="d947c-114">[out]メンバーの相対仮想アドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d947c-114">[out] A pointer to the relative virtual address of the member.</span></span>  
  
 `pdwImplFlags`  
 <span data-ttu-id="d947c-115">[out]メンバーに関連付けられているすべてメソッド実装フラグ。</span><span class="sxs-lookup"><span data-stu-id="d947c-115">[out] Any method implementation flags associated with the member.</span></span>  
  
 `pdwCPlusTypeFlag`  
 <span data-ttu-id="d947c-116">[out]マークするフラグを<xref:System.ValueType>します。</span><span class="sxs-lookup"><span data-stu-id="d947c-116">[out] A flag that marks a <xref:System.ValueType>.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="d947c-117">[out]このメンバーが返される定数文字列値。</span><span class="sxs-lookup"><span data-stu-id="d947c-117">[out] A constant string value returned by this member.</span></span>  
  
 `pcchValue`  
 <span data-ttu-id="d947c-118">[out]サイズの文字で`ppValue`、または場合は 0`ppValue`文字列を保持しません。</span><span class="sxs-lookup"><span data-stu-id="d947c-118">[out] The size in characters of `ppValue`, or zero if `ppValue` does not hold a string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d947c-119">必要条件</span><span class="sxs-lookup"><span data-stu-id="d947c-119">Requirements</span></span>  
 <span data-ttu-id="d947c-120">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d947c-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d947c-121">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="d947c-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d947c-122">**ライブラリ:** MsCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="d947c-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d947c-123">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d947c-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d947c-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="d947c-124">See also</span></span>
- [<span data-ttu-id="d947c-125">IMetaDataImport インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d947c-125">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="d947c-126">IMetaDataImport2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d947c-126">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
