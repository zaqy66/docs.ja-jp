---
title: '&lt;messageSenderAuthentication&gt; 要素'
ms.date: 03/30/2017
ms.assetid: 8d979dfc-a6f9-42ec-96d5-7fbc13a48118
ms.openlocfilehash: cb727df7b8d7605cbe984a8f6737c89bf1bfb2be
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43788965"
---
# <a name="ltmessagesenderauthenticationgt-element"></a><span data-ttu-id="d1bce-102">&lt;messageSenderAuthentication&gt; 要素</span><span class="sxs-lookup"><span data-stu-id="d1bce-102">&lt;messageSenderAuthentication&gt; element</span></span>
<span data-ttu-id="d1bce-103">ピアツーピア メッセージ送信者の認証オプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="d1bce-103">Specifies authentication options for peer-to-peer message senders.</span></span>  
  
 <span data-ttu-id="d1bce-104">ピア ツー ピア プログラミングの詳細については、次を参照してください。[ピア ツー ピア ネットワー キング](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)します。</span><span class="sxs-lookup"><span data-stu-id="d1bce-104">For more information about peer-to-peer programming, see [Peer-to-Peer Networking](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md).</span></span>  
  
 <span data-ttu-id="d1bce-105">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="d1bce-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="d1bce-106">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="d1bce-106">\<behaviors></span></span>  
<span data-ttu-id="d1bce-107">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="d1bce-107">\<endpointBehaviors></span></span>  
<span data-ttu-id="d1bce-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="d1bce-108">\<behavior></span></span>  
<span data-ttu-id="d1bce-109">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="d1bce-109">\<clientCredentials></span></span>  
<span data-ttu-id="d1bce-110">\<ピア ></span><span class="sxs-lookup"><span data-stu-id="d1bce-110">\<peer></span></span>  
<span data-ttu-id="d1bce-111">\<messageSenderAuthentication></span><span class="sxs-lookup"><span data-stu-id="d1bce-111">\<messageSenderAuthentication></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d1bce-112">構文</span><span class="sxs-lookup"><span data-stu-id="d1bce-112">Syntax</span></span>  
  
