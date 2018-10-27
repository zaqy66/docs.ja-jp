---
title: '&lt;claimsAuthenticationManager&gt;'
ms.date: 03/30/2017
ms.assetid: 6d30a450-6d13-4671-81a8-77e0204500c5
author: BrucePerlerMS
ms.openlocfilehash: b0cee2fedb5f90ca2a1f7e379e199cfee66ee745
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50190971"
---
# <a name="ltclaimsauthenticationmanagergt"></a><span data-ttu-id="cbf68-102">&lt;claimsAuthenticationManager&gt;</span><span class="sxs-lookup"><span data-stu-id="cbf68-102">&lt;claimsAuthenticationManager&gt;</span></span>
<span data-ttu-id="cbf68-103">入力方向の要求のクレーム認証マネージャーを登録します。</span><span class="sxs-lookup"><span data-stu-id="cbf68-103">Registers a claims authentication manager for the incoming claims.</span></span>  
  
 <span data-ttu-id="cbf68-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="cbf68-104">\<system.identityModel></span></span>  
<span data-ttu-id="cbf68-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="cbf68-105">\<identityConfiguration></span></span>  
<span data-ttu-id="cbf68-106">\<claimsAuthenticationManager ></span><span class="sxs-lookup"><span data-stu-id="cbf68-106">\<claimsAuthenticationManager></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cbf68-107">構文</span><span class="sxs-lookup"><span data-stu-id="cbf68-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimsAuthenticationManager type=xs:string>  
      <optionalConfigurationElements />  
    </claimsAuthenticationManager>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cbf68-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="cbf68-108">Attributes and Elements</span></span>  
 <span data-ttu-id="cbf68-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="cbf68-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cbf68-110">属性</span><span class="sxs-lookup"><span data-stu-id="cbf68-110">Attributes</span></span>  
  
|<span data-ttu-id="cbf68-111">属性</span><span class="sxs-lookup"><span data-stu-id="cbf68-111">Attribute</span></span>|<span data-ttu-id="cbf68-112">説明</span><span class="sxs-lookup"><span data-stu-id="cbf68-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="cbf68-113">型</span><span class="sxs-lookup"><span data-stu-id="cbf68-113">type</span></span>|<span data-ttu-id="cbf68-114">派生したカスタム型を指定します、<xref:System.Security.Claims.ClaimsAuthenticationManager>クラス。</span><span class="sxs-lookup"><span data-stu-id="cbf68-114">Specifies a custom type that derives from the <xref:System.Security.Claims.ClaimsAuthenticationManager> class.</span></span> <span data-ttu-id="cbf68-115">詳細を指定する方法については、`type`属性を [カスタム型の参照] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cbf68-115">For more information about how to specify the `type` attribute, see [Custom Type References].</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cbf68-116">子要素</span><span class="sxs-lookup"><span data-stu-id="cbf68-116">Child Elements</span></span>  
 <span data-ttu-id="cbf68-117">ある場合ありません`type`属性、または、`type`属性参照、<xref:System.Security.Claims.ClaimsAuthenticationManager>クラス、`<claimsAuthenticationManager>`要素は子要素を取りません。 ただし、から派生したクラス<xref:System.Security.Claims.ClaimsAuthenticationManager>子構成要素を定義できます。</span><span class="sxs-lookup"><span data-stu-id="cbf68-117">If there is no `type` attribute, or if the `type` attribute references the <xref:System.Security.Claims.ClaimsAuthenticationManager> class, the `<claimsAuthenticationManager>` element does not take child elements; however, classes derived from <xref:System.Security.Claims.ClaimsAuthenticationManager> can define child configuration elements.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="cbf68-118">親要素</span><span class="sxs-lookup"><span data-stu-id="cbf68-118">Parent Elements</span></span>  
  
|<span data-ttu-id="cbf68-119">要素</span><span class="sxs-lookup"><span data-stu-id="cbf68-119">Element</span></span>|<span data-ttu-id="cbf68-120">説明</span><span class="sxs-lookup"><span data-stu-id="cbf68-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cbf68-121">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="cbf68-121">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="cbf68-122">サービス レベルの id の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="cbf68-122">Specifies service-level identity settings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cbf68-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="cbf68-123">Remarks</span></span>  
 <span data-ttu-id="cbf68-124">によって提供される既定の動作、<xref:System.Security.Claims.ClaimsAuthenticationManager>クラスは、入力方向の要求をエコーします。</span><span class="sxs-lookup"><span data-stu-id="cbf68-124">The default behavior provided through the <xref:System.Security.Claims.ClaimsAuthenticationManager> class echoes the incoming claims.</span></span> <span data-ttu-id="cbf68-125">いない場合`type`属性が指定されて場合は、`type`属性を指定します、<xref:System.Security.Claims.ClaimsAuthenticationManager>クラス、`<claimsAuthenticationManager>`要素は子要素を取りません。</span><span class="sxs-lookup"><span data-stu-id="cbf68-125">If no `type` attribute is specified or if the `type` attribute specifies the <xref:System.Security.Claims.ClaimsAuthenticationManager> class, the `<claimsAuthenticationManager>` element does not take child elements.</span></span> <span data-ttu-id="cbf68-126">指定することができます、`type`から派生した型を登録する属性、<xref:System.Security.Claims.ClaimsAuthenticationManager>カスタム動作を実装するクラス。</span><span class="sxs-lookup"><span data-stu-id="cbf68-126">You can specify the `type` attribute to register a type derived from the <xref:System.Security.Claims.ClaimsAuthenticationManager> class to implement custom behavior.</span></span> <span data-ttu-id="cbf68-127">派生クラスの子要素を使用した構成をサポートできる、`<claimsAuthenticationManager>`要素をオーバーライドすることで、<xref:System.Security.Claims.ClaimsAuthenticationManager.LoadCustomConfiguration%2A>これらの要素を処理するメソッド。</span><span class="sxs-lookup"><span data-stu-id="cbf68-127">Derived classes can support configuration through child elements of the `<claimsAuthenticationManager>` element by overriding the <xref:System.Security.Claims.ClaimsAuthenticationManager.LoadCustomConfiguration%2A> method to handle these elements.</span></span> <span data-ttu-id="cbf68-128">子要素に対して定義されているスキーマは、最大クラスのデザイナーです。</span><span class="sxs-lookup"><span data-stu-id="cbf68-128">The schema defined for the child elements is up to the designer of the class.</span></span>  
  
 <span data-ttu-id="cbf68-129">`<claimsAuthenticationManager>`要素セット、<xref:System.IdentityModel.Configuration.IdentityConfiguration.ClaimsAuthenticationManager%2A?displayProperty=nameWithType>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="cbf68-129">The `<claimsAuthenticationManager>` element sets the <xref:System.IdentityModel.Configuration.IdentityConfiguration.ClaimsAuthenticationManager%2A?displayProperty=nameWithType> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cbf68-130">例</span><span class="sxs-lookup"><span data-stu-id="cbf68-130">Example</span></span>  
  
```xml  
<system.identityModel>  
    <identityConfiguration name="MyIdentity">  
      <claimsAuthenticationManager type="MyNamespace.CustomClaimsAuthenticationManager, MyAssembly"/>          
    </identityConfiguration>  
</system.identityModel>  
```
