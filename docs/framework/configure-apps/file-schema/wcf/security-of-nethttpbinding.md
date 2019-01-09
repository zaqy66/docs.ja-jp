---
title: '&lt;netHttpBinding&gt; の &lt;security'
ms.date: 03/30/2017
ms.assetid: dc41f6f7-cabc-4a64-9fa0-ceabf861b348
ms.openlocfilehash: a03553c5afe78b3f95526411b8187464da08161b
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149691"
---
# <a name="ltsecuritygt-of-ltnethttpbinding"></a><span data-ttu-id="29636-102">&lt;netHttpBinding&gt; の &lt;security</span><span class="sxs-lookup"><span data-stu-id="29636-102">&lt;security&gt; of &lt;netHttpBinding</span></span>
<span data-ttu-id="29636-103">セキュリティ機能を定義、 [ \<basicHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="29636-103">Defines the security capabilities of the [\<basicHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span></span>  
  
<span data-ttu-id="29636-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="29636-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="29636-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="29636-105">\<bindings></span></span>  
<span data-ttu-id="29636-106">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="29636-106">\<netHttpBinding></span></span>  
<span data-ttu-id="29636-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="29636-107">\<binding></span></span>  
<span data-ttu-id="29636-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="29636-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="29636-109">構文</span><span class="sxs-lookup"><span data-stu-id="29636-109">Syntax</span></span>  
  
```xml  
<security mode="Message/None/Transport/TransportWithCredential">
  <transport clientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"
             proxyCredentialType="Basic/Digest/None/Ntlm/Windows"
             realm="string" />
  <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
           clientCredentialType="Certificate/IssuedToken/None/UserName/Windows" />
</security>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="29636-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="29636-110">Attributes and Elements</span></span>  
 <span data-ttu-id="29636-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="29636-111">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="29636-112">属性</span><span class="sxs-lookup"><span data-stu-id="29636-112">Attributes</span></span>  
  
|<span data-ttu-id="29636-113">属性</span><span class="sxs-lookup"><span data-stu-id="29636-113">Attribute</span></span>|<span data-ttu-id="29636-114">説明</span><span class="sxs-lookup"><span data-stu-id="29636-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="29636-115">モード</span><span class="sxs-lookup"><span data-stu-id="29636-115">mode</span></span>|<span data-ttu-id="29636-116">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="29636-116">Optional.</span></span> <span data-ttu-id="29636-117">使用されるセキュリティの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="29636-117">Specifies the type of security that is used.</span></span> <span data-ttu-id="29636-118">既定値は、`None` です。</span><span class="sxs-lookup"><span data-stu-id="29636-118">The default is `None`.</span></span> <span data-ttu-id="29636-119">この属性は <xref:System.ServiceModel.BasicHttpSecurityMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="29636-119">This attribute is of type <xref:System.ServiceModel.BasicHttpSecurityMode>.</span></span>|
  
## <a name="mode-attribute"></a><span data-ttu-id="29636-120">mode 属性</span><span class="sxs-lookup"><span data-stu-id="29636-120">mode Attribute</span></span>  
  
|<span data-ttu-id="29636-121">値</span><span class="sxs-lookup"><span data-stu-id="29636-121">Value</span></span>|<span data-ttu-id="29636-122">説明</span><span class="sxs-lookup"><span data-stu-id="29636-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="29636-123">なし</span><span class="sxs-lookup"><span data-stu-id="29636-123">None</span></span>|<span data-ttu-id="29636-124">メッセージの数は、転送中にセキュリティ保護されません。</span><span class="sxs-lookup"><span data-stu-id="29636-124">-   Messages are not secured during transfer.</span></span>|  
|<span data-ttu-id="29636-125">Transport</span><span class="sxs-lookup"><span data-stu-id="29636-125">Transport</span></span>|<span data-ttu-id="29636-126">セキュリティは、HTTPS トランスポートを使用して提供されます。</span><span class="sxs-lookup"><span data-stu-id="29636-126">Security is provided using HTTPS transport.</span></span> <span data-ttu-id="29636-127">SOAP メッセージは、HTTPS を使用したセキュリティで保護されます。</span><span class="sxs-lookup"><span data-stu-id="29636-127">The SOAP messages are secured using HTTPS.</span></span> <span data-ttu-id="29636-128">サービスは、サービスの X.509 証明書を使用してクライアントに認証されます。</span><span class="sxs-lookup"><span data-stu-id="29636-128">The service is authenticated to the client using the service's X.509 certificate.</span></span> <span data-ttu-id="29636-129">クライアントは、提供される ClientCredentialType を使用して認証されます。</span><span class="sxs-lookup"><span data-stu-id="29636-129">The client is authenticated using the ClientCredentialType supplied.</span></span>|  
|<span data-ttu-id="29636-130">メッセージ</span><span class="sxs-lookup"><span data-stu-id="29636-130">Message</span></span>|<span data-ttu-id="29636-131">セキュリティは、SOAP メッセージ セキュリティを使用して確保されます。</span><span class="sxs-lookup"><span data-stu-id="29636-131">Security is provided using SOAP message security.</span></span> <span data-ttu-id="29636-132">既定では、本文は暗号化および署名されます。</span><span class="sxs-lookup"><span data-stu-id="29636-132">By default, the body is encrypted and signed.</span></span> <span data-ttu-id="29636-133">このバインディングの場合、サーバー証明書をクライアントの帯域外で提供するように要求されます。</span><span class="sxs-lookup"><span data-stu-id="29636-133">For this binding, the system requires that the server certificate be provided to the client out of band.</span></span> <span data-ttu-id="29636-134">このバインディングの唯一の有効な `ClientCredentialType` は、`Certificate` です。</span><span class="sxs-lookup"><span data-stu-id="29636-134">The only valid `ClientCredentialType` for this binding is `Certificate`.</span></span>|  
|<span data-ttu-id="29636-135">TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="29636-135">TransportWithMessageCredential</span></span>|<span data-ttu-id="29636-136">整合性、機密性、およびサーバー認証は、トランスポート セキュリティによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="29636-136">Integrity, confidentiality and server authentication are provided by transport security.</span></span> <span data-ttu-id="29636-137">クライアント認証は、SOAP メッセージ セキュリティで提供されます。</span><span class="sxs-lookup"><span data-stu-id="29636-137">Client authentication is provided by means of SOAP message security.</span></span> <span data-ttu-id="29636-138">このモードは、ユーザーがユーザー名およびパスワードを使用して認証し、メッセージ転送をセキュリティで保護するために既存の HTTP が配置されている場合に関連します。</span><span class="sxs-lookup"><span data-stu-id="29636-138">This mode is relevant when the user is authenticating using username/password and there is an existing HTTP deployment for securing message transfer.</span></span>|  
|<span data-ttu-id="29636-139">TransportCredentialOnly</span><span class="sxs-lookup"><span data-stu-id="29636-139">TransportCredentialOnly</span></span>|<span data-ttu-id="29636-140">このモードは、メッセージの整合性と機密性を提供しません。</span><span class="sxs-lookup"><span data-stu-id="29636-140">This mode does not provide message integrity and confidentiality.</span></span> <span data-ttu-id="29636-141">http ベースのクライアント認証を提供します。</span><span class="sxs-lookup"><span data-stu-id="29636-141">It provides http-based client authentication.</span></span> <span data-ttu-id="29636-142">このモードを使用するときは、十分に注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29636-142">This mode should be used with caution.</span></span> <span data-ttu-id="29636-143">これは、トランスポート セキュリティ (IPSec) などの他の方法で提供されるされ、クライアント認証だけが、WCF インフラストラクチャによって提供される環境で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29636-143">It should be used in environments where the transport security is being provided by other means (such as IPSec) and only client authentication is provided by the WCF infrastructure.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="29636-144">子要素</span><span class="sxs-lookup"><span data-stu-id="29636-144">Child Elements</span></span>  
  
|<span data-ttu-id="29636-145">要素</span><span class="sxs-lookup"><span data-stu-id="29636-145">Element</span></span>|<span data-ttu-id="29636-146">説明</span><span class="sxs-lookup"><span data-stu-id="29636-146">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="29636-147">\<transport></span><span class="sxs-lookup"><span data-stu-id="29636-147">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-nethttpbinding.md)|<span data-ttu-id="29636-148">基本 HTTP サービスのトランスポート セキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="29636-148">Defines the transport security settings for a basic HTTP service.</span></span> <span data-ttu-id="29636-149">この要素は、<xref:System.ServiceModel.HttpTransportSecurity> に対応しています。</span><span class="sxs-lookup"><span data-stu-id="29636-149">This element corresponds to <xref:System.ServiceModel.HttpTransportSecurity>.</span></span>|  
|[<span data-ttu-id="29636-150">\<message></span><span class="sxs-lookup"><span data-stu-id="29636-150">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-of-nethttpbinding.md)|<span data-ttu-id="29636-151">基本 HTTP サービスのメッセージ セキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="29636-151">Defines the message security settings for a basic HTTP service.</span></span> <span data-ttu-id="29636-152">この要素に対応して<!--zz <xref:System.ServiceModel.NetHttpMessageSecurity> -->`System.ServiceModel.NetHttpMessageSecurity`します。</span><span class="sxs-lookup"><span data-stu-id="29636-152">This element corresponds to <!--zz <xref:System.ServiceModel.NetHttpMessageSecurity> --> `System.ServiceModel.NetHttpMessageSecurity`.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="29636-153">親要素</span><span class="sxs-lookup"><span data-stu-id="29636-153">Parent Elements</span></span>  
  
|<span data-ttu-id="29636-154">要素</span><span class="sxs-lookup"><span data-stu-id="29636-154">Element</span></span>|<span data-ttu-id="29636-155">説明</span><span class="sxs-lookup"><span data-stu-id="29636-155">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="29636-156">バインド</span><span class="sxs-lookup"><span data-stu-id="29636-156">binding</span></span>|<span data-ttu-id="29636-157">バインド要素、 [ \<basicHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="29636-157">The binding element of the [\<basicHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="29636-158">Remarks</span><span class="sxs-lookup"><span data-stu-id="29636-158">Remarks</span></span>  
 <span data-ttu-id="29636-159">既定では、SOAP メッセージはセキュリティで保護されず、クライアントは認証されません。</span><span class="sxs-lookup"><span data-stu-id="29636-159">By default, the SOAP message is not secured and the client is not authenticated.</span></span> <span data-ttu-id="29636-160">この要素を使用すると、`netHttpBinding` 要素に追加のセキュリティ設定を構成できます。</span><span class="sxs-lookup"><span data-stu-id="29636-160">This element enables you to configure additional security settings for the `netHttpBinding` element.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="29636-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="29636-161">See Also</span></span>  
 <xref:System.ServiceModel.NetHttpBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.NetHttpBindingElement.Security%2A>    
 [<span data-ttu-id="29636-162">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="29636-162">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="29636-163">資格情報の種類の選択</span><span class="sxs-lookup"><span data-stu-id="29636-163">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)  
 [<span data-ttu-id="29636-164">バインディング</span><span class="sxs-lookup"><span data-stu-id="29636-164">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="29636-165">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="29636-165">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="29636-166">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="29636-166">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="29636-167">\<binding></span><span class="sxs-lookup"><span data-stu-id="29636-167">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
