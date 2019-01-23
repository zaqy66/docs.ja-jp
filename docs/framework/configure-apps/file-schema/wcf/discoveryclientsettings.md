---
title: '&lt;discoveryClientSettings&gt;'
ms.date: 03/30/2017
ms.assetid: 02e1b823-a8bb-4074-90d5-8599f71e8f9d
ms.openlocfilehash: dd02f6bb7674015d1c153b2dce38e7e29181d25f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54599921"
---
# <a name="ltdiscoveryclientsettingsgt"></a><span data-ttu-id="f2120-102">&lt;discoveryClientSettings&gt;</span><span class="sxs-lookup"><span data-stu-id="f2120-102">&lt;discoveryClientSettings&gt;</span></span>
<span data-ttu-id="f2120-103">サービス探索プロセスにクライアントとして参加するためにアプリケーションが必要とする設定を格納します。</span><span class="sxs-lookup"><span data-stu-id="f2120-103">Contains the settings needed by an application to participate in the service discovery process as a client.</span></span>  
  
<span data-ttu-id="f2120-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="f2120-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="f2120-105">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="f2120-105">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2120-106">構文</span><span class="sxs-lookup"><span data-stu-id="f2120-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <dynamicEndpoint>
      <standardEndpoint>
        <discoveryClientSettings discoveryEndpoint="String">
          <findCriteria duration="TimeSpan"
                        maxResults="Integer"
                        scopeMatchBy="Uri">
            <contractTypeNames>
              <add name="String"
                   namespace="String" />
            <contractTypeNames>
            <extensions />
            <scopes>
              <add scope="URI"/>
            </scopes>
          </findCriteria>
        </discoveryClientSettings>
      <standardEndpoint>
    </dynamicEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f2120-107">属性および要素</span><span class="sxs-lookup"><span data-stu-id="f2120-107">Attributes and Elements</span></span>  
 <span data-ttu-id="f2120-108">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="f2120-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f2120-109">属性</span><span class="sxs-lookup"><span data-stu-id="f2120-109">Attributes</span></span>  
  
|<span data-ttu-id="f2120-110">属性</span><span class="sxs-lookup"><span data-stu-id="f2120-110">Attribute</span></span>|<span data-ttu-id="f2120-111">説明</span><span class="sxs-lookup"><span data-stu-id="f2120-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f2120-112">discoveryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f2120-112">discoveryEndpoint</span></span>|<span data-ttu-id="f2120-113">クライアント アプリケーションが実行時に探索可能なサービスを自動的に検索し、そのアドレスを見つけることができる探索エンドポイントの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="f2120-113">A string that contains the name of the Discovery Endpoint that enables a client application to automatically search for a discoverable service and find its address at runtime.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f2120-114">子要素</span><span class="sxs-lookup"><span data-stu-id="f2120-114">Child Elements</span></span>  
  
|<span data-ttu-id="f2120-115">要素</span><span class="sxs-lookup"><span data-stu-id="f2120-115">Element</span></span>|<span data-ttu-id="f2120-116">説明</span><span class="sxs-lookup"><span data-stu-id="f2120-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f2120-117">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="f2120-117">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="f2120-118">探索サービスの検索にクライアント アプリケーションによって使用される基準を提供する構成要素。</span><span class="sxs-lookup"><span data-stu-id="f2120-118">A configuration element that supplies a set of criteria used by a client application to search for a discovery service.</span></span> <span data-ttu-id="f2120-119">条件は、(探しているサービスの種類を指定して) 検索条件にグループ化することができ、検索 (検索持続期間)、終了条件。</span><span class="sxs-lookup"><span data-stu-id="f2120-119">Criteria can be grouped into search criteria (specifying what services you’re looking for) and find termination criteria (how long the search should last).</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f2120-120">親要素</span><span class="sxs-lookup"><span data-stu-id="f2120-120">Parent Elements</span></span>  
  
|<span data-ttu-id="f2120-121">要素</span><span class="sxs-lookup"><span data-stu-id="f2120-121">Element</span></span>|<span data-ttu-id="f2120-122">説明</span><span class="sxs-lookup"><span data-stu-id="f2120-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f2120-123">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="f2120-123">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="f2120-124">アプリケーションが実行時に動的にエンドポイント アドレスを検索するクライアント プログラムとして機能するための情報を格納する標準エンドポイントを定義します。</span><span class="sxs-lookup"><span data-stu-id="f2120-124">Defines a standard endpoint that contains information to enable an application to function as a client program that can find the endpoint address dynamically at runtime.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f2120-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2120-125">See also</span></span>
- <xref:System.ServiceModel.Discovery.DiscoveryClientBindingElement>
- <xref:System.ServiceModel.Discovery.Configuration.DiscoveryClientSettingsElement>
