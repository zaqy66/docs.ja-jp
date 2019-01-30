---
title: <certificateValidator>
ms.date: 03/30/2017
ms.assetid: 86161897-c20f-4ad8-9d7f-050c247251bf
author: BrucePerlerMS
ms.openlocfilehash: df52212305e0865b8c03fdd49068cb7c7da4fa38
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55277454"
---
# <a name="certificatevalidator"></a><span data-ttu-id="16a3a-101">\<certificateValidator ></span><span class="sxs-lookup"><span data-stu-id="16a3a-101">\<certificateValidator></span></span>
<span data-ttu-id="16a3a-102">証明書の検証のカスタム型を指定します。</span><span class="sxs-lookup"><span data-stu-id="16a3a-102">Specifies a custom type for certificate validation.</span></span> <span data-ttu-id="16a3a-103">場合にのみ、この型が使用される、`certificateValidationMode`の属性、 [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md)要素が"Custom"に設定します。</span><span class="sxs-lookup"><span data-stu-id="16a3a-103">This type is used only if the `certificateValidationMode` attribute of the [\<certificateValidation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) element is set to "Custom".</span></span>  
  
 <span data-ttu-id="16a3a-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="16a3a-104">\<system.identityModel></span></span>  
<span data-ttu-id="16a3a-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="16a3a-105">\<identityConfiguration></span></span>  
<span data-ttu-id="16a3a-106">\<certificateValidation></span><span class="sxs-lookup"><span data-stu-id="16a3a-106">\<certificateValidation></span></span>  
<span data-ttu-id="16a3a-107">\<certificateValidator ></span><span class="sxs-lookup"><span data-stu-id="16a3a-107">\<certificateValidator></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="16a3a-108">構文</span><span class="sxs-lookup"><span data-stu-id="16a3a-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="16a3a-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="16a3a-109">Attributes and Elements</span></span>  
 <span data-ttu-id="16a3a-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="16a3a-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="16a3a-111">属性</span><span class="sxs-lookup"><span data-stu-id="16a3a-111">Attributes</span></span>  
  
|<span data-ttu-id="16a3a-112">属性</span><span class="sxs-lookup"><span data-stu-id="16a3a-112">Attribute</span></span>|<span data-ttu-id="16a3a-113">説明</span><span class="sxs-lookup"><span data-stu-id="16a3a-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="16a3a-114">型</span><span class="sxs-lookup"><span data-stu-id="16a3a-114">type</span></span>|<span data-ttu-id="16a3a-115">派生したカスタム型を指定します、<xref:System.IdentityModel.Selectors.X509CertificateValidator>クラス。</span><span class="sxs-lookup"><span data-stu-id="16a3a-115">Specifies a custom type that derives from the <xref:System.IdentityModel.Selectors.X509CertificateValidator> class.</span></span> <span data-ttu-id="16a3a-116">設定、`certificateValidationMode`の属性、 [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md)要素がこの型を使用するには、"Custom"にします。</span><span class="sxs-lookup"><span data-stu-id="16a3a-116">Set the `certificateValidationMode` attribute of the [\<certificateValidation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) element to "Custom" to use this type.</span></span> <span data-ttu-id="16a3a-117">詳細を指定する方法については、`type`属性は、「[カスタム型の参照](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md)します。</span><span class="sxs-lookup"><span data-stu-id="16a3a-117">For more information about how to specify the `type` attribute, see [Custom Type References](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span> <span data-ttu-id="16a3a-118">任意。</span><span class="sxs-lookup"><span data-stu-id="16a3a-118">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="16a3a-119">子要素</span><span class="sxs-lookup"><span data-stu-id="16a3a-119">Child Elements</span></span>  
 <span data-ttu-id="16a3a-120">なし</span><span class="sxs-lookup"><span data-stu-id="16a3a-120">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="16a3a-121">親要素</span><span class="sxs-lookup"><span data-stu-id="16a3a-121">Parent Elements</span></span>  
  
|<span data-ttu-id="16a3a-122">要素</span><span class="sxs-lookup"><span data-stu-id="16a3a-122">Element</span></span>|<span data-ttu-id="16a3a-123">説明</span><span class="sxs-lookup"><span data-stu-id="16a3a-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="16a3a-124">\<certificateValidation></span><span class="sxs-lookup"><span data-stu-id="16a3a-124">\<certificateValidation></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md)|<span data-ttu-id="16a3a-125">トークン ハンドラーを使用して証明書の検証の設定を制御します。</span><span class="sxs-lookup"><span data-stu-id="16a3a-125">Controls the settings that token handlers use to validate certificates.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="16a3a-126">例</span><span class="sxs-lookup"><span data-stu-id="16a3a-126">Example</span></span>  
  
```xml  
<certificateValidation certificateValidationMode="Custom"  
                       revocationMode="Online"  
                       trustedStoreLocation="LocalMachine">  
    <certificateValidator type="MyNamespace.CustomValidator, MyAssembly" />    
</certificateValidation>        
```
