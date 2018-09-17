---
title: IMetaDataDispenserEx::OpenScopeOnITypeInfo メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.OpenScopeOnITypeInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::OpenScopeOnITypeInfo
helpviewer_keywords:
- OpenScopeOnITypeInfo method [.NET Framework metadata]
- IMetaDataDispenserEx::OpenScopeOnITypeInfo method [.NET Framework metadata]
ms.assetid: 3480bbdb-c442-44a0-b7c6-333354503c52
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d5fd96f390b0bba60d1b95d20273bbf670208d41
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2018
ms.locfileid: "45745578"
---
# <a name="imetadatadispenserexopenscopeonitypeinfo-method"></a>IMetaDataDispenserEx::OpenScopeOnITypeInfo メソッド
このメソッドは実装されていません。 呼び出された場合、E_NOTIMPL を返します。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT OpenScopeOnITypeInfo (  
    [in]  ITypeInfo   *pITI,  
    [in]  DWORD       dwOpenFlags,  
    [in]  REFIID      riid,  
    [out] IUnknown    **ppIUnk  
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `pITI`  
 [in]ポインター、 [ITypeInfo](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo)を開くスコープ型情報を提供するインターフェイスです。  
  
 `dwOpenFlags`  
 [in]Open モード フラグ。  
  
 `riid`  
 [in]必要なインターフェイスです。  
  
 `ppIUnk`  
 [out]返されるインターフェイスへのポインターへのポインター。  
  
## <a name="requirements"></a>要件  
 **Platform:** を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)します。  
  
 **ヘッダー:** Cor.h  
  
 **ライブラリ:** MsCorEE.dll にリソースとして使用  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>関連項目  
 [IMetaDataDispenserEx インターフェイス](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)  
 [IMetaDataDispenser インターフェイス](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)
