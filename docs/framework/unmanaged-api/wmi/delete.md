---
title: Delete 関数 (アンマネージ API リファレンス)
description: 機能の削除は、CIM クラスの定義から、指定したプロパティとその修飾子のすべてを削除します。
ms.date: 11/06/2017
api_name:
- Delete
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- Delete
helpviewer_keywords:
- Delete function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0590c639e7cc6622c2283bfa609ccb31d7ce7e2b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54720575"
---
# <a name="delete-function"></a>関数を削除します。
CIM クラスの定義から、指定したプロパティとその修飾子のすべてを削除します。

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a>構文  
  
```  
HRESULT Delete (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr, 
   [in] LPCWSTR           wszName 
); 
```  

## <a name="parameters"></a>パラメーター

`vFunc`  
[in]このパラメーターは使用されません。

`ptr`  
[in]ポインター、 [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject)インスタンス。

`wszName`  
[in]削除するプロパティの名前。 `wszName` 有効なポインターである必要があります`LPCWSTR`します。

## <a name="return-value"></a>戻り値

この関数によって返される次の値が定義されている、 *WbemCli.h*ヘッダー ファイル、またはすることができますに定数としてコードで定義します。

|定数  |値  |説明  |
|---------|---------|---------|
| `WBEM_E_FAILED` | 0x80041001 | 不明なエラーが発生しました。 |
| `WBEM_E_INVALID_OPERATION` | 0x80041016 | プロパティを削除することはできません。 |
| `WBEM_E_INVALID_PARAMETER` | 0x80041008 | `wszzName` が無効です。 |
| `WBEM_E_NOT_FOUND` | 0x80041002 | 指定したプロパティが存在しません。 |
| `WBEM_E_OUT_OF_MEMORY` | 0x80041006 | 操作を完了するのに十分なメモリがありません。 |
| `WBEM_E_PROPAGATED_PROPERTY` | 0x8004101c | プロパティは、基本クラスから継承されます。 |
| `WBEM_E_SYSTEM_PROPERTY` | | プロパティは、システム プロパティです。 |
|`WBEM_S_NO_ERROR` | 0 | 関数呼び出しに成功しました。  |
| `WBEM_E_RESET_TO_DEFAULT` | 0x80041030 | 関数は、現在のクラスを上書きする既定値を削除します。 親クラスでは、このプロパティの既定値は reactiviated されました。 | 

## <a name="remarks"></a>Remarks

この関数の呼び出しをラップする、 [IWbemClassObject::Delete](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-delete)メソッド。

## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** WMINet_Utils.idl  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>関連項目
- [WMI およびパフォーマンス カウンター (アンマネージ API リファレンス)](index.md)
