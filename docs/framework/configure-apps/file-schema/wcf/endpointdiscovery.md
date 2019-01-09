---
title: '&lt;endpointDiscovery&gt;'
ms.date: 03/30/2017
ms.assetid: 70812717-888a-4748-9640-0df6715ff029
ms.openlocfilehash: 58bab9aef2e20d762c303e8b698214125531a136
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150917"
---
# <a name="ltendpointdiscoverygt"></a><span data-ttu-id="5c76f-102">&lt;endpointDiscovery&gt;</span><span class="sxs-lookup"><span data-stu-id="5c76f-102">&lt;endpointDiscovery&gt;</span></span>
<span data-ttu-id="5c76f-103">エンドポイントのさまざまな探索設定を指定します (探索可能性、スコープ、メタデータに対するカスタム拡張など)。</span><span class="sxs-lookup"><span data-stu-id="5c76f-103">Specifies the various discovery settings for an endpoint, such as its discoverability, scopes, and any custom extensions to its metadata.</span></span>  
  
<span data-ttu-id="5c76f-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="5c76f-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="5c76f-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="5c76f-105">\<behaviors></span></span>  
<span data-ttu-id="5c76f-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="5c76f-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="5c76f-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="5c76f-107">\<behavior></span></span>  
<span data-ttu-id="5c76f-108">\<endpointDiscovery ></span><span class="sxs-lookup"><span data-stu-id="5c76f-108">\<endpointDiscovery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5c76f-109">構文</span><span class="sxs-lookup"><span data-stu-id="5c76f-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="String">
      <endpointDiscovery enabled="Boolean">
        <scopes>
          <add scope="URI"/>
        </scopes>
        <extensions />
      </endpointDiscovery>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5c76f-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="5c76f-110">Attributes and Elements</span></span>  
 <span data-ttu-id="5c76f-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="5c76f-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5c76f-112">属性</span><span class="sxs-lookup"><span data-stu-id="5c76f-112">Attributes</span></span>  
  
|<span data-ttu-id="5c76f-113">属性</span><span class="sxs-lookup"><span data-stu-id="5c76f-113">Attribute</span></span>|<span data-ttu-id="5c76f-114">説明</span><span class="sxs-lookup"><span data-stu-id="5c76f-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5c76f-115">enabled</span><span class="sxs-lookup"><span data-stu-id="5c76f-115">enabled</span></span>|<span data-ttu-id="5c76f-116">このエンドポイントで見つけやすさが有効になっているかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="5c76f-116">A Boolean value that specifies whether discoverability is enabled on this endpoint.</span></span> <span data-ttu-id="5c76f-117">既定値は `false` です。</span><span class="sxs-lookup"><span data-stu-id="5c76f-117">The default is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5c76f-118">子要素</span><span class="sxs-lookup"><span data-stu-id="5c76f-118">Child Elements</span></span>  
  
|<span data-ttu-id="5c76f-119">要素</span><span class="sxs-lookup"><span data-stu-id="5c76f-119">Element</span></span>|<span data-ttu-id="5c76f-120">説明</span><span class="sxs-lookup"><span data-stu-id="5c76f-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5c76f-121">\<スコープ ></span><span class="sxs-lookup"><span data-stu-id="5c76f-121">\<scopes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)|<span data-ttu-id="5c76f-122">エンドポイントのスコープ URI のコレクション。</span><span class="sxs-lookup"><span data-stu-id="5c76f-122">A collection of scope URIs for the endpoint.</span></span> <span data-ttu-id="5c76f-123">複数の URI を 1 つのエンドポイントに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="5c76f-123">More than one scope Uris can be associated with a single endpoint.</span></span>|  
|<span data-ttu-id="5c76f-124">[\<拡張機能 >](../../../../../docs/framework/configure-apps/file-schema/wcf/extensions.md) [の\<endpointDiscovery >]</span><span class="sxs-lookup"><span data-stu-id="5c76f-124">[\<extensions>](../../../../../docs/framework/configure-apps/file-schema/wcf/extensions.md) [of \<endpointDiscovery>]</span></span>|<span data-ttu-id="5c76f-125">エンドポイントで発行されるカスタム メタデータを指定できる、XML 要素のコレクション。</span><span class="sxs-lookup"><span data-stu-id="5c76f-125">A collection of XML elements that allows you to specify custom metadata to be published for an endpoint.</span></span>|  
|<span data-ttu-id="5c76f-126">\<型 ></span><span class="sxs-lookup"><span data-stu-id="5c76f-126">\<types></span></span>|<span data-ttu-id="5c76f-127">検索するインターフェイスのコレクション。</span><span class="sxs-lookup"><span data-stu-id="5c76f-127">A collection of interfaces to search for.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5c76f-128">親要素</span><span class="sxs-lookup"><span data-stu-id="5c76f-128">Parent Elements</span></span>  
  
