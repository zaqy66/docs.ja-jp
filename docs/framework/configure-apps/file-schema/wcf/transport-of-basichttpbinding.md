---
title: '&lt;basicHttpBinding&gt; の &lt;transport&gt;'
ms.date: 03/30/2017
ms.assetid: 4c5ba293-3d7e-47a6-b84e-e9022857b7e5
ms.openlocfilehash: f4e37281539106fef93dc4ab566d94d781c39d29
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2018
ms.locfileid: "48845676"
---
# <a name="lttransportgt-of-ltbasichttpbindinggt"></a><span data-ttu-id="0c084-102">&lt;basicHttpBinding&gt; の &lt;transport&gt;</span><span class="sxs-lookup"><span data-stu-id="0c084-102">&lt;transport&gt; of &lt;basicHttpBinding&gt;</span></span>
<span data-ttu-id="0c084-103">HTTP トランスポートの認証パラメーターを制御するプロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="0c084-103">Defines properties that control authentication parameters for the HTTP transport.</span></span>  
  
 <span data-ttu-id="0c084-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="0c084-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="0c084-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="0c084-105">\<bindings></span></span>  
<span data-ttu-id="0c084-106">\<basicHttpBinding></span><span class="sxs-lookup"><span data-stu-id="0c084-106">\<basicHttpBinding></span></span>  
<span data-ttu-id="0c084-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="0c084-107">\<binding></span></span>  
<span data-ttu-id="0c084-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="0c084-108">\<security></span></span>  
<span data-ttu-id="0c084-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="0c084-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c084-110">構文</span><span class="sxs-lookup"><span data-stu-id="0c084-110">Syntax</span></span>  
  
