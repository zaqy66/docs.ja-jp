---
title: '&lt;certificateValidator&gt;'
ms.date: 03/30/2017
ms.assetid: 86161897-c20f-4ad8-9d7f-050c247251bf
author: BrucePerlerMS
ms.openlocfilehash: 65b8aa6fa4422579ce0d1c5e33d3418ea051612a
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47236781"
---
# <a name="ltcertificatevalidatorgt"></a><span data-ttu-id="32882-102">&lt;certificateValidator&gt;</span><span class="sxs-lookup"><span data-stu-id="32882-102">&lt;certificateValidator&gt;</span></span>
<span data-ttu-id="32882-103">証明書の検証のカスタム型を指定します。</span><span class="sxs-lookup"><span data-stu-id="32882-103">Specifies a custom type for certificate validation.</span></span> <span data-ttu-id="32882-104">場合にのみ、この型が使用される、`certificateValidationMode`の属性、 [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md)要素が"Custom"に設定します。</span><span class="sxs-lookup"><span data-stu-id="32882-104">This type is used only if the `certificateValidationMode` attribute of the [\<certificateValidation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) element is set to "Custom".</span></span>  
  
 <span data-ttu-id="32882-105">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="32882-105">\<system.identityModel></span></span>  
<span data-ttu-id="32882-106">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="32882-106">\<identityConfiguration></span></span>  
<span data-ttu-id="32882-107">\<certificateValidation ></span><span class="sxs-lookup"><span data-stu-id="32882-107">\<certificateValidation></span></span>  
<span data-ttu-id="32882-108">\<certificateValidator ></span><span class="sxs-lookup"><span data-stu-id="32882-108">\<certificateValidator></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="32882-109">構文</span><span class="sxs-lookup"><span data-stu-id="32882-109">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <certificateValidation>  
      <certificateValidator type=xs:string>  
      </certificateValidator>  
    </certificateValidation>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="32882-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="32882-110">Attributes and Elements</span></span>  
 <span data-ttu-id="32882-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="32882-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="32882-112">属性</span><span class="sxs-lookup"><span data-stu-id="32882-112">Attributes</span></span>  
  
|<span data-ttu-id="32882-113">属性</span><span class="sxs-lookup"><span data-stu-id="32882-113">Attribute</span></span>|<span data-ttu-id="32882-114">説明</span><span class="sxs-lookup"><span data-stu-id="32882-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="32882-115">型</span><span class="sxs-lookup"><span data-stu-id="32882-115">type</span></span>|<span data-ttu-id="32882-116">派生したカスタム型を指定します、<xref:System.IdentityModel.Selectors.X509CertificateValidator>クラス。</span><span class="sxs-lookup"><span data-stu-id="32882-116">Specifies a custom type that derives from the <xref:System.IdentityModel.Selectors.X509CertificateValidator> class.</span></span> <span data-ttu-id="32882-117">設定、`certificateValidationMode`の属性、 [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md)要素がこの型を使用するには、"Custom"にします。</span><span class="sxs-lookup"><span data-stu-id="32882-117">Set the `certificateValidationMode` attribute of the [\<certificateValidation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) element to "Custom" to use this type.</span></span> <span data-ttu-id="32882-118">詳細を指定する方法については、`type`属性は、「[カスタム型の参照](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md)します。</span><span class="sxs-lookup"><span data-stu-id="32882-118">For more information about how to specify the `type` attribute, see [Custom Type References](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span> <span data-ttu-id="32882-119">任意。</span><span class="sxs-lookup"><span data-stu-id="32882-119">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="32882-120">子要素</span><span class="sxs-lookup"><span data-stu-id="32882-120">Child Elements</span></span>  
 <span data-ttu-id="32882-121">なし</span><span class="sxs-lookup"><span data-stu-id="32882-121">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="32882-122">親要素</span><span class="sxs-lookup"><span data-stu-id="32882-122">Parent Elements</span></span>  
  
|<span data-ttu-id="32882-123">要素</span><span class="sxs-lookup"><span data-stu-id="32882-123">Element</span></span>|<span data-ttu-id="32882-124">説明</span><span class="sxs-lookup"><span data-stu-id="32882-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="32882-125">\<certificateValidation ></span><span class="sxs-lookup"><span data-stu-id="32882-125">\<certificateValidation></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md)|<span data-ttu-id="32882-126">トークン ハンドラーを使用して証明書の検証の設定を制御します。</span><span class="sxs-lookup"><span data-stu-id="32882-126">Controls the settings that token handlers use to validate certificates.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="32882-127">例</span><span class="sxs-lookup"><span data-stu-id="32882-127">Example</span></span>  
  
```xml  
<certificateValidation certificateValidationMode="Custom"  
                       revocationMode="Online"  
                       trustedStoreLocation="LocalMachine">  
    <certificateValidator type="MyNamespace.CustomValidator, MyAssembly" />    
</certificateValidation>        
```
