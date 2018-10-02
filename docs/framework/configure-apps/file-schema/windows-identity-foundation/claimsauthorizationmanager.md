---
title: '&lt;claimsAuthorizationManager&gt;'
ms.date: 03/30/2017
ms.assetid: 9354eee3-f692-4ad6-8427-3169686b8bcc
author: BrucePerlerMS
ms.openlocfilehash: a745339cffdada56a9b7f27f3f879b9d437c2da2
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48032102"
---
# <a name="ltclaimsauthorizationmanagergt"></a><span data-ttu-id="4c2d4-102">&lt;claimsAuthorizationManager&gt;</span><span class="sxs-lookup"><span data-stu-id="4c2d4-102">&lt;claimsAuthorizationManager&gt;</span></span>
<span data-ttu-id="4c2d4-103">入力方向の要求のクレーム承認マネージャーを登録します。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-103">Registers a claims authorization manager for the incoming claims.</span></span>  
  
 <span data-ttu-id="4c2d4-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="4c2d4-104">\<system.identityModel></span></span>  
<span data-ttu-id="4c2d4-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="4c2d4-105">\<identityConfiguration></span></span>  
<span data-ttu-id="4c2d4-106">\<claimsAuthorizationManager ></span><span class="sxs-lookup"><span data-stu-id="4c2d4-106">\<claimsAuthorizationManager></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4c2d4-107">構文</span><span class="sxs-lookup"><span data-stu-id="4c2d4-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimsAuthorizationManager type = xs:string>  
      <optionalConfigurationElements />  
    </claimsAuthorizationManager>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4c2d4-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="4c2d4-108">Attributes and Elements</span></span>  
 <span data-ttu-id="4c2d4-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4c2d4-110">属性</span><span class="sxs-lookup"><span data-stu-id="4c2d4-110">Attributes</span></span>  
  
