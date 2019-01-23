---
title: TransactionFlowBindingElement
ms.date: 03/30/2017
ms.assetid: 0a9656fe-2400-45ca-ad79-92715c8cf190
ms.openlocfilehash: d0311837ebb8112d9492fb548492bcd3e10230e7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54514572"
---
# <a name="transactionflowbindingelement"></a>TransactionFlowBindingElement
TransactionFlowBindingElement  
  
## <a name="syntax"></a>構文  
  
```csharp
class TransactionFlowBindingElement : BindingElement  
{  
  string IssuedTokens;  
  string TransactionProtocol;  
  boolean Transactions;  
};  
```  
  
## <a name="methods"></a>メソッド  
 TransactionFlowBindingElement クラスは、メソッドを一切定義しません。  
  
## <a name="properties"></a>プロパティ  
 TransactionFlowBindingElement クラスには、次のプロパティがあります。  
  
### <a name="issuedtokens"></a>IssuedTokens  
 データ型: string  
  
 アクセスの種類:読み取り専用  
  
 発行されるセキュリティ トークン ヘッダー (WS-Trust からの IssuedTokens) の要件を指定します。  
  
### <a name="transactionprotocol"></a>TransactionProtocol  
 データ型: string  
  
 アクセスの種類:読み取り専用  
  
 トランザクションをフローさせるためにサービスによって使用されるトランザクション プロトコルです。  
  
### <a name="transactions"></a>トランザクション  
 データ型 : boolean  
  
 アクセスの種類:読み取り専用  
  
 受信トランザクションをサポートするかどうかを示します。  
  
## <a name="requirements"></a>必要条件  
  
|MOF|Servicemodel.mof にて宣言済み。|  
|---------|-----------------------------------|  
|Namespace|root\ServiceModel で定義|  
  
## <a name="see-also"></a>関連項目
- <xref:System.ServiceModel.Channels.TransactionFlowBindingElement>
