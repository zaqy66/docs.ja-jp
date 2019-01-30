---
title: <add> の <claimTypeRequirements>
ms.date: 03/30/2017
ms.assetid: c68e83c9-39e8-4264-b1ce-b6a9eb5b98aa
ms.openlocfilehash: 6a8c96fb2cb2050cac7b8853b84caecc883449d7
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55268783"
---
# <a name="add-of-claimtyperequirements"></a><span data-ttu-id="5c892-102">\<add> of \<claimTypeRequirements></span><span class="sxs-lookup"><span data-stu-id="5c892-102">\<add> of \<claimTypeRequirements></span></span>
<span data-ttu-id="5c892-103">フェデレーション資格情報に表示されると予想される必須のクレームおよび省略可能なクレームの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="5c892-103">Specifies the types of required and optional claims expected to appear in the federated credential.</span></span> <span data-ttu-id="5c892-104">たとえば、サービスは、クレームの種類の特定のセットを処理する必要がある受信資格情報について要件を記述します。</span><span class="sxs-lookup"><span data-stu-id="5c892-104">For example, services state the requirements on incoming credentials, which must possess a certain set of claim types.</span></span>  
  
 <span data-ttu-id="5c892-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="5c892-105">\<system.serviceModel></span></span>  
<span data-ttu-id="5c892-106">\<bindings></span><span class="sxs-lookup"><span data-stu-id="5c892-106">\<bindings></span></span>  
<span data-ttu-id="5c892-107">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="5c892-107">\<customBinding></span></span>  
<span data-ttu-id="5c892-108">\<binding></span><span class="sxs-lookup"><span data-stu-id="5c892-108">\<binding></span></span>  
<span data-ttu-id="5c892-109">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="5c892-109">\<security></span></span>  
<span data-ttu-id="5c892-110">\<issuedTokenParameters></span><span class="sxs-lookup"><span data-stu-id="5c892-110">\<issuedTokenParameters></span></span>  
<span data-ttu-id="5c892-111">\<claimTypeRequirements></span><span class="sxs-lookup"><span data-stu-id="5c892-111">\<claimTypeRequirements></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5c892-112">構文</span><span class="sxs-lookup"><span data-stu-id="5c892-112">Syntax</span></span>  
  
