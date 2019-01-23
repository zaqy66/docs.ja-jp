---
title: '&lt;timeOuts&gt;'
ms.date: 03/30/2017
ms.assetid: 7fccd436-b326-48ec-8de1-c16817a09e0d
ms.openlocfilehash: 42f4db1d954834cbfa3c526328cca45443751506
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629658"
---
# <a name="lttimeoutsgt"></a>&lt;timeOuts&gt;
サービス ホストを開くまたは閉じるまでに待機できる期間を指定する構成要素を表します。  
  
 \<system.ServiceModel >  
\<client>  
\<endpoint>  
\<host>  
\<timeOuts>  
  
## <a name="syntax"></a>構文  
  
```xml  
<timeOuts closeTimeout="TimeSpan"
          openTimeout="TimeSpan" />
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
  
|属性|説明|  
|---------------|-----------------|  
|`closeTimeout`|サービス ホストを閉じるまでに待機できる期間を指定する <xref:System.TimeSpan> 値。|  
|`openTimeout`|サービス ホストを開くまでに待機できる期間を指定する <xref:System.TimeSpan> 値。|  
  
### <a name="child-elements"></a>子要素  
 なし。  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<host>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|サービス ホストの設定を指定する構成要素です。|  
  
## <a name="see-also"></a>関連項目
- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- [ホスティング](../../../../../docs/framework/wcf/feature-details/hosting.md)
