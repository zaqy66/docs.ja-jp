---
title: <transport> の <netMsmqBinding>
ms.date: 03/30/2017
ms.assetid: 72e1b338-39f0-4af1-a5d9-7a2fb79f6a0b
ms.openlocfilehash: c82a786fe8e4a2b2e3243db007f4f705d9fbd79a
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55277148"
---
# <a name="transport-of-netmsmqbinding"></a>\<トランスポート > の\<netMsmqBinding >
トランスポートのセキュリティ設定を定義します。  
  
 \<system.ServiceModel >  
\<bindings>  
\<netMsmqBinding>  
\<binding>  
\<セキュリティ >  
\<transport>  
  
## <a name="syntax"></a>構文  
  
```xml  
<netMsmqBinding>
  <binding>
    <security>
      <transport msmqAuthenticationMode="None/WindowsDomain/Certificate"
                 msmqEncryptionAlgorithm="RC4Stream/AES"
                 msmqProtectionLevel="None/Sign/EncryptAndSign"
                 msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />
    </security>
  </binding>
</netMsmqBinding>
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
  
|属性|説明|  
|---------------|-----------------|  
|msmqAuthenticationMode|MSMQ トランスポートによるメッセージの認証方法を指定します。 以下の値が有効です。<br /><br /> -None。認証はありません。<br />-   WindowsDomain:認証メカニズムは、メッセージに関連付けられたセキュリティ識別子の X.509 証明書を取得するのに Active Directory を使用します。 次に、これを使用してキューの ACL がチェックされ、ユーザーがキューへの書き込み権限を持っていることが確認されます。<br />-証明書:チャネルは、証明書ストアから証明書を取得します。<br /><br /> 既定値は `WindowsDomain` です。<br /><br /> この属性が `None` に設定されている場合、`msmqProtectionLevel` 属性も `None` に設定する必要があります。 この属性は <xref:System.ServiceModel.MsmqAuthenticationMode> 型です。|  
|msmqEncryptionAlgorithm|メッセージ キュー マネージャー間でメッセージを転送するときに、ネットワーク上でメッセージの暗号化に使用されるアルゴリズムを指定します。 以下の値が有効です。<br /><br /> -[Rc4stream]<br />-AES<br />-既定値は`RC4Stream`します。 この属性は <xref:System.ServiceModel.MsmqEncryptionAlgorithm> 型です。|  
|msmqProtectionLevel|MSMQ トランスポートのレベルでメッセージをセキュリティで保護する方法を指定します。 暗号化を行うとメッセージの整合性が確保されますが、署名および暗号化を使用するとメッセージの整合性と否認防止の両方が確保されます。 つまり、メッセージは本当にその送信者から送信されていることになり、記載されている送信者が実際の送信者になります。 以下の値が有効です。<br /><br /> -None。保護されません。<br />署名:メッセージは署名されます。<br />-EncryptAndSign:メッセージは暗号化および署名されます。<br />-既定値は`Sign`します。|  
|msmqSecureHashAlgorithm|メッセージ ダイジェストの計算に使用されるハッシュ アルゴリズムを指定します。 以下の値が有効です。<br /><br /> -   MD5<br />-SHA1<br />-   SHA256<br />-SHA512<br /><br /> 既定値は `SHA1` です。 この属性は <xref:System.ServiceModel.MsmqSecureHashAlgorithm> 型です。|  
  
### <a name="child-elements"></a>子要素  
 なし  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<security>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netmsmqbinding.md)|キューに置かれているトランスポートのセキュリティ設定を定義します。|  
  
## <a name="see-also"></a>関連項目
- <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>
- <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement.Transport%2A>
- <xref:System.ServiceModel.NetMsmqSecurity.Transport%2A>
- <xref:System.ServiceModel.MsmqTransportSecurity>
- [WCF のキュー](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)
- [サービスおよびクライアントのセキュリティ保護](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [バインディング](../../../../../docs/framework/wcf/bindings.md)
- [システムが提供するバインディングの構成](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [サービスとクライアントを構成するためのバインディングの使用](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](../../../../../docs/framework/misc/binding.md)
