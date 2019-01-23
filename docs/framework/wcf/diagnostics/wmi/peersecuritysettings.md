---
title: PeerSecuritySettings
ms.date: 03/30/2017
ms.assetid: 24ae0d35-f3a3-419b-afd6-686e22aae27b
ms.openlocfilehash: 761ed0e30c6acca8c910c5dc97dfbae46c1f89bb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54564839"
---
# <a name="peersecuritysettings"></a>PeerSecuritySettings
PeerSecuritySettings  
  
## <a name="syntax"></a>構文  
  
```csharp
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
  
 アクセスの種類:読み取り専用  
  
 このバインディングで構成されたエンドポイントによって、メッセージ レベルおよびトランスポート レベルのセキュリティが使用されているかどうかを示します。  
  
### <a name="transport"></a>Transport  
 データの種類:PeerTransportSecuritySettings  
  
 アクセスの種類:読み取り専用  
  
 トランスポートのセキュリティ設定です。  
  
## <a name="requirements"></a>必要条件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目
- <xref:System.ServiceModel.PeerSecuritySettings>
