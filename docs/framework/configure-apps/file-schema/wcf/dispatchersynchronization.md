---
title: '&lt;dispatcherSynchronization&gt;'
ms.date: 03/30/2017
ms.assetid: cc030f9c-4e38-4b14-94dc-9a0e41ec8e2d
ms.openlocfilehash: 86660620113b162a9a5260b7026a64455284d184
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151463"
---
# <a name="ltdispatchersynchronizationgt"></a><span data-ttu-id="cf8a6-102">&lt;dispatcherSynchronization&gt;</span><span class="sxs-lookup"><span data-stu-id="cf8a6-102">&lt;dispatcherSynchronization&gt;</span></span>
  
<span data-ttu-id="cf8a6-103">サービスが非同期に応答を返すことができるようにするエンドポイントの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="cf8a6-103">Specifies an endpoint behavior that enables a service to send replies asynchronously.</span></span>  
  
<span data-ttu-id="cf8a6-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="cf8a6-104">\<system.serviceModel></span></span>  
<span data-ttu-id="cf8a6-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="cf8a6-105">\<behaviors></span></span>  
<span data-ttu-id="cf8a6-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="cf8a6-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="cf8a6-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="cf8a6-107">\<behavior></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cf8a6-108">構文</span><span class="sxs-lookup"><span data-stu-id="cf8a6-108">Syntax</span></span>  
  
```xml  
<dispatcherSynchronizationBehavior asynchronousSendEnabled="Boolean"
                                   maxPendingReceives="Integer" />
```  
  
## <a name="type"></a><span data-ttu-id="cf8a6-109">型</span><span class="sxs-lookup"><span data-stu-id="cf8a6-109">Type</span></span>  
  
`Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cf8a6-110">属性と要素</span><span class="sxs-lookup"><span data-stu-id="cf8a6-110">Attributes and elements</span></span>  
  
<span data-ttu-id="cf8a6-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="cf8a6-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cf8a6-112">属性</span><span class="sxs-lookup"><span data-stu-id="cf8a6-112">Attributes</span></span>

| <span data-ttu-id="cf8a6-113">属性</span><span class="sxs-lookup"><span data-stu-id="cf8a6-113">Attribute</span></span>               | <span data-ttu-id="cf8a6-114">説明</span><span class="sxs-lookup"><span data-stu-id="cf8a6-114">Description</span></span>       |
| ----------------------- | ----------------- |
| <span data-ttu-id="cf8a6-115">asynchronousSendEnabled</span><span class="sxs-lookup"><span data-stu-id="cf8a6-115">asynchronousSendEnabled</span></span> | <span data-ttu-id="cf8a6-116">非同期の送信動作が有効かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="cf8a6-116">A Boolean that specifies whether asynchronous send behavior is enabled.</span></span> |
| `maxPendingReceives`    | <span data-ttu-id="cf8a6-117">チャネルで発行可能な同時受信の数を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="cf8a6-117">An integer that specifies the number of concurrent receives that can be issued on the channel.</span></span><br /><br /> <span data-ttu-id="cf8a6-118">この値は、サービス調整の動作を適切に構成した後に構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf8a6-118">This value should be configured only after you have properly configured service throttling behavior.</span></span> |

### <a name="child-elements"></a><span data-ttu-id="cf8a6-119">子要素</span><span class="sxs-lookup"><span data-stu-id="cf8a6-119">Child elements</span></span>

<span data-ttu-id="cf8a6-120">なし。</span><span class="sxs-lookup"><span data-stu-id="cf8a6-120">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="cf8a6-121">親要素</span><span class="sxs-lookup"><span data-stu-id="cf8a6-121">Parent elements</span></span>

| <span data-ttu-id="cf8a6-122">要素</span><span class="sxs-lookup"><span data-stu-id="cf8a6-122">Element</span></span> | <span data-ttu-id="cf8a6-123">説明</span><span class="sxs-lookup"><span data-stu-id="cf8a6-123">Description</span></span> |  
| ------- | ----------- |  
| [<span data-ttu-id="cf8a6-124">\<behavior></span><span class="sxs-lookup"><span data-stu-id="cf8a6-124">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="cf8a6-125">エンドポイントの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="cf8a6-125">Specifies an endpoint behavior.</span></span> |

## <a name="see-also"></a><span data-ttu-id="cf8a6-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf8a6-126">See also</span></span>

 <span data-ttu-id="cf8a6-127"><xref:System.ServiceModel.Configuration.DispatcherSynchronizationElement> <xref:System.ServiceModel.Description.DispatcherSynchronizationBehavior></span><span class="sxs-lookup"><span data-stu-id="cf8a6-127"><xref:System.ServiceModel.Configuration.DispatcherSynchronizationElement> <xref:System.ServiceModel.Description.DispatcherSynchronizationBehavior></span></span>
