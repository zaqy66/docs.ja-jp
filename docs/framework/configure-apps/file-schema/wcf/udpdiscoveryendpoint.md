---
title: '&lt;UdpDiscoveryEndpoint&gt;'
ms.date: 03/30/2017
ms.assetid: 1f485329-2771-43bc-88de-df8f2faa3bb7
ms.openlocfilehash: 6508f73de7920a339e40284c86b0d1d649e7eabe
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145433"
---
# <a name="ltudpdiscoveryendpointgt"></a><span data-ttu-id="e2438-102">&lt;UdpDiscoveryEndpoint&gt;</span><span class="sxs-lookup"><span data-stu-id="e2438-102">&lt;udpDiscoveryEndpoint&gt;</span></span>
<span data-ttu-id="e2438-103">この構成要素は、UDP マルチキャスト バインディングを使用した探索操作用に事前に構成される標準エンドポイントを定義します。</span><span class="sxs-lookup"><span data-stu-id="e2438-103">This configuration element defines a standard endpoint that is pre-configured for discovery operations over a UDP multicast binding.</span></span> <span data-ttu-id="e2438-104">このエンドポイントには固定コントラクトがあり、WS-Discovery プロトコルの 2 つのバージョンをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e2438-104">This endpoint has a fixed contract and supports two WS-Discovery protocol versions.</span></span> <span data-ttu-id="e2438-105">また、WS-Discovery の仕様 (WS-Discovery April 2005 または WS-Discovery V1.1) に規定された固定 UDP バインディングと既定のアドレスも備えています。</span><span class="sxs-lookup"><span data-stu-id="e2438-105">In addition, it has a fixed UDP binding and a default address as specified in the WS-Discovery specifications (WS-Discovery April 2005 or WS-Discovery V1.1).</span></span>  
  
 <span data-ttu-id="e2438-106">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="e2438-106">\<system.ServiceModel></span></span>  
<span data-ttu-id="e2438-107">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="e2438-107">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e2438-108">構文</span><span class="sxs-lookup"><span data-stu-id="e2438-108">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <discoveryEndpoint>
      <standardEndpoint discoveryMode="Adhoc/Managed"
                        discoveryVersion="WSDiscovery11/WSDiscoveryApril2005"
                        maxResponseDelay="Timespan"
                        multicastAddress="Uri"
                        name="String" />
    </discoveryEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e2438-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="e2438-109">Attributes and Elements</span></span>  
 <span data-ttu-id="e2438-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="e2438-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e2438-111">属性</span><span class="sxs-lookup"><span data-stu-id="e2438-111">Attributes</span></span>  
  
