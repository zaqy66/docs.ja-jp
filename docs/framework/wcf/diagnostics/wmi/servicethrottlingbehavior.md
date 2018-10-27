---
title: ServiceThrottlingBehavior
ms.date: 03/30/2017
ms.assetid: 37b9e517-1f1f-4ec4-9fcb-2b8016794f5b
ms.openlocfilehash: edc154fcce0058455f1376a2a45807c92f7f2457
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50190957"
---
# <a name="servicethrottlingbehavior"></a>ServiceThrottlingBehavior
ServiceThrottlingBehavior  
  
## <a name="syntax"></a>構文  
  
```csharp  
class ServiceThrottlingBehavior : Behavior  
{  
  sint32 MaxConcurrentCalls;  
  sint32 MaxConcurrentInstances;  
  sint32 MaxConcurrentSessions;  
};  
```  
  
## <a name="methods"></a>メソッド  
 ServiceThrottlingBehavior クラスは、メソッドを一切定義しません。  
  
## <a name="properties"></a>プロパティ  
 ServiceThrottlingBehavior クラスには、次のプロパティがあります。  
  
### <a name="maxconcurrentcalls"></a>MaxConcurrentCalls  
 データ型 : sint32  
  
 アクセスの種類 : 読み取り専用  
  
 ServiceHost 内のすべてのディスパッチャー オブジェクトでアクティブに処理中のメッセージの最大数。  
  
### <a name="maxconcurrentinstances"></a>MaxConcurrentInstances  
 データ型 : sint32  
  
 アクセスの種類 : 読み取り専用  
  
 一度に実行可能なサービス オブジェクトの最大数。  
  
### <a name="maxconcurrentsessions"></a>MaxConcurrentSessions  
 データ型 : sint32  
  
 アクセスの種類 : 読み取り専用  
  
 ホストが一度に受け入れ可能なセッションの最大数。  
  
## <a name="requirements"></a>必要条件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ServiceModel.Description.ServiceThrottlingBehavior>
