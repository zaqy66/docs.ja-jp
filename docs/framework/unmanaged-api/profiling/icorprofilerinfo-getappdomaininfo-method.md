---
title: ICorProfilerInfo::GetAppDomainInfo メソッド
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetAppDomainInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetAppDomainInfo
helpviewer_keywords:
- ICorProfilerInfo::GetAppDomainInfo method [.NET Framework profiling]
- GetAppDomainInfo method [.NET Framework profiling]
ms.assetid: a6bf5a04-e03e-44f0-917a-96f6a6d3cc96
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: dbf52a352000150766cd9a8277278491ad7d5152
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54616733"
---
# <a name="icorprofilerinfogetappdomaininfo-method"></a>ICorProfilerInfo::GetAppDomainInfo メソッド
アプリケーション ドメイン ID を受け入れます。 アプリケーション ドメインの名前と、そのアプリケーション ドメインを含むプロセスの ID を返します。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT GetAppDomainInfo(  
    [in]  AppDomainID appDomainId,  
    [in]  ULONG       cchName,  
    [out] ULONG       *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
          WCHAR       szName[] ,  
    [out] ProcessID   *pProcessId);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `appDomainId`  
 [in] アプリケーション ドメインの ID。  
  
 `cchName`  
 [in] `szName` 戻りバッファーの長さ (文字単位)。  
  
 `pcchName`  
 [out] アプリケーション ドメイン名の文字列長の合計へのポインター。  
  
 `szName`  
 [out] 呼び出し元が提供したワイド文字バッファー。 このメソッドから制御が戻ると、`szName` にはアプリケーション ドメイン名の全部または一部が格納されます。  
  
 `pProcessId`  
 [out] アプリケーション ドメインを含むプロセスの ID へのポインター。  
  
## <a name="remarks"></a>Remarks  
 このメソッドから制御が戻った後で、`szName` バッファーのサイズが十分で、アプリケーション ドメインの完全名を格納できたかどうかを確認する必要があります。 これを行うには、`pcchName` が指している値を `cchName` パラメーターの値と比較します。 `pcchName` が指している値が `cchName` の値より大きい場合は、`szName` バッファーの割り当てを増やし、`cchName` を新しい大きいサイズに更新して、`GetAppDomainInfo` を再度呼び出します。  
  
 別の方法として、最初に長さ 0 の `szName` バッファーで `GetAppDomainInfo` を呼び出すことで、適切なバッファーのサイズを取得することもできます。 その後、バッファーのサイズを `pcchName` で返された値に設定し、`GetAppDomainInfo` を再度呼び出します。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** CorProf.idl、CorProf.h  
  
 **ライブラリ:** CorGuids.lib  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>関連項目
- [ICorProfilerInfo インターフェイス](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [プロファイリングのインターフェイス](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [プロファイル](../../../../docs/framework/unmanaged-api/profiling/index.md)
