---
title: <add> の <baseAddresses>
ms.date: 03/30/2017
ms.assetid: 1bd7426f-5f4f-43fc-b8e9-de842219aa32
ms.openlocfilehash: d66be51fa2626283063c250905efdb7d47babfb0
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55279943"
---
# <a name="add-of-baseaddresses"></a><span data-ttu-id="5d1b9-102">\<add> of \<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="5d1b9-102">\<add> of \<baseAddresses></span></span>
<span data-ttu-id="5d1b9-103">サービス ホストによって使用されるベース アドレスを指定する構成要素を表します。</span><span class="sxs-lookup"><span data-stu-id="5d1b9-103">Represents a configuration element that specifies the base addresses used by the service host.</span></span>  
  
 <span data-ttu-id="5d1b9-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="5d1b9-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="5d1b9-105">\<client></span><span class="sxs-lookup"><span data-stu-id="5d1b9-105">\<client></span></span>  
<span data-ttu-id="5d1b9-106">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="5d1b9-106">\<endpoint></span></span>  
<span data-ttu-id="5d1b9-107">\<host></span><span class="sxs-lookup"><span data-stu-id="5d1b9-107">\<host></span></span>  
<span data-ttu-id="5d1b9-108">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="5d1b9-108">\<baseAddresses></span></span>  
<span data-ttu-id="5d1b9-109">\<baseAddress></span><span class="sxs-lookup"><span data-stu-id="5d1b9-109">\<baseAddress></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5d1b9-110">構文</span><span class="sxs-lookup"><span data-stu-id="5d1b9-110">Syntax</span></span>  
  
```xml  
<add baseAddress="string" />
```  
  
## <a name="type"></a><span data-ttu-id="5d1b9-111">型</span><span class="sxs-lookup"><span data-stu-id="5d1b9-111">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5d1b9-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="5d1b9-112">Attributes and Elements</span></span>  
 <span data-ttu-id="5d1b9-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="5d1b9-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5d1b9-114">属性</span><span class="sxs-lookup"><span data-stu-id="5d1b9-114">Attributes</span></span>  
  
|<span data-ttu-id="5d1b9-115">属性</span><span class="sxs-lookup"><span data-stu-id="5d1b9-115">Attribute</span></span>|<span data-ttu-id="5d1b9-116">説明</span><span class="sxs-lookup"><span data-stu-id="5d1b9-116">Description</span></span>|  
|---------------|-----------------|  
|`baseAddress`|<span data-ttu-id="5d1b9-117">サービス ホストによって使用されるベース アドレスを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="5d1b9-117">A string that specifies a base address used by the service host.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5d1b9-118">子要素</span><span class="sxs-lookup"><span data-stu-id="5d1b9-118">Child Elements</span></span>  
 <span data-ttu-id="5d1b9-119">なし。</span><span class="sxs-lookup"><span data-stu-id="5d1b9-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5d1b9-120">親要素</span><span class="sxs-lookup"><span data-stu-id="5d1b9-120">Parent Elements</span></span>  
  
|<span data-ttu-id="5d1b9-121">要素</span><span class="sxs-lookup"><span data-stu-id="5d1b9-121">Element</span></span>|<span data-ttu-id="5d1b9-122">説明</span><span class="sxs-lookup"><span data-stu-id="5d1b9-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5d1b9-123">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="5d1b9-123">\<baseAddresses></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/baseaddresses.md)|<span data-ttu-id="5d1b9-124">`baseAddress` 要素のコレクション。</span><span class="sxs-lookup"><span data-stu-id="5d1b9-124">A collection of `baseAddress` elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5d1b9-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d1b9-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- <xref:System.ServiceModel.ServiceHostBase.BaseAddresses%2A>
- [<span data-ttu-id="5d1b9-126">ホスティング</span><span class="sxs-lookup"><span data-stu-id="5d1b9-126">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
