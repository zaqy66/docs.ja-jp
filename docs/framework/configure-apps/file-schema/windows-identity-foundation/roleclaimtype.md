---
title: '&lt;RoleClaimType&gt;'
ms.date: 03/30/2017
ms.assetid: 69a49deb-6369-41ba-806b-ae8d21fac64b
author: BrucePerlerMS
ms.openlocfilehash: 565bf30d334c62c8132c60f411e89f7b260c54f1
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "48777131"
---
# <a name="ltroleclaimtypegt"></a><span data-ttu-id="e897e-102">&lt;RoleClaimType&gt;</span><span class="sxs-lookup"><span data-stu-id="e897e-102">&lt;roleClaimType&gt;</span></span>
<span data-ttu-id="e897e-103">コレクション内のロールの種類の要求を定義する要求の種類を指定します<xref:System.Security.Claims.ClaimsIdentity>によって返されるオブジェクト、<xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A>トークン ハンドラーのメソッド。</span><span class="sxs-lookup"><span data-stu-id="e897e-103">Specifies the claim type that defines the role type claims in the collection of <xref:System.Security.Claims.ClaimsIdentity> objects returned by the <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> method of the token handler.</span></span>  
  
 <span data-ttu-id="e897e-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="e897e-104">\<system.identityModel></span></span>  
<span data-ttu-id="e897e-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="e897e-105">\<identityConfiguration></span></span>  
<span data-ttu-id="e897e-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="e897e-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="e897e-107">\<add></span><span class="sxs-lookup"><span data-stu-id="e897e-107">\<add></span></span>  
<span data-ttu-id="e897e-108">\<samlSecurityTokenRequirement ></span><span class="sxs-lookup"><span data-stu-id="e897e-108">\<samlSecurityTokenRequirement></span></span>  
<span data-ttu-id="e897e-109">\<roleClaimType ></span><span class="sxs-lookup"><span data-stu-id="e897e-109">\<roleClaimType></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e897e-110">構文</span><span class="sxs-lookup"><span data-stu-id="e897e-110">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add>  
        <samlSecurityTokenRequirement>  
          <roleClaimType value=xs:string>  
          </roleClaimType>  
        </samlSecurityTokenRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e897e-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="e897e-111">Attributes and Elements</span></span>  
 <span data-ttu-id="e897e-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="e897e-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e897e-113">属性</span><span class="sxs-lookup"><span data-stu-id="e897e-113">Attributes</span></span>  
  
|<span data-ttu-id="e897e-114">属性</span><span class="sxs-lookup"><span data-stu-id="e897e-114">Attribute</span></span>|<span data-ttu-id="e897e-115">説明</span><span class="sxs-lookup"><span data-stu-id="e897e-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e897e-116">値</span><span class="sxs-lookup"><span data-stu-id="e897e-116">value</span></span>|<span data-ttu-id="e897e-117">ロール要求の種類を使用する要求の要求の種類を表す URI を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="e897e-117">A string that specifies the URI that represents the claim type of the claim to use for the role claim type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e897e-118">子要素</span><span class="sxs-lookup"><span data-stu-id="e897e-118">Child Elements</span></span>  
 <span data-ttu-id="e897e-119">なし</span><span class="sxs-lookup"><span data-stu-id="e897e-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e897e-120">親要素</span><span class="sxs-lookup"><span data-stu-id="e897e-120">Parent Elements</span></span>  
  
|<span data-ttu-id="e897e-121">要素</span><span class="sxs-lookup"><span data-stu-id="e897e-121">Element</span></span>|<span data-ttu-id="e897e-122">説明</span><span class="sxs-lookup"><span data-stu-id="e897e-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e897e-123">\<samlSecurityTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="e897e-123">\<samlSecurityTokenRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/samlsecuritytokenrequirement.md)|<span data-ttu-id="e897e-124">構成を提供、<xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler>クラス、<xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>クラス、またはこれらのクラスのいずれかの派生クラス。</span><span class="sxs-lookup"><span data-stu-id="e897e-124">Provides configuration for the <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> class, the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class, or a derived class of either of these classes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e897e-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="e897e-125">Remarks</span></span>  
 <span data-ttu-id="e897e-126">`<roleClaimType>`要素セット、<xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.RoleClaimType%2A>プロパティと、<xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement>構成からオブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e897e-126">The `<roleClaimType>` element sets the <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.RoleClaimType%2A> property when a <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e897e-127">例</span><span class="sxs-lookup"><span data-stu-id="e897e-127">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SamlSecurityTokenHandler, System.IdentityModel">  
    <samlSecurityTokenRequirement>  
        <roleClaimType value="schemas.microsoft.com/ws/2006/04/identity/claims/role" />  
    </samlSecurityTokenRequirement>  
</add>  
```  
  
## <a name="see-also"></a><span data-ttu-id="e897e-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="e897e-128">See Also</span></span>  
 <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.RoleClaimType%2A>
