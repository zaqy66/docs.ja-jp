---
title: NamedPipeConnectionPoolSettings
ms.date: 03/30/2017
ms.assetid: 079bccb8-54b5-4436-a43d-5567763f72ce
ms.openlocfilehash: 77d8403947d341ea2efcef98bbf166f94f75f31f
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188730"
---
# <a name="namedpipeconnectionpoolsettings"></a>NamedPipeConnectionPoolSettings
NamedPipeConnectionPoolSettings  
  
## <a name="syntax"></a>構文  
  
```csharp
class NamedPipeConnectionPoolSettings  
{  
  string GroupName;  
  datetime IdleTimeout;  
  sint32 MaxOutboundConnectionsPerEndpoint;  
};  
```  
  
## <a name="methods"></a>メソッド  
 NamedPipeConnectionPoolSettings クラスは、メソッドを一切定義しません。  
  
## <a name="properties"></a>プロパティ  
 NamedPipeConnectionPoolSettings クラスには、次のプロパティがあります。  
  
### <a name="groupname"></a>GroupName  
 データ型: string  
  
 アクセスの種類 : 読み取り専用  
  
 バインド要素により使用される接続プールのグループ名。  
  
### <a name="idletimeout"></a>IdleTimeout  
 データ型 : datetime  
  
 アクセスの種類 : 読み取り専用  
  
 接続が切断されるまでの最大アイドル時間。  
  
### <a name="maxoutboundconnectionsperendpoint"></a>MaxOutboundConnectionsPerEndpoint  
 データ型 : sint32  
  
 アクセスの種類 : 読み取り専用  
  
 クライアント上の各エンドポイントでの発信接続の最大数。  
  
## <a name="requirements"></a>必要条件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ServiceModel.Channels.NamedPipeConnectionPoolSettings>
