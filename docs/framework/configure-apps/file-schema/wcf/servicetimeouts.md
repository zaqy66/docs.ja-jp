---
title: '&lt;serviceTimeouts&gt;'
ms.date: 03/30/2017
ms.assetid: ada536cf-97dc-4cd7-89ec-ed1466c1c557
ms.openlocfilehash: f7aa623ee387f67f3bbff32249d3695049359cde
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54524469"
---
# <a name="ltservicetimeoutsgt"></a><span data-ttu-id="cd65a-102">&lt;serviceTimeouts&gt;</span><span class="sxs-lookup"><span data-stu-id="cd65a-102">&lt;serviceTimeouts&gt;</span></span>
<span data-ttu-id="cd65a-103">サービスのタイムアウトを指定します。</span><span class="sxs-lookup"><span data-stu-id="cd65a-103">Specifies the timeout for a service.</span></span>  
  
 <span data-ttu-id="cd65a-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="cd65a-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="cd65a-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="cd65a-105">\<behaviors></span></span>  
<span data-ttu-id="cd65a-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="cd65a-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="cd65a-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="cd65a-107">\<behavior></span></span>  
<span data-ttu-id="cd65a-108">\<serviceTimeouts></span><span class="sxs-lookup"><span data-stu-id="cd65a-108">\<serviceTimeouts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd65a-109">構文</span><span class="sxs-lookup"><span data-stu-id="cd65a-109">Syntax</span></span>  
  
```xml  
<serviceTimeouts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="cd65a-110">型</span><span class="sxs-lookup"><span data-stu-id="cd65a-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cd65a-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="cd65a-111">Attributes and Elements</span></span>  
 <span data-ttu-id="cd65a-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="cd65a-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cd65a-113">属性</span><span class="sxs-lookup"><span data-stu-id="cd65a-113">Attributes</span></span>  
  
|<span data-ttu-id="cd65a-114">属性</span><span class="sxs-lookup"><span data-stu-id="cd65a-114">Attribute</span></span>|<span data-ttu-id="cd65a-115">説明</span><span class="sxs-lookup"><span data-stu-id="cd65a-115">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="cd65a-116">クライアントからサーバーへのトランザクションが発生するまでに待機できる時間を指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="cd65a-116">A <xref:System.TimeSpan> value that specifies the interval of time a transaction must flow from client to server.</span></span> <span data-ttu-id="cd65a-117">既定値は"00: 00:00"。</span><span class="sxs-lookup"><span data-stu-id="cd65a-117">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cd65a-118">子要素</span><span class="sxs-lookup"><span data-stu-id="cd65a-118">Child Elements</span></span>  
 <span data-ttu-id="cd65a-119">なし。</span><span class="sxs-lookup"><span data-stu-id="cd65a-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="cd65a-120">親要素</span><span class="sxs-lookup"><span data-stu-id="cd65a-120">Parent Elements</span></span>  
  
|<span data-ttu-id="cd65a-121">要素</span><span class="sxs-lookup"><span data-stu-id="cd65a-121">Element</span></span>|<span data-ttu-id="cd65a-122">説明</span><span class="sxs-lookup"><span data-stu-id="cd65a-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cd65a-123">\<behavior></span><span class="sxs-lookup"><span data-stu-id="cd65a-123">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="cd65a-124">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="cd65a-124">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="cd65a-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="cd65a-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.ServiceTimeoutsElement>
