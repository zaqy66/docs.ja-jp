---
title: '&lt;contractTypeNames&gt; の &lt;add&gt;'
ms.date: 03/30/2017
ms.assetid: 03aff6be-5dfb-4a64-ada3-e36227cd43c7
ms.openlocfilehash: 79972eaea6918b3fe923c963b6a219fd8f972516
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145615"
---
# <a name="ltaddgt-of-ltcontracttypenamesgt"></a><span data-ttu-id="e4d75-102">&lt;contractTypeNames&gt; の &lt;add&gt;</span><span class="sxs-lookup"><span data-stu-id="e4d75-102">&lt;add&gt; of &lt;contractTypeNames&gt;</span></span>
<span data-ttu-id="e4d75-103">検索対象サービスのコントラクト名と、サービスを検索するときに一般的に使用される条件を指定する構成要素。</span><span class="sxs-lookup"><span data-stu-id="e4d75-103">A configuration element that specifies the contract name of the services being searched for, and the criteria typically used when searching for a service.</span></span> <span data-ttu-id="e4d75-104">複数のコントラクト名が指定されると、すべてのコントラクトに一致するサービス エンドポイントのみが適用されます。</span><span class="sxs-lookup"><span data-stu-id="e4d75-104">If more than one contract name is specified, only service endpoints matching ALL contracts will reply.</span></span> <span data-ttu-id="e4d75-105">Windows Communication Foundation (WCF) エンドポイントがのみサポートしている 1 つのコントラクトに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e4d75-105">Note that in Windows Communication Foundation (WCF), an endpoint can only support one contract.</span></span>  
  
 <span data-ttu-id="e4d75-106">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="e4d75-106">\<system.ServiceModel></span></span>  
<span data-ttu-id="e4d75-107">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="e4d75-107">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4d75-108">構文</span><span class="sxs-lookup"><span data-stu-id="e4d75-108">Syntax</span></span>  
  
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
              <add name="String" namespace="String" />
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e4d75-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="e4d75-109">Attributes and Elements</span></span>  
 <span data-ttu-id="e4d75-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="e4d75-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e4d75-111">属性</span><span class="sxs-lookup"><span data-stu-id="e4d75-111">Attributes</span></span>  
  
|<span data-ttu-id="e4d75-112">属性</span><span class="sxs-lookup"><span data-stu-id="e4d75-112">Attribute</span></span>|<span data-ttu-id="e4d75-113">説明</span><span class="sxs-lookup"><span data-stu-id="e4d75-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e4d75-114">name</span><span class="sxs-lookup"><span data-stu-id="e4d75-114">name</span></span>|<span data-ttu-id="e4d75-115">コントラクト型の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="e4d75-115">A string that specifies the name of the contract type.</span></span>|  
|<span data-ttu-id="e4d75-116">namespace</span><span class="sxs-lookup"><span data-stu-id="e4d75-116">namespace</span></span>|<span data-ttu-id="e4d75-117">コントラクト型の名前空間を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="e4d75-117">A string that specifies the namespace of the contract type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e4d75-118">子要素</span><span class="sxs-lookup"><span data-stu-id="e4d75-118">Child Elements</span></span>  
 <span data-ttu-id="e4d75-119">なし</span><span class="sxs-lookup"><span data-stu-id="e4d75-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e4d75-120">親要素</span><span class="sxs-lookup"><span data-stu-id="e4d75-120">Parent Elements</span></span>  
  
|<span data-ttu-id="e4d75-121">要素</span><span class="sxs-lookup"><span data-stu-id="e4d75-121">Element</span></span>|<span data-ttu-id="e4d75-122">説明</span><span class="sxs-lookup"><span data-stu-id="e4d75-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e4d75-123">\<contractTypeNames ></span><span class="sxs-lookup"><span data-stu-id="e4d75-123">\<contractTypeNames></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/contracttypenames.md)|<span data-ttu-id="e4d75-124">コントラクトの型名のコレクション。</span><span class="sxs-lookup"><span data-stu-id="e4d75-124">A collection of contract type names.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e4d75-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="e4d75-125">See Also</span></span>  
 <xref:System.ServiceModel.Discovery.FindCriteria>  
 <xref:System.ServiceModel.Discovery.Configuration.FindCriteriaElement>  
 <xref:System.ServiceModel.Discovery.Configuration.ContractTypeNameElement>
