---
title: '&lt;issuedTokenParameters&gt; の &lt;issuerMetadata&gt;'
ms.date: 03/30/2017
ms.assetid: 1a85ca37-496d-4fa3-8d44-d6c9383d735c
ms.openlocfilehash: 76956c54739219bbde78f378a12d59563ab785c4
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148748"
---
# <a name="ltissuermetadatagt-of-ltissuedtokenparametersgt"></a><span data-ttu-id="19d2e-102">&lt;issuedTokenParameters&gt; の &lt;issuerMetadata&gt;</span><span class="sxs-lookup"><span data-stu-id="19d2e-102">&lt;issuerMetadata&gt; of &lt;issuedTokenParameters&gt;</span></span>
<span data-ttu-id="19d2e-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="19d2e-103">\<system.serviceModel></span></span>  
<span data-ttu-id="19d2e-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="19d2e-104">\<bindings></span></span>  
<span data-ttu-id="19d2e-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="19d2e-105">\<customBinding></span></span>  
<span data-ttu-id="19d2e-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="19d2e-106">\<binding></span></span>  
<span data-ttu-id="19d2e-107">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="19d2e-107">\<security></span></span>  
<span data-ttu-id="19d2e-108">\<issuedTokenParameters ></span><span class="sxs-lookup"><span data-stu-id="19d2e-108">\<issuedTokenParameters></span></span>  
<span data-ttu-id="19d2e-109">\<issuerMetadata ></span><span class="sxs-lookup"><span data-stu-id="19d2e-109">\<issuerMetadata></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19d2e-110">構文</span><span class="sxs-lookup"><span data-stu-id="19d2e-110">Syntax</span></span>  
  
```xml  
<issuerMetaData address="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="19d2e-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="19d2e-111">Attributes and Elements</span></span>  
 <span data-ttu-id="19d2e-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="19d2e-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="19d2e-113">属性</span><span class="sxs-lookup"><span data-stu-id="19d2e-113">Attributes</span></span>  
  
|<span data-ttu-id="19d2e-114">属性</span><span class="sxs-lookup"><span data-stu-id="19d2e-114">Attribute</span></span>|<span data-ttu-id="19d2e-115">説明</span><span class="sxs-lookup"><span data-stu-id="19d2e-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="19d2e-116">address</span><span class="sxs-lookup"><span data-stu-id="19d2e-116">address</span></span>|<span data-ttu-id="19d2e-117">必ず指定します。</span><span class="sxs-lookup"><span data-stu-id="19d2e-117">Required.</span></span> <span data-ttu-id="19d2e-118">エンドポイントのアドレスを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="19d2e-118">A string that specifies the address of the endpoint.</span></span> <span data-ttu-id="19d2e-119">アドレスは、絶対 URI にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="19d2e-119">The address must be an absolute URI.</span></span> <span data-ttu-id="19d2e-120">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="19d2e-120">The default value is an empty string.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="19d2e-121">子要素</span><span class="sxs-lookup"><span data-stu-id="19d2e-121">Child Elements</span></span>  
  
|<span data-ttu-id="19d2e-122">要素</span><span class="sxs-lookup"><span data-stu-id="19d2e-122">Element</span></span>|<span data-ttu-id="19d2e-123">説明</span><span class="sxs-lookup"><span data-stu-id="19d2e-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="19d2e-124">\<headers></span><span class="sxs-lookup"><span data-stu-id="19d2e-124">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="19d2e-125">アドレス ヘッダーのコレクション。</span><span class="sxs-lookup"><span data-stu-id="19d2e-125">A collection of address headers.</span></span>|  
|[<span data-ttu-id="19d2e-126">\<identity></span><span class="sxs-lookup"><span data-stu-id="19d2e-126">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="19d2e-127">メッセージを交換する他のエンドポイントによるエンドポイントの認証を可能にする ID です。</span><span class="sxs-lookup"><span data-stu-id="19d2e-127">An identity that enables the authentication of an endpoint by other endpoints exchanging messages with it.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="19d2e-128">親要素</span><span class="sxs-lookup"><span data-stu-id="19d2e-128">Parent Elements</span></span>  
  
|<span data-ttu-id="19d2e-129">要素</span><span class="sxs-lookup"><span data-stu-id="19d2e-129">Element</span></span>|<span data-ttu-id="19d2e-130">説明</span><span class="sxs-lookup"><span data-stu-id="19d2e-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="19d2e-131">\<issuedTokenParameters></span><span class="sxs-lookup"><span data-stu-id="19d2e-131">\<issuedTokenParameters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenparameters.md)|<span data-ttu-id="19d2e-132">フェデレーション セキュリティのシナリオで発行されるセキュリティ トークンのパラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="19d2e-132">Specifies the parameters for an security token issued in a Federated security scenario.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="19d2e-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="19d2e-133">See Also</span></span>  
 <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters>  
 <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="19d2e-134">サービス ID と認証</span><span class="sxs-lookup"><span data-stu-id="19d2e-134">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="19d2e-135">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="19d2e-135">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="19d2e-136">カスタム バインドを使用したセキュリティ機能</span><span class="sxs-lookup"><span data-stu-id="19d2e-136">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)  
 [<span data-ttu-id="19d2e-137">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="19d2e-137">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="19d2e-138">バインディング</span><span class="sxs-lookup"><span data-stu-id="19d2e-138">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="19d2e-139">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="19d2e-139">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="19d2e-140">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="19d2e-140">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="19d2e-141">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="19d2e-141">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)  
 [<span data-ttu-id="19d2e-142">方法: SecurityBindingElement を使用してカスタム バインディングを作成します。</span><span class="sxs-lookup"><span data-stu-id="19d2e-142">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)  
 [<span data-ttu-id="19d2e-143">カスタム バインド セキュリティ</span><span class="sxs-lookup"><span data-stu-id="19d2e-143">Custom Binding Security</span></span>](../../../../../docs/framework/wcf/samples/custom-binding-security.md)
