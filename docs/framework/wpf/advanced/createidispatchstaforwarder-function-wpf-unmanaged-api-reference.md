---
title: CreateIDispatchSTAForwarder 関数 (WPF のアンマネージ API リファレンス)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- CreateIDispatchSTAForwarder
api_location:
- PresentationHost_v0400.dll
ms.assetid: 57a02dfa-f091-4ace-9c06-1f4ab52b3527
ms.openlocfilehash: 215f6ff727b814e7e7d7c708c29a8c5221f5797f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54575983"
---
# <a name="createidispatchstaforwarder-function-wpf-unmanaged-api-reference"></a>CreateIDispatchSTAForwarder 関数 (WPF のアンマネージ API リファレンス)
この API は、Windows Presentation Foundation (WPF) インフラストラクチャをサポートしているし、コードから直接使用するものではありません。  
  
 Windows Presentation Foundation (WPF) インフラストラクチャによってスレッドと windows の管理に使用します。  
  
## <a name="syntax"></a>構文  
  
```cpp  
HRESULT CreateIDispatchSTAForwarder(  
   __in IDispatch *pDispatchDelegate,   
   __deref_out IDispatch **ppForwarder  
)  
```  
  
#### <a name="parameters"></a>パラメーター  
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値  
 pDispatchDelegate  
 ポインター、`IDispatch`インターフェイス。  
  
 ppForwarder  
 アドレスへのポインター、`IDispatch`インターフェイス。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:** 参照してください[.NET Framework システム要件](../../../../docs/framework/get-started/system-requirements.md)します。  
  
 **DLL:**  
  
 .NET framework 3.0 および 3.5。PresentationHostDLL.dll  
  
 .NET framework 4 以降では。PresentationHost_v0400.dll  
  
 **.NET framework のバージョン:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]  
  
## <a name="see-also"></a>関連項目
- [WPF のアンマネージ API リファレンス](../../../../docs/framework/wpf/advanced/wpf-unmanaged-api-reference.md)
