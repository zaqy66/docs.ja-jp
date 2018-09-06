---
title: '&lt;ws2007HttpBinding&gt; の &lt;transport&gt;'
ms.date: 03/30/2017
ms.assetid: 692befa3-8b0b-4ec5-b601-755874e98eb0
ms.openlocfilehash: 35af47551f742b0e48220611a874605fb752b626
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43857656"
---
# <a name="lttransportgt-of-ltws2007httpbindinggt"></a><span data-ttu-id="96212-102">&lt;ws2007HttpBinding&gt; の &lt;transport&gt;</span><span class="sxs-lookup"><span data-stu-id="96212-102">&lt;transport&gt; of &lt;ws2007HttpBinding&gt;</span></span>
<span data-ttu-id="96212-103">HTTP トランスポートの認証設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="96212-103">Defines authentication settings for the HTTP transport.</span></span>  
  
 <span data-ttu-id="96212-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="96212-104">\<system.serviceModel></span></span>  
<span data-ttu-id="96212-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="96212-105">\<bindings></span></span>  
<span data-ttu-id="96212-106">\<ws2007HttpBinding ></span><span class="sxs-lookup"><span data-stu-id="96212-106">\<ws2007HttpBinding></span></span>  
<span data-ttu-id="96212-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="96212-107">\<binding></span></span>  
<span data-ttu-id="96212-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="96212-108">\<security></span></span>  
<span data-ttu-id="96212-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="96212-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="96212-110">構文</span><span class="sxs-lookup"><span data-stu-id="96212-110">Syntax</span></span>  
  
```  
transport clientCredentialType =   
       "Basic/Certificate/Digest/None/Ntlm/Windows"  
       proxyCredentialType="Basic/Digest/None/Ntlm/Windows"  
       realm="string"   
```  
  
## <a name="type"></a><span data-ttu-id="96212-111">型</span><span class="sxs-lookup"><span data-stu-id="96212-111">Type</span></span>  
 <xref:System.ServiceModel.HttpTransportSecurity>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="96212-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="96212-112">Attributes and Elements</span></span>  
 <span data-ttu-id="96212-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="96212-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="96212-114">属性</span><span class="sxs-lookup"><span data-stu-id="96212-114">Attributes</span></span>  
  
|<span data-ttu-id="96212-115">属性</span><span class="sxs-lookup"><span data-stu-id="96212-115">Attribute</span></span>|<span data-ttu-id="96212-116">説明</span><span class="sxs-lookup"><span data-stu-id="96212-116">Description</span></span>|  
|---------------|-----------------|  
|`clientCredentialType`|<span data-ttu-id="96212-117">サービスに対するクライアントの認証に使用される資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="96212-117">Specifies the credential used to authenticate the client to the service.</span></span> <span data-ttu-id="96212-118">この属性は <xref:System.ServiceModel.HttpClientCredentialType> 型です。</span><span class="sxs-lookup"><span data-stu-id="96212-118">This attribute is of type <xref:System.ServiceModel.HttpClientCredentialType>.</span></span>|  
|`proxyCredentialType`|<span data-ttu-id="96212-119">ドメイン プロキシに対するクライアントの認証に使用される資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="96212-119">Specifies the credential used to authenticate the client to a domain proxy.</span></span> <span data-ttu-id="96212-120">この属性は <xref:System.ServiceModel.HttpProxyCredentialType> 型です。</span><span class="sxs-lookup"><span data-stu-id="96212-120">This attribute is of type <xref:System.ServiceModel.HttpProxyCredentialType>.</span></span>|  
|`realm`|<span data-ttu-id="96212-121">ダイジェスト認証または基本認証の認証レルム。</span><span class="sxs-lookup"><span data-stu-id="96212-121">The authentication realm for digest or basic authentication.</span></span> <span data-ttu-id="96212-122">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="96212-122">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="96212-123">認証レルムでは、少なくとも、認証を実行するホストの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="96212-123">An authentication realm specifies at least the name of the host that performs the authentication.</span></span> <span data-ttu-id="96212-124">アクセス権のあるユーザーのコレクションも指定できます。</span><span class="sxs-lookup"><span data-stu-id="96212-124">It can also specify a collection of users who have access.</span></span> <span data-ttu-id="96212-125">ユーザーは、認証レルムを照会して、複数のユーザー名とパスワードの候補のうち、どれを使用できるかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="96212-125">A user can query the authentication realm to determine which one of the several possible usernames and passwords can be used.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="96212-126">clientCredentialType 属性</span><span class="sxs-lookup"><span data-stu-id="96212-126">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="96212-127">値</span><span class="sxs-lookup"><span data-stu-id="96212-127">Value</span></span>|<span data-ttu-id="96212-128">説明</span><span class="sxs-lookup"><span data-stu-id="96212-128">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="96212-129">なし</span><span class="sxs-lookup"><span data-stu-id="96212-129">None</span></span>|<span data-ttu-id="96212-130">セキュリティを無効にします。</span><span class="sxs-lookup"><span data-stu-id="96212-130">Security is disabled.</span></span>|  
|<span data-ttu-id="96212-131">Basic</span><span class="sxs-lookup"><span data-stu-id="96212-131">Basic</span></span>|<span data-ttu-id="96212-132">基本認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="96212-132">Uses basic authentication.</span></span>|  
|<span data-ttu-id="96212-133">Digest</span><span class="sxs-lookup"><span data-stu-id="96212-133">Digest</span></span>|<span data-ttu-id="96212-134">ダイジェスト認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="96212-134">Uses digest authentication.</span></span>|  
|<span data-ttu-id="96212-135">Ntlm</span><span class="sxs-lookup"><span data-stu-id="96212-135">Ntlm</span></span>|<span data-ttu-id="96212-136">Windows ドメインのフォールバックとして NTLM 認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="96212-136">Uses NTLM authentication as a fallback with a Windows domain.</span></span>|  
|<span data-ttu-id="96212-137">Windows</span><span class="sxs-lookup"><span data-stu-id="96212-137">Windows</span></span>|<span data-ttu-id="96212-138">統合 Windows 認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="96212-138">Uses integrated Windows authentication.</span></span>|  
|<span data-ttu-id="96212-139">証明書</span><span class="sxs-lookup"><span data-stu-id="96212-139">Certificate</span></span>|<span data-ttu-id="96212-140">X.509 証明書を使用して、クライアントを認証します。</span><span class="sxs-lookup"><span data-stu-id="96212-140">Uses X.509 certificates to authenticate the client.</span></span>|  
  
