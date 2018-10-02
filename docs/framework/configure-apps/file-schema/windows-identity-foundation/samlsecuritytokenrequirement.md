---
title: '&lt;samlSecurityTokenRequirement&gt;'
ms.date: 03/30/2017
ms.assetid: 09202d12-88d3-49cc-953b-703bcc1690eb
author: BrucePerlerMS
ms.openlocfilehash: c9856dae971691baf9dabe845bdecae90cbc8aa5
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48031891"
---
# <a name="ltsamlsecuritytokenrequirementgt"></a><span data-ttu-id="b97d8-102">&lt;samlSecurityTokenRequirement&gt;</span><span class="sxs-lookup"><span data-stu-id="b97d8-102">&lt;samlSecurityTokenRequirement&gt;</span></span>
<span data-ttu-id="b97d8-103">構成を提供、<xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler>クラス、<xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>クラス、またはこれらのクラスのいずれかの派生クラス。</span><span class="sxs-lookup"><span data-stu-id="b97d8-103">Provides configuration for the <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> class, the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class, or a derived class of either of these classes.</span></span> <span data-ttu-id="b97d8-104">によって表される、<xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement>クラス。</span><span class="sxs-lookup"><span data-stu-id="b97d8-104">Represented by the <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> class.</span></span>  
  
 <span data-ttu-id="b97d8-105">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="b97d8-105">\<system.identityModel></span></span>  
<span data-ttu-id="b97d8-106">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="b97d8-106">\<identityConfiguration></span></span>  
<span data-ttu-id="b97d8-107">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="b97d8-107">\<securityTokenHandlers></span></span>  
<span data-ttu-id="b97d8-108">\<add></span><span class="sxs-lookup"><span data-stu-id="b97d8-108">\<add></span></span>  
<span data-ttu-id="b97d8-109">\<samlSecurityTokenRequirement ></span><span class="sxs-lookup"><span data-stu-id="b97d8-109">\<samlSecurityTokenRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b97d8-110">構文</span><span class="sxs-lookup"><span data-stu-id="b97d8-110">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add>  
        <samlSecurityTokenRequirement   
            issuerCertificateValidationMode="None||ChainTrust||PeerTrust||PeerOrChainTrust||Custom"  
            issuerCertificateRevocationMode="NoCheck||Offline||Online"  
            issuerCertificateTrustedStoreLocation="CurrentLocation||LocalMachine"  
            issuerCertificateValidator="Namespace.Class Assembly"  
            mapToWindows=xs:boolean  
          <nameClaimType value=xs:string />  
          <roleClaimType value=xs:string />  
        </samlSecurityTokenRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b97d8-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="b97d8-111">Attributes and Elements</span></span>  
 <span data-ttu-id="b97d8-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="b97d8-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b97d8-113">属性</span><span class="sxs-lookup"><span data-stu-id="b97d8-113">Attributes</span></span>  
  
|<span data-ttu-id="b97d8-114">属性</span><span class="sxs-lookup"><span data-stu-id="b97d8-114">Attribute</span></span>|<span data-ttu-id="b97d8-115">説明</span><span class="sxs-lookup"><span data-stu-id="b97d8-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b97d8-116">mapToWindows</span><span class="sxs-lookup"><span data-stu-id="b97d8-116">mapToWindows</span></span>|<span data-ttu-id="b97d8-117">トークン ハンドラーが、入力方向の UPN 要求を使用して、検証トークンを Windows アカウントにマップする必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b97d8-117">Specifies whether the token handler should map the validating token to a Windows account by using the incoming UPN claim.</span></span> <span data-ttu-id="b97d8-118">既定では"false です"。</span><span class="sxs-lookup"><span data-stu-id="b97d8-118">The default is "false".</span></span>|  
|<span data-ttu-id="b97d8-119">issuerCertificateRevocationMode</span><span class="sxs-lookup"><span data-stu-id="b97d8-119">issuerCertificateRevocationMode</span></span>|<span data-ttu-id="b97d8-120"><xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> X.509 証明書を使用する失効モードを指定する値。</span><span class="sxs-lookup"><span data-stu-id="b97d8-120">An <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> value that specifies the revocation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="b97d8-121">既定値は、"Online"です。</span><span class="sxs-lookup"><span data-stu-id="b97d8-121">The default value is "Online".</span></span>|  
|<span data-ttu-id="b97d8-122">issuerCertificateValidationMode</span><span class="sxs-lookup"><span data-stu-id="b97d8-122">issuerCertificateValidationMode</span></span>|<span data-ttu-id="b97d8-123"><xref:System.ServiceModel.Security.X509CertificateValidationMode> X.509 証明書を使用する検証モードを指定する値。</span><span class="sxs-lookup"><span data-stu-id="b97d8-123">An <xref:System.ServiceModel.Security.X509CertificateValidationMode> value that specifies the validation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="b97d8-124">既定値は、"PeerOrChainTrust"です。</span><span class="sxs-lookup"><span data-stu-id="b97d8-124">The default value is "PeerOrChainTrust".</span></span>|  
|<span data-ttu-id="b97d8-125">issuerCertificateTrustedStoreLocation</span><span class="sxs-lookup"><span data-stu-id="b97d8-125">issuerCertificateTrustedStoreLocation</span></span>|<span data-ttu-id="b97d8-126">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> X.509 証明書ストアを指定する値。</span><span class="sxs-lookup"><span data-stu-id="b97d8-126">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the X.509 certificate store.</span></span> <span data-ttu-id="b97d8-127">既定値は、"LocalMachine"です。</span><span class="sxs-lookup"><span data-stu-id="b97d8-127">The default value is "LocalMachine".</span></span>|  
|<span data-ttu-id="b97d8-128">issuerCertificateValidator</span><span class="sxs-lookup"><span data-stu-id="b97d8-128">issuerCertificateValidator</span></span>|<span data-ttu-id="b97d8-129">派生したカスタム型<xref:System.IdentityModel.Selectors.X509CertificateValidator>します。</span><span class="sxs-lookup"><span data-stu-id="b97d8-129">A custom type that derives from <xref:System.IdentityModel.Selectors.X509CertificateValidator>.</span></span> <span data-ttu-id="b97d8-130">場合、`issuerCertificateValidationMode`属性が"Custom"は、この型のインスタンスが発行者証明書の検証に使用します。</span><span class="sxs-lookup"><span data-stu-id="b97d8-130">If the `issuerCertificateValidationMode` attribute is "Custom", an instance of this type is used for issuer certificate validation.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b97d8-131">子要素</span><span class="sxs-lookup"><span data-stu-id="b97d8-131">Child Elements</span></span>  
  
