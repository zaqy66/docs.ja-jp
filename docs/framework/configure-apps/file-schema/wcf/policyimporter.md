---
title: '&lt;policyImporter&gt;'
ms.date: 03/30/2017
ms.assetid: b0d03456-546f-44bb-ab12-1b2ce7f98fca
ms.openlocfilehash: 4075f7fcb1c65da3d9e2e5e5dab52452ca2c9b60
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54632167"
---
# <a name="ltpolicyimportergt"></a><span data-ttu-id="2aed2-102">&lt;policyImporter&gt;</span><span class="sxs-lookup"><span data-stu-id="2aed2-102">&lt;policyImporter&gt;</span></span>
<span data-ttu-id="2aed2-103">バインディングに関するカスタム ポリシー アサーションのインポートを制御するポリシー インポーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="2aed2-103">Specifies a policy importer that controls the import of custom policy assertions about bindings.</span></span>  
  
 <span data-ttu-id="2aed2-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="2aed2-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="2aed2-105">\<client></span><span class="sxs-lookup"><span data-stu-id="2aed2-105">\<client></span></span>  
<span data-ttu-id="2aed2-106">\<matadata></span><span class="sxs-lookup"><span data-stu-id="2aed2-106">\<metadata></span></span>  
<span data-ttu-id="2aed2-107">\<policyImporters></span><span class="sxs-lookup"><span data-stu-id="2aed2-107">\<policyImporters></span></span>  
<span data-ttu-id="2aed2-108">\<policyImporter></span><span class="sxs-lookup"><span data-stu-id="2aed2-108">\<policyImporter></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2aed2-109">構文</span><span class="sxs-lookup"><span data-stu-id="2aed2-109">Syntax</span></span>  
  
```xml  
<metadata>
  <policyImporters>
    <policyImporter type="String" />
  </policyImporters>
</metadata>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2aed2-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="2aed2-110">Attributes and Elements</span></span>  
 <span data-ttu-id="2aed2-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="2aed2-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2aed2-112">属性</span><span class="sxs-lookup"><span data-stu-id="2aed2-112">Attributes</span></span>  
  
|<span data-ttu-id="2aed2-113">属性</span><span class="sxs-lookup"><span data-stu-id="2aed2-113">Attribute</span></span>|<span data-ttu-id="2aed2-114">説明</span><span class="sxs-lookup"><span data-stu-id="2aed2-114">Description</span></span>|  
|---------------|-----------------|  
|`type`|<span data-ttu-id="2aed2-115">この要素の型です。</span><span class="sxs-lookup"><span data-stu-id="2aed2-115">The type of this element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2aed2-116">子要素</span><span class="sxs-lookup"><span data-stu-id="2aed2-116">Child Elements</span></span>  
 <span data-ttu-id="2aed2-117">なし</span><span class="sxs-lookup"><span data-stu-id="2aed2-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2aed2-118">親要素</span><span class="sxs-lookup"><span data-stu-id="2aed2-118">Parent Elements</span></span>  
  
|<span data-ttu-id="2aed2-119">要素</span><span class="sxs-lookup"><span data-stu-id="2aed2-119">Element</span></span>|<span data-ttu-id="2aed2-120">説明</span><span class="sxs-lookup"><span data-stu-id="2aed2-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2aed2-121">\<policyImporters></span><span class="sxs-lookup"><span data-stu-id="2aed2-121">\<policyImporters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/policyimporters.md)|<span data-ttu-id="2aed2-122">バインディングに関するカスタム ポリシー アサーションのインポートを制御するすべてのポリシー インポーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="2aed2-122">Specifies all the policy importers that control the import of custom policy assertions about bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2aed2-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="2aed2-123">Remarks</span></span>  
 <span data-ttu-id="2aed2-124">ポリシー インポーターは、バインディング機能についてのカスタム ポリシー アサーションの検索、およびアサーションで必要となる機能を実装するカスタム バインディング要素の結び付けに使用されます。</span><span class="sxs-lookup"><span data-stu-id="2aed2-124">A policy importer is used to search custom policy assertions about binding features, as well as attach a custom binding element that implements the features the assertion requires.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2aed2-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="2aed2-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.PolicyImporterElementCollection>
- <xref:System.ServiceModel.Configuration.PolicyImporterElement>
- <xref:System.ServiceModel.Configuration.MetadataElement>
- <xref:System.ServiceModel.Description.MetadataImporter>
- [<span data-ttu-id="2aed2-126">WCF クライアントの構成</span><span class="sxs-lookup"><span data-stu-id="2aed2-126">WCF Client Configuration</span></span>](../../../../../docs/framework/wcf/feature-details/client-configuration.md)
- [<span data-ttu-id="2aed2-127">クライアント</span><span class="sxs-lookup"><span data-stu-id="2aed2-127">Clients</span></span>](../../../../../docs/framework/wcf/feature-details/clients.md)