```xml  
<messageSenderAuthentication  
customCertificateValidatorType= "namespace.typeName, [,AssemblyName] [,Version=version number] [,Culture=culture] [,PublicKeyToken=token]"  
certificateValidationMode = "ChainTrust/None/PeerTrust/PeerOrChainTrust/Custom"  
revocationMode="NoCheck/Online/Offline"  
trustedStoreLocation="CurrentUser/LocalMachine"   
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d1bce-113">属性および要素</span><span class="sxs-lookup"><span data-stu-id="d1bce-113">Attributes and Elements</span></span>  
 <span data-ttu-id="d1bce-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="d1bce-114">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d1bce-115">属性</span><span class="sxs-lookup"><span data-stu-id="d1bce-115">Attributes</span></span>  
  
|<span data-ttu-id="d1bce-116">属性</span><span class="sxs-lookup"><span data-stu-id="d1bce-116">Attribute</span></span>|<span data-ttu-id="d1bce-117">説明</span><span class="sxs-lookup"><span data-stu-id="d1bce-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="d1bce-118">customCertificateValidatorType</span><span class="sxs-lookup"><span data-stu-id="d1bce-118">customCertificateValidatorType</span></span>|<span data-ttu-id="d1bce-119">カスタム型の検証に使用される型およびアセンブリです。</span><span class="sxs-lookup"><span data-stu-id="d1bce-119">A type and assembly used to validate a custom type.</span></span> <span data-ttu-id="d1bce-120">`certificateValidationMode` が `Custom` に設定されている場合は、この属性を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1bce-120">This attribute must be set when `certificateValidationMode` is set to `Custom`.</span></span>|  
|<span data-ttu-id="d1bce-121">certifcateValidationMode</span><span class="sxs-lookup"><span data-stu-id="d1bce-121">certifcateValidationMode</span></span>|<span data-ttu-id="d1bce-122">資格情報の検証に使用される 3 つのモードのいずれかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d1bce-122">Specifies one of three modes used to validate credentials.</span></span> <span data-ttu-id="d1bce-123">`Custom` に設定されている場合、`customCertificateValidator` も指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1bce-123">If set to `Custom`, then a `customCertificateValidator` must also be supplied.</span></span>|  
|<span data-ttu-id="d1bce-124">revocationMode</span><span class="sxs-lookup"><span data-stu-id="d1bce-124">revocationMode</span></span>|<span data-ttu-id="d1bce-125">証明書失効リスト (CRL) のチェックに使用されるモードのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="d1bce-125">One of the modes used to check for a revoked certificate lists (CRL).</span></span>|  
|<span data-ttu-id="d1bce-126">trustedStoreLocation</span><span class="sxs-lookup"><span data-stu-id="d1bce-126">trustedStoreLocation</span></span>|<span data-ttu-id="d1bce-127">2 つのシステム格納場所 (`LocalMachine` または `CurrentUser`) のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="d1bce-127">One of the two system store locations: `LocalMachine` or `CurrentUser`.</span></span> <span data-ttu-id="d1bce-128">この値は、サービス証明書がクライアントにネゴシエートされるときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="d1bce-128">This value is used when a service certificate is negotiated to the client.</span></span> <span data-ttu-id="d1bce-129">に対して検証が実行、**信頼されたユーザー**指定したストアの場所に格納します。</span><span class="sxs-lookup"><span data-stu-id="d1bce-129">Validation is performed against the **Trusted People** store in the specified store location.</span></span>|  
  
## <a name="customcertificatevalidatortype-attribute"></a><span data-ttu-id="d1bce-130">customCertificateValidatorType 属性</span><span class="sxs-lookup"><span data-stu-id="d1bce-130">customCertificateValidatorType Attribute</span></span>  
  
|<span data-ttu-id="d1bce-131">値</span><span class="sxs-lookup"><span data-stu-id="d1bce-131">Value</span></span>|<span data-ttu-id="d1bce-132">説明</span><span class="sxs-lookup"><span data-stu-id="d1bce-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="d1bce-133">String</span><span class="sxs-lookup"><span data-stu-id="d1bce-133">String</span></span>|<span data-ttu-id="d1bce-134">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="d1bce-134">Optional.</span></span> <span data-ttu-id="d1bce-135">タイプ名およびアセンブリと、タイプの検索に使用される他のデータを指定します。</span><span class="sxs-lookup"><span data-stu-id="d1bce-135">Specifies the type name and assembly and other data used to find the type.</span></span> <span data-ttu-id="d1bce-136">少なくとも、名前空間とタイプ名が必要です。</span><span class="sxs-lookup"><span data-stu-id="d1bce-136">At minimum, a namespace and type name are required.</span></span> <span data-ttu-id="d1bce-137">省略可能な情報は、アセンブリ名、バージョン番号、カルチャ、および公開キー トークンです。</span><span class="sxs-lookup"><span data-stu-id="d1bce-137">Optional information includes: assembly name, version number, culture, and public key token.</span></span>|  
  
## <a name="certificatevalidationmode-attribute"></a><span data-ttu-id="d1bce-138">certificateValidationMode 属性</span><span class="sxs-lookup"><span data-stu-id="d1bce-138">certificateValidationMode Attribute</span></span>  
  
|<span data-ttu-id="d1bce-139">値</span><span class="sxs-lookup"><span data-stu-id="d1bce-139">Value</span></span>|<span data-ttu-id="d1bce-140">説明</span><span class="sxs-lookup"><span data-stu-id="d1bce-140">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="d1bce-141">列挙型</span><span class="sxs-lookup"><span data-stu-id="d1bce-141">Enumeration</span></span>|<span data-ttu-id="d1bce-142">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="d1bce-142">Optional.</span></span> <span data-ttu-id="d1bce-143">`None`、`PeerTrust`、`ChainTrust`、`PeerOrChainTrust`、`Custom` のいずれかの値にします。</span><span class="sxs-lookup"><span data-stu-id="d1bce-143">One of the following values: `None`, `PeerTrust`, `ChainTrust`, `PeerOrChainTrust`, `Custom`.</span></span> <span data-ttu-id="d1bce-144">既定値は、`ChainTrust` です。</span><span class="sxs-lookup"><span data-stu-id="d1bce-144">The default is `ChainTrust`.</span></span> <span data-ttu-id="d1bce-145">既定値は `ChainTrust` です。</span><span class="sxs-lookup"><span data-stu-id="d1bce-145">The default is `ChainTrust`.</span></span><br /><br /> <span data-ttu-id="d1bce-146">詳細については、次を参照してください。 [Working with Certificates](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)します。</span><span class="sxs-lookup"><span data-stu-id="d1bce-146">For more information, see [Working with Certificates](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md).</span></span>|  
  
## <a name="revocationmode-attribute"></a><span data-ttu-id="d1bce-147">revocationMode 属性</span><span class="sxs-lookup"><span data-stu-id="d1bce-147">revocationMode Attribute</span></span>  
  
|<span data-ttu-id="d1bce-148">値</span><span class="sxs-lookup"><span data-stu-id="d1bce-148">Value</span></span>|<span data-ttu-id="d1bce-149">説明</span><span class="sxs-lookup"><span data-stu-id="d1bce-149">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="d1bce-150">列挙型</span><span class="sxs-lookup"><span data-stu-id="d1bce-150">Enumeration</span></span>|<span data-ttu-id="d1bce-151">`NoCheck`、`Online`、`Offline` のいずれかの値にします。</span><span class="sxs-lookup"><span data-stu-id="d1bce-151">One of the following values: `NoCheck`, `Online`, `Offline`.</span></span> <span data-ttu-id="d1bce-152">既定値は `Online` です。</span><span class="sxs-lookup"><span data-stu-id="d1bce-152">The default is `Online`.</span></span><br /><br /> <span data-ttu-id="d1bce-153">詳細については、次を参照してください。 [Working with Certificates](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)します。</span><span class="sxs-lookup"><span data-stu-id="d1bce-153">For more information, see [Working with Certificates](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md).</span></span>|  
  
## <a name="trustedstorelocation-attribute"></a><span data-ttu-id="d1bce-154">trustedStoreLocation 属性</span><span class="sxs-lookup"><span data-stu-id="d1bce-154">trustedStoreLocation Attribute</span></span>  
  
|<span data-ttu-id="d1bce-155">値</span><span class="sxs-lookup"><span data-stu-id="d1bce-155">Value</span></span>|<span data-ttu-id="d1bce-156">説明</span><span class="sxs-lookup"><span data-stu-id="d1bce-156">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="d1bce-157">列挙型</span><span class="sxs-lookup"><span data-stu-id="d1bce-157">Enumeration</span></span>|<span data-ttu-id="d1bce-158">`LocalMachine` または `CurrentUser` のいずれかの値にします。</span><span class="sxs-lookup"><span data-stu-id="d1bce-158">One of the following values: `LocalMachine` or `CurrentUser`.</span></span> <span data-ttu-id="d1bce-159">既定値は、`CurrentUser` です。</span><span class="sxs-lookup"><span data-stu-id="d1bce-159">The default is `CurrentUser`.</span></span> <span data-ttu-id="d1bce-160">クライアント アプリケーションがシステム アカウントで実行されている場合、証明書は通常 `LocalMachine` の下にあります。</span><span class="sxs-lookup"><span data-stu-id="d1bce-160">If the client application is running under a system account then the certificate is typically under `LocalMachine`.</span></span> <span data-ttu-id="d1bce-161">クライアント アプリケーションがユーザー アカウントで実行されている場合、証明書は通常 `CurrentUser` の下にあります。</span><span class="sxs-lookup"><span data-stu-id="d1bce-161">If the client application is running under a user account then the certificate is typically in `CurrentUser`.</span></span> <span data-ttu-id="d1bce-162">既定値は `CurrentUser` です。</span><span class="sxs-lookup"><span data-stu-id="d1bce-162">The default is `CurrentUser`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d1bce-163">子要素</span><span class="sxs-lookup"><span data-stu-id="d1bce-163">Child Elements</span></span>  
 <span data-ttu-id="d1bce-164">なし。</span><span class="sxs-lookup"><span data-stu-id="d1bce-164">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d1bce-165">親要素</span><span class="sxs-lookup"><span data-stu-id="d1bce-165">Parent Elements</span></span>  
  
|<span data-ttu-id="d1bce-166">要素</span><span class="sxs-lookup"><span data-stu-id="d1bce-166">Element</span></span>|<span data-ttu-id="d1bce-167">説明</span><span class="sxs-lookup"><span data-stu-id="d1bce-167">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d1bce-168">\<peer></span><span class="sxs-lookup"><span data-stu-id="d1bce-168">\<peer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-clientcredentials-element.md)|<span data-ttu-id="d1bce-169">ピア サービスに対するクライアントの認証に使用される資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="d1bce-169">Specifies a credential used for authenticating the client to a peer service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d1bce-170">Remarks</span><span class="sxs-lookup"><span data-stu-id="d1bce-170">Remarks</span></span>  
 <span data-ttu-id="d1bce-171">メッセージ認証を選択した場合は、この要素を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1bce-171">This element must be configured if message authentication is chosen.</span></span> <span data-ttu-id="d1bce-172">によって提供される証明書を使用して出力チャネルでは、各メッセージが署名されて[\<証明書 >](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-element.md)します。</span><span class="sxs-lookup"><span data-stu-id="d1bce-172">For output channels, each message is signed using the certificate provided by [\<certificate>](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-element.md).</span></span> <span data-ttu-id="d1bce-173">すべてのメッセージは、アプリケーションに配信される前に、この要素の `customCertificateValidatorType` 属性で指定した検証を使用してメッセージ資格情報がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="d1bce-173">All messages, before delivered to the application, are checked against the message credential using the validator specified by the `customCertificateValidatorType` attribute of this element.</span></span> <span data-ttu-id="d1bce-174">検証は、資格情報を受け入れることも拒否することもできます。</span><span class="sxs-lookup"><span data-stu-id="d1bce-174">The validator can either accept or reject the credential.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d1bce-175">例</span><span class="sxs-lookup"><span data-stu-id="d1bce-175">Example</span></span>  
 <span data-ttu-id="d1bce-176">次のコードは、メッセージ送信者検証モードを `PeerOrChainTrust` に設定します。</span><span class="sxs-lookup"><span data-stu-id="d1bce-176">The following code sets the message sender validation mode to `PeerOrChainTrust`.</span></span>  
  
```xml  
<behaviors>  
 <endpointBehaviors>  
  <behavior name="MyEndpointBehavior">  
   <clientCredentials>  
    <peer>  
      <certificate findValue="www.contoso.com"   
                   storeLocation="LocalMachine"  
                   x509FindType="FindByIssuerName" />  
        <messageSenderAuthentication   
          certificateValidationMode="PeerOrChainTrust" />  
       <messageSenderAuthentication certificateValidationMode="None" />  
    </peer>  
   </clientCredentials>  
  </behavior>  
 </endpointBehaviors>  
