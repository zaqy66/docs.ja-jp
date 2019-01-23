---
title: '&lt;defaultPorts&gt;'
ms.date: 03/30/2017
ms.assetid: 725d4ee5-bd46-4f0e-9c20-30ba75d6eb2c
ms.openlocfilehash: 2c742f98315c0e497ac4117953424bae913cb5b9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54614498"
---
# <a name="ltdefaultportsgt"></a><span data-ttu-id="292ff-102">&lt;defaultPorts&gt;</span><span class="sxs-lookup"><span data-stu-id="292ff-102">&lt;defaultPorts&gt;</span></span>
<span data-ttu-id="292ff-103">クライアント アプリケーションがリッスンする既定の通信エンドポイントの一覧を表示する既定のポートのコレクション。</span><span class="sxs-lookup"><span data-stu-id="292ff-103">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>  
  
<span data-ttu-id="292ff-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="292ff-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="292ff-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="292ff-105">\<behaviors></span></span>  
<span data-ttu-id="292ff-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="292ff-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="292ff-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="292ff-107">\<behavior></span></span>  
<span data-ttu-id="292ff-108">\<useRequestHeadersForMetadataAddress ></span><span class="sxs-lookup"><span data-stu-id="292ff-108">\<useRequestHeadersForMetadataAddress></span></span>  
<span data-ttu-id="292ff-109">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="292ff-109">\<defaultPorts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="292ff-110">構文</span><span class="sxs-lookup"><span data-stu-id="292ff-110">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http"
         port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="292ff-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="292ff-111">Attributes and Elements</span></span>  
 <span data-ttu-id="292ff-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="292ff-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="292ff-113">属性</span><span class="sxs-lookup"><span data-stu-id="292ff-113">Attributes</span></span>  
 <span data-ttu-id="292ff-114">なし。</span><span class="sxs-lookup"><span data-stu-id="292ff-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="292ff-115">子要素</span><span class="sxs-lookup"><span data-stu-id="292ff-115">Child Elements</span></span>  
  
|<span data-ttu-id="292ff-116">要素</span><span class="sxs-lookup"><span data-stu-id="292ff-116">Element</span></span>|<span data-ttu-id="292ff-117">説明</span><span class="sxs-lookup"><span data-stu-id="292ff-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="292ff-118">\<追加 > の\<defaultPorts ></span><span class="sxs-lookup"><span data-stu-id="292ff-118">\<add> of \<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-defaultports.md)|<span data-ttu-id="292ff-119">クライアント アプリケーションがリッスンする既定の通信エンドポイント。</span><span class="sxs-lookup"><span data-stu-id="292ff-119">A default communications endpoint that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="292ff-120">親要素</span><span class="sxs-lookup"><span data-stu-id="292ff-120">Parent Elements</span></span>  
  
|<span data-ttu-id="292ff-121">要素</span><span class="sxs-lookup"><span data-stu-id="292ff-121">Element</span></span>|<span data-ttu-id="292ff-122">説明</span><span class="sxs-lookup"><span data-stu-id="292ff-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="292ff-123">\<useRequestHeadersForMetadataAddress ></span><span class="sxs-lookup"><span data-stu-id="292ff-123">\<useRequestHeadersForMetadataAddress></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/userequestheadersformetadataaddress.md)|<span data-ttu-id="292ff-124">既定のポートの一覧。</span><span class="sxs-lookup"><span data-stu-id="292ff-124">A list of default ports.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="292ff-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="292ff-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.DefaultPortElementCollection>
