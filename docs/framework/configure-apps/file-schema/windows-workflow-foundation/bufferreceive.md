---
title: '&lt;bufferReceive&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: b23c3a54-10d4-4f13-ab6d-98b26b76f22a
ms.openlocfilehash: 507d58f852544c0eadcefaf997b2345d5e123cfa
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54607515"
---
# <a name="ltbufferreceivegt"></a><span data-ttu-id="92fe9-102">&lt;bufferReceive&gt;</span><span class="sxs-lookup"><span data-stu-id="92fe9-102">&lt;bufferReceive&gt;</span></span>
<span data-ttu-id="92fe9-103">サービスが、バッファーされた受信処理を使用するためのサービス動作。これにより、ワークフロー サービスは、順番を無視したメッセージを処理できます。</span><span class="sxs-lookup"><span data-stu-id="92fe9-103">A service behavior that enables a service to use buffered receive processing, which enables a workflow service to process out-of-order messages.</span></span>  
  
<span data-ttu-id="92fe9-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="92fe9-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="92fe9-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="92fe9-105">\<behaviors></span></span>  
<span data-ttu-id="92fe9-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="92fe9-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="92fe9-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="92fe9-107">\<behavior></span></span>  
<span data-ttu-id="92fe9-108">\<bufferReceive ></span><span class="sxs-lookup"><span data-stu-id="92fe9-108">\<bufferReceive></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="92fe9-109">構文</span><span class="sxs-lookup"><span data-stu-id="92fe9-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <bufferReceive maxPendingMessagesPerChannel="Integer" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="92fe9-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="92fe9-110">Attributes and Elements</span></span>  
 <span data-ttu-id="92fe9-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="92fe9-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="92fe9-112">属性</span><span class="sxs-lookup"><span data-stu-id="92fe9-112">Attributes</span></span>  
  
|<span data-ttu-id="92fe9-113">属性</span><span class="sxs-lookup"><span data-stu-id="92fe9-113">Attribute</span></span>|<span data-ttu-id="92fe9-114">説明</span><span class="sxs-lookup"><span data-stu-id="92fe9-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="92fe9-115">maxPendingMessagesPerChannel</span><span class="sxs-lookup"><span data-stu-id="92fe9-115">maxPendingMessagesPerChannel</span></span>|<span data-ttu-id="92fe9-116">各チャネルで許容される保留状態のメッセージの最大数を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="92fe9-116">An integer that specifies the maximum number of pending messages allowed for each channel.</span></span> <span data-ttu-id="92fe9-117">既定値は 512 です。</span><span class="sxs-lookup"><span data-stu-id="92fe9-117">The default value is 512.</span></span> <span data-ttu-id="92fe9-118">このプロパティは、ワークフロー サービスで受信できる、順番を無視したメッセージの数を制限します。</span><span class="sxs-lookup"><span data-stu-id="92fe9-118">This property limits the number of out-of-order messages that can be received by a workflow service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="92fe9-119">子要素</span><span class="sxs-lookup"><span data-stu-id="92fe9-119">Child Elements</span></span>  
 <span data-ttu-id="92fe9-120">なし。</span><span class="sxs-lookup"><span data-stu-id="92fe9-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="92fe9-121">親要素</span><span class="sxs-lookup"><span data-stu-id="92fe9-121">Parent Elements</span></span>  
  
|<span data-ttu-id="92fe9-122">要素</span><span class="sxs-lookup"><span data-stu-id="92fe9-122">Element</span></span>|<span data-ttu-id="92fe9-123">説明</span><span class="sxs-lookup"><span data-stu-id="92fe9-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="92fe9-124">\<動作 > の\<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="92fe9-124">\<behavior> of \<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="92fe9-125">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="92fe9-125">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="92fe9-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="92fe9-126">See also</span></span>
<!-- <xref:System.ServiceModel.Activities.Description.BufferReceiveServiceBehavior>  -->
- <xref:System.ServiceModel.Activities.Configuration.BufferedReceiveElement>
