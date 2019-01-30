---
title: <bufferReceive>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: b23c3a54-10d4-4f13-ab6d-98b26b76f22a
ms.openlocfilehash: 6ed37d73440dac22288ae1da526d81b2d0b990a1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55286625"
---
# <a name="bufferreceive"></a><span data-ttu-id="9b9ec-101">\<bufferReceive ></span><span class="sxs-lookup"><span data-stu-id="9b9ec-101">\<bufferReceive></span></span>
<span data-ttu-id="9b9ec-102">サービスが、バッファーされた受信処理を使用するためのサービス動作。これにより、ワークフロー サービスは、順番を無視したメッセージを処理できます。</span><span class="sxs-lookup"><span data-stu-id="9b9ec-102">A service behavior that enables a service to use buffered receive processing, which enables a workflow service to process out-of-order messages.</span></span>  
  
<span data-ttu-id="9b9ec-103">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="9b9ec-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="9b9ec-104">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="9b9ec-104">\<behaviors></span></span>  
<span data-ttu-id="9b9ec-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="9b9ec-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="9b9ec-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="9b9ec-106">\<behavior></span></span>  
<span data-ttu-id="9b9ec-107">\<bufferReceive ></span><span class="sxs-lookup"><span data-stu-id="9b9ec-107">\<bufferReceive></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9b9ec-108">構文</span><span class="sxs-lookup"><span data-stu-id="9b9ec-108">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <bufferReceive maxPendingMessagesPerChannel="Integer" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9b9ec-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="9b9ec-109">Attributes and Elements</span></span>  
 <span data-ttu-id="9b9ec-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="9b9ec-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9b9ec-111">属性</span><span class="sxs-lookup"><span data-stu-id="9b9ec-111">Attributes</span></span>  
  
|<span data-ttu-id="9b9ec-112">属性</span><span class="sxs-lookup"><span data-stu-id="9b9ec-112">Attribute</span></span>|<span data-ttu-id="9b9ec-113">説明</span><span class="sxs-lookup"><span data-stu-id="9b9ec-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9b9ec-114">maxPendingMessagesPerChannel</span><span class="sxs-lookup"><span data-stu-id="9b9ec-114">maxPendingMessagesPerChannel</span></span>|<span data-ttu-id="9b9ec-115">各チャネルで許容される保留状態のメッセージの最大数を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="9b9ec-115">An integer that specifies the maximum number of pending messages allowed for each channel.</span></span> <span data-ttu-id="9b9ec-116">既定値は 512 です。</span><span class="sxs-lookup"><span data-stu-id="9b9ec-116">The default value is 512.</span></span> <span data-ttu-id="9b9ec-117">このプロパティは、ワークフロー サービスで受信できる、順番を無視したメッセージの数を制限します。</span><span class="sxs-lookup"><span data-stu-id="9b9ec-117">This property limits the number of out-of-order messages that can be received by a workflow service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9b9ec-118">子要素</span><span class="sxs-lookup"><span data-stu-id="9b9ec-118">Child Elements</span></span>  
 <span data-ttu-id="9b9ec-119">なし。</span><span class="sxs-lookup"><span data-stu-id="9b9ec-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9b9ec-120">親要素</span><span class="sxs-lookup"><span data-stu-id="9b9ec-120">Parent Elements</span></span>  
  
|<span data-ttu-id="9b9ec-121">要素</span><span class="sxs-lookup"><span data-stu-id="9b9ec-121">Element</span></span>|<span data-ttu-id="9b9ec-122">説明</span><span class="sxs-lookup"><span data-stu-id="9b9ec-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9b9ec-123">\<動作 > の\<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="9b9ec-123">\<behavior> of \<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="9b9ec-124">動作の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="9b9ec-124">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9b9ec-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b9ec-125">See also</span></span>
<!-- <xref:System.ServiceModel.Activities.Description.BufferReceiveServiceBehavior>  -->
- <xref:System.ServiceModel.Activities.Configuration.BufferedReceiveElement>
