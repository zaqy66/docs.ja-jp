---
title: <clientCredentials>
ms.date: 03/30/2017
ms.assetid: 1e6eef0d-a34e-4d74-b0f7-f65d2181858d
ms.openlocfilehash: 7ee49d6960864826dc74fbff629f502fcc70b4bf
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55254809"
---
# <a name="clientcredentials"></a><span data-ttu-id="08ab4-101">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="08ab4-101">\<clientCredentials></span></span>
<span data-ttu-id="08ab4-102">サービスに対するクライアントの認証に使用される資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="08ab4-102">Specifies the credentials used to authenticate the client to a service.</span></span>  
  
 <span data-ttu-id="08ab4-103">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="08ab4-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="08ab4-104">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="08ab4-104">\<behaviors></span></span>  
<span data-ttu-id="08ab4-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="08ab4-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="08ab4-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="08ab4-106">\<behavior></span></span>  
<span data-ttu-id="08ab4-107">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="08ab4-107">\<clientCredentials></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08ab4-108">構文</span><span class="sxs-lookup"><span data-stu-id="08ab4-108">Syntax</span></span>  
  
```xml  
<clientCredentials type="String"
                   supportInteractive="Boolean" >
  <clientCertificate>
  </clientCertificate>
  <digest>
  </digest>
  <isuedToken>
  </isuedToken>
  <peer>
  </peer>
  <serviceCertificate>
  </serviceCertificate>
  <windowsAuthentication>
  </windowsAuthentication>
</clientCredentials>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="08ab4-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="08ab4-109">Attributes and Elements</span></span>  
 <span data-ttu-id="08ab4-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="08ab4-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="08ab4-111">属性</span><span class="sxs-lookup"><span data-stu-id="08ab4-111">Attributes</span></span>  
  
|<span data-ttu-id="08ab4-112">属性</span><span class="sxs-lookup"><span data-stu-id="08ab4-112">Attribute</span></span>|<span data-ttu-id="08ab4-113">説明</span><span class="sxs-lookup"><span data-stu-id="08ab4-113">Description</span></span>|  
|---------------|-----------------|  
|`supportInteractive`|<span data-ttu-id="08ab4-114">実行時にクライアントの資格情報を選択する際に、対話型ユーザーを含めるかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="08ab4-114">A Boolean value that specifies whether an interactive user can be involved in selecting a client credential at runtime.</span></span> <span data-ttu-id="08ab4-115">既定値は `true` です。</span><span class="sxs-lookup"><span data-stu-id="08ab4-115">The default value is `true`.</span></span>|  
|`type`|<span data-ttu-id="08ab4-116">この設定要素の種類を指定する文字列です。</span><span class="sxs-lookup"><span data-stu-id="08ab4-116">A string that specifies the type of this configuration element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="08ab4-117">子要素</span><span class="sxs-lookup"><span data-stu-id="08ab4-117">Child Elements</span></span>  
  
|<span data-ttu-id="08ab4-118">要素</span><span class="sxs-lookup"><span data-stu-id="08ab4-118">Element</span></span>|<span data-ttu-id="08ab4-119">説明</span><span class="sxs-lookup"><span data-stu-id="08ab4-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="08ab4-120">\<clientCertificate></span><span class="sxs-lookup"><span data-stu-id="08ab4-120">\<clientCertificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcertificate-of-clientcredentials-element.md)|<span data-ttu-id="08ab4-121">サービスに対するクライアントの認証に使用される証明書を指定します。</span><span class="sxs-lookup"><span data-stu-id="08ab4-121">Specifies the certificate used to authenticate the client to the service.</span></span> <span data-ttu-id="08ab4-122">この要素は <xref:System.ServiceModel.Configuration.X509InitiatorCertificateClientElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="08ab4-122">This element is of type <xref:System.ServiceModel.Configuration.X509InitiatorCertificateClientElement>.</span></span>|  
|[<span data-ttu-id="08ab4-123">\<httpDigest></span><span class="sxs-lookup"><span data-stu-id="08ab4-123">\<httpDigest></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/httpdigest-element.md)|<span data-ttu-id="08ab4-124">サービスに対するクライアントの認証に使用されるダイジェストを指定します。</span><span class="sxs-lookup"><span data-stu-id="08ab4-124">Specifies a digest used to authenticate the client to the service.</span></span> <span data-ttu-id="08ab4-125">この要素は <xref:System.ServiceModel.Configuration.HttpDigestClientElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="08ab4-125">This element is of type <xref:System.ServiceModel.Configuration.HttpDigestClientElement>.</span></span>|  
|[<span data-ttu-id="08ab4-126">\<issuedToken ></span><span class="sxs-lookup"><span data-stu-id="08ab4-126">\<issuedToken></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtoken.md)|<span data-ttu-id="08ab4-127">セキュリティ トークン サービス (STS) に対するクライアントの認証に使用されるカスタム トークンの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="08ab4-127">Specifies a custom token type used to authenticate the client to a Secure Token Service (STS).</span></span> <span data-ttu-id="08ab4-128">この要素は <xref:System.ServiceModel.Configuration.IssuedTokenClientElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="08ab4-128">This element is of type <xref:System.ServiceModel.Configuration.IssuedTokenClientElement>.</span></span>|  
|[<span data-ttu-id="08ab4-129">\<peer></span><span class="sxs-lookup"><span data-stu-id="08ab4-129">\<peer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-clientcredentials-element.md)|<span data-ttu-id="08ab4-130">現在のピア資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="08ab4-130">Specifies a current peer credential.</span></span> <span data-ttu-id="08ab4-131">この要素は <xref:System.ServiceModel.Configuration.PeerCredentialElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="08ab4-131">This element is of type <xref:System.ServiceModel.Configuration.PeerCredentialElement>.</span></span>|  
|[<span data-ttu-id="08ab4-132">\<serviceCertificate></span><span class="sxs-lookup"><span data-stu-id="08ab4-132">\<serviceCertificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecertificate-of-clientcredentials-element.md)|<span data-ttu-id="08ab4-133">クライアントに対するサービスの認証に使用される証明書を指定し、証明書オプションを設定するための構造を提供します。</span><span class="sxs-lookup"><span data-stu-id="08ab4-133">Specifies the certificate used to authenticate the service to the client and provides a structure for setting certificate options.</span></span> <span data-ttu-id="08ab4-134">この証明書は、クライアントに対するサービスの帯域外に提供される必要があります。</span><span class="sxs-lookup"><span data-stu-id="08ab4-134">This certificate must be supplied out-of-band from the service to the client.</span></span> <span data-ttu-id="08ab4-135">この要素は <xref:System.ServiceModel.Configuration.X509RecipientCertificateClientElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="08ab4-135">This element is of type <xref:System.ServiceModel.Configuration.X509RecipientCertificateClientElement>.</span></span>|  
|[<span data-ttu-id="08ab4-136">\<windows></span><span class="sxs-lookup"><span data-stu-id="08ab4-136">\<windows></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/windows-of-clientcredentials-element.md)|<span data-ttu-id="08ab4-137">Windows 資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="08ab4-137">Specifies a Windows credential.</span></span> <span data-ttu-id="08ab4-138">既定値は、現在のスレッドの資格情報です。</span><span class="sxs-lookup"><span data-stu-id="08ab4-138">The default is the credential of the current thread.</span></span> <span data-ttu-id="08ab4-139">この要素は <xref:System.ServiceModel.Configuration.WindowsClientElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="08ab4-139">This element is of type <xref:System.ServiceModel.Configuration.WindowsClientElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="08ab4-140">親要素</span><span class="sxs-lookup"><span data-stu-id="08ab4-140">Parent Elements</span></span>  
  
|<span data-ttu-id="08ab4-141">要素</span><span class="sxs-lookup"><span data-stu-id="08ab4-141">Element</span></span>|<span data-ttu-id="08ab4-142">説明</span><span class="sxs-lookup"><span data-stu-id="08ab4-142">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="08ab4-143">\<behavior></span><span class="sxs-lookup"><span data-stu-id="08ab4-143">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="08ab4-144">エンドポイントの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="08ab4-144">Specifies an endpoint behavior.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="08ab4-145">Remarks</span><span class="sxs-lookup"><span data-stu-id="08ab4-145">Remarks</span></span>  
 <span data-ttu-id="08ab4-146">クライアント資格情報は、相互認証が必要な場合にサービスに対するクライアントの認証に使用されます。</span><span class="sxs-lookup"><span data-stu-id="08ab4-146">Client credentials are used to authenticate the client to services in cases where mutual authentication is required.</span></span> <span data-ttu-id="08ab4-147">また、この構成セクションを使用して、クライアントがサービスの証明書によってサービスへのメッセージをセキュリティで保護する必要がある場合に使用するサービス証明書を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="08ab4-147">This configuration section can also be used to specify service certificates for scenarios where the client must secure messages to a service with the service's certificate.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08ab4-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="08ab4-148">See also</span></span>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Description.ClientCredentials>
- [<span data-ttu-id="08ab4-149">セキュリティ動作</span><span class="sxs-lookup"><span data-stu-id="08ab4-149">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="08ab4-150">クライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="08ab4-150">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
