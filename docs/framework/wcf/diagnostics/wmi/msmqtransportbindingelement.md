---
title: MsmqTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 1c89f073-9ed3-4025-a8c5-13535a0f526b
ms.openlocfilehash: 33cd9c427ed5ad04eaf9e9889f60f091f335d1e7
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50198108"
---
# <a name="msmqtransportbindingelement"></a>MsmqTransportBindingElement
MsmqTransportBindingElement  
  
## <a name="syntax"></a>構文  
  
```csharp
class MsmqTransportBindingElement : MsmqBindingElementBase  
{  
  sint32 MaxPoolSize;  
  string QueueTransferProtocol;  
  boolean UseActiveDirectory;  
};  
```  
  
## <a name="methods"></a>メソッド  
 MsmqTransportBindingElement クラスは、メソッドを一切定義しません。  
  
## <a name="properties"></a>プロパティ  
 MsmqTransportBindingElement クラスには、次のプロパティがあります。  
  
### <a name="maxpoolsize"></a>MaxPoolSize  
 データ型 : sint32  
  
 アクセスの種類 : 読み取り専用  
  
 内部 MSMQ メッセージ オブジェクトを含むプールの最大サイズです。  
  
### <a name="queuetransferprotocol"></a>QueueTransferProtocol  
 データ型: string  
  
 アクセスの種類 : 読み取り専用  
  
 このバインディングが使用するキューに置かれた通信チャネルのトランスポートを示す列挙値です。  
  
### <a name="useactivedirectory"></a>UseActiveDirectory  
 データ型 : boolean  
  
 アクセスの種類 : 読み取り専用  
  
 キューのアドレスを Active Directory を使用して変換する必要があるかどうかを示すブール値を返します。  
  
## <a name="requirements"></a>必要条件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ServiceModel.Channels.MsmqTransportBindingElement>
