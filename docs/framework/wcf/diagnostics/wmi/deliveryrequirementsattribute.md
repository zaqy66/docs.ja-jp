---
title: DeliveryRequirementsAttribute
ms.date: 03/30/2017
ms.assetid: 40c5435c-a325-4cf8-9dd0-d6e24b4a56a3
ms.openlocfilehash: 809e9d809bce456c831aab83c7ac19a882b2959b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54571325"
---
# <a name="deliveryrequirementsattribute"></a>DeliveryRequirementsAttribute
DeliveryRequirementsAttribute  
  
## <a name="syntax"></a>構文  
  
```csharp
class DeliveryRequirementsAttribute : Behavior  
{  
  string QueuedDeliveryRequirements;  
  boolean RequireOrderedDelivery;  
  string TargetContract;  
};  
```  
  
## <a name="methods"></a>メソッド  
 DeliveryRequirementsAttribute クラスは、メソッドを一切定義しません。  
  
## <a name="properties"></a>プロパティ  
 DeliveryRequirementsAttribute クラスには、次のプロパティがあります。  
  
### <a name="queueddeliveryrequirements"></a>QueuedDeliveryRequirements  
 データ型: string  
  
 アクセスの種類:読み取り専用  
  
 サービスのバインドがコントラクトをサポートするかどうかを指定します。  
  
### <a name="requireordereddelivery"></a>RequireOrderedDelivery  
 データ型 : boolean  
  
 アクセスの種類:読み取り専用  
  
 バインディングが順序付きメッセージをサポートするかどうかを指定します。  
  
### <a name="targetcontract"></a>TargetContract  
 データ型: string  
  
 アクセスの種類:読み取り専用  
  
 適用先となるコントラクトです。  
  
## <a name="requirements"></a>必要条件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目
- <xref:System.ServiceModel.DeliveryRequirementsAttribute>
