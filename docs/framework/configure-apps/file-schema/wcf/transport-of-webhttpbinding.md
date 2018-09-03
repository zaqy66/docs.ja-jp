---
title: '&lt;webHttpBinding&gt; の &lt;transport&gt;'
ms.date: 03/30/2017
ms.assetid: f150fb19-7de1-44af-81f4-86cad881cd05
ms.openlocfilehash: bbbd459e5717722359fe010a27e548d21ff074db
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2018
ms.locfileid: "43482678"
---
# <a name="lttransportgt-of-ltwebhttpbindinggt"></a><span data-ttu-id="ae314-102">&lt;webHttpBinding&gt; の &lt;transport&gt;</span><span class="sxs-lookup"><span data-stu-id="ae314-102">&lt;transport&gt; of &lt;webHttpBinding&gt;</span></span>
<span data-ttu-id="ae314-103">HTTP 要求を受信するように構成されたサービス エンドポイントのトランスポート レベルのセキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="ae314-103">Defines the transport-level security settings for a service endpoint configured to receive HTTP requests.</span></span>  
  
 <span data-ttu-id="ae314-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="ae314-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="ae314-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="ae314-105">\<bindings></span></span>  
<span data-ttu-id="ae314-106">\<webHttpBinding></span><span class="sxs-lookup"><span data-stu-id="ae314-106">\<webHttpBinding></span></span>  
<span data-ttu-id="ae314-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="ae314-107">\<binding></span></span>  
<span data-ttu-id="ae314-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="ae314-108">\<security></span></span>  
<span data-ttu-id="ae314-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="ae314-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae314-110">構文</span><span class="sxs-lookup"><span data-stu-id="ae314-110">Syntax</span></span>  
  
```xml  
<webHttpBinding>  
    <binding>  
        <security  
        mode="None|Transport|Message|TransportWithMessageCredential|TransportCredentialOnly">  
            <transport clientCredentialType="None|Basic|Digest|Ntlm|Windows"  
             proxyCredentialType="None|Basic|Digest|Ntlm|Windows" realm="string" >  
                <extendedProtectionPolicy  
                     policyEnforcement="Never|WhenSupported|Always"  
                     protectionScenario="TransportSelected|TrustedProxy">  
                    <customServiceNames></customServiceNames>  
                        </extendedProtectionPolicy>  
            </transport>  
        </security>  
    </binding>  
</WebHttpBinding>  
```  
  
## <a name="type"></a><span data-ttu-id="ae314-111">型</span><span class="sxs-lookup"><span data-stu-id="ae314-111">Type</span></span>  
 <xref:System.ServiceModel.HttpTransportSecurity>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ae314-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="ae314-112">Attributes and Elements</span></span>  
 <span data-ttu-id="ae314-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="ae314-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ae314-114">属性</span><span class="sxs-lookup"><span data-stu-id="ae314-114">Attributes</span></span>  
  
|<span data-ttu-id="ae314-115">属性</span><span class="sxs-lookup"><span data-stu-id="ae314-115">Attribute</span></span>|<span data-ttu-id="ae314-116">説明</span><span class="sxs-lookup"><span data-stu-id="ae314-116">Description</span></span>|  
|---------------|-----------------|  
|`clientCredentialType`|<span data-ttu-id="ae314-117">サービスに対するクライアントの認証に使用される資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae314-117">Specifies the credential used to authenticate the client to the service.</span></span> <span data-ttu-id="ae314-118">この属性は <xref:System.ServiceModel.HttpClientCredentialType> 型です。</span><span class="sxs-lookup"><span data-stu-id="ae314-118">This attribute is of type <xref:System.ServiceModel.HttpClientCredentialType>.</span></span>|  
|`proxyCredentialType`|<span data-ttu-id="ae314-119">ドメイン プロキシに対するクライアントの認証に使用される資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae314-119">Specifies the credential used to authenticate the client to a domain proxy.</span></span> <span data-ttu-id="ae314-120">この属性は <xref:System.ServiceModel.HttpProxyCredentialType> 型です。</span><span class="sxs-lookup"><span data-stu-id="ae314-120">This attribute is of type <xref:System.ServiceModel.HttpProxyCredentialType>.</span></span>|  
|`realm`|<span data-ttu-id="ae314-121">ダイジェストまたは基本認証の認証レルムを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="ae314-121">A string that specifies the authentication realm for digest or basic authentication.</span></span> <span data-ttu-id="ae314-122">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="ae314-122">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="ae314-123">認証レルムでは、少なくとも、認証を実行するホストの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae314-123">An authentication realm specifies at least the name of the host that performs the authentication.</span></span> <span data-ttu-id="ae314-124">アクセス権のあるユーザーのコレクションも指定できます。</span><span class="sxs-lookup"><span data-stu-id="ae314-124">It can also specify a collection of users that has access.</span></span> <span data-ttu-id="ae314-125">ユーザーは、認証レルムを照会して、複数のユーザー名およびパスワードの候補のうち、どれを使用できるかを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="ae314-125">A user can query the authentication realm to ascertain which one of the several possible usernames and passwords can be used.</span></span>|  
|`policyEnforcement`|<span data-ttu-id="ae314-126">この列挙体は、<xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> を適用するタイミングを指定します。</span><span class="sxs-lookup"><span data-stu-id="ae314-126">This enumeration specifies when the <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> should be enforced.</span></span><br /><br /> <span data-ttu-id="ae314-127">1.Never – ポリシーが適用されることはありません (拡張保護は無効になります)。</span><span class="sxs-lookup"><span data-stu-id="ae314-127">1.  Never – The policy is never enforced (Extended Protection is disabled).</span></span><br /><span data-ttu-id="ae314-128">2.WhenSupported – ポリシーが適用されるのは、クライアントが拡張保護をサポートしている場合のみです。</span><span class="sxs-lookup"><span data-stu-id="ae314-128">2.  WhenSupported – The policy is enforced only if the client supports Extended Protection.</span></span><br /><span data-ttu-id="ae314-129">3.Always – ポリシーは常に適用されます。</span><span class="sxs-lookup"><span data-stu-id="ae314-129">3.  Always – The policy is always enforced.</span></span> <span data-ttu-id="ae314-130">拡張保護をサポートしていないクライアントは認証に失敗します。</span><span class="sxs-lookup"><span data-stu-id="ae314-130">Clients which don’t support Extended Protection will fail to authenticate.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="ae314-131">clientCredentialType 属性</span><span class="sxs-lookup"><span data-stu-id="ae314-131">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="ae314-132">値</span><span class="sxs-lookup"><span data-stu-id="ae314-132">Value</span></span>|<span data-ttu-id="ae314-133">説明</span><span class="sxs-lookup"><span data-stu-id="ae314-133">Description</span></span>|  
|-----------|-----------------|  
|`None`|<span data-ttu-id="ae314-134">セキュリティを無効にします。</span><span class="sxs-lookup"><span data-stu-id="ae314-134">Security is disabled.</span></span>|  
|`Basic`|<span data-ttu-id="ae314-135">基本認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae314-135">Uses basic authentication.</span></span>|  
|`Certificate`|<span data-ttu-id="ae314-136">X.509 証明書を使用して、クライアントを認証します。</span><span class="sxs-lookup"><span data-stu-id="ae314-136">Uses X.509 certificates to authenticate the client.</span></span>|  
|`Digest`|<span data-ttu-id="ae314-137">ダイジェスト認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae314-137">Uses digest authentication.</span></span>|  
|`Ntlm`|<span data-ttu-id="ae314-138">Windows ドメインのフォールバックとして NTLM 認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae314-138">Uses NTLM authentication as a fallback with a Windows domain.</span></span>|  
|`Windows`|<span data-ttu-id="ae314-139">統合 Windows 認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae314-139">Uses integrated Windows authentication.</span></span>|  
  
