---
title: '&lt;設定&gt;要素 (ネットワーク設定)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#settings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings
helpviewer_keywords:
- settings element
- <settings> element
ms.assetid: 189ce989-c39b-427d-b004-6b82a668b931
ms.openlocfilehash: 7db55dd9d2ca79342cadb2320d08ca9235223def
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54671853"
---
# <a name="ltsettingsgt-element-network-settings"></a>&lt;設定&gt;要素 (ネットワーク設定)
<xref:System.Net?displayProperty=nameWithType> 名前空間の基本的なネットワーク オプションを構成します。  
  
 \<configuration>  
\<system.net>  
\<settings>  
  
## <a name="syntax"></a>構文  
  
```xml  
<settings>  
  <httpListener>...</httpListener>  
  <httpWebRequest>...</httpWebRequest>  
  <ipv6>...</ipv6>  
  <performanceCounters>...</performanceCounters>  
  <servicePointManager>...</servicePointManager>  
  <socket>...</socket>  
  <webProxyScript>...</webProxyScript>  
</settings>  
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
 なし。  
  
### <a name="child-elements"></a>子要素  
  
|要素|説明|  
|-------------|-----------------|  
|[httpListener](../../../../../docs/framework/configure-apps/file-schema/network/httplistener-element-network-settings.md)|<xref:System.Net.HttpListener>クラスで使用されるパラメータをカスタマイズします。|  
|[httpWebRequest](../../../../../docs/framework/configure-apps/file-schema/network/httpwebrequest-element-network-settings.md)|Web 要求のパラメーターをカスタマイズします。|  
|[ipv6](../../../../../docs/framework/configure-apps/file-schema/network/ipv6-element-network-settings.md)|により、インターネット プロトコル バージョン 6 (IPv6) をサポートします。|  
|[\<performanceCounter > 要素 (ネットワーク設定)](../../../../../docs/framework/configure-apps/file-schema/network/performancecounter-element-network-settings.md)|ネットワーク パフォーマンス カウンターを有効にします。|  
|[servicePointManager](../../../../../docs/framework/configure-apps/file-schema/network/servicepointmanager-element-network-settings.md)|ネットワーク リソースへの接続を構成します。|  
|[socket](../../../../../docs/framework/configure-apps/file-schema/network/socket-element-network-settings.md)|ソケット操作が完了ポートを使用するかどうかを指定します。|  
|[\<webProxyScript > 要素 (ネットワーク設定)](../../../../../docs/framework/configure-apps/file-schema/network/webproxyscript-element-network-settings.md)|Web プロキシを検出するために使用するスクリプトの特性を構成します。|  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[system.net](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|.NET Framework がネットワークに接続する方法を指定するための設定が含まれています。|  
  
## <a name="remarks"></a>Remarks  
  
## <a name="configuration-files"></a>構成ファイル  
 この要素は、アプリケーション構成ファイルまたはマシン構成ファイル (Machine.config) で使用できます。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Net?displayProperty=nameWithType>
- [ネットワーク設定スキーマ](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
