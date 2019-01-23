---
title: ServiceDebugBehavior
ms.date: 03/30/2017
ms.assetid: a5ec9061-1e95-43fb-b0d9-dbd0a7bc3c44
ms.openlocfilehash: d6f0e4741aa10bff450a29cfd7a9e63e226c6495
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498883"
---
# <a name="servicedebugbehavior"></a>ServiceDebugBehavior
ServiceDebugBehavior  
  
## <a name="syntax"></a>構文  
  
```csharp
class ServiceDebugBehavior : Behavior  
{  
  boolean HttpHelpPageEnabled;  
  string HttpHelpPageUrl;  
  boolean HttpsHelpPageEnabled;  
  string HttpsHelpPageUrl;  
  boolean IncludeExceptionDetailInFaults;  
};  
```  
  
## <a name="methods"></a>メソッド  
 ServiceDebugBehavior クラスで定義されるメソッドはありません。  
  
## <a name="properties"></a>プロパティ  
 ServiceDebugBehavior クラスには、次のプロパティがあります。  
  
### <a name="httphelppageenabled"></a>HttpHelpPageEnabled  
 データ型 : boolean  
  
 アクセスの種類:読み取り専用  
  
 `HttpGetUrl` 属性によって制御されるアドレスで、サービスが WSDL を公開するかどうかを制御します。  
  
### <a name="httphelppageurl"></a>HttpHelpPageUrl  
 データ型: string  
  
 アクセスの種類:読み取り専用  
  
 HTTP を使用した取得のために、サービス WSDL が公開される場所を設定します。  
  
### <a name="httpshelppageenabled"></a>HttpsHelpPageEnabled  
 データ型 : boolean  
  
 アクセスの種類:読み取り専用  
  
 `HttpsGetUrl` 属性によって制御されるアドレスで、サービスが HTTPS を介して WSDL を公開するかどうかを制御します。  
  
### <a name="httpshelppageurl"></a>HttpsHelpPageUrl  
 データ型: string  
  
 アクセスの種類:読み取り専用  
  
 HTTPS を使用した取得のために、サービス WSDL が公開される場所を設定します。  
  
### <a name="includeexceptiondetailinfaults"></a>IncludeExceptionDetailInFaults  
 データ型 : boolean  
  
 アクセスの種類:読み取り専用  
  
 デバッグの目的でクライアントに返される SOAP エラーの詳細に、マネージド例外情報を含めるかどうかを指定します。  
  
## <a name="requirements"></a>必要条件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目
- <xref:System.ServiceModel.Description.ServiceDebugBehavior>