## <a name="proxycredentialtype-attribute"></a><span data-ttu-id="ae314-140">proxyCredentialType 属性</span><span class="sxs-lookup"><span data-stu-id="ae314-140">proxyCredentialType Attribute</span></span>  
  
|<span data-ttu-id="ae314-141">値</span><span class="sxs-lookup"><span data-stu-id="ae314-141">Value</span></span>|<span data-ttu-id="ae314-142">説明</span><span class="sxs-lookup"><span data-stu-id="ae314-142">Description</span></span>|  
|-----------|-----------------|  
|`None`|<span data-ttu-id="ae314-143">セキュリティを無効にします。</span><span class="sxs-lookup"><span data-stu-id="ae314-143">Security is disabled.</span></span>|  
|`Basic`|<span data-ttu-id="ae314-144">基本認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae314-144">Uses basic authentication.</span></span>|  
|`Digest`|<span data-ttu-id="ae314-145">ダイジェスト認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae314-145">Uses digest authentication.</span></span>|  
|`Ntlm`|<span data-ttu-id="ae314-146">Windows ドメインのフォールバックとして NTLM を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae314-146">Uses NTLM as a fallback with a Windows domain.</span></span>|  
|`Windows`|<span data-ttu-id="ae314-147">統合 Windows 認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae314-147">Uses integrated Windows authentication.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ae314-148">子要素</span><span class="sxs-lookup"><span data-stu-id="ae314-148">Child Elements</span></span>  
 <span data-ttu-id="ae314-149">なし。</span><span class="sxs-lookup"><span data-stu-id="ae314-149">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ae314-150">親要素</span><span class="sxs-lookup"><span data-stu-id="ae314-150">Parent Elements</span></span>  
  
|<span data-ttu-id="ae314-151">要素</span><span class="sxs-lookup"><span data-stu-id="ae314-151">Element</span></span>|<span data-ttu-id="ae314-152">説明</span><span class="sxs-lookup"><span data-stu-id="ae314-152">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ae314-153">\<security></span><span class="sxs-lookup"><span data-stu-id="ae314-153">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-webhttpbinding.md)|<span data-ttu-id="ae314-154">セキュリティ機能を表す、 [ \<wsHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md)要素。</span><span class="sxs-lookup"><span data-stu-id="ae314-154">Represents the security capabilities of the [\<wsHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ae314-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae314-155">See Also</span></span>  
 <xref:System.ServiceModel.HttpTransportSecurity>  
 <xref:System.ServiceModel.Configuration.WebHttpSecurityElement.Transport%2A>  
 <xref:System.ServiceModel.WebHttpSecurity.Transport%2A>  
 <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement>  
 [<span data-ttu-id="ae314-156">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="ae314-156">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="ae314-157">バインディング</span><span class="sxs-lookup"><span data-stu-id="ae314-157">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="ae314-158">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="ae314-158">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="ae314-159">バインドを使用して、Windows Communication Foundation サービスとクライアントを構成するには</span><span class="sxs-lookup"><span data-stu-id="ae314-159">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="ae314-160">\<binding></span><span class="sxs-lookup"><span data-stu-id="ae314-160">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)  
 [<span data-ttu-id="ae314-161">WCF Web HTTP プログラミング モデル</span><span class="sxs-lookup"><span data-stu-id="ae314-161">WCF Web HTTP Programming Model</span></span>](../../../../../docs/framework/wcf/feature-details/wcf-web-http-programming-model.md)
