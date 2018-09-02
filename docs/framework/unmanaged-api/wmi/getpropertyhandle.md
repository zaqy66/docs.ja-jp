---
title: GetPropertyHandle 関数 (アンマネージ API リファレンス)
description: GetPropertyHandle 関数では、プロパティの識別子を管理する一意のハンドルを返します。
ms.date: 11/06/2017
api_name:
- GetPropertyHandle
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetPropertyHandle
helpviewer_keywords:
- GetPropertyHandle function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 94171b0708c97eb7510e916e451ed03645d706f3
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2018
ms.locfileid: "43469883"
---
# <a name="getpropertyhandle-function"></a>GetPropertyHandle 関数
プロパティを識別する一意のハンドルを返します。

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a>構文  
  
```  
HRESULT GetPropertyHandle (
   [in] int                  vFunc, 
   [in] IWbemObjectAccess*   ptr, 
   [in] LPCWSTR              wszPropertyName,
   [out] CIMTYPE*            pType,
   [out] long*               pHandle
); 
```  

## <a name="parameters"></a>パラメーター

`vFunc`  
[in]このパラメーターは使用されません。

`ptr`  
[in]ポインター、 [IWbemObjectAccess](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess)インスタンス。

`wszPropertyName`  
[in]プロパティ名を含む UTF16 でエンコードされた characaters の null で終わる文字列。   

`pType`  
[out]ポインターを[ `CIMTYPE` ](https://msdn.microsoft.com/library/aa386309(v=vs.85).aspx)プロパティの CIM 型を表す列挙型メンバー。

`pHandle`   
[out]プロパティのハンドルを格納する整数へのポインター。

## <a name="return-value"></a>戻り値

この関数によって返される次の値が定義されている、 *WbemCli.h*ヘッダー ファイル、またはすることができますに定数としてコードで定義します。

|定数  |値  |説明  |
|---------|---------|---------|
|`WBEM_E_NOT_FOUND` | 0x80041002 | 指定したプロパティ名が見つかりませんでした。 |
|`WBEM_E_INVALID_PARAMETER` | 0x80041008 | パラメーターが無効です。 |
|`WBEM_E_NOT_SUPPORTED` | 0x8004100c | 要求されたプロパティの型は、`CIM_OBJECT`または`CIM_ARRAY`します。 |
|`WBEM_S_NO_ERROR` | 0 | 関数呼び出しに成功しました。  |
  
## <a name="remarks"></a>Remarks

この関数の呼び出しをラップする、 [IWbemClassObject::GetPropertyHandle](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle)メソッド。

使用する場合は、プロパティを識別するために、このハンドルを使用することができます[IWbemObjectAccess](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess)読み取りまたは書き込みのプロパティの値をメソッド。

ハンドルを以外のすべてのデータ型のプロパティを取得できる`CIM_OBJECT`と`CIM_ARRAY`します。 クラスのすべてのインスタンス ハンドルの作業が返されます。

## <a name="requirements"></a>要件  
**:**「[システム要件](../../../../docs/framework/get-started/system-requirements.md)」を参照してください。  
  
 **ヘッダー:** WMINet_Utils.idl  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>関連項目  
[WMI およびパフォーマンス カウンター (アンマネージ API リファレンス)](index.md)
