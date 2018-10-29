---
title: IMetaDataEmit::DefineField メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineField
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineField
helpviewer_keywords:
- IMetaDataEmit::DefineField method [.NET Framework metadata]
- DefineField method, IMetaDataEmit interface [.NET Framework metadata
ms.assetid: 6b5be4fc-2e86-499c-8b09-833160bca767
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b54ceb099df15855b6b30b8c28d7d8917a9c71eb
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50184950"
---
# <a name="imetadataemitdefinefield-method"></a>IMetaDataEmit::DefineField メソッド
指定したメタデータ シグネチャを持つフィールドの定義を作成し、そのフィールド定義トークンを取得します。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT DefineField (   
    [in]  mdTypeDef   td,   
    [in]  LPCWSTR     szName,   
    [in]  DWORD       dwFieldFlags,   
    [in]  PCCOR_SIGNATURE pvSigBlob,   
    [in]  ULONG       cbSigBlob,   
    [in]  DWORD       dwCPlusTypeFlag,   
    [in]  void const  *pValue,   
    [in]  ULONG       cchValue,   
    [out] mdFieldDef  *pmd   
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `td`  
 [in]`mdTypeDef`外側のクラスまたはインターフェイスのトークン。  
  
 `szName`  
 [in]Unicode でフィールド名です。  
  
 `dwFieldFlags`  
 [in]フィールドの属性。 これは、ビットマスクの`CorFieldAttr`値。  
  
 `pvSigBlob`  
 [in]BLOB としてフィールド シグネチャ。  
  
 `cbSigBlob`  
 [in]内のバイト数`pvSigBlob`します。  
  
 `dwCPlusTypeFlag`  
 [in]`ELEMENT_TYPE_` *\** 定数の値。 これは、`CorElementType`値。 場合は、フィールドの定数値を定義しないを使用して、`ELEMENT_TYPE_END`します。  
  
 `pValue`  
 [in]フィールドの定数値。  
  
 `cchValue`  
 [in](Unicode) 文字のサイズ`pValue`します。  
  
 `pmd`  
 [out]`mdFieldDef`に割り当てられたトークン。  
  
## <a name="requirements"></a>必要条件  
 **:**「[システム要件](../../../../docs/framework/get-started/system-requirements.md)」を参照してください。  
  
 **ヘッダー:** Cor.h  
  
 **ライブラリ:** MSCorEE.dll にリソースとして使用  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>関連項目  
 [IMetaDataEmit インターフェイス](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [IMetaDataEmit2 インターフェイス](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
