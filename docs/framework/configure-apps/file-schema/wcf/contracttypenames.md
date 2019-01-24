---
title: '&lt;contractTypeNames&gt;'
ms.date: 03/30/2017
ms.assetid: 5ec5efc6-87f8-4160-9be0-dcd2e01df3df
ms.openlocfilehash: 2c3f501f44d9e3c601e654041eb9d5a7de8a0a07
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54626772"
---
# <a name="ltcontracttypenamesgt"></a><span data-ttu-id="b74e6-102">&lt;contractTypeNames&gt;</span><span class="sxs-lookup"><span data-stu-id="b74e6-102">&lt;contractTypeNames&gt;</span></span>
<span data-ttu-id="b74e6-103">検索対象サービスのコントラクト名であるコントラクト型名のリストと、サービスを検索するときに一般的に使用される条件を指定する構成セクション。</span><span class="sxs-lookup"><span data-stu-id="b74e6-103">A configuration section that specifies a list of contract type names, which are the contract names of the services being searched for, and the criteria typically used when searching for a service.</span></span> <span data-ttu-id="b74e6-104">複数のコントラクト名が指定されると、すべてのコントラクトに一致するサービス エンドポイントのみが適用されます。</span><span class="sxs-lookup"><span data-stu-id="b74e6-104">If more than one contract name is specified, only service endpoints matching ALL contracts will reply.</span></span> <span data-ttu-id="b74e6-105">Windows Communication Foundation (WCF) エンドポイントがのみサポートしている 1 つのコントラクトに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b74e6-105">Note that in Windows Communication Foundation (WCF), an endpoint can only support one contract.</span></span>  
  
 <span data-ttu-id="b74e6-106">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="b74e6-106">\<system.ServiceModel></span></span>  
<span data-ttu-id="b74e6-107">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="b74e6-107">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b74e6-108">構文</span><span class="sxs-lookup"><span data-stu-id="b74e6-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b74e6-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="b74e6-109">Attributes and Elements</span></span>  
 <span data-ttu-id="b74e6-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="b74e6-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b74e6-111">属性</span><span class="sxs-lookup"><span data-stu-id="b74e6-111">Attributes</span></span>  
 <span data-ttu-id="b74e6-112">なし。</span><span class="sxs-lookup"><span data-stu-id="b74e6-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="b74e6-113">子要素</span><span class="sxs-lookup"><span data-stu-id="b74e6-113">Child Elements</span></span>  
  
|<span data-ttu-id="b74e6-114">要素</span><span class="sxs-lookup"><span data-stu-id="b74e6-114">Element</span></span>|<span data-ttu-id="b74e6-115">説明</span><span class="sxs-lookup"><span data-stu-id="b74e6-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b74e6-116">\<add></span><span class="sxs-lookup"><span data-stu-id="b74e6-116">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/contracttypenames.md)|<span data-ttu-id="b74e6-117">コントラクト型名は、サービスを検索するときに一般的に使用される条件セットを参照するプロパティです。</span><span class="sxs-lookup"><span data-stu-id="b74e6-117">A contract type name is a property that refers to the set of criteria typically used when searching for a service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b74e6-118">親要素</span><span class="sxs-lookup"><span data-stu-id="b74e6-118">Parent Elements</span></span>  
  
|<span data-ttu-id="b74e6-119">要素</span><span class="sxs-lookup"><span data-stu-id="b74e6-119">Element</span></span>|<span data-ttu-id="b74e6-120">説明</span><span class="sxs-lookup"><span data-stu-id="b74e6-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b74e6-121">\<findCriteria></span><span class="sxs-lookup"><span data-stu-id="b74e6-121">\<findCriteria></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/findcriteria.md)|<span data-ttu-id="b74e6-122">探索サービスの検索にクライアント アプリケーションによって使用される基準を提供する構成要素。</span><span class="sxs-lookup"><span data-stu-id="b74e6-122">A configuration element that supplies a set of criteria used by a client application to search for a discovery service.</span></span> <span data-ttu-id="b74e6-123">条件は、(探しているサービスの種類を指定して) 検索条件にグループ化することができ、検索 (検索持続期間)、終了条件。</span><span class="sxs-lookup"><span data-stu-id="b74e6-123">Criteria can be grouped into search criteria (specifying what services you’re looking for) and find termination criteria (how long the search should last).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b74e6-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="b74e6-124">See also</span></span>
- <xref:System.ServiceModel.Discovery.FindCriteria>
- <xref:System.ServiceModel.Discovery.Configuration.FindCriteriaElement>
- <xref:System.ServiceModel.Discovery.Configuration.ContractTypeNameElementCollection>
