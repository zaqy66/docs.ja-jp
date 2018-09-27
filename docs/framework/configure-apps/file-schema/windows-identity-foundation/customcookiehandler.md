---
title: '&lt;customCookieHandler&gt;'
ms.date: 03/30/2017
ms.assetid: a03b153d-5ec6-4915-9031-6f0c3fd348be
author: BrucePerlerMS
ms.openlocfilehash: 51ca91de5c77727f5f5506118461d19354f12c14
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47237034"
---
# <a name="ltcustomcookiehandlergt"></a><span data-ttu-id="7e001-102">&lt;customCookieHandler&gt;</span><span class="sxs-lookup"><span data-stu-id="7e001-102">&lt;customCookieHandler&gt;</span></span>
<span data-ttu-id="7e001-103">カスタム クッキー ハンドラーの型を設定します。</span><span class="sxs-lookup"><span data-stu-id="7e001-103">Sets the custom cookie handler type.</span></span> <span data-ttu-id="7e001-104">この要素が存在するのみ場合、`mode`の属性、`<cookieHandler>`要素が"Custom"。</span><span class="sxs-lookup"><span data-stu-id="7e001-104">This element may only be present if the `mode` attribute of the `<cookieHandler>` element is "Custom".</span></span> <span data-ttu-id="7e001-105">カスタム型から派生する必要があります、<xref:System.IdentityModel.Services.CookieHandler>クラス。</span><span class="sxs-lookup"><span data-stu-id="7e001-105">The custom type must be derived from the <xref:System.IdentityModel.Services.CookieHandler> class.</span></span>  
  
 <span data-ttu-id="7e001-106">\<system.identityModel.services ></span><span class="sxs-lookup"><span data-stu-id="7e001-106">\<system.identityModel.services></span></span>  
<span data-ttu-id="7e001-107">\<federationConfiguration ></span><span class="sxs-lookup"><span data-stu-id="7e001-107">\<federationConfiguration></span></span>  
<span data-ttu-id="7e001-108">\<cookieHandler ></span><span class="sxs-lookup"><span data-stu-id="7e001-108">\<cookieHandler></span></span>  
<span data-ttu-id="7e001-109">\<customCookieHandler ></span><span class="sxs-lookup"><span data-stu-id="7e001-109">\<customCookieHandler></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7e001-110">構文</span><span class="sxs-lookup"><span data-stu-id="7e001-110">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <cookieHandler mode="Custom">  
      <customCookieHandler type="MyNamespace.MyCustomCookieHandler, MyAssembly" >  
      </customCookieHandler>  
    </cookieHandler>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7e001-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="7e001-111">Attributes and Elements</span></span>  
 <span data-ttu-id="7e001-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="7e001-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7e001-113">属性</span><span class="sxs-lookup"><span data-stu-id="7e001-113">Attributes</span></span>  
  
|<span data-ttu-id="7e001-114">属性</span><span class="sxs-lookup"><span data-stu-id="7e001-114">Attribute</span></span>|<span data-ttu-id="7e001-115">説明</span><span class="sxs-lookup"><span data-stu-id="7e001-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="7e001-116">型</span><span class="sxs-lookup"><span data-stu-id="7e001-116">type</span></span>|<span data-ttu-id="7e001-117">派生したカスタム型を指定します、<xref:System.IdentityModel.Services.CookieHandler>クラス。</span><span class="sxs-lookup"><span data-stu-id="7e001-117">Specifies a custom type that derives from the <xref:System.IdentityModel.Services.CookieHandler> class.</span></span> <span data-ttu-id="7e001-118">詳細を指定する方法については、`type`属性は、「[カスタム型の参照](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md)します。</span><span class="sxs-lookup"><span data-stu-id="7e001-118">For more information about how to specify the `type` attribute, see [Custom Type References](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7e001-119">子要素</span><span class="sxs-lookup"><span data-stu-id="7e001-119">Child Elements</span></span>  
 <span data-ttu-id="7e001-120">なし</span><span class="sxs-lookup"><span data-stu-id="7e001-120">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7e001-121">親要素</span><span class="sxs-lookup"><span data-stu-id="7e001-121">Parent Elements</span></span>  
  
|<span data-ttu-id="7e001-122">要素</span><span class="sxs-lookup"><span data-stu-id="7e001-122">Element</span></span>|<span data-ttu-id="7e001-123">説明</span><span class="sxs-lookup"><span data-stu-id="7e001-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7e001-124">\<cookieHandler ></span><span class="sxs-lookup"><span data-stu-id="7e001-124">\<cookieHandler></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/cookiehandler.md)|<span data-ttu-id="7e001-125">構成、<xref:System.IdentityModel.Services.CookieHandler>を<xref:System.IdentityModel.Services.SessionAuthenticationModule>読み取りと書き込みの cookie を使用します。</span><span class="sxs-lookup"><span data-stu-id="7e001-125">Configures the <xref:System.IdentityModel.Services.CookieHandler> that the <xref:System.IdentityModel.Services.SessionAuthenticationModule> uses to read and write cookies.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7e001-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="7e001-126">Remarks</span></span>  
 <span data-ttu-id="7e001-127">設定して、カスタム クッキー ハンドラーを指定する場合、`mode`の属性、`<cookieHandler>`要素"Custom"を含めることによって、カスタム クッキー ハンドラーの種類を指定する必要があります、`<customCookieHandler>`クッキー ハンドラーの型を参照する子要素。</span><span class="sxs-lookup"><span data-stu-id="7e001-127">When you specify a custom cookie handler by setting the `mode` attribute of the `<cookieHandler>` element to "Custom", you must specify the type of the custom cookie handler by including a `<customCookieHandler>` child element that references the cookie handler type.</span></span> <span data-ttu-id="7e001-128">この要素にすることはできないときに指定された、`mode`属性が"Chunked"または"Default"に設定します。</span><span class="sxs-lookup"><span data-stu-id="7e001-128">This element cannot be specified when the `mode` attribute is set to "Chunked" or "Default".</span></span> <span data-ttu-id="7e001-129">カスタム クッキー ハンドラーはから派生する必要があります、<xref:System.IdentityModel.Services.CookieHandler>クラス。</span><span class="sxs-lookup"><span data-stu-id="7e001-129">Custom cookie handlers must derive from the <xref:System.IdentityModel.Services.CookieHandler> class.</span></span>  
  
 <span data-ttu-id="7e001-130">`<customCookieHandler>`要素が表される、<xref:System.IdentityModel.Configuration.CustomTypeElement>クラス。</span><span class="sxs-lookup"><span data-stu-id="7e001-130">The `<customCookieHandler>` element is represented by the <xref:System.IdentityModel.Configuration.CustomTypeElement> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7e001-131">例</span><span class="sxs-lookup"><span data-stu-id="7e001-131">Example</span></span>  
 <span data-ttu-id="7e001-132">次の例では型のカスタム cookie ハンドラーを使用して SAM`MyNamespace.MyCustomCookieHandler`します。</span><span class="sxs-lookup"><span data-stu-id="7e001-132">The following example configures the SAM to use a custom cookie handler of type `MyNamespace.MyCustomCookieHandler`.</span></span>  
  
```xml  
<cookieHandler mode="Custom">  
    <customCookieHandler type="MyNamespace.MyCustomCookieHandler, MyAssembly" />  
</cookieHandler>  
```  
  
## <a name="see-also"></a><span data-ttu-id="7e001-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="7e001-133">See Also</span></span>  
 <xref:System.IdentityModel.Services.CookieHandler>
