---
title: '&lt;certificate&gt; 要素'
ms.date: 03/30/2017
ms.assetid: 9b3d9233-ef35-477a-bf5d-efd1e80a52f4
ms.openlocfilehash: 5329fb276766ca2bd24f0fd3aef793fbb3b1f8b8
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43515396"
---
# <a name="ltcertificategt-element"></a><span data-ttu-id="38492-102">&lt;certificate&gt; 要素</span><span class="sxs-lookup"><span data-stu-id="38492-102">&lt;certificate&gt; Element</span></span>
<span data-ttu-id="38492-103">ピアツーピア クライアントのメッセージの署名と暗号化に使用する X.509 証明書を指定します。</span><span class="sxs-lookup"><span data-stu-id="38492-103">Specifies an X.509 certificate to use for signing and encrypting messages for peer-to-peer clients.</span></span>  
  
 <span data-ttu-id="38492-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="38492-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="38492-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="38492-105">\<behaviors></span></span>  
<span data-ttu-id="38492-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="38492-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="38492-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="38492-107">\<behavior></span></span>  
<span data-ttu-id="38492-108">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="38492-108">\<clientCredentials></span></span>  
<span data-ttu-id="38492-109">\<ピア ></span><span class="sxs-lookup"><span data-stu-id="38492-109">\<peer></span></span>  
<span data-ttu-id="38492-110">\<証明書 ></span><span class="sxs-lookup"><span data-stu-id="38492-110">\<certificate></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="38492-111">構文</span><span class="sxs-lookup"><span data-stu-id="38492-111">Syntax</span></span>  
  