|<span data-ttu-id="4c2d4-111">属性</span><span class="sxs-lookup"><span data-stu-id="4c2d4-111">Attribute</span></span>|<span data-ttu-id="4c2d4-112">説明</span><span class="sxs-lookup"><span data-stu-id="4c2d4-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4c2d4-113">型</span><span class="sxs-lookup"><span data-stu-id="4c2d4-113">type</span></span>|<span data-ttu-id="4c2d4-114">派生したカスタム型、<xref:System.Security.Claims.ClaimsAuthorizationManager>クラス。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-114">A custom type that derives from the <xref:System.Security.Claims.ClaimsAuthorizationManager> class.</span></span> <span data-ttu-id="4c2d4-115">詳細を指定する方法については、`type`属性は、「[カスタム型の参照](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md)します。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-115">For more information about how to specify the `type` attribute, see [Custom Type References](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4c2d4-116">子要素</span><span class="sxs-lookup"><span data-stu-id="4c2d4-116">Child Elements</span></span>  
 <span data-ttu-id="4c2d4-117">ある場合ありません`type`属性、または、`type`属性参照、<xref:System.Security.Claims.ClaimsAuthenticationManager>クラス、`<claimsAuthorizationManager>`要素は子要素を取りません。 ただし、から派生したクラス<xref:System.Security.Claims.ClaimsAuthorizationManager>子構成要素を定義できます。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-117">If there is no `type` attribute, or if the `type` attribute references the <xref:System.Security.Claims.ClaimsAuthenticationManager> class, the `<claimsAuthorizationManager>` element does not take child elements; however, classes derived from <xref:System.Security.Claims.ClaimsAuthorizationManager> can define child configuration elements.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4c2d4-118">親要素</span><span class="sxs-lookup"><span data-stu-id="4c2d4-118">Parent Elements</span></span>  
  
|<span data-ttu-id="4c2d4-119">要素</span><span class="sxs-lookup"><span data-stu-id="4c2d4-119">Element</span></span>|<span data-ttu-id="4c2d4-120">説明</span><span class="sxs-lookup"><span data-stu-id="4c2d4-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4c2d4-121">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="4c2d4-121">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="4c2d4-122">サービス レベルの id の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-122">Specifies service-level identity settings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4c2d4-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="4c2d4-123">Remarks</span></span>  
 <span data-ttu-id="4c2d4-124">によって提供される既定の動作、<xref:System.Security.Claims.ClaimsAuthorizationManager>クラスは常に、入力方向の要求を承認します。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-124">The default behavior provided through the <xref:System.Security.Claims.ClaimsAuthorizationManager> class always authorizes the incoming claims.</span></span> <span data-ttu-id="4c2d4-125">いない場合`type`属性が指定されて場合は、`type`属性を指定します、<xref:System.Security.Claims.ClaimsAuthorizationManager>クラス、`<claimsAuthorizationManager>`要素は子要素を取りません。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-125">If no `type` attribute is specified or if the `type` attribute specifies the <xref:System.Security.Claims.ClaimsAuthorizationManager> class, the `<claimsAuthorizationManager>` element does not take child elements.</span></span> <span data-ttu-id="4c2d4-126">指定することができます、`type`から派生した型を登録する属性、<xref:System.Security.Claims.ClaimsAuthorizationManager>カスタム動作を実装するクラス。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-126">You can specify the `type` attribute to register a type derived from the <xref:System.Security.Claims.ClaimsAuthorizationManager> class to implement custom behavior.</span></span> <span data-ttu-id="4c2d4-127">派生クラスの子要素を使用した構成をサポートできる、`<claimsAuthorizationManager>`要素をオーバーライドすることで、<xref:System.Security.Claims.ClaimsAuthorizationManager.LoadCustomConfiguration%2A>これらの要素を処理するメソッド。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-127">Derived classes can support configuration through child elements of the `<claimsAuthorizationManager>` element by overriding the <xref:System.Security.Claims.ClaimsAuthorizationManager.LoadCustomConfiguration%2A> method to handle these elements.</span></span> <span data-ttu-id="4c2d4-128">子要素に対して定義されているスキーマは、最大クラスのデザイナーです。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-128">The schema defined for the child elements is up to the designer of the class.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="4c2d4-129">使用する場合、<xref:System.IdentityModel.Services.ClaimsPrincipalPermission>または<xref:System.IdentityModel.Services.ClaimsPrincipalPermissionAttribute>コードによって参照される id の構成で信頼性情報ベースのアクセス制御を提供するクラス、`<federationConfiguration>`要素は、クレーム承認マネージャーとを使用して、ポリシーを構成します。承認の判断。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-129">When using the <xref:System.IdentityModel.Services.ClaimsPrincipalPermission> or the <xref:System.IdentityModel.Services.ClaimsPrincipalPermissionAttribute> class to provide claims-based access control in your code, the identity configuration that is referenced by the `<federationConfiguration>` element configures the claims authorization manager and policy that is used to make authorization decisions.</span></span> <span data-ttu-id="4c2d4-130">これは Windows Communication Foundation (WCF) アプリケーションまたは Web ベースでないアプリケーションなど、受動的な Web シナリオではないシナリオであっても、当てはまります。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-130">This is true, even in scenarios that are not passive Web scenarios, for example Windows Communication Foundation (WCF) applications or an application that is not Web-based.</span></span> <span data-ttu-id="4c2d4-131">アプリケーションが、パッシブの Web アプリケーションではない場合、`<claimsAuthorizationManager>`要素 (とその子ポリシー要素、存在する場合) の参照先の id 構成だけに適用される設定。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-131">If the application is not a passive Web application, the `<claimsAuthorizationManager>` element (and its child policy elements, if present) of the referenced identity configuration are the only settings applied.</span></span> <span data-ttu-id="4c2d4-132">その他のすべての設定は無視されます。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-132">All other settings are ignored.</span></span> <span data-ttu-id="4c2d4-133">詳細については、次を参照してください。、 [ \<federationConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md)要素。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-133">For more information, see the [\<federationConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md) element.</span></span>  
  
 <span data-ttu-id="4c2d4-134">この要素の設定、<xref:System.IdentityModel.Configuration.IdentityConfiguration.ClaimsAuthorizationManager%2A?displayProperty=nameWithType>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-134">This element sets the <xref:System.IdentityModel.Configuration.IdentityConfiguration.ClaimsAuthorizationManager%2A?displayProperty=nameWithType> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4c2d4-135">例</span><span class="sxs-lookup"><span data-stu-id="4c2d4-135">Example</span></span>  
 <span data-ttu-id="4c2d4-136">次の XML では、リソースの操作を実行する、要求元が持つ必要があるクレームのブール型の組み合わせを指定のリソースとアクションのペアから成るポリシーを実装するマネージャー要求の承認の構成を示します。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-136">The following XML shows the configuration for a claims authorization manager that implements policy composed of resource-action pairs each of which specifies boolean combinations of the claims that a requestor must possess to perform the action on the resource.</span></span> <span data-ttu-id="4c2d4-137">このポリシーを使用できるクレーム承認マネージャーを実装するコードが記載されて、`ClaimsBasedAuthorization`サンプル。</span><span class="sxs-lookup"><span data-stu-id="4c2d4-137">The code that implements the claims authorization manager capable of using this policy can be found in the `ClaimsBasedAuthorization` sample.</span></span>  
  
```xml  
<system.identityModel>  
    <identityConfiguration>  
      <claimsAuthorizationManager type="ClaimsAuthorizationLibrary.MyClaimsAuthorizationManager, ClaimsAuthorizationLibrary">  
        <policy resource="http://localhost:28491/Developers.aspx" action="GET">  
          <or>  
            <claim claimType="http://schemas.microsoft.com/ws/2008/06/identity/claims/role" claimValue="developer" />  
            <claim claimType="http://schemas.xmlsoap.org/claims/Group" claimValue="Administrator" />  
          </or>  
        </policy>  
        <policy resource="http://localhost:28491/Administrators.aspx" action="GET">  
          <and>  
            <claim claimType="http://schemas.xmlsoap.org/claims/Group" claimValue="Administrator" />  
            <claim claimType="http://schemas.xmlsoap.org/ws/2005/05/identity/claims/country" claimValue="USA" />  
          </and>  
        </policy>  
        <policy resource="http://localhost:28491/Default.aspx" action="GET">  
        </policy>  
        <policy resource="http://localhost:28491/" action="GET">  
        </policy>  
        <policy resource="http://localhost:28491/Claims.aspx" action="GET">  
        </policy>  
      </claimsAuthorizationManager>  
    <identityConfiguration>  
<system.identityModel>  
```
