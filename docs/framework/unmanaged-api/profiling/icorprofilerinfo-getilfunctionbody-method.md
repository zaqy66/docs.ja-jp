---
title: ICorProfilerInfo::GetILFunctionBody メソッド
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetILFunctionBody
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetILFunctionBody
helpviewer_keywords:
- GetILFunctionBody method [.NET Framework profiling]
- ICorProfilerInfo::GetILFunctionBody method [.NET Framework profiling]
ms.assetid: e29b46bc-5fdc-4894-b0c2-619df4b65ded
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a9e1ef61271e5b413972b8ba40a8fe8bac60ceeb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54566215"
---
# <a name="icorprofilerinfogetilfunctionbody-method"></a>ICorProfilerInfo::GetILFunctionBody メソッド
開始位置のヘッダーとして、Microsoft intermediate language (MSIL) コードでメソッドの本体にポインターを取得します。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT GetILFunctionBody(  
    [in]  ModuleID    moduleId,  
    [in]  mdMethodDef methodId,  
    [out] LPCBYTE     *ppMethodHeader,  
    [out] ULONG       *pcbMethodSize);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `moduleId`  
 [in]関数が存在するモジュールの ID。  
  
 `methodId`  
 [in]メソッドのメタデータ トークン。  
  
 `ppMethodHeader`  
 [out]メソッドのヘッダーへのポインター。  
  
 `pcbMethodSize`  
 [out]メソッドのサイズを指定する整数。  
  
## <a name="remarks"></a>Remarks  
 メソッドは、中で、モジュールによって制限されます。 `GetILFunctionBody`メソッドが共通言語ランタイム (CLR) によって読み込まれている前に、MSIL コードをツールへのアクセスを付与するように設計、目的のインスタンスを検索するメソッドのメタデータ トークンを使用します。  
  
 `GetILFunctionBody` CORPROF_E_FUNCTION_NOT_IL HRESULT を返す場合、`methodId`せず、任意の MSIL コード (など、抽象メソッドまたはプラットフォーム (PInvoke) のメソッドを呼び出す) メソッドを指します。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** CorProf.idl、CorProf.h  
  
 **ライブラリ:** CorGuids.lib  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>関連項目
- [ICorProfilerInfo インターフェイス](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