```xml  
<claimTypeRequirements>
  <add claimType="URI"
       isOptional="Boolean" />
</claimTypeRequirements>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5c892-113">属性および要素</span><span class="sxs-lookup"><span data-stu-id="5c892-113">Attributes and Elements</span></span>  
 <span data-ttu-id="5c892-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="5c892-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5c892-115">属性</span><span class="sxs-lookup"><span data-stu-id="5c892-115">Attributes</span></span>  
  
|<span data-ttu-id="5c892-116">属性</span><span class="sxs-lookup"><span data-stu-id="5c892-116">Attribute</span></span>|<span data-ttu-id="5c892-117">説明</span><span class="sxs-lookup"><span data-stu-id="5c892-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5c892-118">claimType</span><span class="sxs-lookup"><span data-stu-id="5c892-118">claimType</span></span>|<span data-ttu-id="5c892-119">クレームの種類を定義する URI。</span><span class="sxs-lookup"><span data-stu-id="5c892-119">A URI that defines the type of a claim.</span></span> <span data-ttu-id="5c892-120">たとえば、Web サイトから製品を購入するために、ユーザーは、十分な与信限度額を備えた有効なクレジット カードを示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c892-120">For example, to purchase a product from a Web site, the user must present a valid credit card with sufficient credit limit.</span></span> <span data-ttu-id="5c892-121">クレームの種類として、クレジット カードの URI があります。</span><span class="sxs-lookup"><span data-stu-id="5c892-121">The claim type would be the credit card URI.</span></span>|  
|<span data-ttu-id="5c892-122">isOptional</span><span class="sxs-lookup"><span data-stu-id="5c892-122">isOptional</span></span>|<span data-ttu-id="5c892-123">これが省略可能なクレームかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="5c892-123">A Boolean value that specifies if this is for an optional claim.</span></span> <span data-ttu-id="5c892-124">これが必須のクレームの場合は、この属性を `false` に設定します。</span><span class="sxs-lookup"><span data-stu-id="5c892-124">Set this attribute to `false` if this is a required claim.</span></span><br /><br /> <span data-ttu-id="5c892-125">サービスが必須でない情報を求めるときにこの属性を使用できます。</span><span class="sxs-lookup"><span data-stu-id="5c892-125">You can use this attribute when the service asks for some information but does not require it.</span></span> <span data-ttu-id="5c892-126">たとえば、ユーザーに氏名と住所の入力を要求し、電話番号は省略可能にする場合などです。</span><span class="sxs-lookup"><span data-stu-id="5c892-126">For example, if you require the user to enter his/her first name, last name and address, but decide that phone number is optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5c892-127">子要素</span><span class="sxs-lookup"><span data-stu-id="5c892-127">Child Elements</span></span>  
 <span data-ttu-id="5c892-128">なし。</span><span class="sxs-lookup"><span data-stu-id="5c892-128">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5c892-129">親要素</span><span class="sxs-lookup"><span data-stu-id="5c892-129">Parent Elements</span></span>  
  
|<span data-ttu-id="5c892-130">要素</span><span class="sxs-lookup"><span data-stu-id="5c892-130">Element</span></span>|<span data-ttu-id="5c892-131">説明</span><span class="sxs-lookup"><span data-stu-id="5c892-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5c892-132">\<claimTypeRequirements></span><span class="sxs-lookup"><span data-stu-id="5c892-132">\<claimTypeRequirements></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/claimtyperequirements-element.md)|<span data-ttu-id="5c892-133">必須のクレームの種類のコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="5c892-133">Specifies a collection of required claim types.</span></span><br /><br /> <span data-ttu-id="5c892-134">フェデレーション シナリオでは、サービスが受信資格情報についての要件を記述します。</span><span class="sxs-lookup"><span data-stu-id="5c892-134">In a federated scenario, services state the requirements on incoming credentials.</span></span> <span data-ttu-id="5c892-135">たとえば、受信資格情報は、特定のクレーム タイプのセットを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c892-135">For example, the incoming credentials must possess a certain set of claim types.</span></span> <span data-ttu-id="5c892-136">このコレクションの要素はそれぞれ、フェデレーション資格情報に表示されると予想される必須の要求および省略可能な要求の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="5c892-136">Each element in this collection specifies the types of required and optional claims expected to appear in a federated credential.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5c892-137">Remarks</span><span class="sxs-lookup"><span data-stu-id="5c892-137">Remarks</span></span>  
 <span data-ttu-id="5c892-138">フェデレーション シナリオでは、サービスが受信資格情報についての要件を記述します。</span><span class="sxs-lookup"><span data-stu-id="5c892-138">In a federated scenario, services state the requirements on incoming credentials.</span></span> <span data-ttu-id="5c892-139">たとえば、受信資格情報は、特定のクレーム タイプのセットを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c892-139">For example, the incoming credentials must possess a certain set of claim types.</span></span> <span data-ttu-id="5c892-140">この要件はセキュリティ ポリシー内に明記されます。</span><span class="sxs-lookup"><span data-stu-id="5c892-140">This requirement is manifested in a security policy.</span></span> <span data-ttu-id="5c892-141">クライアントがフェデレーション サービスの資格情報 (CardSpace など) を要求する場合、クライアントは要件をトークン要求 (RequestSecurityToken) に設定します。これにより、フェデレーション サービスは、要件どおりの資格情報を発行できます。</span><span class="sxs-lookup"><span data-stu-id="5c892-141">When a client requests credentials from a federated service (for example, CardSpace), it puts the requirements into a token request (RequestSecurityToken) so that the federated service can issue the credentials that satisfy the requirements accordingly.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5c892-142">例</span><span class="sxs-lookup"><span data-stu-id="5c892-142">Example</span></span>  
 <span data-ttu-id="5c892-143">次の構成では、2 つのクレームの種類の要件をセキュリティ バインディングに追加しています。</span><span class="sxs-lookup"><span data-stu-id="5c892-143">The following configuration adds two claim type requirements to a security binding.</span></span>  
  
```xml  
<bindings>
  <wsFederationHttpBinding>
    <binding name="myFederatedBinding">
      <security mode="Message">
        <message issuedTokenType="urn:oasis:names:tc:SAML:1.0:assertion">
          <claimTypeRequirements>
            <add claimType="http://schemas.microsoft.com/ws/2005/05/identity/claims/EmailAddress" />
            <add claimType="http://schemas.microsoft.com/ws/2005/05/identity/claims/UserName"
                 optional="true" />
          </claimTypeRequirements>
        </message>
      </security>
    </binding>
  </wsFederationHttpBinding>
</bindings>
```  
  
## <a name="see-also"></a><span data-ttu-id="5c892-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c892-144">See also</span></span>
- <xref:System.ServiceModel.Security.Tokens.ClaimTypeRequirement>
- <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Configuration.ClaimTypeElementCollection>
- <xref:System.ServiceModel.Configuration.ClaimTypeElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="5c892-145">\<claimTypeRequirements></span><span class="sxs-lookup"><span data-stu-id="5c892-145">\<claimTypeRequirements></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/claimtyperequirements-element.md)
- [<span data-ttu-id="5c892-146">バインディング</span><span class="sxs-lookup"><span data-stu-id="5c892-146">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="5c892-147">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="5c892-147">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="5c892-148">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="5c892-148">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="5c892-149">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="5c892-149">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
- [<span data-ttu-id="5c892-150">方法: SecurityBindingElement を使用してカスタム バインディングを作成します。</span><span class="sxs-lookup"><span data-stu-id="5c892-150">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
- [<span data-ttu-id="5c892-151">カスタム バインド セキュリティ</span><span class="sxs-lookup"><span data-stu-id="5c892-151">Custom Binding Security</span></span>](../../../../../docs/framework/wcf/samples/custom-binding-security.md)
