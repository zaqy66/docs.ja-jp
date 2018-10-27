---
title: AsymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: 7bd3b6be-8f77-4927-93ae-6fa371893cca
ms.openlocfilehash: 076313548828f1fbce9c68b48c0fa7db9cca095f
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50185119"
---
# <a name="asymmetricsecuritybindingelement"></a>AsymmetricSecurityBindingElement
AsymmetricSecurityBindingElement  
  
## <a name="syntax"></a>構文  
  
```csharp
class AsymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a>メソッド  
 AsymmetricSecurityBindingElement クラスで定義されるメソッドはありません。  
  
## <a name="properties"></a>プロパティ  
 AsymmetricSecurityBindingElement クラスには、次のプロパティがあります。  
  
### <a name="messageprotectionorder"></a>MessageProtectionOrder  
 データ型: string  
  
 アクセスの種類 : 読み取り専用  
  
 このバインディングのメッセージの暗号化と署名の命令。  
  
### <a name="requiresignatureconfirmation"></a>RequireSignatureConfirmation  
 データ型 : boolean  
  
 アクセスの種類 : 読み取り専用  
  
 バインディングで署名の確認が必要かどうか。  
  
## <a name="requirements"></a>必要条件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>