|<span data-ttu-id="e2438-112">属性</span><span class="sxs-lookup"><span data-stu-id="e2438-112">Attribute</span></span>|<span data-ttu-id="e2438-113">説明</span><span class="sxs-lookup"><span data-stu-id="e2438-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e2438-114">discoveryMode</span><span class="sxs-lookup"><span data-stu-id="e2438-114">discoveryMode</span></span>|<span data-ttu-id="e2438-115">探索プロトコルのモードを示す文字列。</span><span class="sxs-lookup"><span data-stu-id="e2438-115">A string that specifies the mode of discovery protocol.</span></span> <span data-ttu-id="e2438-116">有効な値は"Adhoc"と"Managed です"。</span><span class="sxs-lookup"><span data-stu-id="e2438-116">Valid values are "Adhoc" and "Managed".</span></span> <span data-ttu-id="e2438-117">マネージド モードでは、プロトコルは Discoverable サービスのリポジトリとして機能する Discovery Proxy に依存します。</span><span class="sxs-lookup"><span data-stu-id="e2438-117">In managed mode the protocol relies on a Discovery Proxy, which acts as a repository of Discoverable services.</span></span> <span data-ttu-id="e2438-118">アドホック モードでは、プロトコルは UDP マルチキャスト メカニズムを使用して利用可能なサービスを探索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2438-118">Adhoc mode requires the protocol to use UDP multicast mechanism to find available services.</span></span> <span data-ttu-id="e2438-119">この値は、<xref:System.ServiceModel.Discovery.ServiceDiscoveryMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="e2438-119">This value is of type <xref:System.ServiceModel.Discovery.ServiceDiscoveryMode>.</span></span>|  
|<span data-ttu-id="e2438-120">discoveryVersion</span><span class="sxs-lookup"><span data-stu-id="e2438-120">discoveryVersion</span></span>|<span data-ttu-id="e2438-121">WS-Discovery プロトコルの 2 つのバージョンのうち、1 つを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="e2438-121">A string that specifies one of the two versions of WS-Discovery protocol.</span></span> <span data-ttu-id="e2438-122">有効値は WSDiscovery11 と WSDiscoveryApril2005 です。</span><span class="sxs-lookup"><span data-stu-id="e2438-122">Valid values are WSDiscovery11 and WSDiscoveryApril2005.</span></span> <span data-ttu-id="e2438-123">この値は、<xref:System.ServiceModel.Discovery.DiscoveryVersion> 型です。</span><span class="sxs-lookup"><span data-stu-id="e2438-123">This value is of type <xref:System.ServiceModel.Discovery.DiscoveryVersion>.</span></span>|  
|<span data-ttu-id="e2438-124">maxResponseDelay</span><span class="sxs-lookup"><span data-stu-id="e2438-124">maxResponseDelay</span></span>|<span data-ttu-id="e2438-125">Discovery プロトコルが Probe Match や Resolve Match などのメッセージを送信するまでの待機時間の最大値を指定する Timespan 値。</span><span class="sxs-lookup"><span data-stu-id="e2438-125">A Timespan value that specifies the maximum value for the delay the Discovery protocol will wait before sending certain messages such as Probe Match or Resolve Match.</span></span><br /><br /> <span data-ttu-id="e2438-126">すべての ProbeMatch が同時に送信されると、ネットワーク ストームが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="e2438-126">If all ProbeMatches are sent at the same time, a network storm may result.</span></span> <span data-ttu-id="e2438-127">これを防ぐために、各 ProbeMatch はランダムな時間だけ待機して送信されます。</span><span class="sxs-lookup"><span data-stu-id="e2438-127">To prevent this from occurring, ProbeMatches are sent with a random delay between each ProbeMatch.</span></span> <span data-ttu-id="e2438-128">ランダムな待機時間は、0 からこの属性に設定された値の範囲内で設定されます。</span><span class="sxs-lookup"><span data-stu-id="e2438-128">The random delay is in the range of 0 to the value set by this attribute.</span></span> <span data-ttu-id="e2438-129">この属性を 0 に設定すると、ProbeMatch メッセージは待機せずに短いループで送信されます。</span><span class="sxs-lookup"><span data-stu-id="e2438-129">If this attribute is set to 0, then the ProbeMatches messages are sent in a tight loop without any delay.</span></span> <span data-ttu-id="e2438-130">それ以外の場合は、ProbeMatch メッセージはランダムな時間だけ待機して送信されます。すべての ProbeMatch メッセージの送信にかかる合計時間が maxResponseDelay を超えることはありません。</span><span class="sxs-lookup"><span data-stu-id="e2438-130">Otherwise, the ProbeMatches messages are sent with some random delay such that the total time taken to send all ProbeMatches messages does not exceed the maxResponseDelay.</span></span> <span data-ttu-id="e2438-131">この値はサービスのみに関連するもので、クライアントが使用するものではありません。</span><span class="sxs-lookup"><span data-stu-id="e2438-131">This value is only relevant for services, it is not used by clients.</span></span>|  
|<span data-ttu-id="e2438-132">multicastAddress</span><span class="sxs-lookup"><span data-stu-id="e2438-132">multicastAddress</span></span>|<span data-ttu-id="e2438-133">探索メッセージの送受信に使用するマルチキャスト アドレスを指定する URI。</span><span class="sxs-lookup"><span data-stu-id="e2438-133">A Uri that specifies a multicast address to use for sending and receiving the discovery messages.</span></span> <span data-ttu-id="e2438-134">既定値は、プロトコル仕様に準じたマルチキャスト アドレスです。</span><span class="sxs-lookup"><span data-stu-id="e2438-134">The default value is the multicast address as conformant to the protocol specification.</span></span>|  
|`name`|<span data-ttu-id="e2438-135">標準エンドポイントの構成名を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="e2438-135">A String that specifies the name of the configuration of the standard endpoint.</span></span> <span data-ttu-id="e2438-136">この名前は、サービス エンドポイントの `endpointConfiguration` 属性で使用され、標準エンドポイントと構成を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="e2438-136">The name is used in the `endpointConfiguration` attribute of the service endpoint to link a standard endpoint to its configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e2438-137">子要素</span><span class="sxs-lookup"><span data-stu-id="e2438-137">Child Elements</span></span>  
  
|<span data-ttu-id="e2438-138">要素</span><span class="sxs-lookup"><span data-stu-id="e2438-138">Element</span></span>|<span data-ttu-id="e2438-139">説明</span><span class="sxs-lookup"><span data-stu-id="e2438-139">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e2438-140">\<udpTransportSettings ></span><span class="sxs-lookup"><span data-stu-id="e2438-140">\<udpTransportSettings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/udptransportsettings.md)|<span data-ttu-id="e2438-141">UDP エンドポイントの UDP トランスポートを構成できる設定のコレクション。</span><span class="sxs-lookup"><span data-stu-id="e2438-141">A collection of settings that allow you to configure UDP transport for the UDP endpoint.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e2438-142">親要素</span><span class="sxs-lookup"><span data-stu-id="e2438-142">Parent Elements</span></span>  
  
|<span data-ttu-id="e2438-143">要素</span><span class="sxs-lookup"><span data-stu-id="e2438-143">Element</span></span>|<span data-ttu-id="e2438-144">説明</span><span class="sxs-lookup"><span data-stu-id="e2438-144">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e2438-145">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="e2438-145">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="e2438-146">1 つ以上のプロパティ (アドレス、バインディング、コントラクト) が固定されている、あらかじめ定義されたエンドポイントである標準エンドポイントのコレクション。</span><span class="sxs-lookup"><span data-stu-id="e2438-146">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="e2438-147">例</span><span class="sxs-lookup"><span data-stu-id="e2438-147">Example</span></span>  
 <span data-ttu-id="e2438-148">UDP マルチキャスト トランスポート経由で探索メッセージをリッスンするサービスの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e2438-148">The following example demonstrates a service listening for discovery messages over a UDP multicast transport.</span></span>  
  
```xml  
<services>
  <service name="CalculatorService"
           behaviorConfiguration="CalculatorServiceBehavior">
    <endpoint binding="basicHttpBinding"
              address="calculator"
              contract="ICalculatorService" />
    <endpoint name="DiscoveryEndpoint"
              kind="udpDiscoveryEndpoint" />
  </service>
  <standardEndpoints>
    <udpDiscoveryEndpoint>
      <standardEndpoint name="DiscoveryEndpoint"
                        version="WSDiscoveryApril2005" />
    </udpDiscoveryEndpoint>
  </standardEndpoints>
</services>
```  
  
## <a name="see-also"></a><span data-ttu-id="e2438-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2438-149">See Also</span></span>  
 <xref:System.ServiceModel.Discovery.DiscoveryEndpoint>
