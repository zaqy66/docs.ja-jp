---
title: VerifyClientKey 関数 (アンマネージ API リファレンス)
description: VerifyClientKey 関数により、クライアント キーが適切なセキュリティ。
ms.date: 11/06/2017
api_name:
- VerifyClientKey
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- VerifyClientKey
helpviewer_keywords:
- VerifyClientKey function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 94d601125049f0c215b3b03bf8b13d2959872c3d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54711760"
---
# <a name="verifyclientkey-function"></a>VerifyClientKey 関数
クライアント キーに適切なセキュリティが確実に含められます。  
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a>構文  
  
```  
LONG VerifyClientKey(); 
```  

## <a name="return-value"></a>戻り値

関数が成功した場合、戻り値は`ERROR_SUCCESS`(0)。

戻り値で定義されたゼロ以外のエラー コードは、関数が失敗した場合、 *WinError.h*します。

## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** WMINet_Utils.def  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>関連項目
- [WMI およびパフォーマンス カウンター (アンマネージ API リファレンス)](index.md)
