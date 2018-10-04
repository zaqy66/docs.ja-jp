---
title: '&lt;issuerNameRegistry&gt;'
ms.date: 03/30/2017
ms.assetid: 58b39d12-c953-40c4-88af-d7eb3343ca28
author: BrucePerlerMS
ms.openlocfilehash: de3ceb5d84d17307c69e9155834a0a584e6920a1
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2018
ms.locfileid: "48245219"
---
# <a name="ltissuernameregistrygt"></a><span data-ttu-id="a6563-102">&lt;issuerNameRegistry&gt;</span><span class="sxs-lookup"><span data-stu-id="a6563-102">&lt;issuerNameRegistry&gt;</span></span>
<span data-ttu-id="a6563-103">トークン ハンドラー コレクションのハンドラーによって使用される発行者名レジストリを構成します。</span><span class="sxs-lookup"><span data-stu-id="a6563-103">Configures the issuer name registry that is used by handlers in the token handler collection.</span></span>  
  
 <span data-ttu-id="a6563-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="a6563-104">\<system.identityModel></span></span>  
<span data-ttu-id="a6563-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="a6563-105">\<identityConfiguration></span></span>  
<span data-ttu-id="a6563-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="a6563-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="a6563-107">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="a6563-107">\<securityTokenHandlerConfiguration></span></span>  
<span data-ttu-id="a6563-108">\<issuerNameRegistry ></span><span class="sxs-lookup"><span data-stu-id="a6563-108">\<issuerNameRegistry></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a6563-109">構文</span><span class="sxs-lookup"><span data-stu-id="a6563-109">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <issuerNameRegistry type=xs:string>  
          <optionalCustomConfigurationElements />  
        </issuerNameRegistry>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a6563-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="a6563-110">Attributes and Elements</span></span>  
 <span data-ttu-id="a6563-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="a6563-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a6563-112">属性</span><span class="sxs-lookup"><span data-stu-id="a6563-112">Attributes</span></span>  
  
|<span data-ttu-id="a6563-113">属性</span><span class="sxs-lookup"><span data-stu-id="a6563-113">Attribute</span></span>|<span data-ttu-id="a6563-114">説明</span><span class="sxs-lookup"><span data-stu-id="a6563-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a6563-115">型</span><span class="sxs-lookup"><span data-stu-id="a6563-115">type</span></span>|<span data-ttu-id="a6563-116">派生した型、<xref:System.IdentityModel.Tokens.IssuerNameRegistry>クラス。</span><span class="sxs-lookup"><span data-stu-id="a6563-116">A type that derives from the <xref:System.IdentityModel.Tokens.IssuerNameRegistry> class.</span></span> <span data-ttu-id="a6563-117">詳細については、ユーザー設定を指定する方法についての`type`、[カスタム型の参照] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6563-117">For more information about how to specify a custom `type`, see [Custom Type References].</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a6563-118">子要素</span><span class="sxs-lookup"><span data-stu-id="a6563-118">Child Elements</span></span>  
  
|<span data-ttu-id="a6563-119">要素</span><span class="sxs-lookup"><span data-stu-id="a6563-119">Element</span></span>|<span data-ttu-id="a6563-120">説明</span><span class="sxs-lookup"><span data-stu-id="a6563-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a6563-121">\<trustedIssuers ></span><span class="sxs-lookup"><span data-stu-id="a6563-121">\<trustedIssuers></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md)|<span data-ttu-id="a6563-122">ときに、`type`属性が構成ベースの発行者名レジストリを指定します (、<xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>クラス)、 [ \<trustedIssuers >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md)要素を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6563-122">When the `type` attribute specifies the configuration-based issuer name registry (the <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> class), the [\<trustedIssuers>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md) element must be specified.</span></span> <span data-ttu-id="a6563-123">[ \<TrustedIssuers >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md)要素がかかる`<add>`、 `<clear>`、または`<remove>`要素の子要素として。</span><span class="sxs-lookup"><span data-stu-id="a6563-123">The [\<trustedIssuers>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md) element can take `<add>`, `<clear>`, or `<remove>` elements as child elements.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a6563-124">親要素</span><span class="sxs-lookup"><span data-stu-id="a6563-124">Parent Elements</span></span>  
  
