---
title: ICLRErrorReportingManager インターフェイス
ms.date: 03/30/2017
api_name:
- ICLRErrorReportingManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRErrorReportingManager
helpviewer_keywords:
- ICLRErrorReportingManager interface [.NET Framework hosting]
ms.assetid: ea8af0d5-4133-4472-8a1f-50570d7e85fa
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d10fe0240073464e3c2677343288e5379840885d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54732792"
---
# <a name="iclrerrorreportingmanager-interface"></a>ICLRErrorReportingManager インターフェイス
エラー報告のカスタム スタック ダンプの構成をホストできるようにするメソッドを提供します。  
  
## <a name="methods"></a>メソッド  
  
|メソッド|説明|  
|------------|-----------------|  
|[BeginCustomDump メソッド](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-begincustomdump-method.md)|エラー報告のカスタム スタック ダンプの構成を指定します。|  
|[EndCustomDump メソッド](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-endcustomdump-method.md)|以前の呼び出しによって設定されたカスタム スタック ダンプ構成をクリアします`BeginCustomDump`します。|  
|[GetBucketParametersForCurrentException メソッド](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-getbucketparametersforcurrentexception-method.md)|呼び出し元のスレッドで現在の例外のワトソン バケットを取得します。|  
  
## <a name="remarks"></a>Remarks  
 `BeginCustomDump`メソッドは、カスタムのスタック ダンプ構成を設定します。 `EndCustomDump`メソッドは、カスタム スタック ダンプ構成をクリアし、関連付けられている状態を解放します。 これはカスタム ダンプの完了後に呼び出す必要があります。  
  
> [!IMPORTANT]
>  呼び出しに失敗する`EndCustomDump`によりメモリ リークが発生します。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** MSCorEE.h  
  
 **ライブラリ:** MSCorEE.dll でリソースとして含まれます  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>関連項目
- [ECustomDumpItemKind 列挙型](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpitemkind-enumeration.md)
- [ホスト インターフェイス](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
