---
title: '&lt;enableWebScript&gt;'
ms.date: 03/30/2017
ms.assetid: 9c7e96e1-af70-4e6e-ac5c-d67929dddbaa
ms.openlocfilehash: 1115b598776ca7d28698815974e06f3de57be598
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54600103"
---
# <a name="ltenablewebscriptgt"></a><span data-ttu-id="4d17f-102">&lt;enableWebScript&gt;</span><span class="sxs-lookup"><span data-stu-id="4d17f-102">&lt;enableWebScript&gt;</span></span>
<span data-ttu-id="4d17f-103">この要素は、ASP.NET AJAX Web ページからサービスを使用できるようにするエンドポイントの動作を有効にします。</span><span class="sxs-lookup"><span data-stu-id="4d17f-103">This element enables the endpoint behavior that makes it possible to consume the service from ASP.NET AJAX web pages.</span></span>  
  
 <span data-ttu-id="4d17f-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="4d17f-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="4d17f-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="4d17f-105">\<behaviors></span></span>  
<span data-ttu-id="4d17f-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="4d17f-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="4d17f-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="4d17f-107">\<behavior></span></span>  
<span data-ttu-id="4d17f-108">\<enableWebScript></span><span class="sxs-lookup"><span data-stu-id="4d17f-108">\<enableWebScript></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4d17f-109">構文</span><span class="sxs-lookup"><span data-stu-id="4d17f-109">Syntax</span></span>  
  
```xml  
<enableWebScript />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4d17f-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="4d17f-110">Attributes and Elements</span></span>  
 <span data-ttu-id="4d17f-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="4d17f-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4d17f-112">属性</span><span class="sxs-lookup"><span data-stu-id="4d17f-112">Attributes</span></span>  
 <span data-ttu-id="4d17f-113">なし。</span><span class="sxs-lookup"><span data-stu-id="4d17f-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4d17f-114">子要素</span><span class="sxs-lookup"><span data-stu-id="4d17f-114">Child Elements</span></span>  
 <span data-ttu-id="4d17f-115">なし。</span><span class="sxs-lookup"><span data-stu-id="4d17f-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4d17f-116">親要素</span><span class="sxs-lookup"><span data-stu-id="4d17f-116">Parent Elements</span></span>  
  
|<span data-ttu-id="4d17f-117">要素</span><span class="sxs-lookup"><span data-stu-id="4d17f-117">Element</span></span>|<span data-ttu-id="4d17f-118">説明</span><span class="sxs-lookup"><span data-stu-id="4d17f-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4d17f-119">\<behavior></span><span class="sxs-lookup"><span data-stu-id="4d17f-119">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="4d17f-120">エンドポイントの動作のセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="4d17f-120">Specifies the set of endpoint behaviors.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4d17f-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="4d17f-121">Remarks</span></span>  
 <span data-ttu-id="4d17f-122">この動作は、いずれかと組み合わせてのみ使用する必要があります、 [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md)標準バインディングまたは[ \<webMessageEncoding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webmessageencoding.md)バインド要素。</span><span class="sxs-lookup"><span data-stu-id="4d17f-122">This behavior should only be used in conjunction with either the [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) standard binding, or the [\<webMessageEncoding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webmessageencoding.md) binding element.</span></span>  <span data-ttu-id="4d17f-123">この動作の詳細については、「<xref:System.ServiceModel.Description.WebScriptEnablingBehavior>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d17f-123">For more information on this behavior, see <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4d17f-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="4d17f-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.WebScriptEnablingElement>
- <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>
- [<span data-ttu-id="4d17f-125">AJAX の統合と JSON のサポート</span><span class="sxs-lookup"><span data-stu-id="4d17f-125">AJAX Integration and JSON Support</span></span>](../../../../../docs/framework/wcf/feature-details/ajax-integration-and-json-support.md)
- [<span data-ttu-id="4d17f-126">\<webHttp></span><span class="sxs-lookup"><span data-stu-id="4d17f-126">\<webHttp></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md)
