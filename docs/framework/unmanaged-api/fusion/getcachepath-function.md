---
title: GetCachePath 関数
ms.date: 03/30/2017
api_name:
- GetCachePath
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- GetCachePath
helpviewer_keywords:
- GetCachePath function [.NET Framework fusion]
ms.assetid: d977ad29-6619-42e1-b0be-bc25ea950e80
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ac0b6ac09db452eb06c633027e9596bda6627005
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54509390"
---
# <a name="getcachepath-function"></a>GetCachePath 関数
指定したフラグを使用して、キャッシュされたアセンブリへのパスを取得します。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT GetCachePath (  
    [in]      ASM_CACHE_FLAGS  dwCacheFlags,  
    [in]      LPWSTR           pwzCachePath,  
    [in, out] PDWORD           pcchPath  
 );  
```  
  
#### <a name="parameters"></a>パラメーター  
 `dwCacheFlags`  
 [in][ASM_CACHE_FLAGS](../../../../docs/framework/unmanaged-api/fusion/asm-cache-flags-enumeration.md)キャッシュされたアセンブリのソースを示す値。  
  
 `pwzCachePath`  
 [out]パスに返されるポインター。  
  
 `pcchPath`  
 [入力、出力]要求の最大長の`pwzCachePath`、関数が戻るとき、実際の長さと`pwzCachePath`します。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** Fusion.h  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>関連項目
- [ASM_CACHE_FLAGS 列挙型](../../../../docs/framework/unmanaged-api/fusion/asm-cache-flags-enumeration.md)
- [Fusion グローバル静的関数](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
