---
title: '&lt;oneWay&gt;'
ms.date: 03/30/2017
ms.assetid: 00e67e0e-77c0-4695-9138-c0997b0e5f3c
ms.openlocfilehash: 5f3d534ee98100347acaa485e60a3c74f82ee0b9
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150579"
---
# <a name="ltonewaygt"></a><span data-ttu-id="39eb2-102">&lt;oneWay&gt;</span><span class="sxs-lookup"><span data-stu-id="39eb2-102">&lt;oneWay&gt;</span></span>
<span data-ttu-id="39eb2-103">カスタム バインドのパケット ルーティングを有効にし、一方向メソッドを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="39eb2-103">Enables packet routing and the use of one-way methods for a custom binding.</span></span>  
  
 <span data-ttu-id="39eb2-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="39eb2-104">\<system.serviceModel></span></span>  
<span data-ttu-id="39eb2-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="39eb2-105">\<bindings></span></span>  
<span data-ttu-id="39eb2-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="39eb2-106">\<customBinding></span></span>  
<span data-ttu-id="39eb2-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="39eb2-107">\<binding></span></span>  
<span data-ttu-id="39eb2-108">\<oneWay ></span><span class="sxs-lookup"><span data-stu-id="39eb2-108">\<oneWay></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="39eb2-109">構文</span><span class="sxs-lookup"><span data-stu-id="39eb2-109">Syntax</span></span>  
  
```xml  
<oneWay packetRoutable="Boolean">
  <channelPoolSettings idleTimeout="TimeSpan"
                       leaseTimeout="TimeSpan"
                       maxOutboundConnectionsPerEndpopint="Integer" />
</oneWay>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="39eb2-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="39eb2-110">Attributes and Elements</span></span>  
 <span data-ttu-id="39eb2-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="39eb2-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="39eb2-112">属性</span><span class="sxs-lookup"><span data-stu-id="39eb2-112">Attributes</span></span>  
  
|<span data-ttu-id="39eb2-113">属性</span><span class="sxs-lookup"><span data-stu-id="39eb2-113">Attribute</span></span>|<span data-ttu-id="39eb2-114">説明</span><span class="sxs-lookup"><span data-stu-id="39eb2-114">Description</span></span>|  
|---------------|-----------------|  
|`packetRoutable`|<span data-ttu-id="39eb2-115">パケット ルーティングが有効かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="39eb2-115">A Boolean value that specifies whether packet routing is enabled.</span></span> <span data-ttu-id="39eb2-116">既定値は、`false` です。</span><span class="sxs-lookup"><span data-stu-id="39eb2-116">The default is `false`.</span></span>|  
|`MaxAcceptedChannels`|<span data-ttu-id="39eb2-117">許容できるチャネルの最大数を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="39eb2-117">An integer that specifies the maximum number of channels that can be accepted.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="39eb2-118">子要素</span><span class="sxs-lookup"><span data-stu-id="39eb2-118">Child Elements</span></span>  
  
|<span data-ttu-id="39eb2-119">要素</span><span class="sxs-lookup"><span data-stu-id="39eb2-119">Element</span></span>|<span data-ttu-id="39eb2-120">説明</span><span class="sxs-lookup"><span data-stu-id="39eb2-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="39eb2-121">\<channelPoolSettings ></span><span class="sxs-lookup"><span data-stu-id="39eb2-121">\<channelPoolSettings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/channelpoolsettings.md)|<span data-ttu-id="39eb2-122">現在のチャネルのチャネル プールのプロパティを格納する <xref:System.ServiceModel.Configuration.ChannelPoolSettingsElement> オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="39eb2-122">A <xref:System.ServiceModel.Configuration.ChannelPoolSettingsElement> object that contains properties of the channel pool for the current channel.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="39eb2-123">親要素</span><span class="sxs-lookup"><span data-stu-id="39eb2-123">Parent Elements</span></span>  
  
|<span data-ttu-id="39eb2-124">要素</span><span class="sxs-lookup"><span data-stu-id="39eb2-124">Element</span></span>|<span data-ttu-id="39eb2-125">説明</span><span class="sxs-lookup"><span data-stu-id="39eb2-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="39eb2-126">\<binding></span><span class="sxs-lookup"><span data-stu-id="39eb2-126">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="39eb2-127">カスタム バインドのすべてのバインド機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="39eb2-127">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="39eb2-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="39eb2-128">Remarks</span></span>  
 <span data-ttu-id="39eb2-129">パケット ルーティングを有効にするには、この要素が提供する "一方向の変換" 層が必要です。</span><span class="sxs-lookup"><span data-stu-id="39eb2-129">To enable packet routing, a one-way conversion layer is required, which this element provides.</span></span> <span data-ttu-id="39eb2-130">カスタム バインディングを作成し、このバインディングをセッション対応または要求応答のトランスポートの上に重ねて、パケット ルーティング可能にすることができます。</span><span class="sxs-lookup"><span data-stu-id="39eb2-130">A user can create a custom binding that layers this binding over a session-aware or request-reply transport to make it packet routable.</span></span> <span data-ttu-id="39eb2-131">この要素は、一方向メソッドをよりネイティブな形式で公開するときにも役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="39eb2-131">This element is also useful when you want to expose one-way methods in a more native fashion.</span></span> <span data-ttu-id="39eb2-132">複合二重や信頼できるメッセージ機能などのさらに大きい変換は、この層に対して適用できます。</span><span class="sxs-lookup"><span data-stu-id="39eb2-132">More transformations can be applied over this layer, such as Composite Duplex and Reliable Messaging.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="39eb2-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="39eb2-133">See Also</span></span>  
 <xref:System.ServiceModel.Channels.OneWayBindingElement>  
 <xref:System.ServiceModel.Configuration.OneWayElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="39eb2-134">バインディング</span><span class="sxs-lookup"><span data-stu-id="39eb2-134">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="39eb2-135">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="39eb2-135">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="39eb2-136">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="39eb2-136">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="39eb2-137">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="39eb2-137">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