|<span data-ttu-id="5c76f-129">要素</span><span class="sxs-lookup"><span data-stu-id="5c76f-129">Element</span></span>|<span data-ttu-id="5c76f-130">説明</span><span class="sxs-lookup"><span data-stu-id="5c76f-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5c76f-131">\<behavior></span><span class="sxs-lookup"><span data-stu-id="5c76f-131">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="5c76f-132">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="5c76f-132">Specifies a behavior element.</span></span>|  
|||  
  
## <a name="remarks"></a><span data-ttu-id="5c76f-133">Remarks</span><span class="sxs-lookup"><span data-stu-id="5c76f-133">Remarks</span></span>  
 <span data-ttu-id="5c76f-134">エンドポイントの動作構成に追加し、`enabled` 属性を `true` に設定すると、この構成要素の探索可能性が有効になります。</span><span class="sxs-lookup"><span data-stu-id="5c76f-134">When added to the endpoint’s behavior configuration and with the `enabled` attribute set to `true`, this configuration element enables its discoverability.</span></span> <span data-ttu-id="5c76f-135">さらに、使用、 [\<スコープ >](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)カスタム スコープ クエリ中にサービス エンドポイントのフィルター処理に使用できる Uri を指定する子要素だけでなく[\<拡張機能 >](../../../../../docs/framework/configure-apps/file-schema/wcf/extensions.md) (EPR、ContractTypeName、BindingName、スコープおよび ListenURI) は、標準の探索可能なメタデータと共に発行する必要のあるカスタム メタデータを指定する子要素。</span><span class="sxs-lookup"><span data-stu-id="5c76f-135">In addition, you can use the [\<scopes>](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)child element to specifying custom scope Uris that can be used to filter service endpoints during query, as well as the [\<extensions>](../../../../../docs/framework/configure-apps/file-schema/wcf/extensions.md) child element to specify custom metadata that should be published along with the standard discoverable metadata (EPR, ContractTypeName, BindingName, Scope and ListenURI).</span></span>  
  
 <span data-ttu-id="5c76f-136">この構成要素に依存、 [ \<serviceDiscovery >](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md)探索可能性のサービス レベルの制御を提供する要素。</span><span class="sxs-lookup"><span data-stu-id="5c76f-136">This configuration element is dependent on the [\<serviceDiscovery>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md) element that provides the service level control of discoverability.</span></span> <span data-ttu-id="5c76f-137">場合、この要素の設定は無視されます、つまり[ \<serviceDiscovery >](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md)は、構成に存在しません。</span><span class="sxs-lookup"><span data-stu-id="5c76f-137">This means that this element’s settings are ignored if [\<serviceDiscovery>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md) is not present in the configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5c76f-138">例</span><span class="sxs-lookup"><span data-stu-id="5c76f-138">Example</span></span>  
 <span data-ttu-id="5c76f-139">次の構成例では、フィルターのスコープと、エンドポイントで発行される拡張メタデータを指定しています。</span><span class="sxs-lookup"><span data-stu-id="5c76f-139">The following configuration example specifies filtering scopes and extension metadata to be published for an endpoint.</span></span>  
  
```xml  
<services>
  <service name="CalculatorService"
           behaviorConfiguration="CalculatorServiceBehavior">
    <endpoint binding="basicHttpBinding"
              address="calculator"
              contract="ICalculatorService"
              behaviorConfiguration="calculatorEndpointBehavior" />
  </service>
</services>
<behaviors>
  <serviceBehaviors>
    <behavior name="CalculatorServiceBehavior">
      <serviceDiscovery />
    </behavior>
  </serviceBehaviors>
  <endpointBehaviors>
    <behavior name="calculatorEndpointBehavior">
      <endpointDiscovery enabled="true">
        <scopes>
          <add scope="http://contoso/test1" />
          <add scope="http://contoso/test2" />
        </scopes>
        <extensions>
          <e:Publisher xmlns:e="http://example.org">
            <e:Name>The Example Organization</e:Name>
            <e:Address>One Example Way, ExampleTown, EX 12345</e:Address>
            <e:Contact>support@example.org</e:Contact>
          </e:Publisher>
          <AnotherCustomMetadata>Custom Metadata</AnotherCustomMetadata>
        </extensions>
      </endpointDiscovery>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="5c76f-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c76f-140">See Also</span></span>  
 <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
