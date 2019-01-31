---
title: <security> の <wsFederationHttpBinding>
ms.date: 03/30/2017
ms.assetid: a8e5e854-b8dc-4921-843d-34b6a4a6a8ba
ms.openlocfilehash: 5316060d4122a443dd0223ce1ee9cdd39efac0b8
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55282062"
---
# <a name="security-of-wsfederationhttpbinding"></a><span data-ttu-id="3e4cb-102">\<セキュリティ > の\<wsFederationHttpBinding ></span><span class="sxs-lookup"><span data-stu-id="3e4cb-102">\<security> of \<wsFederationHttpBinding></span></span>
<span data-ttu-id="3e4cb-103">セキュリティ設定を定義、 [ \<wsFederationHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-103">Defines the security settings of the [\<wsFederationHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md).</span></span>  
  
 <span data-ttu-id="3e4cb-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="3e4cb-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="3e4cb-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="3e4cb-105">\<bindings></span></span>  
<span data-ttu-id="3e4cb-106">\<wsFederatedBinding></span><span class="sxs-lookup"><span data-stu-id="3e4cb-106">\<wsFederatedBinding></span></span>  
<span data-ttu-id="3e4cb-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="3e4cb-107">\<binding></span></span>  
<span data-ttu-id="3e4cb-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="3e4cb-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e4cb-109">構文</span><span class="sxs-lookup"><span data-stu-id="3e4cb-109">Syntax</span></span>  
  
```xml  
<wsFederationBinding>
  <binding>
    <security mode="None/Message/TransportWithMessageCredential">
      <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
               issuedTokenType="string"
               issuedKeyType="SymmetricKey/PublicKey"
               negotiateServiceCredential="Boolean">
        <claimTypeRequirements>
          <add claimType="URI"
               isOptional="Boolean" />
        </claimTypeRequirements>
        <issuer address="Uri" >
          <headers>
            <add name="String"
                 namespace="String" />
          </headers>
          <identity>
            <certificate encodedValue="String" />
            <certificateReference findValue="String"
                                  isChainIncluded="Boolean"
                                  storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                                  storeLocation="LocalMachine/CurrentUser"
                                  X509FindType="System.Security.Cryptography.X509certificates.X509findtype" />
            <dns value="String" />
            <rsa value="String" />
            <servicePrincipalName value="String" />
            <usePrincipalName value="String" />
          </identity>
        </issuer>
        <issuerMetadata address="String">
          <headers>
            <add name="String"
                 namespace="String" />
          </headers>
          <identity>
            <certificate encodedValue="String" />
            <certificateReference findValue="String"
                                  isChainIncluded="Boolean"
                                  storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                                  storeLocation="LocalMachine/CurrentUser"
                                  X509FindType="System.Security.Cryptography.X509certificates.X509findtype" />
            <dns value="String" />
            <rsa value="String" />
            <servicePrincipalName value="String" />
            <usePrincipalName value="String" />
          </identity>
        </issuerMetadata>
        <tokenRequestParameters>
          <xmlElement>
          </xmlElement>
        </tokenRequestParameters>
      </message>
    </security>
  </binding>
</wsFederationBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3e4cb-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="3e4cb-110">Attributes and Elements</span></span>  
 <span data-ttu-id="3e4cb-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3e4cb-112">属性</span><span class="sxs-lookup"><span data-stu-id="3e4cb-112">Attributes</span></span>  
  
|<span data-ttu-id="3e4cb-113">属性</span><span class="sxs-lookup"><span data-stu-id="3e4cb-113">Attribute</span></span>|<span data-ttu-id="3e4cb-114">説明</span><span class="sxs-lookup"><span data-stu-id="3e4cb-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="3e4cb-115">モード</span><span class="sxs-lookup"><span data-stu-id="3e4cb-115">Mode</span></span>|<span data-ttu-id="3e4cb-116">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-116">Optional.</span></span> <span data-ttu-id="3e4cb-117">適用するセキュリティの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-117">Specifies the type of security that is applied.</span></span> <span data-ttu-id="3e4cb-118">既定値は `Message` です。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-118">The default value is `Message`.</span></span> <span data-ttu-id="3e4cb-119">この属性は <xref:System.ServiceModel.WSFederationHttpSecurityMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-119">This attribute is of type <xref:System.ServiceModel.WSFederationHttpSecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="3e4cb-120">Mode 属性</span><span class="sxs-lookup"><span data-stu-id="3e4cb-120">Mode Attribute</span></span>  
  
|<span data-ttu-id="3e4cb-121">値</span><span class="sxs-lookup"><span data-stu-id="3e4cb-121">Value</span></span>|<span data-ttu-id="3e4cb-122">説明</span><span class="sxs-lookup"><span data-stu-id="3e4cb-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="3e4cb-123">なし</span><span class="sxs-lookup"><span data-stu-id="3e4cb-123">None</span></span>|<span data-ttu-id="3e4cb-124">SOAP メッセージは、転送中はセキュリティで保護されません。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-124">The SOAP message is not secure during transfer.</span></span>|  
|<span data-ttu-id="3e4cb-125">メッセージ</span><span class="sxs-lookup"><span data-stu-id="3e4cb-125">Message</span></span>|<span data-ttu-id="3e4cb-126">SOAP メッセージ セキュリティを使用して、整合性、機密性、サーバー認証、およびクライアント認証を提供します。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-126">Integrity, confidentiality, server authentication and client authentication are provided using SOAP message security.</span></span> <span data-ttu-id="3e4cb-127">既定では、本文は暗号化および署名されます。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-127">By default, the body is encrypted and signed.</span></span> <span data-ttu-id="3e4cb-128">このサービスは、証明書を使用して設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-128">The service needs to be configured with a certificate.</span></span> <span data-ttu-id="3e4cb-129">クライアント認証は、セキュリティ トークン サービスによってクライアントに発行されるトークンに基づいています。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-129">Client authentication is based on the token issued to the client by a security token service</span></span>|  
|<span data-ttu-id="3e4cb-130">TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="3e4cb-130">TransportWithMessageCredential</span></span>|<span data-ttu-id="3e4cb-131">整合性、機密性、およびサーバー認証は、HTTPS によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-131">Integrity, confidentiality and server authentication are provided by HTTPS.</span></span> <span data-ttu-id="3e4cb-132">このサービスは、証明書を使用して設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-132">The service needs to be configured with a certificate.</span></span> <span data-ttu-id="3e4cb-133">クライアント認証は、SOAP メッセージ セキュリティによって提供され、セキュリティ トークン サービスによってクライアントに発行されるトークンに基づいています。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-133">Client authentication is provided by means of SOAP message security and is based on the token issued to the client by a security token service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3e4cb-134">子要素</span><span class="sxs-lookup"><span data-stu-id="3e4cb-134">Child Elements</span></span>  
  
|<span data-ttu-id="3e4cb-135">要素</span><span class="sxs-lookup"><span data-stu-id="3e4cb-135">Element</span></span>|<span data-ttu-id="3e4cb-136">説明</span><span class="sxs-lookup"><span data-stu-id="3e4cb-136">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3e4cb-137">\<message></span><span class="sxs-lookup"><span data-stu-id="3e4cb-137">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-element-of-wsfederationhttpbinding.md)|<span data-ttu-id="3e4cb-138">メッセージ レベル セキュリティの設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-138">Defines the settings for the message-level security.</span></span> <span data-ttu-id="3e4cb-139">この要素は <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-139">This element is of type <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="3e4cb-140">親要素</span><span class="sxs-lookup"><span data-stu-id="3e4cb-140">Parent Elements</span></span>  
  
|<span data-ttu-id="3e4cb-141">要素</span><span class="sxs-lookup"><span data-stu-id="3e4cb-141">Element</span></span>|<span data-ttu-id="3e4cb-142">説明</span><span class="sxs-lookup"><span data-stu-id="3e4cb-142">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3e4cb-143">\<binding></span><span class="sxs-lookup"><span data-stu-id="3e4cb-143">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="3e4cb-144">すべてのバインド機能を定義、 [ \<wsDualHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-144">Defines all binding capabilities of the [\<wsDualHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3e4cb-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="3e4cb-145">See also</span></span>
- <xref:System.ServiceModel.WSFederationHttpSecurity>
- <xref:System.ServiceModel.WSFederationHttpBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.WSFederationHttpBindingElement.Security%2A>
- <xref:System.ServiceModel.Configuration.WSFederationHttpSecurityElement>
- [<span data-ttu-id="3e4cb-146">方法: WSFederationHttpBinding を作成します。</span><span class="sxs-lookup"><span data-stu-id="3e4cb-146">How to: Create a WSFederationHttpBinding</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-wsfederationhttpbinding.md)
- [<span data-ttu-id="3e4cb-147">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="3e4cb-147">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="3e4cb-148">資格情報の種類の選択</span><span class="sxs-lookup"><span data-stu-id="3e4cb-148">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)
- [<span data-ttu-id="3e4cb-149">バインディング</span><span class="sxs-lookup"><span data-stu-id="3e4cb-149">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="3e4cb-150">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="3e4cb-150">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="3e4cb-151">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="3e4cb-151">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="3e4cb-152">\<binding></span><span class="sxs-lookup"><span data-stu-id="3e4cb-152">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
