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
# <a name="imetadataimportgetmemberprops-method"></a>IMetaDataImport::GetMemberProps メソッド
名前、バイナリ シグネチャ、相対仮想アドレスをなどのメタデータ情報を取得、<xref:System.Type>指定したメタデータ トークンによって参照されるメンバー。  
  
## <a name="syntax"></a>構文  
  
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
  
#### <a name="parameters"></a>パラメーター  
 `mb`  
 [in]関連付けられているメタデータを取得するメンバーを参照するトークンです。  
  
 `pClass`  
 [out]メンバーのクラスを表すメタデータ トークンへのポインター。  
  
 `szMember`  
 [out]メンバーの名前。  
  
 `cchMember`  
 [in]ワイド文字のサイズ、`szMember`バッファー。  
  
 `pchMember`  
 [out]返される名前のワイド文字単位のサイズ。  
  
 `pdwAttr`  
 [out]いずれかのフラグ値がメンバーに適用します。  
  
 `ppvSigBlob`  
 [out]メンバーのバイナリ メタデータ シグネチャへのポインター。  
  
 `pcbSigBlob`  
 [out]バイト サイズ`ppvSigBlob`します。  
  
 `pulCodeRVA`  
 [out]メンバーの相対仮想アドレスへのポインター。  
  
 `pdwImplFlags`  
 [out]メンバーに関連付けられているすべてメソッド実装フラグ。  
  
 `pdwCPlusTypeFlag`  
 [out]マークするフラグを<xref:System.ValueType>します。  
  
 `ppValue`  
 [out]このメンバーが返される定数文字列値。  
  
 `pcchValue`  
 [out]サイズの文字で`ppValue`、または場合は 0`ppValue`文字列を保持しません。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** Cor.h  
  
 **ライブラリ:** MsCorEE.dll でリソースとして含まれます  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>関連項目
- [IMetaDataImport インターフェイス](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2 インターフェイス](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
