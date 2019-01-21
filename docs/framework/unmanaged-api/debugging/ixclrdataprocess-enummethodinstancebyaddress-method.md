---
title: IXCLRDataProcess::EnumMethodInstanceByAddress メソッド
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method
helpviewer.keywords:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: b42939e8e64e75337478ace67a9a91c6a03a94e3
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416682"
---
# <a name="ixclrdataprocessenummethodinstancebyaddress-method"></a>IXCLRDataProcess::EnumMethodInstanceByAddress メソッド

このプロセスがアドレス オフセットから始まるのメソッドのインスタンスを列挙します。

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>構文

```
HRESULT EnumMethodInstanceByAddress(
    [in] CLRDATA_ENUM              *handle,
    [out] IXCLRDataMethodInstance **method
);
```

### <a name="parameters"></a>パラメーター

`handle` [in]メソッド インスタンスを列挙するためのハンドル。

`mod` [out]列挙メソッドのインスタンス。

## <a name="remarks"></a>Remarks

指定されたメソッドは、`IXCLRDataProcess`インターフェイスし、仮想メソッド テーブルの 28 のスロットに対応しています。

## <a name="requirements"></a>必要条件

**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。   
**ヘッダー:** なし   
**ライブラリ:** なし   
**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]   
 
## <a name="see-also"></a>関連項目
- [CLRDataSourceType 列挙型](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [デバッグ](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [IXCLRDataProcess インターフェイス](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
