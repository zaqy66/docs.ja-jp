---
title: <userNameSecurityTokenHandlerRequirement>
ms.date: 03/30/2017
ms.assetid: 6ec3bac1-b014-49ae-843c-c54518cb709a
author: BrucePerlerMS
ms.openlocfilehash: 18769794da8528f085c567264827db5aa6b214f1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271890"
---
# <a name="usernamesecuritytokenhandlerrequirement"></a><span data-ttu-id="a48d5-101">\<userNameSecurityTokenHandlerRequirement></span><span class="sxs-lookup"><span data-stu-id="a48d5-101">\<userNameSecurityTokenHandlerRequirement></span></span>
<span data-ttu-id="a48d5-102">構成を提供、<xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler>クラスまたは派生クラス。</span><span class="sxs-lookup"><span data-stu-id="a48d5-102">Provides configuration for the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="a48d5-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="a48d5-103">\<system.identityModel></span></span>  
<span data-ttu-id="a48d5-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="a48d5-104">\<identityConfiguration></span></span>  
<span data-ttu-id="a48d5-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="a48d5-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="a48d5-106">\<add></span><span class="sxs-lookup"><span data-stu-id="a48d5-106">\<add></span></span>  
<span data-ttu-id="a48d5-107">\<userNameSecurityTokenHandlerRequirement></span><span class="sxs-lookup"><span data-stu-id="a48d5-107">\<userNameSecurityTokenHandlerRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a48d5-108">構文</span><span class="sxs-lookup"><span data-stu-id="a48d5-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a48d5-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="a48d5-109">Attributes and Elements</span></span>  
 <span data-ttu-id="a48d5-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="a48d5-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a48d5-111">属性</span><span class="sxs-lookup"><span data-stu-id="a48d5-111">Attributes</span></span>  
  
|<span data-ttu-id="a48d5-112">属性</span><span class="sxs-lookup"><span data-stu-id="a48d5-112">Attribute</span></span>|<span data-ttu-id="a48d5-113">説明</span><span class="sxs-lookup"><span data-stu-id="a48d5-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a48d5-114">membershipProviderName</span><span class="sxs-lookup"><span data-stu-id="a48d5-114">membershipProviderName</span></span>|<span data-ttu-id="a48d5-115">指定します、<xref:System.Web.Security.MembershipProvider>でセキュリティ トークン ハンドラーを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a48d5-115">Specifies the <xref:System.Web.Security.MembershipProvider> that should be used by the security token handler.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a48d5-116">子要素</span><span class="sxs-lookup"><span data-stu-id="a48d5-116">Child Elements</span></span>  
 <span data-ttu-id="a48d5-117">なし</span><span class="sxs-lookup"><span data-stu-id="a48d5-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a48d5-118">親要素</span><span class="sxs-lookup"><span data-stu-id="a48d5-118">Parent Elements</span></span>  
  
|<span data-ttu-id="a48d5-119">要素</span><span class="sxs-lookup"><span data-stu-id="a48d5-119">Element</span></span>|<span data-ttu-id="a48d5-120">説明</span><span class="sxs-lookup"><span data-stu-id="a48d5-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a48d5-121">\<add></span><span class="sxs-lookup"><span data-stu-id="a48d5-121">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="a48d5-122">トークン ハンドラー コレクションには、指定したセキュリティ トークン ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="a48d5-122">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a48d5-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="a48d5-123">Remarks</span></span>  
 <span data-ttu-id="a48d5-124">`<userNameSecurityTokenHandlerRequirement>`要素セット、<xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A>プロパティと、<xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler>構成からオブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a48d5-124">The `<userNameSecurityTokenHandlerRequirement>` element sets the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A> property when a <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a48d5-125">例</span><span class="sxs-lookup"><span data-stu-id="a48d5-125">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler, System.IdentityModel.Services">  
    <userNameSecurityTokenHandlerRequirement membershipProviderName="AspNetSqlProvider/>  
</add>  
```
