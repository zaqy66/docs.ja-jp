---
title: IXCLRDataProcess::EndEnumMethodInstancesByAddress メソッド
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EndEnumMethodInstancesByAddress Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EndEnumMethodInstancesByAddress Method
helpviewer.keywords:
- IXCLRDataProcess::EndEnumMethodInstancesByAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 67978e49a8c23c4b25234ecbb3639c696c7232f4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54655648"
---
# <a name="ixclrdataprocessendenummethodinstancesbyaddress-method"></a>IXCLRDataProcess::EndEnumMethodInstancesByAddress メソッド

インスタンスの列挙中に使用される内部の反復子によって使用されるリソースを解放します。

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>構文

```
HRESULT EndEnumMethodInstancesByAddress(
    [in] CLRDATA_ENUM handle
);
```

### <a name="parameters"></a>パラメーター

`handle` [out]メソッド インスタンスを列挙するためのハンドル。

## <a name="remarks"></a>Remarks

指定されたメソッドは、`IXCLRDataProcess`インターフェイスし、仮想メソッド テーブルの 29 のスロットに対応しています。

## <a name="requirements"></a>必要条件

**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
**ヘッダー:** なし  
**ライブラリ:** なし  
**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>関連項目

- [CLRDataSourceType 列挙型](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [デバッグ](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [IXCLRDataProcess インターフェイス](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
