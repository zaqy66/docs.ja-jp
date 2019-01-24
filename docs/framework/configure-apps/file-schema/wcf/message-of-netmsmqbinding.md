---
title: '&lt;netMsmqBinding&gt; の &lt;message&gt;'
ms.date: 03/30/2017
ms.assetid: 6ebf0240-d7be-4493-b0fe-f00fd5989d77
ms.openlocfilehash: b636a22fe7c6bcfae5b8f81c1566ea39c9f8ced5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54683743"
---
# <a name="ltmessagegt-of-ltnetmsmqbindinggt"></a><span data-ttu-id="7a857-102">&lt;netMsmqBinding&gt; の &lt;message&gt;</span><span class="sxs-lookup"><span data-stu-id="7a857-102">&lt;message&gt; of &lt;netMsmqBinding&gt;</span></span>
<span data-ttu-id="7a857-103">この `netMsmqBinding` バインディングでの SOAP メッセージ セキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="7a857-103">Defines the SOAP message security settings on this `netMsmqBinding` binding.</span></span>  
  
 <span data-ttu-id="7a857-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="7a857-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="7a857-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="7a857-105">\<bindings></span></span>  
<span data-ttu-id="7a857-106">\<netMsmqBinding></span><span class="sxs-lookup"><span data-stu-id="7a857-106">\<netMsmqBinding></span></span>  
<span data-ttu-id="7a857-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="7a857-107">\<binding></span></span>  
<span data-ttu-id="7a857-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="7a857-108">\<security></span></span>  
<span data-ttu-id="7a857-109">\<message></span><span class="sxs-lookup"><span data-stu-id="7a857-109">\<message></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7a857-110">構文</span><span class="sxs-lookup"><span data-stu-id="7a857-110">Syntax</span></span>  
  