```xml  
<basicHttpBinding>  
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
</basicHttpBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0c084-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="0c084-111">Attributes and Elements</span></span>  
 <span data-ttu-id="0c084-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="0c084-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0c084-113">属性</span><span class="sxs-lookup"><span data-stu-id="0c084-113">Attributes</span></span>  
  
|<span data-ttu-id="0c084-114">属性</span><span class="sxs-lookup"><span data-stu-id="0c084-114">Attribute</span></span>|<span data-ttu-id="0c084-115">説明</span><span class="sxs-lookup"><span data-stu-id="0c084-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0c084-116">clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="0c084-116">clientCredentialType</span></span>|<span data-ttu-id="0c084-117">-HTTP 認証を使用してクライアント認証を実行するときに使用される資格情報の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c084-117">-   Specifies the type of credential to be used when performing client authentication using HTTP authentication.</span></span>  <span data-ttu-id="0c084-118">既定値は `None` です。</span><span class="sxs-lookup"><span data-stu-id="0c084-118">The default is `None`.</span></span> <span data-ttu-id="0c084-119">この属性は <xref:System.ServiceModel.HttpClientCredentialType> 型です。</span><span class="sxs-lookup"><span data-stu-id="0c084-119">This attribute is of type <xref:System.ServiceModel.HttpClientCredentialType>.</span></span>|  
|<span data-ttu-id="0c084-120">proxyCredentialType</span><span class="sxs-lookup"><span data-stu-id="0c084-120">proxyCredentialType</span></span>|<span data-ttu-id="0c084-121">-HTTP 経由でプロキシを使用してドメイン内からクライアント認証を実行するときに使用される資格情報の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c084-121">-   Specifies the type of credential to be used when performing client authentication from within a domain using a proxy over HTTP.</span></span> <span data-ttu-id="0c084-122">この属性は、親 `mode` 要素の `security` 属性が `Transport` または `TransportCredentialsOnly` の場合にだけ適用されます。</span><span class="sxs-lookup"><span data-stu-id="0c084-122">This attribute is applicable only when the `mode` attribute of the parent `security` element is `Transport` or `TransportCredentialsOnly`.</span></span> <span data-ttu-id="0c084-123">この属性は <xref:System.ServiceModel.HttpProxyCredentialType> 型です。</span><span class="sxs-lookup"><span data-stu-id="0c084-123">This attribute is of type <xref:System.ServiceModel.HttpProxyCredentialType>.</span></span>|  
|<span data-ttu-id="0c084-124">realm</span><span class="sxs-lookup"><span data-stu-id="0c084-124">realm</span></span>|<span data-ttu-id="0c084-125">ダイジェストまたは基本認証の HTTP 認証方式によって使用されるレルムを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="0c084-125">A string that specifies the realm that is used by the HTTP authentication scheme for digest or basic authentication.</span></span> <span data-ttu-id="0c084-126">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="0c084-126">The default is an empty string.</span></span>|  
|<span data-ttu-id="0c084-127">policyEnforcement</span><span class="sxs-lookup"><span data-stu-id="0c084-127">policyEnforcement</span></span>|<span data-ttu-id="0c084-128">この列挙体は、<xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> を適用するタイミングを指定します。</span><span class="sxs-lookup"><span data-stu-id="0c084-128">This enumeration specifies when the <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> should be enforced.</span></span><br /><br /> <span data-ttu-id="0c084-129">1.Never – ポリシーが適用されることはありません (拡張保護は無効になります)。</span><span class="sxs-lookup"><span data-stu-id="0c084-129">1.  Never – The policy is never enforced (Extended Protection is disabled).</span></span><br /><span data-ttu-id="0c084-130">2.WhenSupported – ポリシーが適用されるのは、クライアントが拡張保護をサポートしている場合のみです。</span><span class="sxs-lookup"><span data-stu-id="0c084-130">2.  WhenSupported – The policy is enforced only if the client supports Extended Protection.</span></span><br /><span data-ttu-id="0c084-131">3.Always – ポリシーは常に適用されます。</span><span class="sxs-lookup"><span data-stu-id="0c084-131">3.  Always – The policy is always enforced.</span></span> <span data-ttu-id="0c084-132">拡張保護をサポートしていないクライアントは認証に失敗します。</span><span class="sxs-lookup"><span data-stu-id="0c084-132">Clients which don’t support Extended Protection will fail to authenticate.</span></span>|  
|<span data-ttu-id="0c084-133">protectionScenario</span><span class="sxs-lookup"><span data-stu-id="0c084-133">protectionScenario</span></span>|<span data-ttu-id="0c084-134">この列挙体は、ポリシーによって適用される保護シナリオを指定します。</span><span class="sxs-lookup"><span data-stu-id="0c084-134">This enumeration specifies the protection scenario enforced by the policy.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="0c084-135">clientCredentialType 属性</span><span class="sxs-lookup"><span data-stu-id="0c084-135">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="0c084-136">値</span><span class="sxs-lookup"><span data-stu-id="0c084-136">Value</span></span>|<span data-ttu-id="0c084-137">説明</span><span class="sxs-lookup"><span data-stu-id="0c084-137">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="0c084-138">なし</span><span class="sxs-lookup"><span data-stu-id="0c084-138">None</span></span>|<span data-ttu-id="0c084-139">メッセージは、転送中はセキュリティで保護されません。</span><span class="sxs-lookup"><span data-stu-id="0c084-139">Messages are not secured during transfer.</span></span>|  
|<span data-ttu-id="0c084-140">Basic</span><span class="sxs-lookup"><span data-stu-id="0c084-140">Basic</span></span>|<span data-ttu-id="0c084-141">基本認証を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c084-141">Specifies basic authentication.</span></span>|  
|<span data-ttu-id="0c084-142">Digest</span><span class="sxs-lookup"><span data-stu-id="0c084-142">Digest</span></span>|<span data-ttu-id="0c084-143">ダイジェスト認証を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c084-143">Specifies digest authentication.</span></span>|  
|<span data-ttu-id="0c084-144">Ntlm</span><span class="sxs-lookup"><span data-stu-id="0c084-144">Ntlm</span></span>|<span data-ttu-id="0c084-145">Windows 認証に失敗した場合で可能な場合は、NTLM 認証を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c084-145">Specifies NTLM authentication when possible, and if Windows authentication fails.</span></span>|  
|<span data-ttu-id="0c084-146">Windows</span><span class="sxs-lookup"><span data-stu-id="0c084-146">Windows</span></span>|<span data-ttu-id="0c084-147">Windows 統合認証を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c084-147">Specifies Windows integrated authentication.</span></span>|  
  
## <a name="proxycredentialtype-attribute"></a><span data-ttu-id="0c084-148">proxyCredentialType 属性</span><span class="sxs-lookup"><span data-stu-id="0c084-148">proxyCredentialType Attribute</span></span>  
  
|<span data-ttu-id="0c084-149">値</span><span class="sxs-lookup"><span data-stu-id="0c084-149">Value</span></span>|<span data-ttu-id="0c084-150">説明</span><span class="sxs-lookup"><span data-stu-id="0c084-150">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="0c084-151">なし</span><span class="sxs-lookup"><span data-stu-id="0c084-151">None</span></span>|<span data-ttu-id="0c084-152">メッセージの数は、転送中にセキュリティ保護されません。</span><span class="sxs-lookup"><span data-stu-id="0c084-152">-   Messages are not secured during transfer.</span></span>|  
|<span data-ttu-id="0c084-153">Basic</span><span class="sxs-lookup"><span data-stu-id="0c084-153">Basic</span></span>|<span data-ttu-id="0c084-154">RFC 2617 『HTTP Authentication: Basic and Digest Authentication』で定義されているとおりに基本認証を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c084-154">Specifies basic authentication as defined by RFC 2617 – HTTP Authentication: Basic and Digest Authentication.</span></span>|  
|<span data-ttu-id="0c084-155">Digest</span><span class="sxs-lookup"><span data-stu-id="0c084-155">Digest</span></span>|<span data-ttu-id="0c084-156">RFC 2617 『HTTP Authentication: Basic and Digest Authentication』で定義されているとおりにダイジェスト認証を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c084-156">Specifies digest authentication as defined by RFC 2617 – HTTP Authentication: Basic and Digest Authentication.</span></span>|  
|<span data-ttu-id="0c084-157">Ntlm</span><span class="sxs-lookup"><span data-stu-id="0c084-157">Ntlm</span></span>|<span data-ttu-id="0c084-158">Windows 認証に失敗した場合で可能な場合は、NTLM 認証を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c084-158">Specifies NTLM authentication when possible, and if Windows authentication fails.</span></span>|  
|<span data-ttu-id="0c084-159">Windows</span><span class="sxs-lookup"><span data-stu-id="0c084-159">Windows</span></span>|<span data-ttu-id="0c084-160">Windows 統合認証を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c084-160">Specifies Windows integrated authentication.</span></span>|  
|<span data-ttu-id="0c084-161">証明書</span><span class="sxs-lookup"><span data-stu-id="0c084-161">Certificate</span></span>|<span data-ttu-id="0c084-162">証明書を使用したクライアント認証を実行します。</span><span class="sxs-lookup"><span data-stu-id="0c084-162">Performs client authentication using a certificate.</span></span> <span data-ttu-id="0c084-163">このオプションは、親要素の `Mode` の `security` 属性が Transport に設定されている場合のみ機能し、TransportCredentialOnly に設定されている場合は機能しません。</span><span class="sxs-lookup"><span data-stu-id="0c084-163">This option works only if the `Mode` attribute of the parent `security` element is set to Transport, and will not work if it is set to TransportCredentialOnly.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0c084-164">子要素</span><span class="sxs-lookup"><span data-stu-id="0c084-164">Child Elements</span></span>  
 <span data-ttu-id="0c084-165">なし</span><span class="sxs-lookup"><span data-stu-id="0c084-165">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0c084-166">親要素</span><span class="sxs-lookup"><span data-stu-id="0c084-166">Parent Elements</span></span>  
  
|<span data-ttu-id="0c084-167">要素</span><span class="sxs-lookup"><span data-stu-id="0c084-167">Element</span></span>|<span data-ttu-id="0c084-168">説明</span><span class="sxs-lookup"><span data-stu-id="0c084-168">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0c084-169">\<security></span><span class="sxs-lookup"><span data-stu-id="0c084-169">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-basichttpbinding.md)|<span data-ttu-id="0c084-170">セキュリティ機能を定義、 [ \<basicHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="0c084-170">Defines the security capabilities for the [\<basicHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span></span>|  
  
## <a name="example"></a><span data-ttu-id="0c084-171">例</span><span class="sxs-lookup"><span data-stu-id="0c084-171">Example</span></span>  
 <span data-ttu-id="0c084-172">基本的なバインディングを使用した SSL トランスポート セキュリティの使用例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0c084-172">The following example demonstrates the use of SSL transport security with the basic binding.</span></span> <span data-ttu-id="0c084-173">既定で、基本的なバインディングは HTTP 通信をサポートします。</span><span class="sxs-lookup"><span data-stu-id="0c084-173">By default, the basic binding supports HTTP communication.</span></span>  
  
```xml  
<system.serviceModel>  
   <services>  
      <service   
          type="Microsoft.ServiceModel.Samples.CalculatorService"  
          behaviorConfiguration="CalculatorServiceBehavior">  
         <endpoint address=""  
               binding="basicHttpBinding"  
               bindingConfiguration="Binding1"   
               contract="Microsoft.ServiceModel.Samples.ICalculator" />  
      </service>  
   </services>  
    <bindings>  
        <basicHttpBinding>  
        <!-- Configure basicHttpBinding with Transport security -- >  
        <!-- mode and clientCredentialType set to None.-->  
           <binding name="Binding1">  
               <security mode="Transport">  
                   <transport clientCredentialType="None"  
                              proxyCredentialType="None">  
                       <extendedProtectionPolicy  
                          policyEnforcement="WhenSupported"  
                          protectionScenario="TransportSelected">  
                    <customServiceNames></customServiceNames>  
                       </extendedProtectionPolicy>  
               </security>  
           </binding>  
        </basicHttpBinding>  
    </bindings>  
</system.serviceModel>  
```  
  
## <a name="see-also"></a><span data-ttu-id="0c084-174">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c084-174">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.BasicHttpSecurityElement.Transport%2A>  
 <xref:System.ServiceModel.BasicHttpSecurity.Transport%2A>  
 <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement>  
 <xref:System.ServiceModel.HttpTransportSecurity>  
 [<span data-ttu-id="0c084-175">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="0c084-175">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="0c084-176">バインディング</span><span class="sxs-lookup"><span data-stu-id="0c084-176">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="0c084-177">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="0c084-177">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="0c084-178">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="0c084-178">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="0c084-179">\<binding></span><span class="sxs-lookup"><span data-stu-id="0c084-179">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
