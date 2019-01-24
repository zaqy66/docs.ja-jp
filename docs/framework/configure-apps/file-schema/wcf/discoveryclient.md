---
title: '&lt;discoveryClient&gt;'
ms.date: 03/30/2017
ms.assetid: a78f74c3-1152-4149-ab29-3f12d316caeb
ms.openlocfilehash: 5046d3342372960211942128372e9f62d98a2952
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54573086"
---
# <a name="ltdiscoveryclientgt"></a><span data-ttu-id="df751-102">&lt;discoveryClient&gt;</span><span class="sxs-lookup"><span data-stu-id="df751-102">&lt;discoveryClient&gt;</span></span>
<span data-ttu-id="df751-103">クライアント アプリケーションが実行時に探索可能なサービスを自動的に検索し、そのアドレスを見つけることができるカスタム バインドを作成するための構成要素。</span><span class="sxs-lookup"><span data-stu-id="df751-103">A configuration element for creating a custom binding that enables a client application to automatically search for a discoverable service and find its address at runtime.</span></span>  
  
<span data-ttu-id="df751-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="df751-104">\<system.serviceModel></span></span>  
<span data-ttu-id="df751-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="df751-105">\<bindings></span></span>  
<span data-ttu-id="df751-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="df751-106">\<customBinding></span></span>  
<span data-ttu-id="df751-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="df751-107">\<binding></span></span>  
<span data-ttu-id="df751-108">\<discoveryClient></span><span class="sxs-lookup"><span data-stu-id="df751-108">\<discoveryClient></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="df751-109">構文</span><span class="sxs-lookup"><span data-stu-id="df751-109">Syntax</span></span>  
  
```xml  
<discoveryClient discoveryEndpoint="String">
  <findCriteria duration="TimeSpan"
                maxResults="Integer"
                scopeMatchBy="Uri">
    <contractTypeNames>
      <add name="String"
           namespace="String" />
    </contractTypeNames>
    <extensions />
    <scopes>
      <add scope="URI"/>
    </scopes>
  </findCriteria>
</discoveryClient>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="df751-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="df751-110">Attributes and Elements</span></span>  
 <span data-ttu-id="df751-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="df751-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="df751-112">属性</span><span class="sxs-lookup"><span data-stu-id="df751-112">Attributes</span></span>  
  
|<span data-ttu-id="df751-113">属性</span><span class="sxs-lookup"><span data-stu-id="df751-113">Attribute</span></span>|<span data-ttu-id="df751-114">説明</span><span class="sxs-lookup"><span data-stu-id="df751-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="df751-115">discoveryEndpoint</span><span class="sxs-lookup"><span data-stu-id="df751-115">discoveryEndpoint</span></span>|<span data-ttu-id="df751-116">クライアント アプリケーションが実行時に探索可能なサービスを自動的に検索し、そのアドレスを見つけることができる探索エンドポイントの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="df751-116">A string that contains the name of the Discovery Endpoint that enables a client application to automatically search for a discoverable service and find its address at runtime.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="df751-117">子要素</span><span class="sxs-lookup"><span data-stu-id="df751-117">Child Elements</span></span>  
  
|<span data-ttu-id="df751-118">要素</span><span class="sxs-lookup"><span data-stu-id="df751-118">Element</span></span>|<span data-ttu-id="df751-119">説明</span><span class="sxs-lookup"><span data-stu-id="df751-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="df751-120">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="df751-120">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="df751-121">探索サービスの検索にクライアント アプリケーションによって使用される基準を提供する構成要素。</span><span class="sxs-lookup"><span data-stu-id="df751-121">A configuration element that supplies a set of criteria used by a client application to search for a discovery service.</span></span> <span data-ttu-id="df751-122">条件は、(探しているサービスの種類を指定して) 検索条件にグループ化することができ、検索 (検索持続期間)、終了条件。</span><span class="sxs-lookup"><span data-stu-id="df751-122">Criteria can be grouped into search criteria (specifying what services you’re looking for) and find termination criteria (how long the search should last).</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="df751-123">親要素</span><span class="sxs-lookup"><span data-stu-id="df751-123">Parent Elements</span></span>  
  
|<span data-ttu-id="df751-124">要素</span><span class="sxs-lookup"><span data-stu-id="df751-124">Element</span></span>|<span data-ttu-id="df751-125">説明</span><span class="sxs-lookup"><span data-stu-id="df751-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="df751-126">\<binding></span><span class="sxs-lookup"><span data-stu-id="df751-126">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="df751-127">カスタム バインドのすべてのバインド機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="df751-127">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="df751-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="df751-128">See also</span></span>
- <xref:System.ServiceModel.Discovery.DiscoveryClientBindingElement>
- <xref:System.ServiceModel.Discovery.Configuration.DiscoveryClientElement>
