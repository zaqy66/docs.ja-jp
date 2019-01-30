---
title: <add>
ms.date: 03/30/2017
ms.assetid: 4712a888-f154-4395-8887-ef14a88a6497
author: BrucePerlerMS
ms.openlocfilehash: cb88d2a37740cf439f4fd2aa0f7fe4c098da1cf2
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55269758"
---
# <a name="add"></a><span data-ttu-id="03def-101">\<add></span><span class="sxs-lookup"><span data-stu-id="03def-101">\<add></span></span>
<span data-ttu-id="03def-102">トークン ハンドラー コレクションには、指定したセキュリティ トークン ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="03def-102">Adds the specified security token handler to the token handler collection.</span></span>  
  
 <span data-ttu-id="03def-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="03def-103">\<system.identityModel></span></span>  
<span data-ttu-id="03def-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="03def-104">\<identityConfiguration></span></span>  
<span data-ttu-id="03def-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="03def-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="03def-106">\<add></span><span class="sxs-lookup"><span data-stu-id="03def-106">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="03def-107">構文</span><span class="sxs-lookup"><span data-stu-id="03def-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type=xs:string>  
        <optionalConfigurationElement>  
        </optionalConfigurationElement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="03def-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="03def-108">Attributes and Elements</span></span>  
 <span data-ttu-id="03def-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="03def-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="03def-110">属性</span><span class="sxs-lookup"><span data-stu-id="03def-110">Attributes</span></span>  
  
|<span data-ttu-id="03def-111">属性</span><span class="sxs-lookup"><span data-stu-id="03def-111">Attribute</span></span>|<span data-ttu-id="03def-112">説明</span><span class="sxs-lookup"><span data-stu-id="03def-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="03def-113">型</span><span class="sxs-lookup"><span data-stu-id="03def-113">type</span></span>|<span data-ttu-id="03def-114">追加するトークン ハンドラーの CLR 型名。</span><span class="sxs-lookup"><span data-stu-id="03def-114">The CLR type name of the token handler to be added.</span></span> <span data-ttu-id="03def-115">詳細を指定する方法については、`type`属性は、「[カスタム型の参照](https://msdn.microsoft.com/library/7286d2e3-c63d-49fd-abdc-ce2705f22c24)します。</span><span class="sxs-lookup"><span data-stu-id="03def-115">For more information about how to specify the `type` attribute, see [Custom Type References](https://msdn.microsoft.com/library/7286d2e3-c63d-49fd-abdc-ce2705f22c24).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="03def-116">子要素</span><span class="sxs-lookup"><span data-stu-id="03def-116">Child Elements</span></span>  
  
|<span data-ttu-id="03def-117">要素</span><span class="sxs-lookup"><span data-stu-id="03def-117">Element</span></span>|<span data-ttu-id="03def-118">説明</span><span class="sxs-lookup"><span data-stu-id="03def-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="03def-119">\<samlSecurityTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="03def-119">\<samlSecurityTokenRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/samlsecuritytokenrequirement.md)|<span data-ttu-id="03def-120">構成を提供、<xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler>クラス、<xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>クラス、またはこれらのクラスのいずれかの派生クラス。</span><span class="sxs-lookup"><span data-stu-id="03def-120">Provides configuration for the <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> class, the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class, or a derived class of either of these classes.</span></span>|  
|[<span data-ttu-id="03def-121">\<sessionTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="03def-121">\<sessionTokenRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/sessiontokenrequirement.md)|<span data-ttu-id="03def-122">構成を提供、<xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler>クラスまたは派生クラス。</span><span class="sxs-lookup"><span data-stu-id="03def-122">Provides configuration for the <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> class or derived classes.</span></span>|  
|[<span data-ttu-id="03def-123">\<userNameSecurityTokenHandlerRequirement></span><span class="sxs-lookup"><span data-stu-id="03def-123">\<userNameSecurityTokenHandlerRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/usernamesecuritytokenhandlerrequirement.md)|<span data-ttu-id="03def-124">構成を提供、<xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler>クラスまたは派生クラス。</span><span class="sxs-lookup"><span data-stu-id="03def-124">Provides configuration for the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> class or derived classes.</span></span>|  
|[<span data-ttu-id="03def-125">\<x509SecurityTokenHandlerRequirement></span><span class="sxs-lookup"><span data-stu-id="03def-125">\<x509SecurityTokenHandlerRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/x509securitytokenhandlerrequirement.md)|<span data-ttu-id="03def-126">オプションの構成を提供します、<xref:System.IdentityModel.Tokens.X509SecurityTokenHandler>クラスまたは派生クラス。</span><span class="sxs-lookup"><span data-stu-id="03def-126">Provides optional configuration for the <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler> class or derived classes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="03def-127">親要素</span><span class="sxs-lookup"><span data-stu-id="03def-127">Parent Elements</span></span>  
  
