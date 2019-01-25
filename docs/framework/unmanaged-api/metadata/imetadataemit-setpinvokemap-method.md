---
title: IMetaDataEmit::SetPinvokeMap メソッド
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetPinvokeMap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetPinvokeMap
helpviewer_keywords:
- IMetaDataEmit::SetPinvokeMap method [.NET Framework metadata]
- SetPinvokeMap method [.NET Framework metadata]
ms.assetid: c6bfd574-1da3-4ba7-82f2-46ca5efcbaba
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7248f4c78684f7211c7b7633095fdc3f3f2fb1f3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54658625"
---
# <a name="imetadataemitsetpinvokemap-method"></a>IMetaDataEmit::SetPinvokeMap メソッド
前回の呼び出しで定義されているメソッドの PInvoke の署名の機能の変更を設定または[imetadataemit::definepinvokemap](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definepinvokemap-method.md)します。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT SetPinvokeMap (   
    [in]  mdToken      tk,   
    [in]  DWORD        dwMappingFlags,  
    [in]  LPCWSTR      szImportName,   
    [in]  mdModuleRef  mrImportDLL   
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `tk`  
 [in]`mdToken`マッピング情報が適用されます。  
  
 `dwMappingFlags`  
 [in]PInvoke によって、マッピングを行うために使用するフラグ。 これは、ビットマスクの`CorPinvokeMap`値。  
  
 `szImportName`  
 [in]ターゲットの名前は、ネイティブ DLL でエクスポートします。  
  
 `mrImportDLL`  
 [in]`mdModuleRef`トークン ターゲットのアンマネージ DLL です。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** Cor.h  
  
 **ライブラリ:** MSCorEE.dll にリソースとして使用  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>関連項目
- [IMetaDataEmit インターフェイス](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [IMetaDataEmit2 インターフェイス](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
