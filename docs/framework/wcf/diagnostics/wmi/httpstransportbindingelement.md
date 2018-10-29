---
title: HttpsTransportBindingElement
ms.date: 03/30/2017
ms.assetid: e78aa8c6-b53b-4105-a900-d3e7a39670f2
ms.openlocfilehash: 6883bab2ed293541d79ac8c5045b0a1853b36e29
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50198238"
---
# <a name="httpstransportbindingelement"></a>HttpsTransportBindingElement
HttpsTransportBindingElement  
  
## <a name="syntax"></a>構文  
  
```csharp  
class HttpsTransportBindingElement : HttpTransportBindingElement  
{  
  boolean RequireClientCertificate;  
};  
```  
  
## <a name="methods"></a>メソッド  
 HttpsTransportBindingElement クラスは、メソッドを一切定義しません。  
  
## <a name="properties"></a>プロパティ  
 HttpsTransportBindingElement クラスには、次のプロパティがあります。  
  
### <a name="requireclientcertificate"></a>RequireClientCertificate  
 データ型 : boolean  
  
 アクセスの種類 : 読み取り専用  
  
 SSL クライアント認証が必要かどうかを示す値。  
  
## <a name="requirements"></a>要件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ServiceModel.Channels.HttpsTransportBindingElement>
