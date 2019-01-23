---
title: IHostMemoryManager::ReleasedVirtualAddressSpace メソッド
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.ReleasedVirtualAddressSpace
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::ReleasedVirtualAddressSpace
helpviewer_keywords:
- ReleasedVirtualAddressSpace method [.NET Framework hosting]
- IHostMemoryManager::ReleasedVirtualAddressSpace method [.NET Framework hosting]
ms.assetid: d1876601-6ab9-48e1-8ebd-184af1d0cd76
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1b7bf2a3e359ca05a147553d89a1d2bb3d235209
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54571050"
---
# <a name="ihostmemorymanagerreleasedvirtualaddressspace-method"></a>IHostMemoryManager::ReleasedVirtualAddressSpace メソッド
共通言語ランタイム (CLR) の指定されたメモリの使用が完了したことをホストに通知します。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT ReleasedVirtualAddressSpace(  
    [in] LPVOID startAddress  
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `startAddress`  
 [in]解放するメモリの開始アドレスへのポインター。  
  
## <a name="remarks"></a>Remarks  
 `ReleasedVirtualAddressSpace`メソッドは、コールバック メソッドであり、ホスト アプリケーションの作成者によって実装する必要があります。 CLR によって呼び出されます。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** MSCorEE.h  
  
 **ライブラリ:** MSCorEE.dll でリソースとして含まれます  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>関連項目
- [IHostMemoryManager インターフェイス](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
