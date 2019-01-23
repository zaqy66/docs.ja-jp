---
title: COR_HEAPINFO 構造体
ms.date: 03/30/2017
api_name:
- COR_HEAPINFO
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_HEAPINFO
helpviewer_keywords:
- COR_HEAPINFO structure [.NET Framework debugging]
ms.assetid: bfb2cd39-3e0b-4d51-ba0c-f009755c1456
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ffca8e076fe6fe966a9a07ed915a7e76ea06f37c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54518073"
---
# <a name="corheapinfo-structure"></a>COR_HEAPINFO 構造体
列挙可能かどうかなど、ガベージ コレクション ヒープに関する情報が提供されます。  
  
## <a name="syntax"></a>構文  
  
```  
typedef struct _COR_HEAPINFO {  
    BOOL areGCStructuresValid;   
    DWORD pointerSize;   
    DWORD numHeaps;  
    BOOL concurrent;   
    CorDebugGCType gcType;   
} COR_HEAPINFO;  
```  
  
## <a name="members"></a>メンバー  
  
|メンバー|説明|  
|------------|-----------------|  
|`areGCStructuresValid`|`true` ガベージ コレクションの構造体が有効な場合に、ヒープを列挙することができます。それ以外の場合、`false`します。|  
|`pointerSize`|ターゲット アーキテクチャ上のポインターのバイト単位のサイズ。|  
|`numHeaps`|プロセスのヒープの論理のガベージ コレクションの数。|  
|`concurrent`|`TRUE` 同時実行の場合 (背景) のガベージ コレクションが有効になっているとします。それ以外の場合、`FALSE`します。|  
|`gcType`|メンバー、 [CorDebugGCType](../../../../docs/framework/unmanaged-api/debugging/cordebuggctype-enumeration.md)ガベージ コレクターがワークステーションまたはサーバーで実行されているかどうかを示す列挙体。|  
  
## <a name="remarks"></a>Remarks  
 インスタンス、`COR_HEAPINFO`構造体が呼び出しによって返される、 [icordebugprocess 5::getgcheapinformation](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-getgcheapinformation-method.md)メソッド。  
  
 ガベージ コレクション ヒープ上のオブジェクトを列挙するには、前に常にオンにしてください、`areGCStructuresValid`フィールドをヒープが列挙可能な状態であることを確認します。 詳細については、次を参照してください。、 [icordebugprocess 5::getgcheapinformation](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-getgcheapinformation-method.md)メソッド。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** CorDebug.idl、CorDebug.h  
  
 **ライブラリ:** CorGuids.lib  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>関連項目
- [デバッグ構造体](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [デバッグ](../../../../docs/framework/unmanaged-api/debugging/index.md)