```  
  
## <a name="see-also"></a><span data-ttu-id="d1bce-177">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1bce-177">See Also</span></span>  
 <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication>  
 <xref:System.ServiceModel.Security.PeerCredential.MessageSenderAuthentication%2A>  
 <xref:System.ServiceModel.Configuration.PeerCredentialElement.MessageSenderAuthentication%2A>  
 <xref:System.ServiceModel.Configuration.X509PeerCertificateAuthenticationElement>  
 [<span data-ttu-id="d1bce-178">証明書の使用</span><span class="sxs-lookup"><span data-stu-id="d1bce-178">Working with Certificates</span></span>](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 [<span data-ttu-id="d1bce-179">ピアツーピア ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d1bce-179">Peer-to-Peer Networking</span></span>](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)  
 [<span data-ttu-id="d1bce-180">ピア チャネル メッセージの認証</span><span class="sxs-lookup"><span data-stu-id="d1bce-180">Peer Channel Message Authentication</span></span>](https://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95)  
 [<span data-ttu-id="d1bce-181">ピア チャネル カスタム認証</span><span class="sxs-lookup"><span data-stu-id="d1bce-181">Peer Channel Custom Authentication</span></span>](https://msdn.microsoft.com/library/4aa8a82e-41a8-48e2-8621-7e1cbabdca7c)  
 [<span data-ttu-id="d1bce-182">セキュリティによるピア チャネル アプリケーションの保護</span><span class="sxs-lookup"><span data-stu-id="d1bce-182">Securing Peer Channel Applications</span></span>](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
