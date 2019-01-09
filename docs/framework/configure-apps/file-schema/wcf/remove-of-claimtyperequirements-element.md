---
title: '&lt;claimTypeRequirements&gt; 要素の &lt;remove&gt;'
ms.date: 03/30/2017
ms.assetid: 8ef05bc4-1950-4ee4-95c5-1c6a394eff7e
ms.openlocfilehash: 7610a8e95996f15133ae58ec33c4afd9e2309cac
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146213"
---
# <a name="ltremovegt-of-ltclaimtyperequirementsgt-element"></a><span data-ttu-id="eaa25-102">&lt;claimTypeRequirements&gt; 要素の &lt;remove&gt;</span><span class="sxs-lookup"><span data-stu-id="eaa25-102">&lt;remove&gt; of &lt;claimTypeRequirements&gt; element</span></span>
<span data-ttu-id="eaa25-103">フェデレーション資格情報から削除するクレームの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="eaa25-103">Specifies the types of claims to be removed in the federated credential.</span></span>  
  
 <span data-ttu-id="eaa25-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="eaa25-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="eaa25-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="eaa25-105">\<bindings></span></span>  
<span data-ttu-id="eaa25-106">\<wsFederatedBinding></span><span class="sxs-lookup"><span data-stu-id="eaa25-106">\<wsFederatedBinding></span></span>  
<span data-ttu-id="eaa25-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="eaa25-107">\<binding></span></span>  
<span data-ttu-id="eaa25-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="eaa25-108">\<security></span></span>  
<span data-ttu-id="eaa25-109">\<message></span><span class="sxs-lookup"><span data-stu-id="eaa25-109">\<message></span></span>  
<span data-ttu-id="eaa25-110">\<claimTypeRequirements ></span><span class="sxs-lookup"><span data-stu-id="eaa25-110">\<claimTypeRequirements></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eaa25-111">構文</span><span class="sxs-lookup"><span data-stu-id="eaa25-111">Syntax</span></span>  
  
```xml  
<claimTypeRequirements>
  <remove claimType="URI" />
</claimTypeRequirements>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="eaa25-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="eaa25-112">Attributes and Elements</span></span>  
 <span data-ttu-id="eaa25-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="eaa25-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="eaa25-114">属性</span><span class="sxs-lookup"><span data-stu-id="eaa25-114">Attributes</span></span>  
  
|<span data-ttu-id="eaa25-115">属性</span><span class="sxs-lookup"><span data-stu-id="eaa25-115">Attribute</span></span>|<span data-ttu-id="eaa25-116">説明</span><span class="sxs-lookup"><span data-stu-id="eaa25-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="eaa25-117">claimType</span><span class="sxs-lookup"><span data-stu-id="eaa25-117">claimType</span></span>|<span data-ttu-id="eaa25-118">削除するクレームの種類を定義する URI。</span><span class="sxs-lookup"><span data-stu-id="eaa25-118">A URI that defines the type of a claim to be removed.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="eaa25-119">子要素</span><span class="sxs-lookup"><span data-stu-id="eaa25-119">Child Elements</span></span>  
 <span data-ttu-id="eaa25-120">なし。</span><span class="sxs-lookup"><span data-stu-id="eaa25-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="eaa25-121">親要素</span><span class="sxs-lookup"><span data-stu-id="eaa25-121">Parent Elements</span></span>  
  
|<span data-ttu-id="eaa25-122">要素</span><span class="sxs-lookup"><span data-stu-id="eaa25-122">Element</span></span>|<span data-ttu-id="eaa25-123">説明</span><span class="sxs-lookup"><span data-stu-id="eaa25-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="eaa25-124">\<claimTypeRequirements></span><span class="sxs-lookup"><span data-stu-id="eaa25-124">\<claimTypeRequirements></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/claimtyperequirements-for-message.md)|<span data-ttu-id="eaa25-125">必須のクレームの種類のコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="eaa25-125">Specifies a collection of required claim types.</span></span> <span data-ttu-id="eaa25-126">各要素は <xref:System.ServiceModel.Configuration.ClaimTypeElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="eaa25-126">Each element is of type <xref:System.ServiceModel.Configuration.ClaimTypeElement>.</span></span><br /><br /> <span data-ttu-id="eaa25-127">フェデレーション シナリオでは、サービスが受信資格情報についての要件を記述します。</span><span class="sxs-lookup"><span data-stu-id="eaa25-127">In a federated scenario, services state the requirements on incoming credentials.</span></span> <span data-ttu-id="eaa25-128">たとえば、受信資格情報は、特定のクレーム タイプのセットを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaa25-128">For example, the incoming credentials must possess a certain set of claim types.</span></span> <span data-ttu-id="eaa25-129">このコレクションの要素はそれぞれ、フェデレーション資格情報に表示されると予想される必須の要求および省略可能な要求の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="eaa25-129">Each element in this collection specifies the types of required and optional claims expected to appear in a federated credential.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="eaa25-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="eaa25-130">See Also</span></span>  
 <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.ClaimTypeRequirements%2A>  
 <xref:System.ServiceModel.Security.Tokens.ClaimTypeRequirement>  
 <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.ClaimTypeRequirements%2A>  
 <xref:System.ServiceModel.Configuration.ClaimTypeElementCollection>  
 <xref:System.ServiceModel.Configuration.ClaimTypeElement>
