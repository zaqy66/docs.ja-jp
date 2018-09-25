---
title: PeerSecuritySettings
ms.date: 03/30/2017
ms.assetid: 24ae0d35-f3a3-419b-afd6-686e22aae27b
author: BrucePerlerMS
ms.openlocfilehash: c74ee82d7aa3a23f0ee6a69185ad45857c31bb0b
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47087880"
---
# <a name="peersecuritysettings"></a>PeerSecuritySettings
PeerSecuritySettings  
  
## <a name="syntax"></a>構文  
  
```  
class PeerSecuritySettings  
{  
  string Mode;  
  PeerTransportSecuritySettings Transport;  
};  
```  
  
## <a name="methods"></a>メソッド  
 PeerSecuritySettings クラスは、メソッドを一切定義しません。  
  
## <a name="properties"></a>プロパティ  
 PeerSecuritySettings クラスには、次のプロパティがあります。  
  
### <a name="mode"></a>モード  
 データ型: string  
  
 アクセスの種類 : 読み取り専用  
  
 このバインディングで構成されたエンドポイントによって、メッセージ レベルおよびトランスポート レベルのセキュリティが使用されているかどうかを示します。  
  
### <a name="transport"></a>Transport  
 データ型 : PeerTransportSecuritySettings  
  
 アクセスの種類 : 読み取り専用  
  
 トランスポートのセキュリティ設定です。  
  
## <a name="requirements"></a>要件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ServiceModel.PeerSecuritySettings>
