---
title: ISOSDacInterface::GetMethodDescData メソッド
ms.date: 01/16/2019
api.name:
- ISOSDacInterface::GetMethodDescData Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface::GetMethodDescData Method
helpviewer.keywords:
- ISOSDacInterface::GetMethodDescData Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 3f22752446413c622a20340541b0ac328f63c77b
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416732"
---
# <a name="isosdacinterfacegetmethoddescdata-method"></a>ISOSDacInterface::GetMethodDescData メソッド

データを取得、指定された[MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md)します。

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>構文

```
HRESULT GetMethodDescData(
    CLRDATA_ADDRESS            methodDesc,
    CLRDATA_ADDRESS            ip,
    void                       *data,
    ULONG                      cRevertedRejitVersions,
    void                      *rgRevertedRejitData,
    void                      *pcNeededRevertedRejitData
);
```

### <a name="parameters"></a>パラメーター

`methodDesc` [in]MethodDesc アドレス。

`ip` [in]メソッドの IP アドレス。

`data` [out]関連付けられている、MethodDesc 内部 Api から返されるデータ。 構造体には、少なくとも 168 バイトが必要があります。

`cRevertedRejitVersions` [out]元に戻された rejit バージョンの数。

`rgRevertedRejitData` [out]内部 Api から返されるように、元に戻された rejit バージョンに関連付けられたデータ。 構造体には、少なくとも 24 バイト必要があります。

`pcNeededRevertedRejitData` [out]元に戻された ReJit バージョンに関連付けられたデータを格納するために必要なバイト数。

## <a name="remarks"></a>Remarks

指定されたメソッドは、`ISOSDacInterface`インターフェイスし、仮想メソッド テーブルの 20 のスロットに対応しています。 また、`CLRDATA_ADDRESS`は 64 ビット符号なし整数。

## <a name="requirements"></a>必要条件

**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
**ヘッダー:** なし  
**ライブラリ:** なし  
**.NET Framework のバージョン:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>関連項目

- [デバッグ](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [ISOSDacInterface インターフェイス](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-interface.md)
