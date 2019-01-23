---
title: ICorDebugEval::CallFunction メソッド
ms.date: 03/30/2017
api_name:
- ICorDebugEval.CallFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::CallFunction
helpviewer_keywords:
- ICorDebugEval::CallFunction method [.NET Framework debugging]
- CallFunction method [.NET Framework debugging]
ms.assetid: 7f470c5c-e1c0-4d8d-aad8-830f113ae751
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 493b4850436b3724287210878992d1d8ce8fe168
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54589400"
---
# <a name="icordebugevalcallfunction-method"></a>ICorDebugEval::CallFunction メソッド
指定した関数の呼び出しを設定します。  
  
 このメソッドは、.NET Framework version 2.0 で廃止されています。 使用[icordebugeval 2::callparameterizedfunction](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-callparameterizedfunction-method.md)代わりにします。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT CallFunction (  
    [in] ICorDebugFunction  *pFunction,  
    [in] ULONG32            nArgs,  
    [in, size_is(nArgs)] ICorDebugValue *ppArgs[]  
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `pFunction`  
 [in]呼び出される関数を指定する ICorDebugFunction オブジェクトへのポインター。  
  
 `nArgs`  
 [in]関数の引数の数。  
  
 `ppArgs`  
 [in]関数に渡される引数を指定する ICorDebugValue オブジェクトを指す各ポインターの配列。  
  
## <a name="remarks"></a>Remarks  
 関数が仮想場合、`CallFunction`仮想ディスパッチを実行します。 関数は、別のアプリケーション ドメインでは、すべての引数がそのアプリケーション ドメイン内にも限りの移行が発生します。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:** WindowSee[システム要件](../../../../docs/framework/get-started/system-requirements.md)します。  
  
 **ヘッダー:** CorDebug.idl、CorDebug.h  
  
 **ライブラリ:** CorGuids.lib  
  
 **.NET framework のバージョン:** 1.1, 1.0  
  
## <a name="see-also"></a>関連項目
- [CallParameterizedFunction メソッド](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-callparameterizedfunction-method.md)