|<span data-ttu-id="03def-128">要素</span><span class="sxs-lookup"><span data-stu-id="03def-128">Element</span></span>|<span data-ttu-id="03def-129">説明</span><span class="sxs-lookup"><span data-stu-id="03def-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="03def-130">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="03def-130">\<securityTokenHandlers></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlers.md)|<span data-ttu-id="03def-131">エンドポイントに登録されているセキュリティ トークン ハンドラーのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="03def-131">Specifies a collection of security token handlers that are registered with the endpoint.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="03def-132">Remarks</span><span class="sxs-lookup"><span data-stu-id="03def-132">Remarks</span></span>  
 <span data-ttu-id="03def-133">`<add>`要素がトークン ハンドラーの構成を指定する 1 つの子要素を取得します。</span><span class="sxs-lookup"><span data-stu-id="03def-133">The `<add>` element can take a single child element that specifies the configuration for the token handler.</span></span> <span data-ttu-id="03def-134">これはを通じてハンドラー クラスを参照するかどうかによって異なります、`type`の属性、`<add>`要素は、この機能のサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="03def-134">This is dependent on whether the handler class referenced through the `type` attribute of the `<add>` element provides support for this feature.</span></span> <span data-ttu-id="03def-135">この機能を提供するトークン ハンドラー クラスを受け取るコンス トラクターを公開する必要があります、<xref:System.Xml.XmlElement>オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="03def-135">Token handler classes that provide this feature must expose a constructor that takes an <xref:System.Xml.XmlElement> object.</span></span>  
  
```  
public class CustomTokenHandler : Microsoft.IdentityModel.Tokens.SecurityTokenHandler  
{  
    public CustomTokenHandler( XmlElement customConfig )  
    {  
    }  
}  
```  
  
 <span data-ttu-id="03def-136">この機能を提供、組み込みのセキュリティ トークン ハンドラー クラスのいくつかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="03def-136">Several of the built-in security token handler classes do provide this functionality.</span></span> <span data-ttu-id="03def-137">これらのクラスは<xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler>、 <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>、 <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler>、 <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler>、および<xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler>します。</span><span class="sxs-lookup"><span data-stu-id="03def-137">These classes are <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>, <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler>, and <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler>.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="03def-138">トークン ハンドラー コレクションには、任意の型の 1 つのハンドラーのみ含めることができます。</span><span class="sxs-lookup"><span data-stu-id="03def-138">The token handler collection can only contain a single handler of any given type.</span></span> <span data-ttu-id="03def-139">つまり、たとえばから派生したハンドラーを追加する場合、<xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>クラスのコレクションを削除する必要あります、<xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>は既定では、コレクションから存在します。</span><span class="sxs-lookup"><span data-stu-id="03def-139">This means, for example, that if you want to add a handler that is derived from the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class to the collection, you must first remove the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>, which is present by default, from the collection.</span></span> <span data-ttu-id="03def-140">使用することができます、 [\<削除 >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/remove.md)コレクションまたは使用してから、単一のハンドラーを削除する要素、 [\<オフ >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/clear.md)コレクションからすべてのイベント ハンドラーを削除する要素。</span><span class="sxs-lookup"><span data-stu-id="03def-140">You can use the [\<remove>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/remove.md) element to remove a single handler from the collection or use the [\<clear>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/clear.md) element to remove all handlers from the collection.</span></span>  
  
 <span data-ttu-id="03def-141">ハンドラーで指定した設定の下に、トークン ハンドラー コレクションで指定された同等の設定を上書きする、 [ \<securityTokenHandlerConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)要素とその下でサービス レベルで指定されています。[ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)要素。</span><span class="sxs-lookup"><span data-stu-id="03def-141">Settings specified on a handler override equivalent settings specified on the token handler collection under the [\<securityTokenHandlerConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md) element and those specified at the service-level under the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="03def-142">例</span><span class="sxs-lookup"><span data-stu-id="03def-142">Example</span></span>  
 <span data-ttu-id="03def-143">次の XML の使用を示しています、`<add>`と`<remove>`に既定のセッション トークン ハンドラーをカスタム セッション トークン ハンドラーに置き換える要素。</span><span class="sxs-lookup"><span data-stu-id="03def-143">The following XML shows the use of the `<add>` and `<remove>` elements to replace the default session token handler with a custom session token handler.</span></span> <span data-ttu-id="03def-144">XML から取得されますが、`ClaimsAwareWebFarm`サンプル。</span><span class="sxs-lookup"><span data-stu-id="03def-144">The XML is taken from the `ClaimsAwareWebFarm` sample.</span></span>  
  
```xml  
<securityTokenHandlers>  
  <remove type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
  <add type="System.IdentityModel.Services.Tokens.MachineKeySessionSecurityTokenHandler, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
</securityTokenHandlers>  
```
