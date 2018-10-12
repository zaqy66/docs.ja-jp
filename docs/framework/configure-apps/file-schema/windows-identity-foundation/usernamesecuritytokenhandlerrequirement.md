---
title: '&lt;userNameSecurityTokenHandlerRequirement&gt;'
ms.date: 03/30/2017
ms.assetid: 6ec3bac1-b014-49ae-843c-c54518cb709a
author: BrucePerlerMS
ms.openlocfilehash: dfcaad8b150321fda2a86e601bf57204cbdc1a0e
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2018
ms.locfileid: "49123385"
---
# <a name="ltusernamesecuritytokenhandlerrequirementgt"></a><span data-ttu-id="7347d-102">&lt;userNameSecurityTokenHandlerRequirement&gt;</span><span class="sxs-lookup"><span data-stu-id="7347d-102">&lt;userNameSecurityTokenHandlerRequirement&gt;</span></span>
<span data-ttu-id="7347d-103">構成を提供、<xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler>クラスまたは派生クラス。</span><span class="sxs-lookup"><span data-stu-id="7347d-103">Provides configuration for the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="7347d-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="7347d-104">\<system.identityModel></span></span>  
<span data-ttu-id="7347d-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="7347d-105">\<identityConfiguration></span></span>  
<span data-ttu-id="7347d-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="7347d-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="7347d-107">\<add></span><span class="sxs-lookup"><span data-stu-id="7347d-107">\<add></span></span>  
<span data-ttu-id="7347d-108">\<userNameSecurityTokenHandlerRequirement ></span><span class="sxs-lookup"><span data-stu-id="7347d-108">\<userNameSecurityTokenHandlerRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7347d-109">構文</span><span class="sxs-lookup"><span data-stu-id="7347d-109">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7347d-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="7347d-110">Attributes and Elements</span></span>  
 <span data-ttu-id="7347d-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="7347d-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7347d-112">属性</span><span class="sxs-lookup"><span data-stu-id="7347d-112">Attributes</span></span>  
  
|<span data-ttu-id="7347d-113">属性</span><span class="sxs-lookup"><span data-stu-id="7347d-113">Attribute</span></span>|<span data-ttu-id="7347d-114">説明</span><span class="sxs-lookup"><span data-stu-id="7347d-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="7347d-115">membershipProviderName</span><span class="sxs-lookup"><span data-stu-id="7347d-115">membershipProviderName</span></span>|<span data-ttu-id="7347d-116">指定します、<xref:System.Web.Security.MembershipProvider>でセキュリティ トークン ハンドラーを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7347d-116">Specifies the <xref:System.Web.Security.MembershipProvider> that should be used by the security token handler.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7347d-117">子要素</span><span class="sxs-lookup"><span data-stu-id="7347d-117">Child Elements</span></span>  
 <span data-ttu-id="7347d-118">なし</span><span class="sxs-lookup"><span data-stu-id="7347d-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7347d-119">親要素</span><span class="sxs-lookup"><span data-stu-id="7347d-119">Parent Elements</span></span>  
  
|<span data-ttu-id="7347d-120">要素</span><span class="sxs-lookup"><span data-stu-id="7347d-120">Element</span></span>|<span data-ttu-id="7347d-121">説明</span><span class="sxs-lookup"><span data-stu-id="7347d-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7347d-122">\<add></span><span class="sxs-lookup"><span data-stu-id="7347d-122">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="7347d-123">トークン ハンドラー コレクションには、指定したセキュリティ トークン ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="7347d-123">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7347d-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="7347d-124">Remarks</span></span>  
 <span data-ttu-id="7347d-125">`<userNameSecurityTokenHandlerRequirement>`要素セット、<xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A>プロパティと、<xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler>構成からオブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7347d-125">The `<userNameSecurityTokenHandlerRequirement>` element sets the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A> property when a <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7347d-126">例</span><span class="sxs-lookup"><span data-stu-id="7347d-126">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler, System.IdentityModel.Services">  
    <userNameSecurityTokenHandlerRequirement membershipProviderName="AspNetSqlProvider/>  
</add>  
```
