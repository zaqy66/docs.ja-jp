---
title: '&lt;policyImporter&gt;'
ms.date: 03/30/2017
ms.assetid: b0d03456-546f-44bb-ab12-1b2ce7f98fca
ms.openlocfilehash: 22d90ff9d0cd5325300cf42437836f075cbf8c31
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148488"
---
# <a name="ltpolicyimportergt"></a><span data-ttu-id="2c7c7-102">&lt;policyImporter&gt;</span><span class="sxs-lookup"><span data-stu-id="2c7c7-102">&lt;policyImporter&gt;</span></span>
<span data-ttu-id="2c7c7-103">バインディングに関するカスタム ポリシー アサーションのインポートを制御するポリシー インポーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="2c7c7-103">Specifies a policy importer that controls the import of custom policy assertions about bindings.</span></span>  
  
 <span data-ttu-id="2c7c7-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="2c7c7-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="2c7c7-105">\<client></span><span class="sxs-lookup"><span data-stu-id="2c7c7-105">\<client></span></span>  
<span data-ttu-id="2c7c7-106">\<matadata></span><span class="sxs-lookup"><span data-stu-id="2c7c7-106">\<metadata></span></span>  
<span data-ttu-id="2c7c7-107">\<policyImporters ></span><span class="sxs-lookup"><span data-stu-id="2c7c7-107">\<policyImporters></span></span>  
<span data-ttu-id="2c7c7-108">\<policyImporter ></span><span class="sxs-lookup"><span data-stu-id="2c7c7-108">\<policyImporter></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2c7c7-109">構文</span><span class="sxs-lookup"><span data-stu-id="2c7c7-109">Syntax</span></span>  
  
```xml  
<metadata>
  <policyImporters>
    <policyImporter type="String" />
  </policyImporters>
</metadata>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2c7c7-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="2c7c7-110">Attributes and Elements</span></span>  
 <span data-ttu-id="2c7c7-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="2c7c7-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2c7c7-112">属性</span><span class="sxs-lookup"><span data-stu-id="2c7c7-112">Attributes</span></span>  
  
|<span data-ttu-id="2c7c7-113">属性</span><span class="sxs-lookup"><span data-stu-id="2c7c7-113">Attribute</span></span>|<span data-ttu-id="2c7c7-114">説明</span><span class="sxs-lookup"><span data-stu-id="2c7c7-114">Description</span></span>|  
|---------------|-----------------|  
|`type`|<span data-ttu-id="2c7c7-115">この要素の型です。</span><span class="sxs-lookup"><span data-stu-id="2c7c7-115">The type of this element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2c7c7-116">子要素</span><span class="sxs-lookup"><span data-stu-id="2c7c7-116">Child Elements</span></span>  
 <span data-ttu-id="2c7c7-117">なし</span><span class="sxs-lookup"><span data-stu-id="2c7c7-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2c7c7-118">親要素</span><span class="sxs-lookup"><span data-stu-id="2c7c7-118">Parent Elements</span></span>  
  
|<span data-ttu-id="2c7c7-119">要素</span><span class="sxs-lookup"><span data-stu-id="2c7c7-119">Element</span></span>|<span data-ttu-id="2c7c7-120">説明</span><span class="sxs-lookup"><span data-stu-id="2c7c7-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2c7c7-121">\<policyImporters ></span><span class="sxs-lookup"><span data-stu-id="2c7c7-121">\<policyImporters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/policyimporters.md)|<span data-ttu-id="2c7c7-122">バインディングに関するカスタム ポリシー アサーションのインポートを制御するすべてのポリシー インポーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="2c7c7-122">Specifies all the policy importers that control the import of custom policy assertions about bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2c7c7-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="2c7c7-123">Remarks</span></span>  
 <span data-ttu-id="2c7c7-124">ポリシー インポーターは、バインディング機能についてのカスタム ポリシー アサーションの検索、およびアサーションで必要となる機能を実装するカスタム バインディング要素の結び付けに使用されます。</span><span class="sxs-lookup"><span data-stu-id="2c7c7-124">A policy importer is used to search custom policy assertions about binding features, as well as attach a custom binding element that implements the features the assertion requires.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c7c7-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="2c7c7-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PolicyImporterElementCollection>  
 <xref:System.ServiceModel.Configuration.PolicyImporterElement>  
 <xref:System.ServiceModel.Configuration.MetadataElement>  
 <xref:System.ServiceModel.Description.MetadataImporter>  
 [<span data-ttu-id="2c7c7-126">WCF クライアントの構成</span><span class="sxs-lookup"><span data-stu-id="2c7c7-126">WCF Client Configuration</span></span>](../../../../../docs/framework/wcf/feature-details/client-configuration.md)  
 [<span data-ttu-id="2c7c7-127">クライアント</span><span class="sxs-lookup"><span data-stu-id="2c7c7-127">Clients</span></span>](../../../../../docs/framework/wcf/feature-details/clients.md)
