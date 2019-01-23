---
title: CorDebugStateChange 列挙体
ms.date: 03/30/2017
api_name:
- CorDebugStateChange
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 1d4424ab-5143-4e50-a84a-ceeb4ddf3bba
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0f0f692b692628d50755ce813c66823f940dccb8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54513786"
---
# <a name="cordebugstatechange-enumeration"></a>CorDebugStateChange 列挙体
プロセスへの変更に基づいて破棄が必要となった、キャッシュされたデータの量を示します。  
  
## <a name="syntax"></a>構文  
  
```  
typedef enum CorDebugStateChange  
{  
    PROCESS_RUNNING = 0x0000001,   
    FLUSH_ALL       = 0x0000002,   
} CorDebugStateChange;  
```  
  
## <a name="members"></a>メンバー  
  
|メンバー|説明|  
|------------|-----------------|  
|`PROCESS_RUNNING`|プロセスはフォワード実行によって新しいメモリ状態に達しています。|  
|`SET_CONTEXT_FLAG_UNWIND_FRAME`|プロセスのメモリは、以前とは異なる状態になっている場合があります。|  
  
## <a name="remarks"></a>Remarks  
 メンバー、`CorDebugStateChange`デバッガーを呼び出すと、列挙型が、引数として指定された、 [ProcessStateChanged](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-processstatechanged-method.md)メソッド  
  
> [!NOTE]
>  この列挙体は .NET ネイティブのデバッグ シナリオのみで使用することを目的としています。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** CorDebug.idl、CorDebug.h  
  
 **ライブラリ:** CorGuids.lib  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>関連項目
- [列挙型のデバッグ](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
- [デバッグ](../../../../docs/framework/unmanaged-api/debugging/index.md)