```xml  
<certificate findValue="String"   
  
storeLocation="LocalMachine/CurrentUser"  
      storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"  
      X509FindType="FindByThumbPrint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="38492-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="38492-112">Attributes and Elements</span></span>  
 <span data-ttu-id="38492-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="38492-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="38492-114">属性</span><span class="sxs-lookup"><span data-stu-id="38492-114">Attributes</span></span>  
  
|<span data-ttu-id="38492-115">属性</span><span class="sxs-lookup"><span data-stu-id="38492-115">Attribute</span></span>|<span data-ttu-id="38492-116">説明</span><span class="sxs-lookup"><span data-stu-id="38492-116">Description</span></span>|  
|---------------|-----------------|  
|`findValue`|<span data-ttu-id="38492-117">X.509 証明書ストアで検索する値を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="38492-117">A string that contains the value to search for in the X.509 certificate store.</span></span> <span data-ttu-id="38492-118">属性に格納されている型は、指定された `x509FindType` の要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="38492-118">The type contained in the attribute must satisfy the requirements of the specified `x509FindType`.</span></span> <span data-ttu-id="38492-119">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="38492-119">The default is an empty string.</span></span>|  
|`storeLocation`|<span data-ttu-id="38492-120">クライアントがピアの証明書の検証に使用する X.509 証明書ストアの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="38492-120">Specifies the location of the X.509 certificate store that the client uses to validate the peer's certificate against.</span></span> <span data-ttu-id="38492-121">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="38492-121">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="38492-122">-LocalMachine: ローカル マシンに割り当てられている証明書ストア。</span><span class="sxs-lookup"><span data-stu-id="38492-122">-   LocalMachine: the certificate store assigned to the local machine.</span></span><br /><span data-ttu-id="38492-123">-CurrentUser: 現在のユーザーに割り当てられている証明書ストア。</span><span class="sxs-lookup"><span data-stu-id="38492-123">-   CurrentUser: the certificate store assigned to the current user.</span></span><br /><br /> <span data-ttu-id="38492-124">既定は LocalMachine です。</span><span class="sxs-lookup"><span data-stu-id="38492-124">The default is LocalMachine.</span></span>|  
|`storeName`|<span data-ttu-id="38492-125">開く X.509 証明書ストアの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="38492-125">Specifies the name of the X.509 certificate store to open.</span></span> <span data-ttu-id="38492-126">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="38492-126">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="38492-127">-AddressBook: 他のユーザー証明書ストア。</span><span class="sxs-lookup"><span data-stu-id="38492-127">-   AddressBook: Certificate store for other users.</span></span><br /><span data-ttu-id="38492-128">-AuthRoot: サードパーティ証明機関 (Ca) のストアの証明書します。</span><span class="sxs-lookup"><span data-stu-id="38492-128">-   AuthRoot: Certificate store for third-party certification authorities (CAs).</span></span><br /><span data-ttu-id="38492-129">-CertificateAuthority: 中間証明機関 (Ca) 証明書ストア。</span><span class="sxs-lookup"><span data-stu-id="38492-129">-   CertificateAuthority: Certificate store for intermediate certification authorities (CAs).</span></span><br /><span data-ttu-id="38492-130">-許可されていません。 証明書失効した証明書ストア。</span><span class="sxs-lookup"><span data-stu-id="38492-130">-   Disallowed: Certificate store for revoked certificates.</span></span><br /><span data-ttu-id="38492-131">-個人用証明書の証明書ストアが my: です。</span><span class="sxs-lookup"><span data-stu-id="38492-131">-   My: Certificate store for personal certificates.</span></span><br /><span data-ttu-id="38492-132">Root: 信頼されたルート証明機関 (Ca) 証明書ストア。</span><span class="sxs-lookup"><span data-stu-id="38492-132">-   Root: Certificate store for trusted root certification authorities (CAs).</span></span><br /><span data-ttu-id="38492-133">-証明書ストアを TrustedPeople: 直接信頼されたユーザーやリソース。</span><span class="sxs-lookup"><span data-stu-id="38492-133">-   TrustedPeople: Certificate store for directly-trusted people and resources.</span></span><br /><span data-ttu-id="38492-134">-TrustedPublisher: 直接信頼された発行元証明書ストア。</span><span class="sxs-lookup"><span data-stu-id="38492-134">-   TrustedPublisher: Certificate store for directly-trusted publishers.</span></span><br /><br /> <span data-ttu-id="38492-135">既定値は My です。</span><span class="sxs-lookup"><span data-stu-id="38492-135">The default is My.</span></span>|  
|`X509FindType`|<span data-ttu-id="38492-136">実行する X.509 検索の種類を定義します。</span><span class="sxs-lookup"><span data-stu-id="38492-136">Defines the type of X.509 search to be executed.</span></span> <span data-ttu-id="38492-137">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="38492-137">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="38492-138">-FindByThumbPrint</span><span class="sxs-lookup"><span data-stu-id="38492-138">-   FindByThumbPrint</span></span><br /><span data-ttu-id="38492-139">-   FindBySubjectName</span><span class="sxs-lookup"><span data-stu-id="38492-139">-   FindBySubjectName</span></span><br /><span data-ttu-id="38492-140">-FindBySubjectDistinguishedName</span><span class="sxs-lookup"><span data-stu-id="38492-140">-   FindBySubjectDistinguishedName</span></span><br /><span data-ttu-id="38492-141">-   FindByIssuerName</span><span class="sxs-lookup"><span data-stu-id="38492-141">-   FindByIssuerName</span></span><br /><span data-ttu-id="38492-142">-FindByIssuerDistinguishedName</span><span class="sxs-lookup"><span data-stu-id="38492-142">-   FindByIssuerDistinguishedName</span></span><br /><span data-ttu-id="38492-143">-   FindBySerialNumber</span><span class="sxs-lookup"><span data-stu-id="38492-143">-   FindBySerialNumber</span></span><br /><span data-ttu-id="38492-144">-   FindByTimeValid</span><span class="sxs-lookup"><span data-stu-id="38492-144">-   FindByTimeValid</span></span><br /><span data-ttu-id="38492-145">-   FindByTimeNotYetValid</span><span class="sxs-lookup"><span data-stu-id="38492-145">-   FindByTimeNotYetValid</span></span><br /><span data-ttu-id="38492-146">-   FindByTemplateName</span><span class="sxs-lookup"><span data-stu-id="38492-146">-   FindByTemplateName</span></span><br /><span data-ttu-id="38492-147">-   FindByApplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="38492-147">-   FindByApplicationPolicy</span></span><br /><span data-ttu-id="38492-148">-FindByCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="38492-148">-   FindByCertificatePolicy</span></span><br /><span data-ttu-id="38492-149">-FindByExtension</span><span class="sxs-lookup"><span data-stu-id="38492-149">-   FindByExtension</span></span><br /><span data-ttu-id="38492-150">-   FindByKeyUsage</span><span class="sxs-lookup"><span data-stu-id="38492-150">-   FindByKeyUsage</span></span><br /><span data-ttu-id="38492-151">-   FindBySubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="38492-151">-   FindBySubjectKeyIdentifier</span></span><br /><br /> <span data-ttu-id="38492-152">`findValue` 属性に格納されている型は、指定された `X509FindType` の要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="38492-152">The type contained in the `findValue` attribute must satisfy the requirements of the specified `X509FindType`.</span></span><br /><br /> <span data-ttu-id="38492-153">既定値は FindBySubjectDistinguishedName です。</span><span class="sxs-lookup"><span data-stu-id="38492-153">The default value is FindBySubjectDistinguishedName.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="38492-154">子要素</span><span class="sxs-lookup"><span data-stu-id="38492-154">Child Elements</span></span>  
 <span data-ttu-id="38492-155">なし。</span><span class="sxs-lookup"><span data-stu-id="38492-155">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="38492-156">親要素</span><span class="sxs-lookup"><span data-stu-id="38492-156">Parent Elements</span></span>  
  
|<span data-ttu-id="38492-157">要素</span><span class="sxs-lookup"><span data-stu-id="38492-157">Element</span></span>|<span data-ttu-id="38492-158">説明</span><span class="sxs-lookup"><span data-stu-id="38492-158">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="38492-159">\<peer></span><span class="sxs-lookup"><span data-stu-id="38492-159">\<peer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-clientcredentials-element.md)|<span data-ttu-id="38492-160">ピアツーピア クライアントの認証時に使用される資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="38492-160">Specifies credentials used when authenticating peer-to-peer clients.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="38492-161">Remarks</span><span class="sxs-lookup"><span data-stu-id="38492-161">Remarks</span></span>  
 <span data-ttu-id="38492-162">この構成要素には、ピア メッシュ内の近隣ノードを認証するときに使用される X509Certificate2 インスタンスが格納されます。</span><span class="sxs-lookup"><span data-stu-id="38492-162">This configuration element contains a X509Certificate2 instance used when authenticating neighbors in the peer mesh.</span></span>  
  
 <span data-ttu-id="38492-163">ピア ツー ピア プログラミングの詳細については、次を参照してください。[ピア ツー ピア ネットワー キング](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)します。</span><span class="sxs-lookup"><span data-stu-id="38492-163">For more information about peer-to-peer programming, see [Peer-to-Peer Networking](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="38492-164">例</span><span class="sxs-lookup"><span data-stu-id="38492-164">Example</span></span>  
 <span data-ttu-id="38492-165">次のコードは、ピアツーピア シナリオで使用される証明書の検索方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="38492-165">The following code specifies how to find the certificate used in a peer-to-peer scenario.</span></span>  
  
```xml  
<behaviors>  
 <endpointBehaviors>  
  <behavior name="MyEndpointBehavior">  
   <clientCredentials>  
    <peer>  
     <certificate findValue="www.contoso.com"   
                   storeLocation="LocalMachine"  
                   x509FindType="FindByIssuerName" />  
    </peer>  
   </clientCredentials>  
  </behavior>  
