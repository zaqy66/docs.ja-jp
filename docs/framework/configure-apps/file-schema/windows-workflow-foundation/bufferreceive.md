---
title: <bufferReceive>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: b23c3a54-10d4-4f13-ab6d-98b26b76f22a
ms.openlocfilehash: 1e095e3da11277c6b7b3c24e98a769500e1a0c0b
ms.sourcegitcommit: 01ea420eaa4bf76d5fc47673294c8881379b3369
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2019
ms.locfileid: "55759536"
---
# <a name="bufferreceive"></a><span data-ttu-id="a6482-101">\<bufferReceive ></span><span class="sxs-lookup"><span data-stu-id="a6482-101">\<bufferReceive></span></span>
<span data-ttu-id="a6482-102">サービスが、バッファーされた受信処理を使用するためのサービス動作。これにより、ワークフロー サービスは、順番を無視したメッセージを処理できます。</span><span class="sxs-lookup"><span data-stu-id="a6482-102">A service behavior that enables a service to use buffered receive processing, which enables a workflow service to process out-of-order messages.</span></span>  
  
<span data-ttu-id="a6482-103">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="a6482-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="a6482-104">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="a6482-104">\<behaviors></span></span>  
<span data-ttu-id="a6482-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="a6482-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="a6482-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="a6482-106">\<behavior></span></span>  
<span data-ttu-id="a6482-107">\<bufferReceive ></span><span class="sxs-lookup"><span data-stu-id="a6482-107">\<bufferReceive></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a6482-108">構文</span><span class="sxs-lookup"><span data-stu-id="a6482-108">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <bufferReceive maxPendingMessagesPerChannel="Integer" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a6482-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="a6482-109">Attributes and Elements</span></span>  
 <span data-ttu-id="a6482-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="a6482-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a6482-111">属性</span><span class="sxs-lookup"><span data-stu-id="a6482-111">Attributes</span></span>  
  
|<span data-ttu-id="a6482-112">属性</span><span class="sxs-lookup"><span data-stu-id="a6482-112">Attribute</span></span>|<span data-ttu-id="a6482-113">説明</span><span class="sxs-lookup"><span data-stu-id="a6482-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a6482-114">maxPendingMessagesPerChannel</span><span class="sxs-lookup"><span data-stu-id="a6482-114">maxPendingMessagesPerChannel</span></span>|<span data-ttu-id="a6482-115">各チャネルで許容される保留状態のメッセージの最大数を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="a6482-115">An integer that specifies the maximum number of pending messages allowed for each channel.</span></span> <span data-ttu-id="a6482-116">既定値は 512 です。</span><span class="sxs-lookup"><span data-stu-id="a6482-116">The default value is 512.</span></span> <span data-ttu-id="a6482-117">このプロパティは、ワークフロー サービスで受信できる、順番を無視したメッセージの数を制限します。</span><span class="sxs-lookup"><span data-stu-id="a6482-117">This property limits the number of out-of-order messages that can be received by a workflow service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a6482-118">子要素</span><span class="sxs-lookup"><span data-stu-id="a6482-118">Child Elements</span></span>  
 <span data-ttu-id="a6482-119">なし。</span><span class="sxs-lookup"><span data-stu-id="a6482-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a6482-120">親要素</span><span class="sxs-lookup"><span data-stu-id="a6482-120">Parent Elements</span></span>  
  
|<span data-ttu-id="a6482-121">要素</span><span class="sxs-lookup"><span data-stu-id="a6482-121">Element</span></span>|<span data-ttu-id="a6482-122">説明</span><span class="sxs-lookup"><span data-stu-id="a6482-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a6482-123">\<動作 > の\<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="a6482-123">\<behavior> of \<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="a6482-124">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="a6482-124">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a6482-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6482-125">See also</span></span>
- <xref:System.ServiceModel.Activities.Description.BufferedReceiveServiceBehavior>
- <xref:System.ServiceModel.Activities.Configuration.BufferedReceiveElement>
