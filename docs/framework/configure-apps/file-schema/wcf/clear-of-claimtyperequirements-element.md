---
title: '&lt;claimTypeRequirements&gt; 要素の &lt;clear&gt;'
ms.date: 03/30/2017
ms.assetid: ef42fde7-f292-4610-9111-9fea382c3b5f
ms.openlocfilehash: c64e5450e01fdb011eb726f3bef1a85a5698d0d2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54568336"
---
# <a name="ltcleargt-of-ltclaimtyperequirementsgt-element"></a><span data-ttu-id="f324d-102">&lt;claimTypeRequirements&gt; 要素の &lt;clear&gt;</span><span class="sxs-lookup"><span data-stu-id="f324d-102">&lt;clear&gt; of &lt;claimTypeRequirements&gt; element</span></span>
<span data-ttu-id="f324d-103">すべてのクレームの種類をフェデレーション資格情報から削除するように指定します。</span><span class="sxs-lookup"><span data-stu-id="f324d-103">Specifies that all the claim types to be removed in the federated credential.</span></span> <span data-ttu-id="f324d-104">これにより、コレクションの初期値を確実に空にできます。</span><span class="sxs-lookup"><span data-stu-id="f324d-104">This ensures that the collection starts empty.</span></span>  
  
 <span data-ttu-id="f324d-105">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="f324d-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="f324d-106">\<bindings></span><span class="sxs-lookup"><span data-stu-id="f324d-106">\<bindings></span></span>  
<span data-ttu-id="f324d-107">\<wsFederatedBinding></span><span class="sxs-lookup"><span data-stu-id="f324d-107">\<wsFederatedBinding></span></span>  
<span data-ttu-id="f324d-108">\<binding></span><span class="sxs-lookup"><span data-stu-id="f324d-108">\<binding></span></span>  
<span data-ttu-id="f324d-109">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="f324d-109">\<security></span></span>  
<span data-ttu-id="f324d-110">\<message></span><span class="sxs-lookup"><span data-stu-id="f324d-110">\<message></span></span>  
<span data-ttu-id="f324d-111">\<claimTypeRequirements></span><span class="sxs-lookup"><span data-stu-id="f324d-111">\<claimTypeRequirements></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f324d-112">構文</span><span class="sxs-lookup"><span data-stu-id="f324d-112">Syntax</span></span>  
  
```xml  
<claimTypeRequirements>
  <clear />
</claimTypeRequirements>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f324d-113">属性および要素</span><span class="sxs-lookup"><span data-stu-id="f324d-113">Attributes and Elements</span></span>  
 <span data-ttu-id="f324d-114">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="f324d-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f324d-115">属性</span><span class="sxs-lookup"><span data-stu-id="f324d-115">Attributes</span></span>  
 <span data-ttu-id="f324d-116">なし。</span><span class="sxs-lookup"><span data-stu-id="f324d-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="f324d-117">子要素</span><span class="sxs-lookup"><span data-stu-id="f324d-117">Child Elements</span></span>  
 <span data-ttu-id="f324d-118">なし。</span><span class="sxs-lookup"><span data-stu-id="f324d-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f324d-119">親要素</span><span class="sxs-lookup"><span data-stu-id="f324d-119">Parent Elements</span></span>  
  
|<span data-ttu-id="f324d-120">要素</span><span class="sxs-lookup"><span data-stu-id="f324d-120">Element</span></span>|<span data-ttu-id="f324d-121">説明</span><span class="sxs-lookup"><span data-stu-id="f324d-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f324d-122">\<claimTypeRequirements></span><span class="sxs-lookup"><span data-stu-id="f324d-122">\<claimTypeRequirements></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/claimtyperequirements-for-message.md)|<span data-ttu-id="f324d-123">必須のクレームの種類のコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="f324d-123">Specifies a collection of required claim types.</span></span> <span data-ttu-id="f324d-124">各要素は <xref:System.ServiceModel.Configuration.ClaimTypeElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="f324d-124">Each element is of type <xref:System.ServiceModel.Configuration.ClaimTypeElement>.</span></span><br /><br /> <span data-ttu-id="f324d-125">フェデレーション シナリオでは、サービスが受信資格情報についての要件を記述します。</span><span class="sxs-lookup"><span data-stu-id="f324d-125">In a federated scenario, services state the requirements on incoming credentials.</span></span> <span data-ttu-id="f324d-126">たとえば、受信資格情報は、特定のクレーム タイプのセットを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f324d-126">For example, the incoming credentials must possess a certain set of claim types.</span></span> <span data-ttu-id="f324d-127">このコレクションの要素はそれぞれ、フェデレーション資格情報に表示されると予想される必須の要求および省略可能な要求の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="f324d-127">Each element in this collection specifies the types of required and optional claims expected to appear in a federated credential.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f324d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="f324d-128">See also</span></span>
- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Security.Tokens.ClaimTypeRequirement>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Configuration.ClaimTypeElementCollection>
- <xref:System.ServiceModel.Configuration.ClaimTypeElement>
