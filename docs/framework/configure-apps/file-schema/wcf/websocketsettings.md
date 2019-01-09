---
title: '&lt;webSocketSettings&gt;'
ms.date: 03/30/2017
ms.assetid: bbf97e02-8dd1-4922-acac-3cd33397b249
ms.openlocfilehash: 134a233a337c40d21f7547fe385ec788cef2165b
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150059"
---
# <a name="ltwebsocketsettingsgt"></a><span data-ttu-id="d5374-102">&lt;webSocketSettings&gt;</span><span class="sxs-lookup"><span data-stu-id="d5374-102">&lt;webSocketSettings&gt;</span></span>
<span data-ttu-id="d5374-103">Web ソケット設定を指定するために使用される構成要素。</span><span class="sxs-lookup"><span data-stu-id="d5374-103">A configuration element used to specify Web Socket settings.</span></span>  
  
<span data-ttu-id="d5374-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="d5374-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="d5374-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="d5374-105">\<bindings></span></span>  
<span data-ttu-id="d5374-106">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="d5374-106">\<netHttpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d5374-107">構文</span><span class="sxs-lookup"><span data-stu-id="d5374-107">Syntax</span></span>  
  
```xml  
<netHttpBinding>
  <binding>
    <webSocketSettings createNotificationOnConnection="Boolean"
                       disablePayloadMasking="Boolean"
                       keepAliveInterval="TimeSpan"
                       maxPendingConnections="Integer"
                       receiveBufferSize="Integer"
                       sendBufferSize="Integer"
                       subProtocol="String"
                       transportUsage="WhenDuplex/Always/Never" />
  </binding>
</netHttpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d5374-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="d5374-108">Attributes and Elements</span></span>  
 <span data-ttu-id="d5374-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="d5374-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d5374-110">属性</span><span class="sxs-lookup"><span data-stu-id="d5374-110">Attributes</span></span>  
  
|<span data-ttu-id="d5374-111">属性</span><span class="sxs-lookup"><span data-stu-id="d5374-111">Attribute</span></span>|<span data-ttu-id="d5374-112">説明</span><span class="sxs-lookup"><span data-stu-id="d5374-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="d5374-113">createNotificationOnConnection</span><span class="sxs-lookup"><span data-stu-id="d5374-113">createNotificationOnConnection</span></span>|<span data-ttu-id="d5374-114">通知を接続時に送信するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d5374-114">Specifies whether a notification is sent upon connection.</span></span>|  
|<span data-ttu-id="d5374-115">disablePayloadMasking</span><span class="sxs-lookup"><span data-stu-id="d5374-115">disablePayloadMasking</span></span>|<span data-ttu-id="d5374-116">Web ソケットのマスクが無効であるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d5374-116">Specifies whether Web Socket masking is disabled.</span></span>|  
|<span data-ttu-id="d5374-117">keepAliveInterval</span><span class="sxs-lookup"><span data-stu-id="d5374-117">keepAliveInterval</span></span>|<span data-ttu-id="d5374-118">接続維持の間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5374-118">Specifies the keep alive interval.</span></span>|  
|<span data-ttu-id="d5374-119">maxPendingConnections</span><span class="sxs-lookup"><span data-stu-id="d5374-119">maxPendingConnections</span></span>|<span data-ttu-id="d5374-120">サービスでのディスパッチを待機している接続の最大数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5374-120">Specifies the maximum number of connections awaiting dispatch on the service.</span></span>|  
|<span data-ttu-id="d5374-121">receiveBufferSize</span><span class="sxs-lookup"><span data-stu-id="d5374-121">receiveBufferSize</span></span>|<span data-ttu-id="d5374-122">受信バッファーのサイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="d5374-122">Specifies the size of the receive buffer.</span></span>|  
|<span data-ttu-id="d5374-123">sendBufferSize</span><span class="sxs-lookup"><span data-stu-id="d5374-123">sendBufferSize</span></span>|<span data-ttu-id="d5374-124">送信バッファーのサイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="d5374-124">Specifies the size of the send buffer.</span></span>|  
|<span data-ttu-id="d5374-125">subProtocol</span><span class="sxs-lookup"><span data-stu-id="d5374-125">subProtocol</span></span>|<span data-ttu-id="d5374-126">Web ソケットのサブプロトコルを指定します。</span><span class="sxs-lookup"><span data-stu-id="d5374-126">Specifies the Web Socket subprotocol.</span></span>|  
|<span data-ttu-id="d5374-127">transportUsage</span><span class="sxs-lookup"><span data-stu-id="d5374-127">transportUsage</span></span>|<span data-ttu-id="d5374-128">Web ソケットを使用するタイミングを指定します。</span><span class="sxs-lookup"><span data-stu-id="d5374-128">Specifies when to use Web Sockets.</span></span>|  
  
## <a name="transportusage-attribute"></a><span data-ttu-id="d5374-129">transportUsage 属性</span><span class="sxs-lookup"><span data-stu-id="d5374-129">transportUsage Attribute</span></span>  
  
|<span data-ttu-id="d5374-130">値</span><span class="sxs-lookup"><span data-stu-id="d5374-130">Value</span></span>|<span data-ttu-id="d5374-131">説明</span><span class="sxs-lookup"><span data-stu-id="d5374-131">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="d5374-132">WhenDuplex</span><span class="sxs-lookup"><span data-stu-id="d5374-132">WhenDuplex</span></span>|<span data-ttu-id="d5374-133">コントラクトが双方向の場合に、Web ソケット プロトコルを使用します。</span><span class="sxs-lookup"><span data-stu-id="d5374-133">Use the Web Socket protocol when the contract is duplex.</span></span>|  
|<span data-ttu-id="d5374-134">Always</span><span class="sxs-lookup"><span data-stu-id="d5374-134">Always</span></span>|<span data-ttu-id="d5374-135">コントラクトにかかわらず、常にWeb ソケット プロトコルを使用します。</span><span class="sxs-lookup"><span data-stu-id="d5374-135">Always use the Web Socket protocol regardless of the contract.</span></span>|  
|<span data-ttu-id="d5374-136">Never</span><span class="sxs-lookup"><span data-stu-id="d5374-136">Never</span></span>|<span data-ttu-id="d5374-137">Web ソケット プロトコルを使用しません。</span><span class="sxs-lookup"><span data-stu-id="d5374-137">Never use the Web Socket protocol.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d5374-138">子要素</span><span class="sxs-lookup"><span data-stu-id="d5374-138">Child Elements</span></span>  
 <span data-ttu-id="d5374-139">なし</span><span class="sxs-lookup"><span data-stu-id="d5374-139">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d5374-140">親要素</span><span class="sxs-lookup"><span data-stu-id="d5374-140">Parent Elements</span></span>  
  
|<span data-ttu-id="d5374-141">要素</span><span class="sxs-lookup"><span data-stu-id="d5374-141">Element</span></span>|<span data-ttu-id="d5374-142">説明</span><span class="sxs-lookup"><span data-stu-id="d5374-142">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d5374-143">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="d5374-143">\<netHttpBinding></span></span>|<span data-ttu-id="d5374-144">NetHttpBinding を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5374-144">Specifies the NetHttpBinding</span></span>|  
  
## <a name="example"></a><span data-ttu-id="d5374-145">例</span><span class="sxs-lookup"><span data-stu-id="d5374-145">Example</span></span>  
 <span data-ttu-id="d5374-146">次の例は、使用する方法を示します、 \<webSocketSettings > 要素。</span><span class="sxs-lookup"><span data-stu-id="d5374-146">The following example shows how to use the \<webSocketSettings> element.</span></span>  
  
```xml  
<netHttpBinding>
  <binding>
    <webSocketSettings createNotificationOnConnection="true"
                       disablePayloadMasking="false"
                       keepAliveInterval="00:10:00"
                       maxPendingConnections="100"
                       receiveBufferSize="1000"
                       sendBufferSize="1000"
                       subProtocol="Soap"
                       transportUsage="WhenDuplex/Always/Never" />
  </binding>
</netHttpBinding>
```  
  
## <a name="see-also"></a><span data-ttu-id="d5374-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="d5374-147">See Also</span></span>  
 <xref:System.ServiceModel.Channels.Binding>  
 <xref:System.ServiceModel.Channels.BindingElement>  
 <xref:System.ServiceModel.BasicHttpBinding>  
 <xref:System.ServiceModel.Configuration.BasicHttpBindingElement>  
 [<span data-ttu-id="d5374-148">バインディング</span><span class="sxs-lookup"><span data-stu-id="d5374-148">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="d5374-149">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="d5374-149">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="d5374-150">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="d5374-150">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="d5374-151">\<binding></span><span class="sxs-lookup"><span data-stu-id="d5374-151">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
