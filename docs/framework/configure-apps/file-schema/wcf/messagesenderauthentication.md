---
title: '&lt;messageSenderAuthentication&gt;'
ms.date: 03/30/2017
ms.assetid: ea62fc06-55fb-42e0-aa2b-8867bdf4b415
ms.openlocfilehash: 8a3beb42d1064e6c6629014369628248b4cd5c8d
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43749708"
---
# <a name="ltmessagesenderauthenticationgt"></a>&lt;messageSenderAuthentication&gt;
メッセージ送信者により使用されるピア証明書の認証設定を指定します。  
  
 \<system.ServiceModel >  
\<<behaviors>  
\<serviceBehaviors>  
\<behavior>  
\<serviceCredentials>  
\<ピア >  
\<messageSenderAuthentication>  
  
## <a name="syntax"></a>構文  
  
```xml  
<messageSenderAuthentication  
   customCertificateValidatorType="namespace.typeName, [,AssemblyName] [,Version=version number] [,Culture=culture] [,PublicKeyToken=token]"  
   certificateValidationMode="ChainTrust/None/PeerTrust/PeerOrChainTrust/Custom"  
   revocationMode="NoCheck/Online/Offline"  
   trustedStoreLocation="CurrentUser/LocalMachine"   
/>  
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
  
|属性|説明|  
|---------------|-----------------|  
|`certificateValidationMode`|省略可能な列挙体です。 資格情報の検証に使用される 5 つのモードのいずれかを指定します。 この属性は <xref:System.ServiceModel.Security.X509CertificateValidationMode> 型です。 `Custom` に設定されている場合、`customCertificateValidator` も指定する必要があります。|  
|`customCertificateValidatorType`|省略可能な文字列。 ユーザー設定タイプの検証に使用されるタイプおよびアセンブリを指定します。 `certificateValidationMode` が `Custom` に設定されている場合は、この属性を設定する必要があります。 この属性は <xref:System.IdentityModel.Selectors.X509CertificateValidator> 型です。 Windows Communication Foundation (WCF) は、既定のピア信頼されたユーザー ストアに対してピア証明書を検証する証明書検証を提供します。 証明書が有効なルートまでつながっていることを検証します。 カスタム検証を実装して別の動作を指定したり、この属性を使用してカスタム検証を指定することができます。|  
|`revocationMode`|省略可能な列挙体です。 証明書失効モードを指定します。 この属性は <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> 型です。 システムは、ピア証明書を失効証明書リストで検索して、それが失効していないことを検証します。 このチェックは、オンラインで、またはキャッシュされた失効リストをチェックする方法で実行されます。 失効チェックは、この属性を NoCheck に設定することにより無効にできます。|  
|`trustedStoreLocation`|省略可能な列挙体です。 WCF セキュリティ システムによってピア証明書を検証する信頼されたストアの場所を指定します。 この属性は <xref:System.Security.Cryptography.X509Certificates.StoreLocation> 型です。|  
  
### <a name="child-elements"></a>子要素  
 なし。  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<peer>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-servicecredentials.md)|ピア ノードの現在の資格情報を指定します。|  
  
## <a name="remarks"></a>Remarks  
 メッセージ認証を選択した場合は、この要素を構成する必要があります。 によって提供される証明書を使用して出力チャネルでは、各メッセージが署名されて[\<証明書 >](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-element.md)します。 すべてのメッセージは、アプリケーションに配信される前に、この要素の `customCertificateValidatorType` 属性で指定した検証を使用してメッセージ資格情報がチェックされます。 検証は、資格情報を受け入れることも拒否することもできます。  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ServiceModel.Configuration.X509PeerCertificateAuthenticationElement>  
 <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication>  
 <xref:System.ServiceModel.Security.PeerCredential.MessageSenderAuthentication%2A>  
 <xref:System.ServiceModel.Configuration.PeerCredentialElement.MessageSenderAuthentication%2A>  
 [証明書の使用](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 [ピアツーピア ネットワーク](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)  
 [ピア チャネル メッセージの認証](https://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95)  
 [ピア チャネル カスタム認証](https://msdn.microsoft.com/library/4aa8a82e-41a8-48e2-8621-7e1cbabdca7c)  
 [セキュリティによるピア チャネル アプリケーションの保護](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
