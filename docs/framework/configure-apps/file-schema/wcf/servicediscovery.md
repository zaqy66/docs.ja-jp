---
title: '&lt;serviceDiscovery&gt;'
ms.date: 03/30/2017
ms.assetid: a3c68a4a-fc95-43c5-aacb-785936c0cf39
ms.openlocfilehash: 2b3061274ef670ccd672c3155ca7285d567834bd
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146902"
---
# <a name="ltservicediscoverygt"></a><span data-ttu-id="c4779-102">&lt;serviceDiscovery&gt;</span><span class="sxs-lookup"><span data-stu-id="c4779-102">&lt;serviceDiscovery&gt;</span></span>
<span data-ttu-id="c4779-103">サービス エンドポイントの探索可能性を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4779-103">Specifies the discoverability of service endpoints.</span></span>  
  
 <span data-ttu-id="c4779-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="c4779-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="c4779-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="c4779-105">\<behaviors></span></span>  
<span data-ttu-id="c4779-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="c4779-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="c4779-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="c4779-107">\<behavior></span></span>  
<span data-ttu-id="c4779-108">\<serviceDiscovery ></span><span class="sxs-lookup"><span data-stu-id="c4779-108">\<serviceDiscovery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4779-109">構文</span><span class="sxs-lookup"><span data-stu-id="c4779-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <serviceDiscovery>
        <announcementEndpoints>
          <endpoint name="String"
                    kind="Type" />
        </announcementEndpoints>
        <discoveryEndpoints>
          <endpoint name="String"
                    kind="Type" />
        </discoveryEndpoints>
      </serviceDiscovery>
    </behavior>
  </serviceBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c4779-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="c4779-110">Attributes and Elements</span></span>  
 <span data-ttu-id="c4779-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="c4779-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c4779-112">属性</span><span class="sxs-lookup"><span data-stu-id="c4779-112">Attributes</span></span>  
 <span data-ttu-id="c4779-113">なし。</span><span class="sxs-lookup"><span data-stu-id="c4779-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="c4779-114">子要素</span><span class="sxs-lookup"><span data-stu-id="c4779-114">Child Elements</span></span>  
  
|<span data-ttu-id="c4779-115">要素</span><span class="sxs-lookup"><span data-stu-id="c4779-115">Element</span></span>|<span data-ttu-id="c4779-116">説明</span><span class="sxs-lookup"><span data-stu-id="c4779-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c4779-117">\<announcementEndpoint ></span><span class="sxs-lookup"><span data-stu-id="c4779-117">\<announcementEndpoint></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md)|<span data-ttu-id="c4779-118">アナウンス エンドポイントのコレクション。</span><span class="sxs-lookup"><span data-stu-id="c4779-118">A collection of announcement endpoints.</span></span> <span data-ttu-id="c4779-119">このセクションを使用して、アナウンス メッセージの送信に使用するエンドポイントを指定します。</span><span class="sxs-lookup"><span data-stu-id="c4779-119">Use this section to specify the endpoints to use for sending announcement messages.</span></span>|  
|[<span data-ttu-id="c4779-120">\<discoveryEndpoint ></span><span class="sxs-lookup"><span data-stu-id="c4779-120">\<discoveryEndpoint></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md)|<span data-ttu-id="c4779-121">探索エンドポイントのコレクション。</span><span class="sxs-lookup"><span data-stu-id="c4779-121">A collection of discovery endpoints.</span></span> <span data-ttu-id="c4779-122">このセクションを使用して、探索メッセージをリッスンするエンドポイントを指定します。</span><span class="sxs-lookup"><span data-stu-id="c4779-122">Use this section to specify the endpoints on which to listen for the discovery messages.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c4779-123">親要素</span><span class="sxs-lookup"><span data-stu-id="c4779-123">Parent Elements</span></span>  
  
|<span data-ttu-id="c4779-124">要素</span><span class="sxs-lookup"><span data-stu-id="c4779-124">Element</span></span>|<span data-ttu-id="c4779-125">説明</span><span class="sxs-lookup"><span data-stu-id="c4779-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c4779-126">\<behavior></span><span class="sxs-lookup"><span data-stu-id="c4779-126">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="c4779-127">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4779-127">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c4779-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="c4779-128">Remarks</span></span>  
 <span data-ttu-id="c4779-129">サービスの動作構成に追加すると、この構成要素により、サービスの探索可能性はすべてのエンドポイントで有効になります。</span><span class="sxs-lookup"><span data-stu-id="c4779-129">When added to the service’s behavior configuration, this configuration element makes all of the endpoints of that service discoverable.</span></span> <span data-ttu-id="c4779-130">使用してこのようなエンドポイントの探索機能をさらに構成できる、 [ \<discoveryEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md)または[ \<announcementEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md)子要素。</span><span class="sxs-lookup"><span data-stu-id="c4779-130">You can further configure the discovery features of such endpoints by using the [\<discoveryEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md) or [\<announcementEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md) child elements.</span></span> <span data-ttu-id="c4779-131">使用して、 [ \<announcementEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md)サービス アナウンス (こんにちは/オンラインおよびオフライン/Bye) の送信に使用するエンドポイント構成を指定して、アナウンスを構成するセクション。</span><span class="sxs-lookup"><span data-stu-id="c4779-131">Use the [\<announcementEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md) section to configure the announcements by specifying the endpoint configuration to be use to send service announcements (online/Hello and offline/Bye).</span></span> <span data-ttu-id="c4779-132">使用して、 [ \<discoveryEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md)セクションを手動で探索メッセージをリッスンするエンドポイントを指定します。</span><span class="sxs-lookup"><span data-stu-id="c4779-132">Use the [\<discoveryEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md) section to manually specify the endpoint on which to listen for the discovery messages.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c4779-133">例</span><span class="sxs-lookup"><span data-stu-id="c4779-133">Example</span></span>  
 <span data-ttu-id="c4779-134">次の構成例では、CalculatorService を探索可能に指定しています。また、オプションで、使用するアナウンス エンドポイントを指定しています。</span><span class="sxs-lookup"><span data-stu-id="c4779-134">The following configuration example specifies that the CalculatorService to be discoverable, and optionally specifies the announcement endpoint to be used.</span></span>  
  
```xml  
<services>
  <service name="CalculatorService"
           behaviorConfiguration="CalculatorServiceBehavior">
    ...
  </service>
</services>
<behaviors>
  <serviceBehaviors>
    <behavior name="CalculatorServiceBehavior">
      <serviceDiscovery>
        <announcementEndpoints>
          <endpoint name="udpEndpoint"
                    kind="udpAnnouncementEndpoint" />
        </announcementEndpoints>
      </serviceDiscovery>
    </behavior>
  </serviceBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="c4779-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="c4779-135">See Also</span></span>  
 <xref:System.ServiceModel.Discovery.ServiceDiscoveryBehavior>
