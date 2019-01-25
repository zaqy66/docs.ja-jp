---
title: TransportBindingElement
ms.date: 03/30/2017
ms.assetid: 54ecfbee-53c0-410c-a7fa-a98f2e40c545
ms.openlocfilehash: 303e5523befb68c65bc50ee3933af58897929363
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54668454"
---
# <a name="transportbindingelement"></a>TransportBindingElement
TransportBindingElement  
  
## <a name="syntax"></a>構文  
  
```csharp
class TransportBindingElement : BindingElement  
{  
  boolean ManualAddressing;  
  sint64 MaxBufferPoolSize;  
  sint64 MaxReceivedMessageSize;  
  string Scheme;  
};  
```  
  
## <a name="methods"></a>メソッド  
 TransportBindingElement クラスは、メソッドを一切定義しません。  
  
## <a name="properties"></a>プロパティ  
 TransportBindingElement クラスには、次のプロパティがあります。  
  
### <a name="manualaddressing"></a>ManualAddressing  
 データ型 : boolean  
  
 アクセスの種類:読み取り専用  
  
 メッセージのアドレス指定をユーザーが制御するかどうかを指定するブール値。  
  
### <a name="maxbufferpoolsize"></a>MaxBufferPoolSize  
 データ型 : sint64  
  
 アクセスの種類:読み取り専用  
  
 バインディングに使用するバッファー プールの最大サイズ。  
  
### <a name="maxreceivedmessagesize"></a>MaxReceivedMessageSize  
 データ型 : sint64  
  
 アクセスの種類:読み取り専用  
  
 このバインディングで処理されるメッセージの最大サイズ。  
  
### <a name="scheme"></a>Scheme  
 データ型: string  
  
 アクセスの種類:読み取り専用  
  
 トランスポートの URI スキーム。  
  
## <a name="requirements"></a>必要条件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目
- <xref:System.ServiceModel.Channels.TransportBindingElement>
