---
title: '&lt;issuedTokenParameters&gt; の &lt;issuer&gt;'
ms.date: 03/30/2017
ms.assetid: d6a95f32-d58c-40fc-8658-dd92564d3c90
ms.openlocfilehash: aa647f448bad74e25ffce4a5622c7489274996c7
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151138"
---
# <a name="ltissuergt-of-ltissuedtokenparametersgt"></a><span data-ttu-id="103d3-102">&lt;issuedTokenParameters&gt; の &lt;issuer&gt;</span><span class="sxs-lookup"><span data-stu-id="103d3-102">&lt;issuer&gt; of &lt;issuedTokenParameters&gt;</span></span>
<span data-ttu-id="103d3-103">セキュリティ トークンを発行するセキュリティ トークン サービス (STS) を指定します。</span><span class="sxs-lookup"><span data-stu-id="103d3-103">Specifies the Security Token Service (STS) that issues security tokens.</span></span>  
  
 <span data-ttu-id="103d3-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="103d3-104">\<system.serviceModel></span></span>  
<span data-ttu-id="103d3-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="103d3-105">\<bindings></span></span>  
<span data-ttu-id="103d3-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="103d3-106">\<customBinding></span></span>  
<span data-ttu-id="103d3-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="103d3-107">\<binding></span></span>  
<span data-ttu-id="103d3-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="103d3-108">\<security></span></span>  
<span data-ttu-id="103d3-109">\<issuedTokenParameters ></span><span class="sxs-lookup"><span data-stu-id="103d3-109">\<issuedTokenParameters></span></span>  
<span data-ttu-id="103d3-110">\<発行者 ></span><span class="sxs-lookup"><span data-stu-id="103d3-110">\<issuer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="103d3-111">構文</span><span class="sxs-lookup"><span data-stu-id="103d3-111">Syntax</span></span>  
  
```xml  
<issuer address="Uri" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="103d3-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="103d3-112">Attributes and Elements</span></span>  
 <span data-ttu-id="103d3-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="103d3-113">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="103d3-114">属性</span><span class="sxs-lookup"><span data-stu-id="103d3-114">Attributes</span></span>  
  
|<span data-ttu-id="103d3-115">属性</span><span class="sxs-lookup"><span data-stu-id="103d3-115">Attribute</span></span>|<span data-ttu-id="103d3-116">説明</span><span class="sxs-lookup"><span data-stu-id="103d3-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="103d3-117">address</span><span class="sxs-lookup"><span data-stu-id="103d3-117">address</span></span>|<span data-ttu-id="103d3-118">必須の文字列。</span><span class="sxs-lookup"><span data-stu-id="103d3-118">Required string.</span></span> <span data-ttu-id="103d3-119">STS の URL です。</span><span class="sxs-lookup"><span data-stu-id="103d3-119">The URL of the STS.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="103d3-120">子要素</span><span class="sxs-lookup"><span data-stu-id="103d3-120">Child Elements</span></span>  
  
|<span data-ttu-id="103d3-121">要素</span><span class="sxs-lookup"><span data-stu-id="103d3-121">Element</span></span>|<span data-ttu-id="103d3-122">説明</span><span class="sxs-lookup"><span data-stu-id="103d3-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="103d3-123">\<headers></span><span class="sxs-lookup"><span data-stu-id="103d3-123">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="103d3-124">ビルダーが作成できるエンドポイントのアドレス ヘッダーのコレクション。</span><span class="sxs-lookup"><span data-stu-id="103d3-124">A collection of address headers for the endpoints that the builder can create.</span></span>|  
|[<span data-ttu-id="103d3-125">\<identity></span><span class="sxs-lookup"><span data-stu-id="103d3-125">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="103d3-126">発行されたトークンを使用する場合、クライアントでサーバーの認証を有効にする設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="103d3-126">When using an issued token, specifies settings that enable the client to authenticate the server.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="103d3-127">親要素</span><span class="sxs-lookup"><span data-stu-id="103d3-127">Parent Elements</span></span>  
  
|<span data-ttu-id="103d3-128">要素</span><span class="sxs-lookup"><span data-stu-id="103d3-128">Element</span></span>|<span data-ttu-id="103d3-129">説明</span><span class="sxs-lookup"><span data-stu-id="103d3-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="103d3-130">\<issuedTokenParameters></span><span class="sxs-lookup"><span data-stu-id="103d3-130">\<issuedTokenParameters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenparameters.md)|<span data-ttu-id="103d3-131">現在発行されているトークンを指定します。</span><span class="sxs-lookup"><span data-stu-id="103d3-131">Specifies the current issued token.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="103d3-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="103d3-132">See Also</span></span>  
 <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters.AdditionalRequestParameters%2A>  
 <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement.AdditionalRequestParameters%2A>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="103d3-133">サービス ID と認証</span><span class="sxs-lookup"><span data-stu-id="103d3-133">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="103d3-134">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="103d3-134">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="103d3-135">カスタム バインドを使用したセキュリティ機能</span><span class="sxs-lookup"><span data-stu-id="103d3-135">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)  
 [<span data-ttu-id="103d3-136">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="103d3-136">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="103d3-137">バインディング</span><span class="sxs-lookup"><span data-stu-id="103d3-137">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="103d3-138">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="103d3-138">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="103d3-139">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="103d3-139">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="103d3-140">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="103d3-140">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)  
 [<span data-ttu-id="103d3-141">方法: SecurityBindingElement を使用してカスタム バインディングを作成します。</span><span class="sxs-lookup"><span data-stu-id="103d3-141">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)  
 [<span data-ttu-id="103d3-142">カスタム バインド セキュリティ</span><span class="sxs-lookup"><span data-stu-id="103d3-142">Custom Binding Security</span></span>](../../../../../docs/framework/wcf/samples/custom-binding-security.md)