|<span data-ttu-id="a6563-125">要素</span><span class="sxs-lookup"><span data-stu-id="a6563-125">Element</span></span>|<span data-ttu-id="a6563-126">説明</span><span class="sxs-lookup"><span data-stu-id="a6563-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a6563-127">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="a6563-127">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="a6563-128">トークン ハンドラー コレクションのセキュリティの構成を提供します。</span><span class="sxs-lookup"><span data-stu-id="a6563-128">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a6563-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="a6563-129">Remarks</span></span>  
 <span data-ttu-id="a6563-130">すべての発行者トークンは、発行者名レジストリを使用して検証されます。</span><span class="sxs-lookup"><span data-stu-id="a6563-130">All issuer tokens are validated using an issuer name registry.</span></span> <span data-ttu-id="a6563-131">これはオブジェクトから派生した、<xref:System.IdentityModel.Tokens.IssuerNameRegistry>クラス。</span><span class="sxs-lookup"><span data-stu-id="a6563-131">This is an object that derives from the <xref:System.IdentityModel.Tokens.IssuerNameRegistry> class.</span></span> <span data-ttu-id="a6563-132">発行者名レジストリを使用して、対応する発行者によって生成されたトークンの署名を検証するために必要な暗号化マテリアルにニーモニック名を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="a6563-132">The issuer name registry is used to associate a mnemonic name to the cryptographic material that is needed to verify the signatures of tokens produced by the corresponding issuer.</span></span> <span data-ttu-id="a6563-133">発行者名レジストリは、証明書利用者 (RP) アプリケーションによって信頼されている発行者の一覧を保持します。</span><span class="sxs-lookup"><span data-stu-id="a6563-133">The issuer name registry maintains a list of issuers that are trusted by the relying party (RP) application.</span></span> <span data-ttu-id="a6563-134">使用して、発行者名レジストリの種類を指定、`type`属性。</span><span class="sxs-lookup"><span data-stu-id="a6563-134">The type of the issuer name registry is specified using the `type` attribute.</span></span> <span data-ttu-id="a6563-135">`<issuerNameRegistry>`要素は、指定した型の構成を提供する 1 つまたは複数の子要素を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="a6563-135">The `<issuerNameRegistry>` element can have one or more child elements that provide configuration for the specified type.</span></span> <span data-ttu-id="a6563-136">これらの子要素をオーバーライドすることで処理するロジックを提供する、<xref:System.IdentityModel.Tokens.IssuerNameRegistry.LoadCustomConfiguration%2A>メソッド。</span><span class="sxs-lookup"><span data-stu-id="a6563-136">You provide the logic that processes these child elements by overriding the <xref:System.IdentityModel.Tokens.IssuerNameRegistry.LoadCustomConfiguration%2A> method.</span></span>  
  
 <span data-ttu-id="a6563-137">WIF には単一の発行者名レジストリの種類をすぐに使える、<xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>クラス。</span><span class="sxs-lookup"><span data-stu-id="a6563-137">WIF provides a single issuer name registry type out of the box, the <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> class.</span></span> <span data-ttu-id="a6563-138">このクラスは、一連の構成で指定されている信頼された発行者の証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="a6563-138">This class uses a set of trusted issuer certificates that are specified in configuration.</span></span> <span data-ttu-id="a6563-139">構成の子要素に要する`<trustedIssuers>`、信頼された発行者の証明書のコレクションが構成されています。</span><span class="sxs-lookup"><span data-stu-id="a6563-139">It requires a child configuration element, `<trustedIssuers>`, under which the collection of trusted issuer certificates is configured.</span></span> <span data-ttu-id="a6563-140">証明書が指定の ASN.1 を使用してエンコードされた証明書の拇印の形式とが追加または削除、コレクションからを使用して信頼された`<add>`、 `<clear>`、または`<remove>`要素。</span><span class="sxs-lookup"><span data-stu-id="a6563-140">Trusted certificates are specified using the ASN.1 encoded form of the certificate thumbprint and are added or removed from the collection by using `<add>`, `<clear>`, or `<remove>` elements.</span></span>  
  
 <span data-ttu-id="a6563-141">`<issuerNameRegistry>`要素が表される、<xref:System.IdentityModel.Configuration.IssuerNameRegistryElement>クラス。</span><span class="sxs-lookup"><span data-stu-id="a6563-141">The `<issuerNameRegistry>` element is represented by the <xref:System.IdentityModel.Configuration.IssuerNameRegistryElement> class.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a6563-142">指定する、`<issuerNameRegistry>`要素の子要素として、 [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)要素は非推奨とされましたが、旧バージョンとの互換性もサポートします。</span><span class="sxs-lookup"><span data-stu-id="a6563-142">Specifying the `<issuerNameRegistry>` element as a child element of the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element has been deprecated, but is still supported for backward compatibility.</span></span> <span data-ttu-id="a6563-143">上の設定、`<securityTokenHandlerConfiguration>`要素のオーバーライド、`<identityConfiguration>`要素。</span><span class="sxs-lookup"><span data-stu-id="a6563-143">Settings on the `<securityTokenHandlerConfiguration>` element override those on the `<identityConfiguration>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a6563-144">例</span><span class="sxs-lookup"><span data-stu-id="a6563-144">Example</span></span>  
 <span data-ttu-id="a6563-145">次の XML では、名前のレジストリをベースの構成の発行者を指定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a6563-145">The following XML shows how to specify the configuration based issuer name registry.</span></span>  
  
```xml  
<issuerNameRegistry type="System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">  
  <trustedIssuers>  
    <add thumbprint="9B74CB … 1EF40D0" name="LocalSTS" />  
  </trustedIssuers>  
</issuerNameRegistry>  
```  
  
## <a name="see-also"></a><span data-ttu-id="a6563-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6563-146">See Also</span></span>  
 <xref:System.IdentityModel.Tokens.IssuerNameRegistry>  
 <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>
