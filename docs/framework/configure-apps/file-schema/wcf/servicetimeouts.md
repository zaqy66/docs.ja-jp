---
title: <serviceTimeouts>
ms.date: 03/30/2017
ms.assetid: ada536cf-97dc-4cd7-89ec-ed1466c1c557
ms.openlocfilehash: b67ea137e6c116d00a8a098b9c0df99430114dc5
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55267288"
---
# <a name="servicetimeouts"></a><span data-ttu-id="a68e1-101">\<serviceTimeouts></span><span class="sxs-lookup"><span data-stu-id="a68e1-101">\<serviceTimeouts></span></span>
<span data-ttu-id="a68e1-102">サービスのタイムアウトを指定します。</span><span class="sxs-lookup"><span data-stu-id="a68e1-102">Specifies the timeout for a service.</span></span>  
  
 <span data-ttu-id="a68e1-103">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="a68e1-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="a68e1-104">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="a68e1-104">\<behaviors></span></span>  
<span data-ttu-id="a68e1-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="a68e1-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="a68e1-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="a68e1-106">\<behavior></span></span>  
<span data-ttu-id="a68e1-107">\<serviceTimeouts></span><span class="sxs-lookup"><span data-stu-id="a68e1-107">\<serviceTimeouts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a68e1-108">構文</span><span class="sxs-lookup"><span data-stu-id="a68e1-108">Syntax</span></span>  
  
```xml  
<serviceTimeouts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="a68e1-109">型</span><span class="sxs-lookup"><span data-stu-id="a68e1-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a68e1-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="a68e1-110">Attributes and Elements</span></span>  
 <span data-ttu-id="a68e1-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="a68e1-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a68e1-112">属性</span><span class="sxs-lookup"><span data-stu-id="a68e1-112">Attributes</span></span>  
  
|<span data-ttu-id="a68e1-113">属性</span><span class="sxs-lookup"><span data-stu-id="a68e1-113">Attribute</span></span>|<span data-ttu-id="a68e1-114">説明</span><span class="sxs-lookup"><span data-stu-id="a68e1-114">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="a68e1-115">クライアントからサーバーへのトランザクションが発生するまでに待機できる時間を指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="a68e1-115">A <xref:System.TimeSpan> value that specifies the interval of time a transaction must flow from client to server.</span></span> <span data-ttu-id="a68e1-116">既定値は"00: 00:00"。</span><span class="sxs-lookup"><span data-stu-id="a68e1-116">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a68e1-117">子要素</span><span class="sxs-lookup"><span data-stu-id="a68e1-117">Child Elements</span></span>  
 <span data-ttu-id="a68e1-118">なし。</span><span class="sxs-lookup"><span data-stu-id="a68e1-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a68e1-119">親要素</span><span class="sxs-lookup"><span data-stu-id="a68e1-119">Parent Elements</span></span>  
  
|<span data-ttu-id="a68e1-120">要素</span><span class="sxs-lookup"><span data-stu-id="a68e1-120">Element</span></span>|<span data-ttu-id="a68e1-121">説明</span><span class="sxs-lookup"><span data-stu-id="a68e1-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a68e1-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="a68e1-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="a68e1-123">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="a68e1-123">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a68e1-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="a68e1-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.ServiceTimeoutsElement>
