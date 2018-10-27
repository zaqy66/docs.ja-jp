---
title: ServiceAppDomain
ms.date: 03/30/2017
ms.assetid: f28e5186-a66d-46c1-abe9-b50e07f8cb4f
ms.openlocfilehash: 05be495dbfe87e7dd14b0cfbb38b30c6f8278e6d
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50192240"
---
# <a name="serviceappdomain"></a>ServiceAppDomain
アプリケーション ドメインにサービスを割り当てます。  
  
## <a name="syntax"></a>構文  
  
```csharp
class ServiceAppDomain  
{  
  Service ref;  
  AppDomainInfo ref;  
};  
```  
  
## <a name="methods"></a>メソッド  
 ServiceAppDomain クラスは、メソッドを一切定義しません。  
  
## <a name="properties"></a>プロパティ  
 ServiceAppDomain クラスには、次のプロパティがあります。  
  
### <a name="ref"></a>ref  
 データ型 : Service  
修飾子: キー  
  
 アクセスの種類 : 読み取り専用  
  
 このアプリケーション ドメインのサービスです。  
  
### <a name="ref"></a>ref  
 データ型: AppDomainInfo  
修飾子: キー  
  
 アクセスの種類 : 読み取り専用  
  
 アプリケーション ドメインのプロパティが格納されています。  
  
## <a name="requirements"></a>要件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|
