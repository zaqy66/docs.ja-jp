---
title: '&lt;mexHttpsBinding&gt;'
ms.date: 03/30/2017
ms.assetid: f2ed3774-78b9-4a15-b79b-655f1ad68b86
ms.openlocfilehash: d56e90162f2a852ff4d0b66abcf3fe03c4110c37
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/07/2018
ms.locfileid: "48846488"
---
# <a name="ltmexhttpsbindinggt"></a><span data-ttu-id="62228-102">&lt;mexHttpsBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="62228-102">&lt;mexHttpsBinding&gt;</span></span>
<span data-ttu-id="62228-103">HTTPS 経由の WS-MetadataExchange (WS-MEX) メッセージ交換に使用されるバインディングの設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="62228-103">Specifies the settings for a binding used for the WS-MetadataExchange (WS-MEX) message exchange over HTTPS.</span></span>  
  
 <span data-ttu-id="62228-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="62228-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="62228-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="62228-105">\<bindings></span></span>  
<span data-ttu-id="62228-106">\<mexHttpsBinding></span><span class="sxs-lookup"><span data-stu-id="62228-106">\<mexHttpsBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="62228-107">構文</span><span class="sxs-lookup"><span data-stu-id="62228-107">Syntax</span></span>  
  
```xml  
<mexHttpsBinding>  
   <binding   
       closeTimeout="TimeSpan"   
       name="string"   
       openTimeout="TimeSpan"   
       receiveTimeout="TimeSpan"  
       sendTimeout="TimeSpan">  
   </binding>  
</mexHttpsBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="62228-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="62228-108">Attributes and Elements</span></span>  
 <span data-ttu-id="62228-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="62228-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="62228-110">属性</span><span class="sxs-lookup"><span data-stu-id="62228-110">Attributes</span></span>  
  
|<span data-ttu-id="62228-111">属性</span><span class="sxs-lookup"><span data-stu-id="62228-111">Attribute</span></span>|<span data-ttu-id="62228-112">説明</span><span class="sxs-lookup"><span data-stu-id="62228-112">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="62228-113">クローズ操作が完了するまでの期間を指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="62228-113">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="62228-114">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="62228-114">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="62228-115">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="62228-115">The default is 00:01:00.</span></span>|  
|`name`|<span data-ttu-id="62228-116">バインディングの構成名を格納する文字列です。</span><span class="sxs-lookup"><span data-stu-id="62228-116">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="62228-117">この値は、バインディングの ID として使用されるため、一意にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="62228-117">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="62228-118">各バインドには、サービスのメタデータでこれをまとめて一意に識別する `name` および `namespace` 属性が含まれています。</span><span class="sxs-lookup"><span data-stu-id="62228-118">Each binding has a `name` and `namespace` attribute that together uniquely identify it in the metadata of the service.</span></span> <span data-ttu-id="62228-119">また、この名前は、同じ種類のバインディング間で一意です。</span><span class="sxs-lookup"><span data-stu-id="62228-119">In addition, this name is unique among bindings of the same type.</span></span> <span data-ttu-id="62228-120">[!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)] 以降では、バインディングおよび動作に名前を付ける必要はありません。</span><span class="sxs-lookup"><span data-stu-id="62228-120">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="62228-121">既定の構成と無名のバインディングおよび動作の詳細については、「[簡略化された構成](../../../../../docs/framework/wcf/simplified-configuration.md)」と「[WCF サービスの構成を簡略化](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62228-121">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|`openTimeout`|<span data-ttu-id="62228-122">実行中の操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。</span><span class="sxs-lookup"><span data-stu-id="62228-122">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="62228-123">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="62228-123">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="62228-124">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="62228-124">The default is 00:01:00.</span></span>|  
|`receiveTimeout`|<span data-ttu-id="62228-125">受信操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。</span><span class="sxs-lookup"><span data-stu-id="62228-125">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="62228-126">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="62228-126">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="62228-127">既定値は 00:10:00 です。</span><span class="sxs-lookup"><span data-stu-id="62228-127">The default is 00:10:00.</span></span>|  
|`sendTimeout`|<span data-ttu-id="62228-128">送信操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。</span><span class="sxs-lookup"><span data-stu-id="62228-128">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="62228-129">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="62228-129">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="62228-130">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="62228-130">The default is 00:01:00.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="62228-131">子要素</span><span class="sxs-lookup"><span data-stu-id="62228-131">Child Elements</span></span>  
 <span data-ttu-id="62228-132">なし。</span><span class="sxs-lookup"><span data-stu-id="62228-132">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="62228-133">親要素</span><span class="sxs-lookup"><span data-stu-id="62228-133">Parent Elements</span></span>  
  
|<span data-ttu-id="62228-134">要素</span><span class="sxs-lookup"><span data-stu-id="62228-134">Element</span></span>|<span data-ttu-id="62228-135">説明</span><span class="sxs-lookup"><span data-stu-id="62228-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="62228-136">\<bindings></span><span class="sxs-lookup"><span data-stu-id="62228-136">\<bindings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|<span data-ttu-id="62228-137">この要素には、標準バインディングおよびカスタム バインドのコレクションが保持されます。</span><span class="sxs-lookup"><span data-stu-id="62228-137">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="62228-138">Remarks</span><span class="sxs-lookup"><span data-stu-id="62228-138">Remarks</span></span>  
 <span data-ttu-id="62228-139">このバインディングは、基本的には証明書を使用してトランスポート レベルのセキュリティをサポートする `WSHttpBinding` バインディングです。</span><span class="sxs-lookup"><span data-stu-id="62228-139">This binding is essentially a `WSHttpBinding` binding that supports transport-level security using certificates.</span></span> <span data-ttu-id="62228-140">構成して、このようなメタデータ エンドポイントを使用しての詳細については、次を参照してください[方法: カスタム Ws-metadata Exchange バインディングを構成する](../../../../../docs/framework/wcf/extending/how-to-configure-a-custom-ws-metadata-exchange-binding.md)、[方法: 取得メタデータ経由で、MEX 以外のバインディング](../../../../../docs/framework/wcf/extending/how-to-retrieve-metadata-over-a-non-mex-binding.md)、および。サンプル[メタデータ エンドポイントのセキュリティで保護されたカスタム](../../../../../docs/framework/wcf/samples/custom-secure-metadata-endpoint.md)します。</span><span class="sxs-lookup"><span data-stu-id="62228-140">For more information about configuring and using such a metadata endpoint, see [How to: Configure a Custom WS-Metadata Exchange Binding](../../../../../docs/framework/wcf/extending/how-to-configure-a-custom-ws-metadata-exchange-binding.md), [How to: Retrieve Metadata Over a non-MEX Binding](../../../../../docs/framework/wcf/extending/how-to-retrieve-metadata-over-a-non-mex-binding.md), and the sample [Custom Secure Metadata Endpoint](../../../../../docs/framework/wcf/samples/custom-secure-metadata-endpoint.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62228-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="62228-141">See Also</span></span>  
 <xref:System.ServiceModel.Description.MetadataExchangeBindings.CreateMexHttpsBinding%2A>  
 <xref:System.ServiceModel.Configuration.MexHttpsBindingElement>  
 [<span data-ttu-id="62228-142">方法 : 構成ファイルを使用してサービスのメタデータを公開する</span><span class="sxs-lookup"><span data-stu-id="62228-142">How to: Publish Metadata for a Service Using a Configuration File</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)  
 [<span data-ttu-id="62228-143">カスタム バインディングを介したメタデータの公開と取得</span><span class="sxs-lookup"><span data-stu-id="62228-143">Publishing and Retrieving Metadata Over a Custom Binding</span></span>](../../../../../docs/framework/wcf/extending/publishing-and-retrieving-metadata-over-a-custom-binding.md)  
 [<span data-ttu-id="62228-144">方法 : カスタム WS-Metadata Exchange バインディングを構成する</span><span class="sxs-lookup"><span data-stu-id="62228-144">How to: Configure a Custom WS-Metadata Exchange Binding</span></span>](../../../../../docs/framework/wcf/extending/how-to-configure-a-custom-ws-metadata-exchange-binding.md)  
 [<span data-ttu-id="62228-145">方法 : MEX 以外のバインディングを介してメタデータを取得する</span><span class="sxs-lookup"><span data-stu-id="62228-145">How to: Retrieve Metadata Over a non-MEX Binding</span></span>](../../../../../docs/framework/wcf/extending/how-to-retrieve-metadata-over-a-non-mex-binding.md)  
 [<span data-ttu-id="62228-146">カスタム セキュア メタデータ エンドポイント</span><span class="sxs-lookup"><span data-stu-id="62228-146">Custom Secure Metadata Endpoint</span></span>](../../../../../docs/framework/wcf/samples/custom-secure-metadata-endpoint.md)  
 [<span data-ttu-id="62228-147">メタデータ</span><span class="sxs-lookup"><span data-stu-id="62228-147">Metadata</span></span>](../../../../../docs/framework/wcf/feature-details/metadata.md)  
 [<span data-ttu-id="62228-148">バインディング</span><span class="sxs-lookup"><span data-stu-id="62228-148">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="62228-149">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="62228-149">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="62228-150">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="62228-150">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="62228-151">\<binding></span><span class="sxs-lookup"><span data-stu-id="62228-151">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
