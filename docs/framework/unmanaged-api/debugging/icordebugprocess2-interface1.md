---
title: ICorDebugProcess2 Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugProcess2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess2
helpviewer_keywords:
- ICorDebugProcess2 interface [.NET Framework debugging]
ms.assetid: 73332138-5fea-441f-b893-61af87d45a42
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0b37cb8ecd178b90a4dcd2d2eab9fa7c4cd3211d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54647323"
---
# <a name="icordebugprocess2-interface1"></a>ICorDebugProcess2 Interface1
プロセス実行中のマネージ コードを表す ICorDebugProcess インターフェイスを論理的に拡張します。  
  
## <a name="methods"></a>メソッド  
  
|メソッド|説明|  
|------------|-----------------|  
|[ClearUnmanagedBreakpoint メソッド](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-clearunmanagedbreakpoint-method.md)|以前の呼び出しによって設定された指定したオフセット位置にブレークポイントを削除`ICorDebugProcess2::SetUnmanagedBreakpoint`します。|  
|[GetDesiredNGENCompilerFlags メソッド](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-getdesiredngencompilerflags-method.md)|これによって参照されているプロセスにイメージの読み込みに共通言語ランタイム (CLR) に設定する必要があるフラグを取得`ICorDebugProcess2`します。|  
|[GetReferenceValueFromGCHandle メソッド](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-getreferencevaluefromgchandle-method.md)|ガベージ コレクション ハンドルが、指定した管理対象のオブジェクト参照ポインターを取得します。|  
|[GetThreadForTaskID メソッド](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-getthreadfortaskid-method.md)|指定した識別子を持つタスクを実行するスレッドを取得します。|  
|[GetVersion メソッド](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-getversion-method.md)|デバッグ中のプロセスが実行されている CLR のバージョンを取得します。|  
|[SetDesiredNGENCompilerFlags メソッド](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-setdesiredngencompilerflags-method.md)|デバッグ中のプロセスにイメージを読み込む - イン タイム (JIT) コンパイラに必要なフラグを設定します。|  
|[SetUnmanagedBreakpoint メソッド](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-setunmanagedbreakpoint-method.md)|ネイティブ イメージを指定したオフセットで非管理対象のブレークポイントを設定します。|  
  
## <a name="remarks"></a>Remarks  
  
> [!NOTE]
>  このインターフェイスは、コンピューター間またはプロセス間でのリモート呼び出しをサポートしていません。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** CorDebug.idl、CorDebug.h  
  
 **ライブラリ:** CorGuids.lib  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>関連項目
- [デバッグ インターフェイス](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
