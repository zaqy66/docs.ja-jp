---
title: <backupLists>
ms.date: 03/30/2017
ms.assetid: 593b3390-f65b-4684-ad40-0596b62f0954
ms.openlocfilehash: 6ac7ff19c76097cb54e7b77db21cad50b49513c0
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55280749"
---
# <a name="backuplists"></a>\<backupLists >
エラー処理に使用されるバックアップ サービス セットを定義する構成セクションを表します。 各子要素は、プライマリ エンドポイントに接続できない場合に使用するルーティング サービスが希望されるエンドポイントのセットを列挙したバックアップ リストです。 リストの最初のエンドポイントがダウンしていると、ルーティング サービスは自動的にリスト内で次にあるエンドポイントにフェールオーバーします。  これにより、クライアント アプリケーションに複雑なパターンの処理方法やサービスの配置場所を示すことなく、アプリケーションの信頼性を高めることができます。  
  
 \<system.serviceModel>  
\<ルーティング >  
\<backupLists >  
  
## <a name="syntax"></a>構文  
  
```xml  
<routing>
  <backupLists>
    <backupList name="String">
      <add endpointName="String" />
    </backupList>
  </backupLists>
</routing>
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
 なし。  
  
### <a name="child-elements"></a>子要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<filter>](../../../../../docs/framework/configure-apps/file-schema/wcf/filter.md)|プライマリ エンドポイントに接続できない場合に使用するルーティング サービスが希望されるエンドポイントの一覧が含まれています。 .|  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<ルーティング >](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|Windows Communication Foundation (WCF) の種類を指定するルーティング フィルター セットを定義する構成セクションを表します<xref:System.ServiceModel.Dispatcher.MessageFilter>受信メッセージの評価とルーティング テーブルをするターゲット エンドポイントを定義するときに使用される。フィルターが一致したときにメッセージを送信します。|  
  
## <a name="see-also"></a>関連項目
- <xref:System.ServiceModel.Routing.Configuration.BackupEndpointCollection?displayProperty=nameWithType>
