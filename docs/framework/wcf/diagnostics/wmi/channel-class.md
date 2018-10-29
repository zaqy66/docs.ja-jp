---
title: チャネル クラス
ms.date: 03/30/2017
ms.assetid: d9fae2ca-209c-4341-a0f5-6b79d1a67776
ms.openlocfilehash: 108d5f8e3cd092863dbd48e2bb9d180798b091a4
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50197874"
---
# <a name="channel-class"></a>チャネル クラス
チャネル  
  
## <a name="syntax"></a>構文  
  
```csharp
class Channel  
{  
  string LocalAddress;  
  Endpoint ref;  
  string RemoteAddress;  
  string SessionId;  
  string Type;  
};  
```  
  
## <a name="methods"></a>メソッド  
 チャネル クラスは、メソッドを一切定義しません。  
  
## <a name="properties"></a>プロパティ  
 チャネル クラスには、次のプロパティがあります。  
  
### <a name="localaddress"></a>LocalAddress  
 データ型: string  
  
 アクセスの種類 : 読み取り専用  
  
 チャネルのローカル エンドポイント。  
  
### <a name="ref"></a>ref  
 データ型 : Endpoint  
  
 アクセスの種類 : 読み取り専用  
  
 チャネルが接続するエンドポイントへの参照。  
  
### <a name="remoteaddress"></a>RemoteAddress  
 データ型: string  
  
 アクセスの種類 : 読み取り専用  
  
 チャネルに関連するリモート アドレス。  
  
### <a name="sessionid"></a>SessionId  
 データ型: string  
  
 アクセスの種類 : 読み取り専用  
  
 現在のセッション ID (存在する場合)。  
  
### <a name="type"></a>種類  
 データ型: string  
  
 アクセスの種類 : 読み取り専用  
  
 チャネルの型。  
  
## <a name="requirements"></a>要件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ServiceModel.Channels.ChannelBase>
