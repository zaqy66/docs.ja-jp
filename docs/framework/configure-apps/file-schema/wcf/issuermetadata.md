---
title: '&lt;issuerMetadata&gt;'
ms.date: 03/30/2017
ms.assetid: e7eae2c0-cc17-4281-af59-e4eb8d54f92a
ms.openlocfilehash: 22e30e0962ec8d2eb0f7e52f4db143fba9bbf703
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491559"
---
# <a name="ltissuermetadatagt"></a><span data-ttu-id="66497-102">&lt;issuerMetadata&gt;</span><span class="sxs-lookup"><span data-stu-id="66497-102">&lt;issuerMetadata&gt;</span></span>
<span data-ttu-id="66497-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="66497-103">\<system.serviceModel></span></span>  
<span data-ttu-id="66497-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="66497-104">\<bindings></span></span>  
<span data-ttu-id="66497-105">\<wsFederationHttpBinding ></span><span class="sxs-lookup"><span data-stu-id="66497-105">\<wsFederationHttpBinding></span></span>  
<span data-ttu-id="66497-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="66497-106">\<binding></span></span>  
<span data-ttu-id="66497-107">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="66497-107">\<security></span></span>  
<span data-ttu-id="66497-108">\<message></span><span class="sxs-lookup"><span data-stu-id="66497-108">\<message></span></span>  
<span data-ttu-id="66497-109">\<issuerMetadata ></span><span class="sxs-lookup"><span data-stu-id="66497-109">\<issuerMetadata></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="66497-110">構文</span><span class="sxs-lookup"><span data-stu-id="66497-110">Syntax</span></span>  
  
```xml  
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
                          x509FindType="System.Security.Cryptography.X509certificates.X509findtype" />
    <dns value="String" />
    <rsa value="String" />
    <servicePrincipalName value="String" />
    <usePrincipalName value="String" />
  </identity>
</issuerMetadata>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="66497-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="66497-111">Attributes and Elements</span></span>  
 <span data-ttu-id="66497-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="66497-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="66497-113">属性</span><span class="sxs-lookup"><span data-stu-id="66497-113">Attributes</span></span>  
  
|<span data-ttu-id="66497-114">属性</span><span class="sxs-lookup"><span data-stu-id="66497-114">Attribute</span></span>|<span data-ttu-id="66497-115">説明</span><span class="sxs-lookup"><span data-stu-id="66497-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="66497-116">address</span><span class="sxs-lookup"><span data-stu-id="66497-116">address</span></span>|<span data-ttu-id="66497-117">必須の `string` 属性です。</span><span class="sxs-lookup"><span data-stu-id="66497-117">Required `string` attribute.</span></span><br /><br /> <span data-ttu-id="66497-118">エンドポイントのアドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="66497-118">Specifies the address of the endpoint.</span></span> <span data-ttu-id="66497-119">アドレスは、絶対 URI にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="66497-119">The address must be an absolute URI.</span></span> <span data-ttu-id="66497-120">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="66497-120">The default value is an empty string.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="66497-121">子要素</span><span class="sxs-lookup"><span data-stu-id="66497-121">Child Elements</span></span>  
  
|<span data-ttu-id="66497-122">要素</span><span class="sxs-lookup"><span data-stu-id="66497-122">Element</span></span>|<span data-ttu-id="66497-123">説明</span><span class="sxs-lookup"><span data-stu-id="66497-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="66497-124">\<headers></span><span class="sxs-lookup"><span data-stu-id="66497-124">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="66497-125">アドレス ヘッダーのコレクション。</span><span class="sxs-lookup"><span data-stu-id="66497-125">A collection of address headers.</span></span>|  
|[<span data-ttu-id="66497-126">\<identity></span><span class="sxs-lookup"><span data-stu-id="66497-126">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="66497-127">メッセージを交換する他のエンドポイントによるエンドポイントの認証を可能にする ID です。</span><span class="sxs-lookup"><span data-stu-id="66497-127">An identity that enables the authentication of an endpoint by other endpoints exchanging messages with it.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="66497-128">親要素</span><span class="sxs-lookup"><span data-stu-id="66497-128">Parent Elements</span></span>  
  
|<span data-ttu-id="66497-129">要素</span><span class="sxs-lookup"><span data-stu-id="66497-129">Element</span></span>|<span data-ttu-id="66497-130">説明</span><span class="sxs-lookup"><span data-stu-id="66497-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="66497-131">\<message></span><span class="sxs-lookup"><span data-stu-id="66497-131">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-element-of-wsfederationhttpbinding.md)|<span data-ttu-id="66497-132">メッセージ レベル セキュリティの設定を定義、 [ \<wsFederationHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md)要素。</span><span class="sxs-lookup"><span data-stu-id="66497-132">Defines the settings for the message-level security for the [\<wsFederationHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="66497-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="66497-133">See also</span></span>
- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.IssuerMetadataAddress%2A>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.IssuerMetadata%2A>
- [<span data-ttu-id="66497-134">サービス ID と認証</span><span class="sxs-lookup"><span data-stu-id="66497-134">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="66497-135">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="66497-135">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="66497-136">カスタム バインドを使用したセキュリティ機能</span><span class="sxs-lookup"><span data-stu-id="66497-136">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="66497-137">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="66497-137">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
