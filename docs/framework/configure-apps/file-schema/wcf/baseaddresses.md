---
title: '&lt;BaseAddresses&gt;'
ms.date: 03/30/2017
ms.assetid: 78918102-2898-46e0-9ea8-6b8afe65603e
ms.openlocfilehash: 0af5dee41c6adf560c90874e6e9a44b62c5decc6
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147357"
---
# <a name="ltbaseaddressesgt"></a><span data-ttu-id="30d2a-102">&lt;BaseAddresses&gt;</span><span class="sxs-lookup"><span data-stu-id="30d2a-102">&lt;baseAddresses&gt;</span></span>
<span data-ttu-id="30d2a-103">自己ホスト環境でのサービス ホストのベース アドレスである `baseAddress` 要素のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="30d2a-103">Represents a collection of `baseAddress` elements, which are base addresses for a service host in a self-hosted environment.</span></span> <span data-ttu-id="30d2a-104">ベース アドレスが存在すると、そのベース アドレスに関連したアドレスを使用してエンドポイントを構成できます。</span><span class="sxs-lookup"><span data-stu-id="30d2a-104">If a base address is present, endpoints can be configured with addresses relative to the base address.</span></span>  
  
 <span data-ttu-id="30d2a-105">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="30d2a-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="30d2a-106">\<client></span><span class="sxs-lookup"><span data-stu-id="30d2a-106">\<client></span></span>  
<span data-ttu-id="30d2a-107">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="30d2a-107">\<endpoint></span></span>  
<span data-ttu-id="30d2a-108">\<ホスト ></span><span class="sxs-lookup"><span data-stu-id="30d2a-108">\<host></span></span>  
<span data-ttu-id="30d2a-109">\<baseAddresses ></span><span class="sxs-lookup"><span data-stu-id="30d2a-109">\<baseAddresses></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="30d2a-110">構文</span><span class="sxs-lookup"><span data-stu-id="30d2a-110">Syntax</span></span>  
  
```xml  
<baseAddresses>
  <add baseAddress="string" />
</baseAddresses>
```  
  
## <a name="type"></a><span data-ttu-id="30d2a-111">型</span><span class="sxs-lookup"><span data-stu-id="30d2a-111">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="30d2a-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="30d2a-112">Attributes and Elements</span></span>  
 <span data-ttu-id="30d2a-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="30d2a-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="30d2a-114">属性</span><span class="sxs-lookup"><span data-stu-id="30d2a-114">Attributes</span></span>  
 <span data-ttu-id="30d2a-115">なし。</span><span class="sxs-lookup"><span data-stu-id="30d2a-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="30d2a-116">子要素</span><span class="sxs-lookup"><span data-stu-id="30d2a-116">Child Elements</span></span>  
  
|<span data-ttu-id="30d2a-117">要素</span><span class="sxs-lookup"><span data-stu-id="30d2a-117">Element</span></span>|<span data-ttu-id="30d2a-118">説明</span><span class="sxs-lookup"><span data-stu-id="30d2a-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="30d2a-119">\<add></span><span class="sxs-lookup"><span data-stu-id="30d2a-119">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-baseaddresses.md)|<span data-ttu-id="30d2a-120">サービス ホストによって使用されるベース アドレスを指定する構成要素。</span><span class="sxs-lookup"><span data-stu-id="30d2a-120">A configuration element that specifies the base addresses used by the service host.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="30d2a-121">親要素</span><span class="sxs-lookup"><span data-stu-id="30d2a-121">Parent Elements</span></span>  
  
|<span data-ttu-id="30d2a-122">要素</span><span class="sxs-lookup"><span data-stu-id="30d2a-122">Element</span></span>|<span data-ttu-id="30d2a-123">説明</span><span class="sxs-lookup"><span data-stu-id="30d2a-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="30d2a-124">\<ホスト ></span><span class="sxs-lookup"><span data-stu-id="30d2a-124">\<host></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|<span data-ttu-id="30d2a-125">サービス ホストの設定を指定する構成要素です。</span><span class="sxs-lookup"><span data-stu-id="30d2a-125">A configuration element that specifies settings for a service host.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="30d2a-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="30d2a-126">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.HostElement>  
 <xref:System.ServiceModel.ServiceHost>  
 <xref:System.ServiceModel.ServiceHostBase.BaseAddresses%2A>  
 [<span data-ttu-id="30d2a-127">ホスティング</span><span class="sxs-lookup"><span data-stu-id="30d2a-127">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
