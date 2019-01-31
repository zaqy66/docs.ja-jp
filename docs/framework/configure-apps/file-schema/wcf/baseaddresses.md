---
title: <baseAddresses>
ms.date: 03/30/2017
ms.assetid: 78918102-2898-46e0-9ea8-6b8afe65603e
ms.openlocfilehash: dc4b31e729f9037da101bdf3e6cde28e91b1a070
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55277018"
---
# <a name="baseaddresses"></a><span data-ttu-id="05487-101">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="05487-101">\<baseAddresses></span></span>
<span data-ttu-id="05487-102">自己ホスト環境でのサービス ホストのベース アドレスである `baseAddress` 要素のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="05487-102">Represents a collection of `baseAddress` elements, which are base addresses for a service host in a self-hosted environment.</span></span> <span data-ttu-id="05487-103">ベース アドレスが存在すると、そのベース アドレスに関連したアドレスを使用してエンドポイントを構成できます。</span><span class="sxs-lookup"><span data-stu-id="05487-103">If a base address is present, endpoints can be configured with addresses relative to the base address.</span></span>  
  
 <span data-ttu-id="05487-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="05487-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="05487-105">\<client></span><span class="sxs-lookup"><span data-stu-id="05487-105">\<client></span></span>  
<span data-ttu-id="05487-106">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="05487-106">\<endpoint></span></span>  
<span data-ttu-id="05487-107">\<host></span><span class="sxs-lookup"><span data-stu-id="05487-107">\<host></span></span>  
<span data-ttu-id="05487-108">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="05487-108">\<baseAddresses></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="05487-109">構文</span><span class="sxs-lookup"><span data-stu-id="05487-109">Syntax</span></span>  
  
```xml  
<baseAddresses>
  <add baseAddress="string" />
</baseAddresses>
```  
  
## <a name="type"></a><span data-ttu-id="05487-110">型</span><span class="sxs-lookup"><span data-stu-id="05487-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="05487-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="05487-111">Attributes and Elements</span></span>  
 <span data-ttu-id="05487-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="05487-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="05487-113">属性</span><span class="sxs-lookup"><span data-stu-id="05487-113">Attributes</span></span>  
 <span data-ttu-id="05487-114">なし。</span><span class="sxs-lookup"><span data-stu-id="05487-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="05487-115">子要素</span><span class="sxs-lookup"><span data-stu-id="05487-115">Child Elements</span></span>  
  
|<span data-ttu-id="05487-116">要素</span><span class="sxs-lookup"><span data-stu-id="05487-116">Element</span></span>|<span data-ttu-id="05487-117">説明</span><span class="sxs-lookup"><span data-stu-id="05487-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="05487-118">\<add></span><span class="sxs-lookup"><span data-stu-id="05487-118">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-baseaddresses.md)|<span data-ttu-id="05487-119">サービス ホストによって使用されるベース アドレスを指定する構成要素。</span><span class="sxs-lookup"><span data-stu-id="05487-119">A configuration element that specifies the base addresses used by the service host.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="05487-120">親要素</span><span class="sxs-lookup"><span data-stu-id="05487-120">Parent Elements</span></span>  
  
|<span data-ttu-id="05487-121">要素</span><span class="sxs-lookup"><span data-stu-id="05487-121">Element</span></span>|<span data-ttu-id="05487-122">説明</span><span class="sxs-lookup"><span data-stu-id="05487-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="05487-123">\<host></span><span class="sxs-lookup"><span data-stu-id="05487-123">\<host></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|<span data-ttu-id="05487-124">サービス ホストの設定を指定する構成要素です。</span><span class="sxs-lookup"><span data-stu-id="05487-124">A configuration element that specifies settings for a service host.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="05487-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="05487-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- <xref:System.ServiceModel.ServiceHostBase.BaseAddresses%2A>
- [<span data-ttu-id="05487-126">ホスティング</span><span class="sxs-lookup"><span data-stu-id="05487-126">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
