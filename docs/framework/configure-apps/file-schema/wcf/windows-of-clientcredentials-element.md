---
title: '&lt;clientCredentials&gt; 要素の &lt;windows&gt;'
ms.date: 03/30/2017
ms.assetid: 793e41c2-31ea-4159-abbc-2123bf097233
ms.openlocfilehash: 1331456f6defc24511064684181f615451be5b93
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54610748"
---
# <a name="ltwindowsgt-of-ltclientcredentialsgt-element"></a>&lt;clientCredentials&gt; 要素の &lt;windows&gt;
クライアントを表すために使用される Windows 資格情報の設定を指定します。  
  
 \<system.ServiceModel >  
\<<behaviors>  
\<endpointBehaviors>  
\<behavior>  
\<clientCredentials>  
\<windows>  
  
## <a name="syntax"></a>構文  
  
```xml  
<windows allowedImpersonationLevel="Identification/Impersonation/Delegation/Anonymous/None"
         allowNtlm="Boolean" />
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
  
|属性|説明|  
|---------------|-----------------|  
|`allowedImpersonationLevel`|クライアントがサーバーと通信する偽装設定を設定します。 クライアントが選択する偽装モードは、サーバーでは適用されません。 以下の値が有効です。<br /><br /> 識別します。サーバーは、id およびクライアントの権限を取得できますが、クライアントを偽装できません。<br />-Impersonation:サーバーは、ローカル システム上のクライアントのセキュリティ コンテキストを偽装できます。<br />委任します。サーバーは、リモート システム上のクライアントのセキュリティ コンテキストを偽装できます。<br />匿名。サーバーは、権限を借用またはクライアントを識別できません。<br />-None。偽装レベルが割り当てられていません。<br /><br /> 既定値は Identification です。 この属性は <xref:System.Security.Principal.TokenImpersonationLevel> 型です。|  
|`allowNtlm`|このプロパティを `true` に設定すると、Kerberos 認証を利用できない場合、NTLM 認証にダウングレードできます。<br /><br /> このプロパティを設定`false`させるベスト エフォートで NTLM が使用されている場合に例外をスローするように、Windows Communication Foundation (WCF) が発生します。 ただし、このプロパティを `false` に設定しても、ネットワーク経由で NTLM 資格情報が送信されなくなるとは限りません。|  
  
### <a name="child-elements"></a>子要素  
 なし。  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<clientCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)|サービスに対するクライアントの認証に使用される資格情報を指定します。|  
  
## <a name="see-also"></a>関連項目
- <xref:System.ServiceModel.Configuration.WindowsClientElement>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement.Windows%2A>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Description.ClientCredentials.Windows%2A>
- <xref:System.ServiceModel.Security.WindowsClientCredential>
- [クライアントのセキュリティ保護](../../../../../docs/framework/wcf/securing-clients.md)
- [証明書の使用](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)
- [サービスおよびクライアントのセキュリティ保護](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
