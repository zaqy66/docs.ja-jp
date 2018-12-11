---
title: Binding2
ms.date: 03/30/2017
ms.assetid: 09511c6c-5749-4bb0-874e-0f0be36bfe04
ms.openlocfilehash: 84e304f3dedcbd785d6238e6cb5eb142c288b995
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53149706"
---
# <a name="binding"></a>バインド
wmi バインディング  
  
## <a name="syntax"></a>構文  
  
```csharp
class Binding  
{  
  BindingElement BindingElements[];  
  datetime CloseTimeout;  
  string Name;  
  string Namespace;  
  datetime OpenTimeout;  
  datetime ReceiveTimeout;  
  string Scheme;  
  datetime SendTimeout;  
};  
```  
  
## <a name="methods"></a>メソッド  
 Binding クラスは、メソッドを一切定義しません。  
  
## <a name="properties"></a>プロパティ  
 Binding クラスには、次のプロパティがあります。  
  
### <a name="bindingelements"></a>BindingElements  
 データの種類:BindingElement 配列  
  
 アクセスの種類:読み取り専用  
  
 バインディングによって実装されるバインド要素のコレクションです。  
  
### <a name="closetimeout"></a>CloseTimeout  
 データ型 : datetime  
  
 アクセスの種類:読み取り専用  
  
 クローズ操作が完了するまで待機する時間です。  
  
### <a name="name"></a>名前  
 データ型: string  
  
 アクセスの種類:読み取り専用  
  
 バインディングの名前。  
  
### <a name="namespace"></a>名前空間  
 データ型: string  
  
 アクセスの種類:読み取り専用  
  
 バインディングの XML 名前空間。  
  
### <a name="opentimeout"></a>OpenTimeout  
 データ型 : datetime  
  
 アクセスの種類:読み取り専用  
  
 オープン操作が完了するまで待機する時間です。  
  
### <a name="receivetimeout"></a>ReceiveTimeout  
 データ型 : datetime  
  
 アクセスの種類:読み取り専用  
  
 受信操作が完了するまで待機する時間です。  
  
### <a name="scheme"></a>Scheme  
 データ型: string  
  
 アクセスの種類:読み取り専用  
  
 このバインディングに組み込まれているチャネルおよびリスナー ファクトリによって使用される URI トランスポート スキームです。  
  
### <a name="sendtimeout"></a>SendTimeout  
 データ型 : datetime  
  
 アクセスの種類:読み取り専用  
  
 送信操作が完了するまで待機する時間です。  
  
## <a name="requirements"></a>必要条件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ServiceModel.Channels.Binding>
