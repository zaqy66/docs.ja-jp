---
title: '&lt;スコープ&gt;'
ms.date: 03/30/2017
ms.assetid: 9a0dd3ce-e383-4ac3-b7be-7d604388304a
ms.openlocfilehash: 1235b483f63ab71405803c16f2d3c9926b15cfad
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54642988"
---
# <a name="ltscopesgt"></a>&lt;スコープ&gt;
クエリの実行中に、サービス エンドポイントのフィルター処理に使用できるカスタム スコープ URI を指定する構成要素のコレクションを含んでいます。  
  
\<system.ServiceModel >  
\<<behaviors>  
\<endpointBehaviors>  
\<behavior>  
\<endpointDiscovery>  
\<scopes>  
  
## <a name="syntax"></a>構文  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="String">
      <endpointDiscovery enable="Boolean">
        <scopes>
          <add scope="URI" />
        </scopes>
      </endpointDiscovery>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
 なし。  
  
### <a name="child-elements"></a>子要素  
  
|属性|説明|  
|---------------|-----------------|  
|[\<add>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-scopes.md)|サービス検索の一致条件に使用できるエンドポイントのスコープ情報を追加します。|  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<endpointDiscovery>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpointdiscovery.md)|エンドポイントのさまざまな探索設定を指定します (探索可能性、スコープ、メタデータに対するカスタム拡張など)。|  
  
## <a name="see-also"></a>関連項目
- <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
