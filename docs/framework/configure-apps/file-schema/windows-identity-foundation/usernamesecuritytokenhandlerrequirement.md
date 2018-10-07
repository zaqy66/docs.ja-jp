---
title: '&lt;userNameSecurityTokenHandlerRequirement&gt;'
ms.date: 03/30/2017
ms.assetid: 6ec3bac1-b014-49ae-843c-c54518cb709a
author: BrucePerlerMS
ms.openlocfilehash: dfcaad8b150321fda2a86e601bf57204cbdc1a0e
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2018
ms.locfileid: "48844242"
---
# <a name="ltusernamesecuritytokenhandlerrequirementgt"></a><span data-ttu-id="9c07c-102">&lt;userNameSecurityTokenHandlerRequirement&gt;</span><span class="sxs-lookup"><span data-stu-id="9c07c-102">&lt;userNameSecurityTokenHandlerRequirement&gt;</span></span>
<span data-ttu-id="9c07c-103">構成を提供、<xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler>クラスまたは派生クラス。</span><span class="sxs-lookup"><span data-stu-id="9c07c-103">Provides configuration for the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="9c07c-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="9c07c-104">\<system.identityModel></span></span>  
<span data-ttu-id="9c07c-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="9c07c-105">\<identityConfiguration></span></span>  
<span data-ttu-id="9c07c-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="9c07c-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="9c07c-107">\<add></span><span class="sxs-lookup"><span data-stu-id="9c07c-107">\<add></span></span>  
<span data-ttu-id="9c07c-108">\<userNameSecurityTokenHandlerRequirement ></span><span class="sxs-lookup"><span data-stu-id="9c07c-108">\<userNameSecurityTokenHandlerRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9c07c-109">構文</span><span class="sxs-lookup"><span data-stu-id="9c07c-109">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type="System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler, System.IdentityModel.Services">  
        <userNameSecurityTokenHandlerRequirement membershipProviderName=xs:string >  
        </userNameSecurityTokenHandlerRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9c07c-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="9c07c-110">Attributes and Elements</span></span>  
 <span data-ttu-id="9c07c-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="9c07c-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9c07c-112">属性</span><span class="sxs-lookup"><span data-stu-id="9c07c-112">Attributes</span></span>  
  
|<span data-ttu-id="9c07c-113">属性</span><span class="sxs-lookup"><span data-stu-id="9c07c-113">Attribute</span></span>|<span data-ttu-id="9c07c-114">説明</span><span class="sxs-lookup"><span data-stu-id="9c07c-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9c07c-115">membershipProviderName</span><span class="sxs-lookup"><span data-stu-id="9c07c-115">membershipProviderName</span></span>|<span data-ttu-id="9c07c-116">指定します、<xref:System.Web.Security.MembershipProvider>でセキュリティ トークン ハンドラーを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c07c-116">Specifies the <xref:System.Web.Security.MembershipProvider> that should be used by the security token handler.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9c07c-117">子要素</span><span class="sxs-lookup"><span data-stu-id="9c07c-117">Child Elements</span></span>  
 <span data-ttu-id="9c07c-118">なし</span><span class="sxs-lookup"><span data-stu-id="9c07c-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9c07c-119">親要素</span><span class="sxs-lookup"><span data-stu-id="9c07c-119">Parent Elements</span></span>  
  
|<span data-ttu-id="9c07c-120">要素</span><span class="sxs-lookup"><span data-stu-id="9c07c-120">Element</span></span>|<span data-ttu-id="9c07c-121">説明</span><span class="sxs-lookup"><span data-stu-id="9c07c-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9c07c-122">\<add></span><span class="sxs-lookup"><span data-stu-id="9c07c-122">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="9c07c-123">トークン ハンドラー コレクションには、指定したセキュリティ トークン ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="9c07c-123">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9c07c-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="9c07c-124">Remarks</span></span>  
 <span data-ttu-id="9c07c-125">`<userNameSecurityTokenHandlerRequirement>`要素セット、<xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A>プロパティと、<xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler>構成からオブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9c07c-125">The `<userNameSecurityTokenHandlerRequirement>` element sets the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A> property when a <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9c07c-126">例</span><span class="sxs-lookup"><span data-stu-id="9c07c-126">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler, System.IdentityModel.Services">  
    <userNameSecurityTokenHandlerRequirement membershipProviderName="AspNetSqlProvider/>  
</add>  
```
