---
title: '&lt;nameClaimType&gt;'
ms.date: 03/30/2017
ms.assetid: 17514d95-f0f5-4789-8e28-346640dc227c
author: BrucePerlerMS
ms.openlocfilehash: bd4033b2edea7450b66c25f446669b3ded65e9af
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "48777894"
---
# <a name="ltnameclaimtypegt"></a><span data-ttu-id="cdd5a-102">&lt;nameClaimType&gt;</span><span class="sxs-lookup"><span data-stu-id="cdd5a-102">&lt;nameClaimType&gt;</span></span>
<span data-ttu-id="cdd5a-103">設定を指定するクレームの種類、<xref:System.Security.Principal.IIdentity.Name%2A>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="cdd5a-103">Sets the claim type that specifies the <xref:System.Security.Principal.IIdentity.Name%2A> property.</span></span> <span data-ttu-id="cdd5a-104">要求の種類が検索に使用される、<xref:System.Security.Claims.Claim>のコレクションで<xref:System.Security.Claims.ClaimsIdentity>によって返されるオブジェクト、<xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A>このトークン ハンドラーのメソッド。</span><span class="sxs-lookup"><span data-stu-id="cdd5a-104">The claim type is used to search for a <xref:System.Security.Claims.Claim> in the collection of <xref:System.Security.Claims.ClaimsIdentity> objects returned by the <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> method of this token handler.</span></span> <span data-ttu-id="cdd5a-105">名前と一致するクレームの値が設定し、<xref:System.Security.Principal.IIdentity>このトークン ハンドラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="cdd5a-105">The value of the matching claim is then set as the name of the <xref:System.Security.Principal.IIdentity> generated from this token handler.</span></span>  
  
 <span data-ttu-id="cdd5a-106">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="cdd5a-106">\<system.identityModel></span></span>  
<span data-ttu-id="cdd5a-107">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="cdd5a-107">\<identityConfiguration></span></span>  
<span data-ttu-id="cdd5a-108">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="cdd5a-108">\<securityTokenHandlers></span></span>  
<span data-ttu-id="cdd5a-109">\<add></span><span class="sxs-lookup"><span data-stu-id="cdd5a-109">\<add></span></span>  
<span data-ttu-id="cdd5a-110">\<samlSecurityTokenRequirement ></span><span class="sxs-lookup"><span data-stu-id="cdd5a-110">\<samlSecurityTokenRequirement></span></span>  
<span data-ttu-id="cdd5a-111">\<nameClaimType ></span><span class="sxs-lookup"><span data-stu-id="cdd5a-111">\<nameClaimType></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cdd5a-112">構文</span><span class="sxs-lookup"><span data-stu-id="cdd5a-112">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add>  
        <samlSecurityTokenRequirement>  
          <nameClaimType value=xs:string>  
          </nameClaimType>  
        </samlSecurityTokenRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cdd5a-113">属性および要素</span><span class="sxs-lookup"><span data-stu-id="cdd5a-113">Attributes and Elements</span></span>  
 <span data-ttu-id="cdd5a-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="cdd5a-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cdd5a-115">属性</span><span class="sxs-lookup"><span data-stu-id="cdd5a-115">Attributes</span></span>  
  
|<span data-ttu-id="cdd5a-116">属性</span><span class="sxs-lookup"><span data-stu-id="cdd5a-116">Attribute</span></span>|<span data-ttu-id="cdd5a-117">説明</span><span class="sxs-lookup"><span data-stu-id="cdd5a-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="cdd5a-118">値</span><span class="sxs-lookup"><span data-stu-id="cdd5a-118">value</span></span>|<span data-ttu-id="cdd5a-119">使用する要求の要求の種類を表す URI を指定する文字列、<xref:System.Security.Principal.IIdentity.Name%2A>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="cdd5a-119">A string that specifies the URI that represents the claim type of the claim to use for the <xref:System.Security.Principal.IIdentity.Name%2A> property.</span></span> <span data-ttu-id="cdd5a-120">必須。</span><span class="sxs-lookup"><span data-stu-id="cdd5a-120">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cdd5a-121">子要素</span><span class="sxs-lookup"><span data-stu-id="cdd5a-121">Child Elements</span></span>  
 <span data-ttu-id="cdd5a-122">なし</span><span class="sxs-lookup"><span data-stu-id="cdd5a-122">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="cdd5a-123">親要素</span><span class="sxs-lookup"><span data-stu-id="cdd5a-123">Parent Elements</span></span>  
  
|<span data-ttu-id="cdd5a-124">要素</span><span class="sxs-lookup"><span data-stu-id="cdd5a-124">Element</span></span>|<span data-ttu-id="cdd5a-125">説明</span><span class="sxs-lookup"><span data-stu-id="cdd5a-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cdd5a-126">\<samlSecurityTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="cdd5a-126">\<samlSecurityTokenRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/samlsecuritytokenrequirement.md)|<span data-ttu-id="cdd5a-127">構成を提供、<xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler>クラス、<xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>クラス、またはこれらのクラスのいずれかの派生クラス。</span><span class="sxs-lookup"><span data-stu-id="cdd5a-127">Provides configuration for the <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> class, the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class, or a derived class of either of these classes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cdd5a-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="cdd5a-128">Remarks</span></span>  
 <span data-ttu-id="cdd5a-129">`<nameClaimType>`要素セット、<xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.NameClaimType%2A>プロパティと、<xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement>構成からオブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cdd5a-129">The `<nameClaimType>` element sets the <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.NameClaimType%2A> property when a <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cdd5a-130">例</span><span class="sxs-lookup"><span data-stu-id="cdd5a-130">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SamlSecurityTokenHandler, System.IdentityModel">  
    <samlSecurityTokenRequirement>  
        <nameClaimType value="http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name" />  
    </samlSecurityTokenRequirement>  
</add>  
```  
  
## <a name="see-also"></a><span data-ttu-id="cdd5a-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="cdd5a-131">See Also</span></span>  
 <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.NameClaimType%2A>
