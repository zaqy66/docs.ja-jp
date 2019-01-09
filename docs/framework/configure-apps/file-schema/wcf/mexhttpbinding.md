---
title: '&lt;mexHttpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: e50b2e1f-9668-41a5-8077-dee7abff9f0f
ms.openlocfilehash: c60fcf5071d52d30c1b6b99a19640a0fdc1265f8
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148657"
---
# <a name="ltmexhttpbindinggt"></a><span data-ttu-id="9fac5-102">&lt;mexHttpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="9fac5-102">&lt;mexHttpBinding&gt;</span></span>
<span data-ttu-id="9fac5-103">HTTP 経由の WS-MetadataExchange (WS-MEX) メッセージ交換に使用されるバインディングの設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="9fac5-103">Specifies the settings for a binding used for the WS-MetadataExchange (WS-MEX) message exchange over HTTP.</span></span>  
  
 <span data-ttu-id="9fac5-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="9fac5-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="9fac5-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="9fac5-105">\<bindings></span></span>  
<span data-ttu-id="9fac5-106">\<mexHttpBinding></span><span class="sxs-lookup"><span data-stu-id="9fac5-106">\<mexHttpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9fac5-107">構文</span><span class="sxs-lookup"><span data-stu-id="9fac5-107">Syntax</span></span>  
  
```xml  
<mexHttpBinding>
  <binding closeTimeout="TimeSpan"
           name="string"
           openTimeout="TimeSpan"
           receiveTimeout="TimeSpan"
           sendTimeout="TimeSpan">
  </binding>
</mexHttpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9fac5-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="9fac5-108">Attributes and Elements</span></span>  
 <span data-ttu-id="9fac5-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="9fac5-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9fac5-110">属性</span><span class="sxs-lookup"><span data-stu-id="9fac5-110">Attributes</span></span>  
  
|<span data-ttu-id="9fac5-111">属性</span><span class="sxs-lookup"><span data-stu-id="9fac5-111">Attribute</span></span>|<span data-ttu-id="9fac5-112">説明</span><span class="sxs-lookup"><span data-stu-id="9fac5-112">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="9fac5-113">クローズ操作が完了するまでの期間を指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="9fac5-113">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="9fac5-114">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9fac5-114">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="9fac5-115">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="9fac5-115">The default is 00:01:00.</span></span>|  
|`name`|<span data-ttu-id="9fac5-116">バインディングの構成名を格納する文字列です。</span><span class="sxs-lookup"><span data-stu-id="9fac5-116">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="9fac5-117">この値は、バインディングの ID として使用されるため、一意にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9fac5-117">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="9fac5-118">各バインドには、サービスのメタデータでこれをまとめて一意に識別する `name` および `namespace` 属性が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9fac5-118">Each binding has a `name` and `namespace` attribute that together uniquely identify it in the metadata of the service.</span></span> <span data-ttu-id="9fac5-119">また、この名前は、同じ種類のバインディング間で一意です。</span><span class="sxs-lookup"><span data-stu-id="9fac5-119">In addition, this name is unique among bindings of the same type.</span></span> <span data-ttu-id="9fac5-120">[!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)] 以降では、バインディングおよび動作に名前を付ける必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9fac5-120">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="9fac5-121">既定の構成と無名のバインディングおよび動作の詳細については、「[簡略化された構成](../../../../../docs/framework/wcf/simplified-configuration.md)」と「[WCF サービスの構成を簡略化](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9fac5-121">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|`openTimeout`|<span data-ttu-id="9fac5-122">実行中の操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。</span><span class="sxs-lookup"><span data-stu-id="9fac5-122">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="9fac5-123">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9fac5-123">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="9fac5-124">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="9fac5-124">The default is 00:01:00.</span></span>|  
|`receiveTimeout`|<span data-ttu-id="9fac5-125">受信操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。</span><span class="sxs-lookup"><span data-stu-id="9fac5-125">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="9fac5-126">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9fac5-126">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="9fac5-127">既定値は 00:10:00 です。</span><span class="sxs-lookup"><span data-stu-id="9fac5-127">The default is 00:10:00.</span></span>|  
|`sendTimeout`|<span data-ttu-id="9fac5-128">送信操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。</span><span class="sxs-lookup"><span data-stu-id="9fac5-128">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="9fac5-129">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9fac5-129">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="9fac5-130">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="9fac5-130">The default is 00:01:00.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9fac5-131">子要素</span><span class="sxs-lookup"><span data-stu-id="9fac5-131">Child Elements</span></span>  
 <span data-ttu-id="9fac5-132">なし。</span><span class="sxs-lookup"><span data-stu-id="9fac5-132">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9fac5-133">親要素</span><span class="sxs-lookup"><span data-stu-id="9fac5-133">Parent Elements</span></span>  
  
|<span data-ttu-id="9fac5-134">要素</span><span class="sxs-lookup"><span data-stu-id="9fac5-134">Element</span></span>|<span data-ttu-id="9fac5-135">説明</span><span class="sxs-lookup"><span data-stu-id="9fac5-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9fac5-136">\<bindings></span><span class="sxs-lookup"><span data-stu-id="9fac5-136">\<bindings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|<span data-ttu-id="9fac5-137">この要素には、標準バインディングおよびカスタム バインドのコレクションが保持されます。</span><span class="sxs-lookup"><span data-stu-id="9fac5-137">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9fac5-138">Remarks</span><span class="sxs-lookup"><span data-stu-id="9fac5-138">Remarks</span></span>  
 <span data-ttu-id="9fac5-139">このバインディングは、基本的にはセキュリティを無効にした `WSHttpBinding` バインディングです。</span><span class="sxs-lookup"><span data-stu-id="9fac5-139">This binding is essentially a `WSHttpBinding` binding with security disabled.</span></span> <span data-ttu-id="9fac5-140">ほとんどのメタデータ要求に対応します。</span><span class="sxs-lookup"><span data-stu-id="9fac5-140">It supports most metadata requests.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9fac5-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="9fac5-141">See Also</span></span>  
 <xref:System.ServiceModel.Description.MetadataExchangeBindings.CreateMexHttpBinding%2A>  
 <xref:System.ServiceModel.Configuration.MexHttpBindingElement>  
 [<span data-ttu-id="9fac5-142">方法: 構成ファイルを使用してサービスのメタデータを公開します。</span><span class="sxs-lookup"><span data-stu-id="9fac5-142">How to: Publish Metadata for a Service Using a Configuration File</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)  
 [<span data-ttu-id="9fac5-143">カスタム バインディングを介したメタデータの公開と取得</span><span class="sxs-lookup"><span data-stu-id="9fac5-143">Publishing and Retrieving Metadata Over a Custom Binding</span></span>](../../../../../docs/framework/wcf/extending/publishing-and-retrieving-metadata-over-a-custom-binding.md)  
 [<span data-ttu-id="9fac5-144">メタデータ</span><span class="sxs-lookup"><span data-stu-id="9fac5-144">Metadata</span></span>](../../../../../docs/framework/wcf/feature-details/metadata.md)  
 [<span data-ttu-id="9fac5-145">バインディング</span><span class="sxs-lookup"><span data-stu-id="9fac5-145">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="9fac5-146">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="9fac5-146">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="9fac5-147">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="9fac5-147">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="9fac5-148">\<binding></span><span class="sxs-lookup"><span data-stu-id="9fac5-148">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
