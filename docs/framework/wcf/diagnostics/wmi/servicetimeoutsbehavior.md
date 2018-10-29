---
title: ServiceTimeoutsBehavior
ms.date: 03/30/2017
ms.assetid: 4412525d-a3cc-4eae-b3e8-a50ce766d09d
ms.openlocfilehash: 1a5284915de739e95325234318842a4d1ab607be
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2018
ms.locfileid: "50196979"
---
# <a name="servicetimeoutsbehavior"></a>ServiceTimeoutsBehavior
ServiceTimeoutsBehavior  
  
## <a name="syntax"></a>構文  
  
```csharp
class ServiceTimeoutsBehavior : Behavior  
{  
  datetime TransactionTimeout;  
};  
```  
  
## <a name="methods"></a>メソッド  
 ServiceTimeoutsBehavior クラスは、メソッドを一切定義しません。  
  
## <a name="properties"></a>プロパティ  
 ServiceTimeoutsBehavior クラスには、次のプロパティがあります。  
  
### <a name="transactiontimeout"></a>TransactionTimeout  
 データ型 : datetime  
  
 アクセスの種類 : 読み取り専用  
  
 トランザクションを完了しなければならない期間。  
  
## <a name="requirements"></a>必要条件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ServiceModel.Configuration.ServiceTimeoutsElement>