## <a name="proxycredentialtype-attribute"></a><span data-ttu-id="96212-141">proxyCredentialType 属性</span><span class="sxs-lookup"><span data-stu-id="96212-141">proxyCredentialType Attribute</span></span>  
  
|<span data-ttu-id="96212-142">値</span><span class="sxs-lookup"><span data-stu-id="96212-142">Value</span></span>|<span data-ttu-id="96212-143">説明</span><span class="sxs-lookup"><span data-stu-id="96212-143">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="96212-144">なし</span><span class="sxs-lookup"><span data-stu-id="96212-144">None</span></span>|<span data-ttu-id="96212-145">セキュリティを無効にします。</span><span class="sxs-lookup"><span data-stu-id="96212-145">Security is disabled.</span></span>|  
|<span data-ttu-id="96212-146">Basic</span><span class="sxs-lookup"><span data-stu-id="96212-146">Basic</span></span>|<span data-ttu-id="96212-147">基本認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="96212-147">Uses basic authentication.</span></span>|  
|<span data-ttu-id="96212-148">Digest</span><span class="sxs-lookup"><span data-stu-id="96212-148">Digest</span></span>|<span data-ttu-id="96212-149">ダイジェスト認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="96212-149">Uses digest authentication.</span></span>|  
|<span data-ttu-id="96212-150">Ntlm</span><span class="sxs-lookup"><span data-stu-id="96212-150">Ntlm</span></span>|<span data-ttu-id="96212-151">Windows ドメインのフォールバックとして NTLM を使用します。</span><span class="sxs-lookup"><span data-stu-id="96212-151">Uses NTLM as a fallback with a Windows domain.</span></span>|  
|<span data-ttu-id="96212-152">Windows</span><span class="sxs-lookup"><span data-stu-id="96212-152">Windows</span></span>|<span data-ttu-id="96212-153">統合 Windows 認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="96212-153">Uses integrated Windows authentication.</span></span>|  
|<span data-ttu-id="96212-154">証明書</span><span class="sxs-lookup"><span data-stu-id="96212-154">Certificate</span></span>|<span data-ttu-id="96212-155">X.509 証明書を使用して、クライアントを認証します。</span><span class="sxs-lookup"><span data-stu-id="96212-155">Uses X.509 certificates to authenticate the client.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="96212-156">子要素</span><span class="sxs-lookup"><span data-stu-id="96212-156">Child Elements</span></span>  
 <span data-ttu-id="96212-157">なし</span><span class="sxs-lookup"><span data-stu-id="96212-157">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="96212-158">親要素</span><span class="sxs-lookup"><span data-stu-id="96212-158">Parent Elements</span></span>  
  
|<span data-ttu-id="96212-159">要素</span><span class="sxs-lookup"><span data-stu-id="96212-159">Element</span></span>|<span data-ttu-id="96212-160">説明</span><span class="sxs-lookup"><span data-stu-id="96212-160">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="96212-161">\<security></span><span class="sxs-lookup"><span data-stu-id="96212-161">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-ws2007httpbinding.md)|<span data-ttu-id="96212-162">セキュリティ機能を表す、 [ \<ws2007HttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007httpbinding.md)要素。</span><span class="sxs-lookup"><span data-stu-id="96212-162">Represents the security capabilities of the [\<ws2007HttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007httpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="96212-163">関連項目</span><span class="sxs-lookup"><span data-stu-id="96212-163">See Also</span></span>  
 <xref:System.ServiceModel.HttpTransportSecurity>  
 <xref:System.ServiceModel.Configuration.BasicHttpSecurityElement.Transport%2A>  
 <xref:System.ServiceModel.WSHttpSecurity.Transport%2A>  
 <xref:System.ServiceModel.Configuration.WSHttpTransportSecurityElement>  
 [<span data-ttu-id="96212-164">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="96212-164">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="96212-165">バインディング</span><span class="sxs-lookup"><span data-stu-id="96212-165">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="96212-166">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="96212-166">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="96212-167">バインドを使用して、Windows Communication Foundation サービスとクライアントを構成するには</span><span class="sxs-lookup"><span data-stu-id="96212-167">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="96212-168">\<binding></span><span class="sxs-lookup"><span data-stu-id="96212-168">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