```xml  
<netMsmqBinding>
  <binding>
    <security>
      <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
               clientCredentialType="None/Windows/UserName/Certificate/CardSpace" />
    </security>
  </binding>
</netMsmqBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7a857-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="7a857-111">Attributes and Elements</span></span>  
 <span data-ttu-id="7a857-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a857-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7a857-113">属性</span><span class="sxs-lookup"><span data-stu-id="7a857-113">Attributes</span></span>  
  
|<span data-ttu-id="7a857-114">属性</span><span class="sxs-lookup"><span data-stu-id="7a857-114">Attribute</span></span>|<span data-ttu-id="7a857-115">説明</span><span class="sxs-lookup"><span data-stu-id="7a857-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="7a857-116">algorithmSuite</span><span class="sxs-lookup"><span data-stu-id="7a857-116">algorithmSuite</span></span>|<span data-ttu-id="7a857-117">MSMQ トランスポートを介して送信されるメッセージにメッセージ ベースのセキュリティを実現するために使用されるメッセージの暗号化およびキー ラップ アルゴリズムを設定します。</span><span class="sxs-lookup"><span data-stu-id="7a857-117">Sets the message encryption and key-wrap algorithms that are used to achieve message-based security for messages sent over MSMQ transport.</span></span><br /><br /> <span data-ttu-id="7a857-118">既定値は `Aes256` です。</span><span class="sxs-lookup"><span data-stu-id="7a857-118">The default value is `Aes256`.</span></span> <span data-ttu-id="7a857-119">この属性は <xref:System.ServiceModel.Security.SecurityAlgorithmSuite> 型です。</span><span class="sxs-lookup"><span data-stu-id="7a857-119">This attribute is of type <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>.</span></span>|  
|<span data-ttu-id="7a857-120">clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="7a857-120">clientCredentialType</span></span>|<span data-ttu-id="7a857-121">MSMQ トランスポートで送信されるメッセージに対してクライアント認証を実行するときに使用される資格情報の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="7a857-121">Specifies the type of credential to be used when performing client authentication for messages sent over the MSMQ transport.</span></span> <span data-ttu-id="7a857-122">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="7a857-122">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="7a857-123">-None。サービスが匿名クライアントと対話できるようになります。</span><span class="sxs-lookup"><span data-stu-id="7a857-123">-   None: This allows the service to interact with anonymous clients.</span></span> <span data-ttu-id="7a857-124">サービスとクライアントはいずれも資格情報を要求しません。</span><span class="sxs-lookup"><span data-stu-id="7a857-124">Neither the service nor the client requires a credential.</span></span><br /><span data-ttu-id="7a857-125">-Windows:これにより、SOAP 交換を Windows 資格情報の認証済みコンテキストの下にあることができます。</span><span class="sxs-lookup"><span data-stu-id="7a857-125">-   Windows: This enables the SOAP exchanges to be under the authenticated context of a Windows credential.</span></span> <span data-ttu-id="7a857-126">これは、常に Kerberos ベースの認証を実行します。</span><span class="sxs-lookup"><span data-stu-id="7a857-126">This always performs Kerberos-based authentication.</span></span><br /><span data-ttu-id="7a857-127">-ユーザー名:これにより、サービスを必要とする UserName 資格情報を使用してクライアントを認証します。</span><span class="sxs-lookup"><span data-stu-id="7a857-127">-   UserName: This enables the service to require that the client be authenticated using a UserName credential.</span></span> <span data-ttu-id="7a857-128">この場合、資格情報を使用して指定する必要があります、`clientCredentials`動作**注意が必要です。** Windows Communication Foundation (WCF) は、パスワード ダイジェストの送信、またはパスワードを使用して、このようなキーを使用して、メッセージ セキュリティのためのキーの派生をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="7a857-128">The credential in this case needs to be specified using the `clientCredentials` behavior **Caution:**  Windows Communication Foundation (WCF) does not support sending a password digest or deriving keys using password and using such keys for message security.</span></span> <span data-ttu-id="7a857-129">そのため、WCF は、UserName 資格情報を使用する場合、exchange がセキュリティで保護を適用します。</span><span class="sxs-lookup"><span data-stu-id="7a857-129">Therefore, WCF enforces that the exchange is secured when using UserName credentials.</span></span> <span data-ttu-id="7a857-130">このモードは、サービス証明書が、`clientCredential` 動作および `serviceCertificate` を使用してクライアント側で指定されることを要求します。</span><span class="sxs-lookup"><span data-stu-id="7a857-130">This mode requires that the service certificate be specified on the client side using `clientCredential` behavior and `serviceCertificate`.</span></span> <br /><br /> <span data-ttu-id="7a857-131">-証明書:これにより、必要とするサービス証明書を使用してクライアントを認証します。</span><span class="sxs-lookup"><span data-stu-id="7a857-131">-   Certificate: This enables the service to require that the client be authenticated using a certificate.</span></span> <span data-ttu-id="7a857-132">この場合のクライアント資格情報は、`clientCredentials` 動作を使用して指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a857-132">The client credential in this case needs to be specified using the `clientCredentials` behavior.</span></span> <span data-ttu-id="7a857-133">この場合のサービス資格情報は、`clientCredentials` を指定して `serviceCertificate` 動作を使用することで、指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a857-133">The service credential in this case needs to be specified using the `clientCredentials` behavior by specifying the `serviceCertificate`.</span></span><br /><span data-ttu-id="7a857-134">-CardSpace:これにより、サービスが要求、CardSpace を使用してクライアントを認証します。</span><span class="sxs-lookup"><span data-stu-id="7a857-134">-   CardSpace: This allows the service to require that the client be authenticated using a CardSpace.</span></span> <span data-ttu-id="7a857-135">`serviceCertiifcate` は、`clientCredential` 動作で提供される必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a857-135">The `serviceCertiifcate` must be provisioned in the `clientCredential` behavior.</span></span><br /><br /> <span data-ttu-id="7a857-136">既定値は `Windows` です。</span><span class="sxs-lookup"><span data-stu-id="7a857-136">The default value is `Windows`.</span></span> <span data-ttu-id="7a857-137">この属性は <xref:System.ServiceModel.MessageCredentialType> 型です。</span><span class="sxs-lookup"><span data-stu-id="7a857-137">This attribute is of type <xref:System.ServiceModel.MessageCredentialType>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7a857-138">子要素</span><span class="sxs-lookup"><span data-stu-id="7a857-138">Child Elements</span></span>  
 <span data-ttu-id="7a857-139">なし</span><span class="sxs-lookup"><span data-stu-id="7a857-139">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7a857-140">親要素</span><span class="sxs-lookup"><span data-stu-id="7a857-140">Parent Elements</span></span>  
  
|<span data-ttu-id="7a857-141">要素</span><span class="sxs-lookup"><span data-stu-id="7a857-141">Element</span></span>|<span data-ttu-id="7a857-142">説明</span><span class="sxs-lookup"><span data-stu-id="7a857-142">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7a857-143">\<security></span><span class="sxs-lookup"><span data-stu-id="7a857-143">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netmsmqbinding.md)|<span data-ttu-id="7a857-144">バインディングのセキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="7a857-144">Defines the security settings for a binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7a857-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a857-145">See also</span></span>
- <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement>
- <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement.Message%2A>
- <xref:System.ServiceModel.NetMsmqSecurity.Message%2A>
- <xref:System.ServiceModel.MessageSecurityOverMsmq>
- [<span data-ttu-id="7a857-146">WCF のキュー</span><span class="sxs-lookup"><span data-stu-id="7a857-146">Queues in WCF</span></span>](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)
- [<span data-ttu-id="7a857-147">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="7a857-147">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="7a857-148">バインディング</span><span class="sxs-lookup"><span data-stu-id="7a857-148">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="7a857-149">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="7a857-149">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="7a857-150">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="7a857-150">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="7a857-151">\<binding></span><span class="sxs-lookup"><span data-stu-id="7a857-151">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
