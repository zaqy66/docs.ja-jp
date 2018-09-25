---
title: '&lt;x509SecurityTokenHandlerRequirement&gt;'
ms.date: 03/30/2017
ms.assetid: aca22c2c-5ae7-42af-9bbd-15c2524692ce
author: BrucePerlerMS
ms.openlocfilehash: 994677904cada71dbc7cce4b6ca0de1d4dc65014
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47085664"
---
# <a name="ltx509securitytokenhandlerrequirementgt"></a><span data-ttu-id="57ee3-102">&lt;x509SecurityTokenHandlerRequirement&gt;</span><span class="sxs-lookup"><span data-stu-id="57ee3-102">&lt;x509SecurityTokenHandlerRequirement&gt;</span></span>
<span data-ttu-id="57ee3-103">オプションの構成を提供します、<xref:System.IdentityModel.Tokens.X509SecurityTokenHandler>クラスまたは派生クラス。</span><span class="sxs-lookup"><span data-stu-id="57ee3-103">Provides optional configuration for the <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="57ee3-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="57ee3-104">\<system.identityModel></span></span>  
<span data-ttu-id="57ee3-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="57ee3-105">\<identityConfiguration></span></span>  
<span data-ttu-id="57ee3-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="57ee3-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="57ee3-107">\<add></span><span class="sxs-lookup"><span data-stu-id="57ee3-107">\<add></span></span>  
<span data-ttu-id="57ee3-108">\<x509SecurityTokenHandlerRequirement ></span><span class="sxs-lookup"><span data-stu-id="57ee3-108">\<x509SecurityTokenHandlerRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57ee3-109">構文</span><span class="sxs-lookup"><span data-stu-id="57ee3-109">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type="System.IdentityModel.Tokens.X509SecurityTokenHandler, System.IdentityModel">  
        <x509SecurityTokenHandlerRequirement>  
          mapToWindows=xs:boolean  
          certificateValidationMode="None||ChainTrust||PeerTrust||PeerOrChainTrust||Custom"  
          certificateValidator="Namespace.Class, Assembly"  
          revocationMode="NoCheck||Offline||Online"  
          trustedStoreLocation="CurrentUser||LocalMachine"  
        </x509SecurityTokenHandlerRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="57ee3-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="57ee3-110">Attributes and Elements</span></span>  
 <span data-ttu-id="57ee3-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="57ee3-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="57ee3-112">属性</span><span class="sxs-lookup"><span data-stu-id="57ee3-112">Attributes</span></span>  
  
|<span data-ttu-id="57ee3-113">属性</span><span class="sxs-lookup"><span data-stu-id="57ee3-113">Attribute</span></span>|<span data-ttu-id="57ee3-114">説明</span><span class="sxs-lookup"><span data-stu-id="57ee3-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="57ee3-115">certificateValidationMode</span><span class="sxs-lookup"><span data-stu-id="57ee3-115">certificateValidationMode</span></span>|<span data-ttu-id="57ee3-116"><xref:System.ServiceModel.Security.X509CertificateValidationMode> X.509 証明書を使用する検証モードを指定する値。</span><span class="sxs-lookup"><span data-stu-id="57ee3-116">An <xref:System.ServiceModel.Security.X509CertificateValidationMode> value that specifies the validation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="57ee3-117">既定値は、"PeerOrChainTrust"です。</span><span class="sxs-lookup"><span data-stu-id="57ee3-117">The default value is "PeerOrChainTrust".</span></span>|  
|<span data-ttu-id="57ee3-118">mapToWindows</span><span class="sxs-lookup"><span data-stu-id="57ee3-118">mapToWindows</span></span>|<span data-ttu-id="57ee3-119">トークン ハンドラーが、入力方向の UPN 要求を使用して、検証トークンを Windows アカウントにマップする必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="57ee3-119">Specifies whether the token handler should map the validating token to a Windows account by using the incoming UPN claim.</span></span> <span data-ttu-id="57ee3-120">既定では"false です"。</span><span class="sxs-lookup"><span data-stu-id="57ee3-120">The default is "false".</span></span>|  
|<span data-ttu-id="57ee3-121">revocationMode</span><span class="sxs-lookup"><span data-stu-id="57ee3-121">revocationMode</span></span>|<span data-ttu-id="57ee3-122"><xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> X.509 証明書を使用する失効モードを指定する値。</span><span class="sxs-lookup"><span data-stu-id="57ee3-122">An <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> value that specifies the revocation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="57ee3-123">既定値は、"Online"です。</span><span class="sxs-lookup"><span data-stu-id="57ee3-123">The default value is "Online".</span></span>|  
|<span data-ttu-id="57ee3-124">trustedStoreLocation</span><span class="sxs-lookup"><span data-stu-id="57ee3-124">trustedStoreLocation</span></span>|<span data-ttu-id="57ee3-125">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> X.509 証明書ストアを指定する値。</span><span class="sxs-lookup"><span data-stu-id="57ee3-125">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the X.509 certificate store.</span></span> <span data-ttu-id="57ee3-126">既定値は、"LocalMachine"です。</span><span class="sxs-lookup"><span data-stu-id="57ee3-126">The default value is "LocalMachine".</span></span>|  
|<span data-ttu-id="57ee3-127">certificateValidator</span><span class="sxs-lookup"><span data-stu-id="57ee3-127">certificateValidator</span></span>|<span data-ttu-id="57ee3-128">派生したカスタム型<xref:System.IdentityModel.Selectors.X509CertificateValidator>します。</span><span class="sxs-lookup"><span data-stu-id="57ee3-128">A custom type that derives from <xref:System.IdentityModel.Selectors.X509CertificateValidator>.</span></span> <span data-ttu-id="57ee3-129">場合、`certificateValidationMode`属性が"Custom"は、この型のインスタンスが発行者証明書の検証に使用します。</span><span class="sxs-lookup"><span data-stu-id="57ee3-129">If the `certificateValidationMode` attribute is "Custom", an instance of this type is used for issuer certificate validation.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="57ee3-130">子要素</span><span class="sxs-lookup"><span data-stu-id="57ee3-130">Child Elements</span></span>  
 <span data-ttu-id="57ee3-131">なし</span><span class="sxs-lookup"><span data-stu-id="57ee3-131">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="57ee3-132">親要素</span><span class="sxs-lookup"><span data-stu-id="57ee3-132">Parent Elements</span></span>  
  
|<span data-ttu-id="57ee3-133">要素</span><span class="sxs-lookup"><span data-stu-id="57ee3-133">Element</span></span>|<span data-ttu-id="57ee3-134">説明</span><span class="sxs-lookup"><span data-stu-id="57ee3-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="57ee3-135">\<add></span><span class="sxs-lookup"><span data-stu-id="57ee3-135">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="57ee3-136">トークン ハンドラー コレクションには、指定したセキュリティ トークン ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="57ee3-136">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="57ee3-137">例</span><span class="sxs-lookup"><span data-stu-id="57ee3-137">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.X509SecurityTokenHandler, System.IdentityModel">  
    <x509SecurityTokenHandlerRequirement mapToWindows="true"   
                                         certificateValidationMode="PeerOrChainTrust"   
                                         revocationMode="Online"   
                                         trustedStoreLocation="LocalMachine" />  
</add>  
```
