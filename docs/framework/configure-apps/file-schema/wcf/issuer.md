---
title: '&lt;発行者&gt;'
ms.date: 03/30/2017
ms.assetid: 8c49c6ae-fa1a-4179-a84b-613c3216dcde
ms.openlocfilehash: d2728bf3613b41ed9f0810207d27d6d67477afd2
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149554"
---
# <a name="ltissuergt"></a><span data-ttu-id="27a17-102">&lt;発行者&gt;</span><span class="sxs-lookup"><span data-stu-id="27a17-102">&lt;issuer&gt;</span></span>
<span data-ttu-id="27a17-103">セキュリティ トークンを発行するセキュリティ トークン サービス (STS) を指定します。</span><span class="sxs-lookup"><span data-stu-id="27a17-103">Specifies the Security Token Service (STS) that issues security tokens.</span></span>  
  
 <span data-ttu-id="27a17-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="27a17-104">\<system.serviceModel></span></span>  
<span data-ttu-id="27a17-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="27a17-105">\<bindings></span></span>  
<span data-ttu-id="27a17-106">\<wsFederationHttpBinding ></span><span class="sxs-lookup"><span data-stu-id="27a17-106">\<wsFederationHttpBinding></span></span>  
<span data-ttu-id="27a17-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="27a17-107">\<binding></span></span>  
<span data-ttu-id="27a17-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="27a17-108">\<security></span></span>  
<span data-ttu-id="27a17-109">\<message></span><span class="sxs-lookup"><span data-stu-id="27a17-109">\<message></span></span>  
<span data-ttu-id="27a17-110">\<発行者 ></span><span class="sxs-lookup"><span data-stu-id="27a17-110">\<issuer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="27a17-111">構文</span><span class="sxs-lookup"><span data-stu-id="27a17-111">Syntax</span></span>  
  
```xml  
<issuer address="Uri">
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
</issuer>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="27a17-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="27a17-112">Attributes and Elements</span></span>  
 <span data-ttu-id="27a17-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="27a17-113">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="27a17-114">属性</span><span class="sxs-lookup"><span data-stu-id="27a17-114">Attributes</span></span>  
  
|<span data-ttu-id="27a17-115">属性</span><span class="sxs-lookup"><span data-stu-id="27a17-115">Attribute</span></span>|<span data-ttu-id="27a17-116">説明</span><span class="sxs-lookup"><span data-stu-id="27a17-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="27a17-117">address</span><span class="sxs-lookup"><span data-stu-id="27a17-117">address</span></span>|<span data-ttu-id="27a17-118">必須の文字列。</span><span class="sxs-lookup"><span data-stu-id="27a17-118">Required string.</span></span> <span data-ttu-id="27a17-119">STS の URL です。</span><span class="sxs-lookup"><span data-stu-id="27a17-119">The URL of the STS.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="27a17-120">子要素</span><span class="sxs-lookup"><span data-stu-id="27a17-120">Child Elements</span></span>  
  
|<span data-ttu-id="27a17-121">要素</span><span class="sxs-lookup"><span data-stu-id="27a17-121">Element</span></span>|<span data-ttu-id="27a17-122">説明</span><span class="sxs-lookup"><span data-stu-id="27a17-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="27a17-123">\<headers></span><span class="sxs-lookup"><span data-stu-id="27a17-123">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="27a17-124">ビルダーが作成できるエンドポイントのアドレス ヘッダーのコレクション。</span><span class="sxs-lookup"><span data-stu-id="27a17-124">A collection of address headers for the endpoints that the builder can create.</span></span>|  
|[<span data-ttu-id="27a17-125">\<identity></span><span class="sxs-lookup"><span data-stu-id="27a17-125">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="27a17-126">発行されたトークンを使用する場合、クライアントでサーバーの認証を有効にする設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="27a17-126">When using an issued token, specifies settings that enable the client to authenticate the server.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="27a17-127">親要素</span><span class="sxs-lookup"><span data-stu-id="27a17-127">Parent Elements</span></span>  
  
|<span data-ttu-id="27a17-128">要素</span><span class="sxs-lookup"><span data-stu-id="27a17-128">Element</span></span>|<span data-ttu-id="27a17-129">説明</span><span class="sxs-lookup"><span data-stu-id="27a17-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="27a17-130">\<message></span><span class="sxs-lookup"><span data-stu-id="27a17-130">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-element-of-wsfederationhttpbinding.md)|<span data-ttu-id="27a17-131">メッセージ レベル セキュリティの設定を定義、 [ \<wsFederationHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md)要素。</span><span class="sxs-lookup"><span data-stu-id="27a17-131">Defines the settings for the message-level security for the [\<wsFederationHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="27a17-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="27a17-132">See Also</span></span>  
 <xref:System.ServiceModel.FederatedMessageSecurityOverHttp>  
 <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.Issuer%2A>  
 <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>  
 [<span data-ttu-id="27a17-133">サービス ID と認証</span><span class="sxs-lookup"><span data-stu-id="27a17-133">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="27a17-134">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="27a17-134">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="27a17-135">サービス ID と認証</span><span class="sxs-lookup"><span data-stu-id="27a17-135">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="27a17-136">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="27a17-136">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="27a17-137">カスタム バインドを使用したセキュリティ機能</span><span class="sxs-lookup"><span data-stu-id="27a17-137">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)  
 [<span data-ttu-id="27a17-138">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="27a17-138">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
