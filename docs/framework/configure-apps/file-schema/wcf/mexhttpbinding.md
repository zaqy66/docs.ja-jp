---
title: <mexHttpBinding>
ms.date: 03/30/2017
ms.assetid: e50b2e1f-9668-41a5-8077-dee7abff9f0f
ms.openlocfilehash: 9d37a4918101b18c3002f2dcb926b9a03e0057a2
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55266335"
---
# <a name="mexhttpbinding"></a><span data-ttu-id="9347d-101">\<mexHttpBinding></span><span class="sxs-lookup"><span data-stu-id="9347d-101">\<mexHttpBinding></span></span>
<span data-ttu-id="9347d-102">HTTP 経由の WS-MetadataExchange (WS-MEX) メッセージ交換に使用されるバインディングの設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="9347d-102">Specifies the settings for a binding used for the WS-MetadataExchange (WS-MEX) message exchange over HTTP.</span></span>  
  
 <span data-ttu-id="9347d-103">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="9347d-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="9347d-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="9347d-104">\<bindings></span></span>  
<span data-ttu-id="9347d-105">\<mexHttpBinding></span><span class="sxs-lookup"><span data-stu-id="9347d-105">\<mexHttpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9347d-106">構文</span><span class="sxs-lookup"><span data-stu-id="9347d-106">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9347d-107">属性および要素</span><span class="sxs-lookup"><span data-stu-id="9347d-107">Attributes and Elements</span></span>  
 <span data-ttu-id="9347d-108">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="9347d-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9347d-109">属性</span><span class="sxs-lookup"><span data-stu-id="9347d-109">Attributes</span></span>  
  
|<span data-ttu-id="9347d-110">属性</span><span class="sxs-lookup"><span data-stu-id="9347d-110">Attribute</span></span>|<span data-ttu-id="9347d-111">説明</span><span class="sxs-lookup"><span data-stu-id="9347d-111">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="9347d-112">クローズ操作が完了するまでの期間を指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="9347d-112">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="9347d-113">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9347d-113">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="9347d-114">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="9347d-114">The default is 00:01:00.</span></span>|  
|`name`|<span data-ttu-id="9347d-115">バインディングの構成名を格納する文字列です。</span><span class="sxs-lookup"><span data-stu-id="9347d-115">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="9347d-116">この値は、バインディングの ID として使用されるため、一意にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9347d-116">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="9347d-117">各バインドには、サービスのメタデータでこれをまとめて一意に識別する `name` および `namespace` 属性が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9347d-117">Each binding has a `name` and `namespace` attribute that together uniquely identify it in the metadata of the service.</span></span> <span data-ttu-id="9347d-118">また、この名前は、同じ種類のバインディング間で一意です。</span><span class="sxs-lookup"><span data-stu-id="9347d-118">In addition, this name is unique among bindings of the same type.</span></span> <span data-ttu-id="9347d-119">[!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)] 以降では、バインディングおよび動作に名前を付ける必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9347d-119">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="9347d-120">既定の構成と無名のバインディングおよび動作の詳細については、「[簡略化された構成](../../../../../docs/framework/wcf/simplified-configuration.md)」と「[WCF サービスの構成を簡略化](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9347d-120">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|`openTimeout`|<span data-ttu-id="9347d-121">実行中の操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。</span><span class="sxs-lookup"><span data-stu-id="9347d-121">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="9347d-122">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9347d-122">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="9347d-123">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="9347d-123">The default is 00:01:00.</span></span>|  
|`receiveTimeout`|<span data-ttu-id="9347d-124">受信操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。</span><span class="sxs-lookup"><span data-stu-id="9347d-124">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="9347d-125">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9347d-125">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="9347d-126">既定値は 00:10:00 です。</span><span class="sxs-lookup"><span data-stu-id="9347d-126">The default is 00:10:00.</span></span>|  
|`sendTimeout`|<span data-ttu-id="9347d-127">送信操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。</span><span class="sxs-lookup"><span data-stu-id="9347d-127">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="9347d-128">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9347d-128">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="9347d-129">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="9347d-129">The default is 00:01:00.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9347d-130">子要素</span><span class="sxs-lookup"><span data-stu-id="9347d-130">Child Elements</span></span>  
 <span data-ttu-id="9347d-131">なし。</span><span class="sxs-lookup"><span data-stu-id="9347d-131">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9347d-132">親要素</span><span class="sxs-lookup"><span data-stu-id="9347d-132">Parent Elements</span></span>  
  
|<span data-ttu-id="9347d-133">要素</span><span class="sxs-lookup"><span data-stu-id="9347d-133">Element</span></span>|<span data-ttu-id="9347d-134">説明</span><span class="sxs-lookup"><span data-stu-id="9347d-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9347d-135">\<bindings></span><span class="sxs-lookup"><span data-stu-id="9347d-135">\<bindings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|<span data-ttu-id="9347d-136">この要素には、標準バインディングおよびカスタム バインドのコレクションが保持されます。</span><span class="sxs-lookup"><span data-stu-id="9347d-136">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9347d-137">Remarks</span><span class="sxs-lookup"><span data-stu-id="9347d-137">Remarks</span></span>  
 <span data-ttu-id="9347d-138">このバインディングは、基本的にはセキュリティを無効にした `WSHttpBinding` バインディングです。</span><span class="sxs-lookup"><span data-stu-id="9347d-138">This binding is essentially a `WSHttpBinding` binding with security disabled.</span></span> <span data-ttu-id="9347d-139">ほとんどのメタデータ要求に対応します。</span><span class="sxs-lookup"><span data-stu-id="9347d-139">It supports most metadata requests.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9347d-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="9347d-140">See also</span></span>
- <xref:System.ServiceModel.Description.MetadataExchangeBindings.CreateMexHttpBinding%2A>
- <xref:System.ServiceModel.Configuration.MexHttpBindingElement>
- [<span data-ttu-id="9347d-141">方法: 構成ファイルを使用してサービスのメタデータを公開します。</span><span class="sxs-lookup"><span data-stu-id="9347d-141">How to: Publish Metadata for a Service Using a Configuration File</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [<span data-ttu-id="9347d-142">カスタム バインディングを介したメタデータの公開と取得</span><span class="sxs-lookup"><span data-stu-id="9347d-142">Publishing and Retrieving Metadata Over a Custom Binding</span></span>](../../../../../docs/framework/wcf/extending/publishing-and-retrieving-metadata-over-a-custom-binding.md)
- [<span data-ttu-id="9347d-143">メタデータ</span><span class="sxs-lookup"><span data-stu-id="9347d-143">Metadata</span></span>](../../../../../docs/framework/wcf/feature-details/metadata.md)
- [<span data-ttu-id="9347d-144">バインディング</span><span class="sxs-lookup"><span data-stu-id="9347d-144">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="9347d-145">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="9347d-145">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="9347d-146">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="9347d-146">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="9347d-147">\<binding></span><span class="sxs-lookup"><span data-stu-id="9347d-147">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