</endpointBehaviors>  
```  
  
## <a name="see-also"></a><span data-ttu-id="38492-166">関連項目</span><span class="sxs-lookup"><span data-stu-id="38492-166">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PeerCredentialElement>  
 <xref:System.ServiceModel.Configuration.PeerCredentialElement.Certificate%2A>  
 <xref:System.ServiceModel.Configuration.X509PeerCertificateElement>  
 <xref:System.ServiceModel.Security.PeerCredential.Certificate%2A>  
 [<span data-ttu-id="38492-167">証明書の使用</span><span class="sxs-lookup"><span data-stu-id="38492-167">Working with Certificates</span></span>](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 [<span data-ttu-id="38492-168">ピアツーピア ネットワーク</span><span class="sxs-lookup"><span data-stu-id="38492-168">Peer-to-Peer Networking</span></span>](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)  
 [<span data-ttu-id="38492-169">ピア チャネル メッセージの認証</span><span class="sxs-lookup"><span data-stu-id="38492-169">Peer Channel Message Authentication</span></span>](https://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95)  
 [<span data-ttu-id="38492-170">ピア チャネル カスタム認証</span><span class="sxs-lookup"><span data-stu-id="38492-170">Peer Channel Custom Authentication</span></span>](https://msdn.microsoft.com/library/4aa8a82e-41a8-48e2-8621-7e1cbabdca7c)  
 [<span data-ttu-id="38492-171">セキュリティによるピア チャネル アプリケーションの保護</span><span class="sxs-lookup"><span data-stu-id="38492-171">Securing Peer Channel Applications</span></span>](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
