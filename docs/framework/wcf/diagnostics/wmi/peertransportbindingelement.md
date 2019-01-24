---
title: PeerTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 40bf6be2-8087-4cb3-a66c-408d53eb9269
ms.openlocfilehash: 437ccc0446e3cc05596ab12b7908177b7f78e431
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54670655"
---
# <a name="peertransportbindingelement"></a>PeerTransportBindingElement
PeerTransportBindingElement  
  
## <a name="syntax"></a>構文  
  
```csharp
class PeerTransportBindingElement : TransportBindingElement  
{  
  string ListenIPAddress;  
  sint32 Port;  
  PeerSecuritySettings Security;  
};  
```  
  
## <a name="methods"></a>メソッド  
 PeerTransportBindingElement クラスは、メソッドを一切定義しません。  
  
## <a name="properties"></a>プロパティ  
 PeerTransportBindingElement クラスには、次のプロパティがあります。  
  
### <a name="listenipaddress"></a>ListenIPAddress  
 データ型: string  
  
 アクセスの種類:読み取り専用  
  
 ピア ノードがメッセージをリッスンする IP アドレスです。  
  
### <a name="port"></a>ポート  
 データ型 : sint32  
  
 アクセスの種類:読み取り専用  
  
 このバインディングがピア チャネル メッセージを処理するネットワーク インターフェイス ポートです。  
  
### <a name="security"></a>セキュリティ  
 データの種類:PeerSecuritySettings  
  
 アクセスの種類:読み取り専用  
  
 ピア トランスポートのセキュリティ設定です。  
  
## <a name="requirements"></a>必要条件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目
- <xref:System.ServiceModel.Channels.PeerTransportBindingElement>