|<span data-ttu-id="b97d8-132">要素</span><span class="sxs-lookup"><span data-stu-id="b97d8-132">Element</span></span>|<span data-ttu-id="b97d8-133">説明</span><span class="sxs-lookup"><span data-stu-id="b97d8-133">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b97d8-134">\<nameClaimType ></span><span class="sxs-lookup"><span data-stu-id="b97d8-134">\<nameClaimType></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/nameclaimtype.md)|<span data-ttu-id="b97d8-135">設定を指定するクレームの種類、<xref:System.Security.Principal.IIdentity.Name%2A>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="b97d8-135">Sets the claim type that specifies the <xref:System.Security.Principal.IIdentity.Name%2A> property.</span></span>|  
|[<span data-ttu-id="b97d8-136">\<roleClaimType ></span><span class="sxs-lookup"><span data-stu-id="b97d8-136">\<roleClaimType></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/roleclaimtype.md)|<span data-ttu-id="b97d8-137">コレクション内のロールの種類の要求を定義する要求の種類を指定します<xref:System.Security.Claims.ClaimsIdentity>によって返されるオブジェクト、<xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A>トークン ハンドラーのメソッド。</span><span class="sxs-lookup"><span data-stu-id="b97d8-137">Specifies the claim type that defines the role type claims in the collection of <xref:System.Security.Claims.ClaimsIdentity> objects returned by the <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> method of the token handler.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b97d8-138">親要素</span><span class="sxs-lookup"><span data-stu-id="b97d8-138">Parent Elements</span></span>  
  
|<span data-ttu-id="b97d8-139">要素</span><span class="sxs-lookup"><span data-stu-id="b97d8-139">Element</span></span>|<span data-ttu-id="b97d8-140">説明</span><span class="sxs-lookup"><span data-stu-id="b97d8-140">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b97d8-141">\<add></span><span class="sxs-lookup"><span data-stu-id="b97d8-141">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="b97d8-142">トークン ハンドラー コレクションには、指定したセキュリティ トークン ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="b97d8-142">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b97d8-143">Remarks</span><span class="sxs-lookup"><span data-stu-id="b97d8-143">Remarks</span></span>  
 <span data-ttu-id="b97d8-144">`<samlSecurityTokenRequirement>`要素が表される、<xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement>オブジェクト モデルのクラスを構成するために使用、`SamlSecurityTokenRequirement`プロパティを<xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler>または<xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>します。</span><span class="sxs-lookup"><span data-stu-id="b97d8-144">The `<samlSecurityTokenRequirement>` element is represented by the <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> class in the object model and is used to configure the `SamlSecurityTokenRequirement` property on a <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> or a <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b97d8-145">例</span><span class="sxs-lookup"><span data-stu-id="b97d8-145">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SamlSecurityTokenHandler, System.IdentityModel">  
    <samlSecurityTokenRequirement issuerCertificateValidationMode="PeerOrChainTrust"  
                                  issuerCertificateRevocationMode="Online"  
                                  issuerCertificateTrustedStoreLocation="LocalMachine"  
                                  mapToWindows="false">  
  
        <nameClaimType value="http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name" />  
        <roleClaimType value="schemas.microsoft.com/ws/2006/04/identity/claims/role" />  
    </samlSecurityTokenRequirement>  
</add>  
```
