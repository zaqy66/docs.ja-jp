---
title: '&lt;useRequestHeadersForMetadataAddress&gt;'
ms.date: 03/30/2017
ms.assetid: 679f0eae-f353-44d1-b42d-a9e247509774
ms.openlocfilehash: 6c03057fca23b037702c702b9a574045ebb302b4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54656628"
---
# <a name="ltuserequestheadersformetadataaddressgt"></a><span data-ttu-id="40d57-102">&lt;useRequestHeadersForMetadataAddress&gt;</span><span class="sxs-lookup"><span data-stu-id="40d57-102">&lt;useRequestHeadersForMetadataAddress&gt;</span></span>
<span data-ttu-id="40d57-103">メタデータのアドレス情報を要求メッセージ ヘッダーから取得できるようにします。</span><span class="sxs-lookup"><span data-stu-id="40d57-103">Enables the retrieval of metadata address information from the request message headers.</span></span>  
  
<span data-ttu-id="40d57-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="40d57-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="40d57-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="40d57-105">\<behaviors></span></span>  
<span data-ttu-id="40d57-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="40d57-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="40d57-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="40d57-107">\<behavior></span></span>  
<span data-ttu-id="40d57-108">\<useRequestHeadersForMetadataAddress ></span><span class="sxs-lookup"><span data-stu-id="40d57-108">\<useRequestHeadersForMetadataAddress></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="40d57-109">構文</span><span class="sxs-lookup"><span data-stu-id="40d57-109">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http"
         port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="40d57-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="40d57-110">Attributes and Elements</span></span>  
 <span data-ttu-id="40d57-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="40d57-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="40d57-112">属性</span><span class="sxs-lookup"><span data-stu-id="40d57-112">Attributes</span></span>  
 <span data-ttu-id="40d57-113">なし。</span><span class="sxs-lookup"><span data-stu-id="40d57-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="40d57-114">子要素</span><span class="sxs-lookup"><span data-stu-id="40d57-114">Child Elements</span></span>  
  
|<span data-ttu-id="40d57-115">要素</span><span class="sxs-lookup"><span data-stu-id="40d57-115">Element</span></span>|<span data-ttu-id="40d57-116">説明</span><span class="sxs-lookup"><span data-stu-id="40d57-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="40d57-117">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="40d57-117">\<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/defaultports.md)|<span data-ttu-id="40d57-118">クライアント アプリケーションがリッスンする既定の通信エンドポイントの一覧を表示する既定のポートのコレクション。</span><span class="sxs-lookup"><span data-stu-id="40d57-118">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="40d57-119">親要素</span><span class="sxs-lookup"><span data-stu-id="40d57-119">Parent Elements</span></span>  
  
|<span data-ttu-id="40d57-120">要素</span><span class="sxs-lookup"><span data-stu-id="40d57-120">Element</span></span>|<span data-ttu-id="40d57-121">説明</span><span class="sxs-lookup"><span data-stu-id="40d57-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="40d57-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="40d57-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="40d57-123">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="40d57-123">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="40d57-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="40d57-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.UseRequestHeadersForMetadataAddressElement>
