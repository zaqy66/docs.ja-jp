---
title: <scopes>
ms.date: 03/30/2017
ms.assetid: 9a0dd3ce-e383-4ac3-b7be-7d604388304a
ms.openlocfilehash: eee6382c578648866045fd9b283454d9e0e76fcb
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55275025"
---
# <a name="scopes"></a><span data-ttu-id="ba658-101">\<scopes></span><span class="sxs-lookup"><span data-stu-id="ba658-101">\<scopes></span></span>
<span data-ttu-id="ba658-102">クエリの実行中に、サービス エンドポイントのフィルター処理に使用できるカスタム スコープ URI を指定する構成要素のコレクションを含んでいます。</span><span class="sxs-lookup"><span data-stu-id="ba658-102">Contains a collection of configuration elements that specify custom scope Uris that can be used to filter service endpoints during query.</span></span>  
  
<span data-ttu-id="ba658-103">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="ba658-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="ba658-104">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="ba658-104">\<behaviors></span></span>  
<span data-ttu-id="ba658-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="ba658-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="ba658-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="ba658-106">\<behavior></span></span>  
<span data-ttu-id="ba658-107">\<endpointDiscovery></span><span class="sxs-lookup"><span data-stu-id="ba658-107">\<endpointDiscovery></span></span>  
<span data-ttu-id="ba658-108">\<scopes></span><span class="sxs-lookup"><span data-stu-id="ba658-108">\<scopes></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ba658-109">構文</span><span class="sxs-lookup"><span data-stu-id="ba658-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="String">
      <endpointDiscovery enable="Boolean">
        <scopes>
          <add scope="URI" />
        </scopes>
      </endpointDiscovery>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ba658-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="ba658-110">Attributes and Elements</span></span>  
 <span data-ttu-id="ba658-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba658-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ba658-112">属性</span><span class="sxs-lookup"><span data-stu-id="ba658-112">Attributes</span></span>  
 <span data-ttu-id="ba658-113">なし。</span><span class="sxs-lookup"><span data-stu-id="ba658-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="ba658-114">子要素</span><span class="sxs-lookup"><span data-stu-id="ba658-114">Child Elements</span></span>  
  
|<span data-ttu-id="ba658-115">属性</span><span class="sxs-lookup"><span data-stu-id="ba658-115">Attribute</span></span>|<span data-ttu-id="ba658-116">説明</span><span class="sxs-lookup"><span data-stu-id="ba658-116">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="ba658-117">\<add></span><span class="sxs-lookup"><span data-stu-id="ba658-117">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-scopes.md)|<span data-ttu-id="ba658-118">サービス検索の一致条件に使用できるエンドポイントのスコープ情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="ba658-118">Adds the scope information for the endpoint that can be used in matching criteria for finding services.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ba658-119">親要素</span><span class="sxs-lookup"><span data-stu-id="ba658-119">Parent Elements</span></span>  
  
|<span data-ttu-id="ba658-120">要素</span><span class="sxs-lookup"><span data-stu-id="ba658-120">Element</span></span>|<span data-ttu-id="ba658-121">説明</span><span class="sxs-lookup"><span data-stu-id="ba658-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ba658-122">\<endpointDiscovery></span><span class="sxs-lookup"><span data-stu-id="ba658-122">\<endpointDiscovery></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpointdiscovery.md)|<span data-ttu-id="ba658-123">エンドポイントのさまざまな探索設定を指定します (探索可能性、スコープ、メタデータに対するカスタム拡張など)。</span><span class="sxs-lookup"><span data-stu-id="ba658-123">Specifies the various discovery settings for an endpoint, such as its discoverability, scopes, and any custom extensions to its metadata.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ba658-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="ba658-124">See also</span></span>
- <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
