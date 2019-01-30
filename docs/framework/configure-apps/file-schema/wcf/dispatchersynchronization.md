---
title: <dispatcherSynchronization>
ms.date: 03/30/2017
ms.assetid: cc030f9c-4e38-4b14-94dc-9a0e41ec8e2d
ms.openlocfilehash: 6be9752e8102a5d4db4fed31aae8ff6d56fdd24e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55273333"
---
# <a name="dispatchersynchronization"></a><span data-ttu-id="22024-101">\<dispatcherSynchronization ></span><span class="sxs-lookup"><span data-stu-id="22024-101">\<dispatcherSynchronization></span></span>
  
<span data-ttu-id="22024-102">サービスが非同期に応答を返すことができるようにするエンドポイントの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="22024-102">Specifies an endpoint behavior that enables a service to send replies asynchronously.</span></span>  
  
<span data-ttu-id="22024-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="22024-103">\<system.serviceModel></span></span>  
<span data-ttu-id="22024-104">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="22024-104">\<behaviors></span></span>  
<span data-ttu-id="22024-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="22024-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="22024-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="22024-106">\<behavior></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="22024-107">構文</span><span class="sxs-lookup"><span data-stu-id="22024-107">Syntax</span></span>  
  
```xml  
<dispatcherSynchronizationBehavior asynchronousSendEnabled="Boolean"
                                   maxPendingReceives="Integer" />
```  
  
## <a name="type"></a><span data-ttu-id="22024-108">型</span><span class="sxs-lookup"><span data-stu-id="22024-108">Type</span></span>  
  
`Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="22024-109">属性と要素</span><span class="sxs-lookup"><span data-stu-id="22024-109">Attributes and elements</span></span>  
  
<span data-ttu-id="22024-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="22024-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="22024-111">属性</span><span class="sxs-lookup"><span data-stu-id="22024-111">Attributes</span></span>

| <span data-ttu-id="22024-112">属性</span><span class="sxs-lookup"><span data-stu-id="22024-112">Attribute</span></span>               | <span data-ttu-id="22024-113">説明</span><span class="sxs-lookup"><span data-stu-id="22024-113">Description</span></span>       |
| ----------------------- | ----------------- |
| <span data-ttu-id="22024-114">asynchronousSendEnabled</span><span class="sxs-lookup"><span data-stu-id="22024-114">asynchronousSendEnabled</span></span> | <span data-ttu-id="22024-115">非同期の送信動作が有効かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="22024-115">A Boolean that specifies whether asynchronous send behavior is enabled.</span></span> |
| `maxPendingReceives`    | <span data-ttu-id="22024-116">チャネルで発行可能な同時受信の数を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="22024-116">An integer that specifies the number of concurrent receives that can be issued on the channel.</span></span><br /><br /> <span data-ttu-id="22024-117">この値は、サービス調整の動作を適切に構成した後に構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="22024-117">This value should be configured only after you have properly configured service throttling behavior.</span></span> |

### <a name="child-elements"></a><span data-ttu-id="22024-118">子要素</span><span class="sxs-lookup"><span data-stu-id="22024-118">Child elements</span></span>

<span data-ttu-id="22024-119">なし。</span><span class="sxs-lookup"><span data-stu-id="22024-119">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="22024-120">親要素</span><span class="sxs-lookup"><span data-stu-id="22024-120">Parent elements</span></span>

| <span data-ttu-id="22024-121">要素</span><span class="sxs-lookup"><span data-stu-id="22024-121">Element</span></span> | <span data-ttu-id="22024-122">説明</span><span class="sxs-lookup"><span data-stu-id="22024-122">Description</span></span> |  
| ------- | ----------- |  
| [<span data-ttu-id="22024-123">\<behavior></span><span class="sxs-lookup"><span data-stu-id="22024-123">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="22024-124">エンドポイントの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="22024-124">Specifies an endpoint behavior.</span></span> |

## <a name="see-also"></a><span data-ttu-id="22024-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="22024-125">See also</span></span>

- <xref:System.ServiceModel.Configuration.DispatcherSynchronizationElement>
- <xref:System.ServiceModel.Description.DispatcherSynchronizationBehavior>
