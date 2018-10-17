---
title: ServiceToEndpointAssociation
ms.date: 03/30/2017
ms.assetid: 03c3cd15-e1b2-4dc2-bdc2-59fdccdae110
ms.openlocfilehash: 3d23a3ee10c47e04ea7bdba202ea5063c0d84fac
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "49372188"
---
# <a name="servicetoendpointassociation"></a>ServiceToEndpointAssociation
エンドポイントにサービスを割り当てます。  
  
## <a name="syntax"></a>構文  
  
```csharp
class ServiceToEndpointAssociation  
{  
  Service ref;  
  Endpoint ref;  
};  
```  
  
## <a name="methods"></a>メソッド  
 ServiceToEndpointAssociation クラスは、メソッドを一切定義しません。  
  
## <a name="properties"></a>プロパティ  
 ServiceToEndpointAssociation クラスには、次のプロパティがあります。  
  
### <a name="ref"></a>ref  
 データ型 : Service  
  
 アクセスの種類 : 読み取り専用  
修飾子: キー  
  
 エンドポイントに関連付けられるサービス。  
  
### <a name="ref"></a>ref  
 データ型 : Endpoint  
  
 アクセスの種類 : 読み取り専用  
修飾子: キー  
  
 サービスに関連付けられるエンドポイント。  
  
## <a name="requirements"></a>要件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|
