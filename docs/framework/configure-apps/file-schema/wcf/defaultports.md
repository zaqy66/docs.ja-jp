---
title: <defaultPorts>
ms.date: 03/30/2017
ms.assetid: 725d4ee5-bd46-4f0e-9c20-30ba75d6eb2c
ms.openlocfilehash: 595970a56e05c4fc1c9b2c0eb669ec3b3a120fe1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55262386"
---
# <a name="defaultports"></a><span data-ttu-id="a678d-101">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="a678d-101">\<defaultPorts></span></span>
<span data-ttu-id="a678d-102">クライアント アプリケーションがリッスンする既定の通信エンドポイントの一覧を表示する既定のポートのコレクション。</span><span class="sxs-lookup"><span data-stu-id="a678d-102">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>  
  
<span data-ttu-id="a678d-103">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="a678d-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="a678d-104">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="a678d-104">\<behaviors></span></span>  
<span data-ttu-id="a678d-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="a678d-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="a678d-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="a678d-106">\<behavior></span></span>  
<span data-ttu-id="a678d-107">\<useRequestHeadersForMetadataAddress ></span><span class="sxs-lookup"><span data-stu-id="a678d-107">\<useRequestHeadersForMetadataAddress></span></span>  
<span data-ttu-id="a678d-108">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="a678d-108">\<defaultPorts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a678d-109">構文</span><span class="sxs-lookup"><span data-stu-id="a678d-109">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http"
         port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a678d-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="a678d-110">Attributes and Elements</span></span>  
 <span data-ttu-id="a678d-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="a678d-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a678d-112">属性</span><span class="sxs-lookup"><span data-stu-id="a678d-112">Attributes</span></span>  
 <span data-ttu-id="a678d-113">なし。</span><span class="sxs-lookup"><span data-stu-id="a678d-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="a678d-114">子要素</span><span class="sxs-lookup"><span data-stu-id="a678d-114">Child Elements</span></span>  
  
|<span data-ttu-id="a678d-115">要素</span><span class="sxs-lookup"><span data-stu-id="a678d-115">Element</span></span>|<span data-ttu-id="a678d-116">説明</span><span class="sxs-lookup"><span data-stu-id="a678d-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a678d-117">\<追加 > の\<defaultPorts ></span><span class="sxs-lookup"><span data-stu-id="a678d-117">\<add> of \<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-defaultports.md)|<span data-ttu-id="a678d-118">クライアント アプリケーションがリッスンする既定の通信エンドポイント。</span><span class="sxs-lookup"><span data-stu-id="a678d-118">A default communications endpoint that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a678d-119">親要素</span><span class="sxs-lookup"><span data-stu-id="a678d-119">Parent Elements</span></span>  
  
|<span data-ttu-id="a678d-120">要素</span><span class="sxs-lookup"><span data-stu-id="a678d-120">Element</span></span>|<span data-ttu-id="a678d-121">説明</span><span class="sxs-lookup"><span data-stu-id="a678d-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a678d-122">\<useRequestHeadersForMetadataAddress ></span><span class="sxs-lookup"><span data-stu-id="a678d-122">\<useRequestHeadersForMetadataAddress></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/userequestheadersformetadataaddress.md)|<span data-ttu-id="a678d-123">既定のポートの一覧。</span><span class="sxs-lookup"><span data-stu-id="a678d-123">A list of default ports.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a678d-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="a678d-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.DefaultPortElementCollection>
