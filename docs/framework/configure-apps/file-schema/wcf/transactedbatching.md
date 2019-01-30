---
title: <transactedBatching>
ms.date: 03/30/2017
ms.assetid: 2f790a0d-8f03-4b86-81b5-ce1bc1a6c575
ms.openlocfilehash: 1e8ce41a27bd328c861f2f376a89c57bcd035389
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55281295"
---
# <a name="transactedbatching"></a><span data-ttu-id="114cd-101">\<transactedBatching ></span><span class="sxs-lookup"><span data-stu-id="114cd-101">\<transactedBatching></span></span>
<span data-ttu-id="114cd-102">受信操作でトランザクション バッチがサポートされるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="114cd-102">Specifies whether transaction batching is supported for receive operations.</span></span>  
  
 <span data-ttu-id="114cd-103">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="114cd-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="114cd-104">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="114cd-104">\<behaviors></span></span>  
<span data-ttu-id="114cd-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="114cd-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="114cd-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="114cd-106">\<behavior></span></span>  
<span data-ttu-id="114cd-107">\<transactedBatching ></span><span class="sxs-lookup"><span data-stu-id="114cd-107">\<transactedBatching></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="114cd-108">構文</span><span class="sxs-lookup"><span data-stu-id="114cd-108">Syntax</span></span>  
  
```xml  
<transactedBatching maxBatchSize="Integer" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="114cd-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="114cd-109">Attributes and Elements</span></span>  
 <span data-ttu-id="114cd-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="114cd-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="114cd-111">属性</span><span class="sxs-lookup"><span data-stu-id="114cd-111">Attributes</span></span>  
  
|<span data-ttu-id="114cd-112">属性</span><span class="sxs-lookup"><span data-stu-id="114cd-112">Attribute</span></span>|<span data-ttu-id="114cd-113">説明</span><span class="sxs-lookup"><span data-stu-id="114cd-113">Description</span></span>|  
|---------------|-----------------|  
|`maxBatchSize`|<span data-ttu-id="114cd-114">1 回のトランザクションでまとめてバッチ処理できる受信操作の最大数を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="114cd-114">An integer that specifies the maximum number of receive operations that can be batched together in one transaction.</span></span> <span data-ttu-id="114cd-115">既定値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="114cd-115">The default is 0.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="114cd-116">子要素</span><span class="sxs-lookup"><span data-stu-id="114cd-116">Child Elements</span></span>  
 <span data-ttu-id="114cd-117">なし。</span><span class="sxs-lookup"><span data-stu-id="114cd-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="114cd-118">親要素</span><span class="sxs-lookup"><span data-stu-id="114cd-118">Parent Elements</span></span>  
  
|<span data-ttu-id="114cd-119">要素</span><span class="sxs-lookup"><span data-stu-id="114cd-119">Element</span></span>|<span data-ttu-id="114cd-120">説明</span><span class="sxs-lookup"><span data-stu-id="114cd-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="114cd-121">\<behavior></span><span class="sxs-lookup"><span data-stu-id="114cd-121">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="114cd-122">エンドポイントの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="114cd-122">Specifies an endpoint behavior.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="114cd-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="114cd-123">Remarks</span></span>  
 <span data-ttu-id="114cd-124">トランザクション バッチで構成されるトランスポートは、複数の受信操作を 1 つのトランザクションにバッチ処理しようとします。</span><span class="sxs-lookup"><span data-stu-id="114cd-124">A transport that is configured with transaction batching attempts to batch several receive operations into one transaction.</span></span> <span data-ttu-id="114cd-125">これを実行することにより、受信操作のたびに行うトランザクションの作成とそのコミットの比較的高いコストを回避できます。</span><span class="sxs-lookup"><span data-stu-id="114cd-125">By doing so, the relatively high cost of creating a transaction and committing it in every receive operation is avoided.</span></span>  
  
## <a name="example"></a><span data-ttu-id="114cd-126">例</span><span class="sxs-lookup"><span data-stu-id="114cd-126">Example</span></span>  
 <span data-ttu-id="114cd-127">構成ファイル内でサービスにトランザクション バッチ動作を追加する方法を次の例に示します。</span><span class="sxs-lookup"><span data-stu-id="114cd-127">The following example shows how to add the transacted batching behavior to a service in a configuration file.</span></span>  
  
```xml  
<system.serviceModel>
  <services>
    <service name="Microsoft.ServiceModel.Samples.CalculatorService"
             behaviorConfiguration="CalculatorServiceBehavior">
      <host>
        <baseAddresses>
          <add baseAddress="http://localhost:8000/ServiceModelSamples/service" />
        </baseAddresses>
      </host>
      <!-- Define NetMsmqEndpoint -->
      <endpoint address="net.msmq://localhost/private/ServiceModelSamples"
                binding="netMsmqBinding"
                contract="Microsoft.ServiceModel.Samples.IQueueCalculator" />
      <!-- the mex endpoint is explosed at http://localhost:8000/ServiceModelSamples/service/mex -->
      <endpoint address="mex"
                binding="mexHttpBinding"
                contract="IMetadataExchange" />
    </service>
  </services>
  <behaviors>
    <endpointBehaviors>
      <behavior name="endpointBehavior">
        <transactedBatching maxBatchSize="10" />
      </behavior>
    </endpointBehaviors>
    <serviceBehaviors>
      <behavior name="CalculatorServiceBehavior">
        <serviceMetadata httpGetEnabled="true" />
      </behavior>
    </serviceBehaviors>
  </behaviors>
</system.serviceModel>
```  
  
## <a name="see-also"></a><span data-ttu-id="114cd-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="114cd-128">See also</span></span>
- <xref:System.ServiceModel.Configuration.TransactedBatchingElement>
- <xref:System.ServiceModel.Description.TransactedBatchingBehavior>
