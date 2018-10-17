---
title: MtomMessageEncodingBindingElement
ms.date: 03/30/2017
ms.assetid: 4a9c6c3d-e561-4b2d-a693-7e84bdd3534a
ms.openlocfilehash: 49a640a666131491366646d6d486d25a515e35bf
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "49373433"
---
# <a name="mtommessageencodingbindingelement"></a>MtomMessageEncodingBindingElement
MtomMessageEncodingBindingElement  
  
## <a name="syntax"></a>構文  
  
```csharp
class MtomMessageEncodingBindingElement : MessageEncodingBindingElement  
{  
  string Encoding;  
  sint32 MaxReadPoolSize;  
  sint32 MaxWritePoolSize;  
  XmlDictionaryReaderQuotas ReaderQuotas;  
};  
```  
  
## <a name="methods"></a>メソッド  
 MtomMessageEncodingBindingElement クラスで定義されているメソッドはありません。  
  
## <a name="properties"></a>プロパティ  
 MtomMessageEncodingBindingElement クラスには、次のプロパティがあります。  
  
### <a name="encoding"></a>エンコード  
 データ型: string  
  
 アクセスの種類 : 読み取り専用  
  
 バインディングでメッセージの送信に使用される文字セット エンコーディング。  
  
### <a name="maxreadpoolsize"></a>MaxReadPoolSize  
 データ型 : sint32  
  
 アクセスの種類 : 読み取り専用  
  
 新しいリーダーを割り当てずに同時に読み取り可能なメッセージの数を定義する整数です。  
  
### <a name="maxwritepoolsize"></a>MaxWritePoolSize  
 データ型 : sint32  
  
 アクセスの種類 : 読み取り専用  
  
 新しいライターを割り当てずに同時に送信可能なメッセージの数を定義する整数です。  
  
### <a name="readerquotas"></a>ReaderQuotas  
 データ型 : XmlDictionaryReaderQuotas  
  
 アクセスの種類 : 読み取り専用  
  
 リーダのクォータ。  
  
## <a name="requirements"></a>要件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ServiceModel.Channels.MtomMessageEncodingBindingElement>
