---
title: ICorDebug::SetManagedHandler メソッド
ms.date: 03/30/2017
api_name:
- ICorDebug.SetManagedHandler
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::SetManagedHandler
helpviewer_keywords:
- ICorDebug::SetManagedHandler method [.NET Framework debugging]
- SetManagedHandler method [.NET Framework debugging]
ms.assetid: d079131b-685b-4869-95be-826b88d28bd2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c195e61b5929acdb0aec7d9043ce6122b0a80739
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54643274"
---
# <a name="icordebugsetmanagedhandler-method"></a>ICorDebug::SetManagedHandler メソッド
管理対象のイベントのイベント ハンドラー オブジェクトを指定します。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT SetManagedHandler (  
    [in] ICorDebugManagedCallback     *pCallback  
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `pCallback`  
 [in]ポインター、 [ICorDebugManagedCallback](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)イベント ハンドラー オブジェクトであるオブジェクト。  
  
## <a name="remarks"></a>Remarks  
 `SetManagedHandler` 作成時に呼び出す必要があります。  
  
 場合、`ICorDebugManagedCallback`実装には、デバッグ中、アプリケーションのデバッグ イベントを処理するための十分なインターフェイスが含まれていない`SetManagedHandler`HRESULT の E_NOINTERFACE を返します。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** CorDebug.idl、CorDebug.h  
  
 **ライブラリ:** CorGuids.lib  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>関連項目
- [ICorDebug インターフェイス](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
