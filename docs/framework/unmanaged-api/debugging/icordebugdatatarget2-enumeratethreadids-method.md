---
title: ICorDebugDataTarget2::EnumerateThreadIDs メソッド
ms.date: 03/30/2017
ms.assetid: af02460f-2a45-496e-bc4e-a1ac4f80fe11
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 594fcb74988cadaa4801fc6f0bb2d05b27a7f441
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54563393"
---
# <a name="icordebugdatatarget2enumeratethreadids-method"></a>ICorDebugDataTarget2::EnumerateThreadIDs メソッド
アクティブなスレッド ID の一覧を返します。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT EnumerateThreadIDs(  
    [in] ULONG32 cThreadIds,   
    [out] ULONG32 *pcThreadIds,   
    [out, size_is(cThreadIds), length_is(*pcThreadIds)] ULONG32 pThreadIds[]  
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 cThreadIDs  
 [入力] ID を返すことのできるスレッドの最大数。  
  
 pcThreadIds  
 [出力] `ULONG32` 配列に書き込まれたスレッド ID の実際の数を示す `pThreadIds` へのポインター。  
  
 pThreadIDs  
 スレッド識別子の配列。  
  
## <a name="remarks"></a>Remarks  
  
> [!NOTE]
>  このメソッドは .NET ネイティブでのみ使用できます。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:** 参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md).**ヘッダー:** CorDebug.idl、CorDebug.h  
  
 **ライブラリ:** CorGuids.lib  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>関連項目
- [ICorDebugDataTarget2 インターフェイス](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-interface.md)
- [デバッグ インターフェイス](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
