---
title: '&lt;baseAddresses&gt;'
ms.date: 03/30/2017
ms.assetid: 78918102-2898-46e0-9ea8-6b8afe65603e
ms.openlocfilehash: 34d400e74b24e9eb4140d1b43597b0217b23d80c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54730127"
---
# <a name="ltbaseaddressesgt"></a><span data-ttu-id="28a35-102">&lt;baseAddresses&gt;</span><span class="sxs-lookup"><span data-stu-id="28a35-102">&lt;baseAddresses&gt;</span></span>
<span data-ttu-id="28a35-103">自己ホスト環境でのサービス ホストのベース アドレスである `baseAddress` 要素のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="28a35-103">Represents a collection of `baseAddress` elements, which are base addresses for a service host in a self-hosted environment.</span></span> <span data-ttu-id="28a35-104">ベース アドレスが存在すると、そのベース アドレスに関連したアドレスを使用してエンドポイントを構成できます。</span><span class="sxs-lookup"><span data-stu-id="28a35-104">If a base address is present, endpoints can be configured with addresses relative to the base address.</span></span>  
  
 <span data-ttu-id="28a35-105">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="28a35-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="28a35-106">\<client></span><span class="sxs-lookup"><span data-stu-id="28a35-106">\<client></span></span>  
<span data-ttu-id="28a35-107">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="28a35-107">\<endpoint></span></span>  
<span data-ttu-id="28a35-108">\<host></span><span class="sxs-lookup"><span data-stu-id="28a35-108">\<host></span></span>  
<span data-ttu-id="28a35-109">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="28a35-109">\<baseAddresses></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="28a35-110">構文</span><span class="sxs-lookup"><span data-stu-id="28a35-110">Syntax</span></span>  
  
```xml  
<baseAddresses>
  <add baseAddress="string" />
</baseAddresses>
```  
  
## <a name="type"></a><span data-ttu-id="28a35-111">型</span><span class="sxs-lookup"><span data-stu-id="28a35-111">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="28a35-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="28a35-112">Attributes and Elements</span></span>  
 <span data-ttu-id="28a35-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="28a35-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="28a35-114">属性</span><span class="sxs-lookup"><span data-stu-id="28a35-114">Attributes</span></span>  
 <span data-ttu-id="28a35-115">なし。</span><span class="sxs-lookup"><span data-stu-id="28a35-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="28a35-116">子要素</span><span class="sxs-lookup"><span data-stu-id="28a35-116">Child Elements</span></span>  
  
|<span data-ttu-id="28a35-117">要素</span><span class="sxs-lookup"><span data-stu-id="28a35-117">Element</span></span>|<span data-ttu-id="28a35-118">説明</span><span class="sxs-lookup"><span data-stu-id="28a35-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="28a35-119">\<add></span><span class="sxs-lookup"><span data-stu-id="28a35-119">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-baseaddresses.md)|<span data-ttu-id="28a35-120">サービス ホストによって使用されるベース アドレスを指定する構成要素。</span><span class="sxs-lookup"><span data-stu-id="28a35-120">A configuration element that specifies the base addresses used by the service host.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="28a35-121">親要素</span><span class="sxs-lookup"><span data-stu-id="28a35-121">Parent Elements</span></span>  
  
|<span data-ttu-id="28a35-122">要素</span><span class="sxs-lookup"><span data-stu-id="28a35-122">Element</span></span>|<span data-ttu-id="28a35-123">説明</span><span class="sxs-lookup"><span data-stu-id="28a35-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="28a35-124">\<host></span><span class="sxs-lookup"><span data-stu-id="28a35-124">\<host></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|<span data-ttu-id="28a35-125">サービス ホストの設定を指定する構成要素です。</span><span class="sxs-lookup"><span data-stu-id="28a35-125">A configuration element that specifies settings for a service host.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="28a35-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="28a35-126">See also</span></span>
- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- <xref:System.ServiceModel.ServiceHostBase.BaseAddresses%2A>
- [<span data-ttu-id="28a35-127">ホスティング</span><span class="sxs-lookup"><span data-stu-id="28a35-127">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
