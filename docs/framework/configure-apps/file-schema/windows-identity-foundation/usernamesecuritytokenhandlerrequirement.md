---
title: '&lt;userNameSecurityTokenHandlerRequirement&gt;'
ms.date: 03/30/2017
ms.assetid: 6ec3bac1-b014-49ae-843c-c54518cb709a
author: BrucePerlerMS
ms.openlocfilehash: dfcaad8b150321fda2a86e601bf57204cbdc1a0e
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47075034"
---
# <a name="ltusernamesecuritytokenhandlerrequirementgt"></a><span data-ttu-id="034db-102">&lt;userNameSecurityTokenHandlerRequirement&gt;</span><span class="sxs-lookup"><span data-stu-id="034db-102">&lt;userNameSecurityTokenHandlerRequirement&gt;</span></span>
<span data-ttu-id="034db-103">構成を提供、<xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler>クラスまたは派生クラス。</span><span class="sxs-lookup"><span data-stu-id="034db-103">Provides configuration for the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="034db-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="034db-104">\<system.identityModel></span></span>  
<span data-ttu-id="034db-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="034db-105">\<identityConfiguration></span></span>  
<span data-ttu-id="034db-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="034db-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="034db-107">\<add></span><span class="sxs-lookup"><span data-stu-id="034db-107">\<add></span></span>  
<span data-ttu-id="034db-108">\<userNameSecurityTokenHandlerRequirement ></span><span class="sxs-lookup"><span data-stu-id="034db-108">\<userNameSecurityTokenHandlerRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="034db-109">構文</span><span class="sxs-lookup"><span data-stu-id="034db-109">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="034db-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="034db-110">Attributes and Elements</span></span>  
 <span data-ttu-id="034db-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="034db-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="034db-112">属性</span><span class="sxs-lookup"><span data-stu-id="034db-112">Attributes</span></span>  
  
|<span data-ttu-id="034db-113">属性</span><span class="sxs-lookup"><span data-stu-id="034db-113">Attribute</span></span>|<span data-ttu-id="034db-114">説明</span><span class="sxs-lookup"><span data-stu-id="034db-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="034db-115">membershipProviderName</span><span class="sxs-lookup"><span data-stu-id="034db-115">membershipProviderName</span></span>|<span data-ttu-id="034db-116">指定します、<xref:System.Web.Security.MembershipProvider>でセキュリティ トークン ハンドラーを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="034db-116">Specifies the <xref:System.Web.Security.MembershipProvider> that should be used by the security token handler.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="034db-117">子要素</span><span class="sxs-lookup"><span data-stu-id="034db-117">Child Elements</span></span>  
 <span data-ttu-id="034db-118">なし</span><span class="sxs-lookup"><span data-stu-id="034db-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="034db-119">親要素</span><span class="sxs-lookup"><span data-stu-id="034db-119">Parent Elements</span></span>  
  
|<span data-ttu-id="034db-120">要素</span><span class="sxs-lookup"><span data-stu-id="034db-120">Element</span></span>|<span data-ttu-id="034db-121">説明</span><span class="sxs-lookup"><span data-stu-id="034db-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="034db-122">\<add></span><span class="sxs-lookup"><span data-stu-id="034db-122">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="034db-123">トークン ハンドラー コレクションには、指定したセキュリティ トークン ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="034db-123">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="034db-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="034db-124">Remarks</span></span>  
 <span data-ttu-id="034db-125">`<userNameSecurityTokenHandlerRequirement>`要素セット、<xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A>プロパティと、<xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler>構成からオブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="034db-125">The `<userNameSecurityTokenHandlerRequirement>` element sets the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A> property when a <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="034db-126">例</span><span class="sxs-lookup"><span data-stu-id="034db-126">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler, System.IdentityModel.Services">  
    <userNameSecurityTokenHandlerRequirement membershipProviderName="AspNetSqlProvider/>  
</add>  
```
