---
title: '&lt;dispatcherSynchronization&gt;'
ms.date: 03/30/2017
ms.assetid: cc030f9c-4e38-4b14-94dc-9a0e41ec8e2d
ms.openlocfilehash: 537dee408f1af29a06042de439a2c1e7d7874222
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54555389"
---
# <a name="ltdispatchersynchronizationgt"></a><span data-ttu-id="440bd-102">&lt;dispatcherSynchronization&gt;</span><span class="sxs-lookup"><span data-stu-id="440bd-102">&lt;dispatcherSynchronization&gt;</span></span>
  
<span data-ttu-id="440bd-103">サービスが非同期に応答を返すことができるようにするエンドポイントの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="440bd-103">Specifies an endpoint behavior that enables a service to send replies asynchronously.</span></span>  
  
<span data-ttu-id="440bd-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="440bd-104">\<system.serviceModel></span></span>  
<span data-ttu-id="440bd-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="440bd-105">\<behaviors></span></span>  
<span data-ttu-id="440bd-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="440bd-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="440bd-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="440bd-107">\<behavior></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="440bd-108">構文</span><span class="sxs-lookup"><span data-stu-id="440bd-108">Syntax</span></span>  
  
```xml  
<dispatcherSynchronizationBehavior asynchronousSendEnabled="Boolean"
                                   maxPendingReceives="Integer" />
```  
  
## <a name="type"></a><span data-ttu-id="440bd-109">型</span><span class="sxs-lookup"><span data-stu-id="440bd-109">Type</span></span>  
  
`Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="440bd-110">属性と要素</span><span class="sxs-lookup"><span data-stu-id="440bd-110">Attributes and elements</span></span>  
  
<span data-ttu-id="440bd-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="440bd-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="440bd-112">属性</span><span class="sxs-lookup"><span data-stu-id="440bd-112">Attributes</span></span>

| <span data-ttu-id="440bd-113">属性</span><span class="sxs-lookup"><span data-stu-id="440bd-113">Attribute</span></span>               | <span data-ttu-id="440bd-114">説明</span><span class="sxs-lookup"><span data-stu-id="440bd-114">Description</span></span>       |
| ----------------------- | ----------------- |
| <span data-ttu-id="440bd-115">asynchronousSendEnabled</span><span class="sxs-lookup"><span data-stu-id="440bd-115">asynchronousSendEnabled</span></span> | <span data-ttu-id="440bd-116">非同期の送信動作が有効かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="440bd-116">A Boolean that specifies whether asynchronous send behavior is enabled.</span></span> |
| `maxPendingReceives`    | <span data-ttu-id="440bd-117">チャネルで発行可能な同時受信の数を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="440bd-117">An integer that specifies the number of concurrent receives that can be issued on the channel.</span></span><br /><br /> <span data-ttu-id="440bd-118">この値は、サービス調整の動作を適切に構成した後に構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="440bd-118">This value should be configured only after you have properly configured service throttling behavior.</span></span> |

### <a name="child-elements"></a><span data-ttu-id="440bd-119">子要素</span><span class="sxs-lookup"><span data-stu-id="440bd-119">Child elements</span></span>

<span data-ttu-id="440bd-120">なし。</span><span class="sxs-lookup"><span data-stu-id="440bd-120">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="440bd-121">親要素</span><span class="sxs-lookup"><span data-stu-id="440bd-121">Parent elements</span></span>

| <span data-ttu-id="440bd-122">要素</span><span class="sxs-lookup"><span data-stu-id="440bd-122">Element</span></span> | <span data-ttu-id="440bd-123">説明</span><span class="sxs-lookup"><span data-stu-id="440bd-123">Description</span></span> |  
| ------- | ----------- |  
| [<span data-ttu-id="440bd-124">\<behavior></span><span class="sxs-lookup"><span data-stu-id="440bd-124">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="440bd-125">エンドポイントの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="440bd-125">Specifies an endpoint behavior.</span></span> |

## <a name="see-also"></a><span data-ttu-id="440bd-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="440bd-126">See also</span></span>

- <xref:System.ServiceModel.Configuration.DispatcherSynchronizationElement>
- <xref:System.ServiceModel.Description.DispatcherSynchronizationBehavior>
