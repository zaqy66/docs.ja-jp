---
title: '&lt;tcpTransport&gt;'
ms.date: 03/30/2017
ms.assetid: 8fcd18c1-9958-42e7-b442-7903f7bdb563
ms.openlocfilehash: 39fb57af6ad97c1a0e51a2c5dcf06245ddf293ba
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152469"
---
# <a name="lttcptransportgt"></a><span data-ttu-id="9125d-102">&lt;tcpTransport&gt;</span><span class="sxs-lookup"><span data-stu-id="9125d-102">&lt;tcpTransport&gt;</span></span>
<span data-ttu-id="9125d-103">カスタム バインドのメッセージを転送するためにチャネルで使用できる TCP トランスポートを定義します。</span><span class="sxs-lookup"><span data-stu-id="9125d-103">Defines a TCP transport that can be used by a channel to transfers messages for a custom binding.</span></span>  
  
 <span data-ttu-id="9125d-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="9125d-104">\<system.serviceModel></span></span>  
<span data-ttu-id="9125d-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="9125d-105">\<bindings></span></span>  
<span data-ttu-id="9125d-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="9125d-106">\<customBinding></span></span>  
<span data-ttu-id="9125d-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="9125d-107">\<binding></span></span>  
<span data-ttu-id="9125d-108">\<tcpTransport></span><span class="sxs-lookup"><span data-stu-id="9125d-108">\<tcpTransport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9125d-109">構文</span><span class="sxs-lookup"><span data-stu-id="9125d-109">Syntax</span></span>  
  
```xml  
<tcpTransport   
      channelInitializationTimeout="TimeSpan"   
      connectionBufferSize="Integer"   
      hostNameComparisonMode="StrongWildcard/Exact/WeakWildcard"  
      listenBacklog="Integer"  
      manualAddressing="Boolean"   
      maxBufferPoolSize="Integer"  
      maxBufferSize="Integer"  
      maxOutputDelay="TimeSpan"  
      maxPendingAccepts="Integer"   
      maxPendingConnections="Integer"  
      maxReceivedMessageSize="Integer"   
      portSharingEnabled="Boolean"  
      teredoEnabled="Boolean"  
      transferMode="Buffered/Streamed/StreamedRequest/StreamedResponse" >  
      <connectionPoolSettings  
            groupName="String"  
            idleTimeout"TimeSpan"  
            leaseTimeout="TimeSpan"  
            maxOutboundConnectionsPerEndpopint="Integer" />  
</tcpTransport>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9125d-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="9125d-110">Attributes and Elements</span></span>  
 <span data-ttu-id="9125d-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="9125d-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9125d-112">属性</span><span class="sxs-lookup"><span data-stu-id="9125d-112">Attributes</span></span>  
  
|<span data-ttu-id="9125d-113">属性</span><span class="sxs-lookup"><span data-stu-id="9125d-113">Attribute</span></span>|<span data-ttu-id="9125d-114">説明</span><span class="sxs-lookup"><span data-stu-id="9125d-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9125d-115">channelInitializationTimeout</span><span class="sxs-lookup"><span data-stu-id="9125d-115">channelInitializationTimeout</span></span>|<span data-ttu-id="9125d-116">チャネルの初期化に対して許容される時間制限を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9125d-116">Gets or sets the time limit for initializing a channel to be accepted.</span></span>  <span data-ttu-id="9125d-117">接続が切断されるまでのチャネルの初期化ステータスの最大時間 (秒単位)。</span><span class="sxs-lookup"><span data-stu-id="9125d-117">The maximum time a channel can be in the initialization state before being disconnected in seconds.</span></span> <span data-ttu-id="9125d-118">このクォータは、.Net メッセージ フレーム プロトコルを使用して TCP 接続が接続を認証するのに必要な時間を含みます。</span><span class="sxs-lookup"><span data-stu-id="9125d-118">This quota includes the time a TCP connection can take to authenticate itself using the .Net Message Framing protocol.</span></span> <span data-ttu-id="9125d-119">クライアントは、サーバーが認証を実行するための十分な情報を得る前に初期データを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9125d-119">A client needs to send some initial data before the server has enough information to perform authentication.</span></span> <span data-ttu-id="9125d-120">既定値は 30 秒です。</span><span class="sxs-lookup"><span data-stu-id="9125d-120">The default is 30 seconds.</span></span>|  
|<span data-ttu-id="9125d-121">connectionBufferSize</span><span class="sxs-lookup"><span data-stu-id="9125d-121">connectionBufferSize</span></span>|<span data-ttu-id="9125d-122">クライアントまたサービスからネットワークでシリアル化されたメッセージのチャンクを転送するために使用されるバッファーのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9125d-122">Gets or sets the size of the buffer used to transmit a chunk of the serialized message on the wire from the client or service.</span></span>|  
|<span data-ttu-id="9125d-123">hostNameComparisonMode</span><span class="sxs-lookup"><span data-stu-id="9125d-123">hostNameComparisonMode</span></span>|<span data-ttu-id="9125d-124">URI で一致する場合にサービスに到達するためにホスト名を使用するかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9125d-124">Gets or sets a value that indicates whether the hostname is used to reach the service when matching on the URI.</span></span>|  
|<span data-ttu-id="9125d-125">listenBacklog</span><span class="sxs-lookup"><span data-stu-id="9125d-125">listenBacklog</span></span>|<span data-ttu-id="9125d-126">Web サービスの保留可能なキュー内の接続要求の最大数。</span><span class="sxs-lookup"><span data-stu-id="9125d-126">The maximum number of queued connection requests that can be pending for a Web service.</span></span> <span data-ttu-id="9125d-127">`connectionLeaseTimeout` 属性は、クライアントが接続されるのを待つ時間を制限します。この時間が経過すると接続の例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="9125d-127">The `connectionLeaseTimeout` attribute limits the duration the client will wait to be connected before throwing a connection exception.</span></span> <span data-ttu-id="9125d-128">これは、Web サービスに対して保留可能なキュー内の接続要求の最大数を制御するソケット レベルのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="9125d-128">This is a socket level property which controls the maximum number of queued connection requests that can be pending for a Web service.</span></span> <span data-ttu-id="9125d-129">ListenBacklog が低すぎると、WCF は要求の受け入れを停止し、そのため、サーバーが既存のキューに置かれた接続の一部を認識するまで新しい接続を削除します。</span><span class="sxs-lookup"><span data-stu-id="9125d-129">When ListenBacklog is too low, WCF will stop accepting requests and therefore drop new connections until the server acknowledges some of the existing queued connections.</span></span> <span data-ttu-id="9125d-130">既定値は 16 \* プロセッサの数。</span><span class="sxs-lookup"><span data-stu-id="9125d-130">The default is 16 \* number of processors.</span></span>|  
|<span data-ttu-id="9125d-131">manualAddressing</span><span class="sxs-lookup"><span data-stu-id="9125d-131">manualAddressing</span></span>|<span data-ttu-id="9125d-132">メッセージの手動アドレス指定が必要かどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9125d-132">Gets or sets a value that indicates whether manual addressing of the message is required.</span></span>|  
|<span data-ttu-id="9125d-133">maxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="9125d-133">maxBufferPoolSize</span></span>|<span data-ttu-id="9125d-134">トランスポートが使用するバッファー プールの最大サイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9125d-134">Gets or sets the maximum size of any buffer pools used by the transport.</span></span>|  
|<span data-ttu-id="9125d-135">maxBufferSize</span><span class="sxs-lookup"><span data-stu-id="9125d-135">maxBufferSize</span></span>|<span data-ttu-id="9125d-136">使用するバッファーの最大サイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9125d-136">Gets or sets the maximum size of the buffer to use.</span></span> <span data-ttu-id="9125d-137">ストリーム メッセージの場合、この値は少なくともメッセージ ヘッダーで使用できる最大サイズにする必要があります。これは、バッファー モードで読み取られます。</span><span class="sxs-lookup"><span data-stu-id="9125d-137">For streamed messages, this value should be at least the maximum possible size of the message headers, which are read in buffered mode.</span></span>|  
|<span data-ttu-id="9125d-138">maxOutputDelay</span><span class="sxs-lookup"><span data-stu-id="9125d-138">maxOutputDelay</span></span>|<span data-ttu-id="9125d-139">メッセージのチャンクまたは完全なメッセージを、送信前にメモリ内のバッファーに残したままにできる最長期間を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9125d-139">Gets or sets the maximum interval of time that a chunk of a message or a full message can remain buffered in memory before being sent out.</span></span>|  
|<span data-ttu-id="9125d-140">maxPendingAccepts</span><span class="sxs-lookup"><span data-stu-id="9125d-140">maxPendingAccepts</span></span>|<span data-ttu-id="9125d-141">サービスに対する着信接続処理に使用できる保留中の非同期受け入れ操作の最大数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9125d-141">Gets or sets the maximum number of pending asynchronous accept operations that are available for processing incoming connections to the service.</span></span>|  
|<span data-ttu-id="9125d-142">maxPendingConnections</span><span class="sxs-lookup"><span data-stu-id="9125d-142">maxPendingConnections</span></span>|<span data-ttu-id="9125d-143">サービスでディスパッチを待機している最大接続数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9125d-143">Gets or sets the maximum number of connections awaiting dispatch on the service.</span></span>|  
|<span data-ttu-id="9125d-144">maxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="9125d-144">maxReceivedMessageSize</span></span>|<span data-ttu-id="9125d-145">受信できる最大メッセージ サイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9125d-145">Gets and sets the maximum allowable message size that can be received.</span></span>|  
|<span data-ttu-id="9125d-146">portSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="9125d-146">portSharingEnabled</span></span>|<span data-ttu-id="9125d-147">TCP ポート共有をこの接続で有効にする場合に指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="9125d-147">A Boolean value that specifies if TCP port sharing is enabled for this connection.</span></span> <span data-ttu-id="9125d-148">これが `false` の場合、各バインディングは独自の排他ポートを使用します。</span><span class="sxs-lookup"><span data-stu-id="9125d-148">If this is `false`, each binding will use its own exclusive port.</span></span> <span data-ttu-id="9125d-149">既定値は、`false` です。</span><span class="sxs-lookup"><span data-stu-id="9125d-149">The default is `false`.</span></span><br /><br /> <span data-ttu-id="9125d-150">この設定は、サービスのみに関連します。</span><span class="sxs-lookup"><span data-stu-id="9125d-150">This setting is relevant only to services.</span></span> <span data-ttu-id="9125d-151">クライアントには影響はありません。</span><span class="sxs-lookup"><span data-stu-id="9125d-151">Clients are not affected.</span></span><br /><br /> <span data-ttu-id="9125d-152">この設定を使用するには、[スタートアップの種類] を [手動] または [自動] に変更して、Windows Communication Foundation (WCF) の TCP ポート共有サービスを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9125d-152">Using this setting requires enabling the Windows Communication Foundation (WCF) TCP Port Sharing Service by changing its Startup Type to Manual or Automatic</span></span>|  
|<span data-ttu-id="9125d-153">teredoEnabled</span><span class="sxs-lookup"><span data-stu-id="9125d-153">teredoEnabled</span></span>|<span data-ttu-id="9125d-154">Teredo (ファイアウォールの内側にあるクライアントをアドレス指定するためのテクノロジ) が有効であるかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="9125d-154">A Boolean value that specifies whether Teredo (a technology for addressing clients that are behind firewalls) is enabled.</span></span> <span data-ttu-id="9125d-155">既定値は、`false` です。</span><span class="sxs-lookup"><span data-stu-id="9125d-155">The default is `false`.</span></span><br /><br /> <span data-ttu-id="9125d-156">このプロパティは、基になる TCP ソケットで Tredo を有効にします。</span><span class="sxs-lookup"><span data-stu-id="9125d-156">This property enables Teredo for the underlying TCP socket.</span></span> <span data-ttu-id="9125d-157">詳細については、次を参照してください。 [Teredo の概要](https://go.microsoft.com/fwlink/?LinkId=95339)します。</span><span class="sxs-lookup"><span data-stu-id="9125d-157">For more information, see [Teredo Overview](https://go.microsoft.com/fwlink/?LinkId=95339).</span></span><br /><br /> <span data-ttu-id="9125d-158">このプロパティは [!INCLUDE[wxpsp2](../../../../../includes/wxpsp2-md.md)] および [!INCLUDE[ws2003](../../../../../includes/ws2003-md.md)] にのみ適用できます。</span><span class="sxs-lookup"><span data-stu-id="9125d-158">This property is applicable only on [!INCLUDE[wxpsp2](../../../../../includes/wxpsp2-md.md)] and [!INCLUDE[ws2003](../../../../../includes/ws2003-md.md)].</span></span> [!INCLUDE[wv](../../../../../includes/wv-md.md)] <span data-ttu-id="9125d-159">には、Teredo 用のコンピューター全体の構成オプションがあるので、Vista を実行する場合は、このプロパティは無視されます。</span><span class="sxs-lookup"><span data-stu-id="9125d-159">has a machine-wide configuration option for Teredo, so when running Vista, this property is ignored.</span></span> <span data-ttu-id="9125d-160">Teredo の場合、クライアント コンピューターおよびサービス コンピューターの両方に Microsoft IPv6 スタックをインストールし、Teredo 用に正しく設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9125d-160">Teredo requires that the client and service machines both have the Microsoft IPv6 stack installed and correctly configured for Teredo usage.</span></span> <span data-ttu-id="9125d-161">Teredo を構成する方法の詳細については、次を参照してください。 [Teredo の概要](https://go.microsoft.com/fwlink/?LinkId=95339)します。</span><span class="sxs-lookup"><span data-stu-id="9125d-161">For more information about configuring Teredo, see [Teredo Overview](https://go.microsoft.com/fwlink/?LinkId=95339).</span></span> <span data-ttu-id="9125d-162">詳細については、次を参照してください。 [Windows Server 2003 Technology Centers](https://go.microsoft.com/fwlink/?LinkId=49888)します。</span><span class="sxs-lookup"><span data-stu-id="9125d-162">For more information, see [Windows Server 2003 Technology Centers](https://go.microsoft.com/fwlink/?LinkId=49888).</span></span>|  
|<span data-ttu-id="9125d-163">transferMode</span><span class="sxs-lookup"><span data-stu-id="9125d-163">transferMode</span></span>|<span data-ttu-id="9125d-164">接続指向のトランスポートでメッセージをバッファーするか、ストリーム配信するかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="9125d-164">Gets or sets a value that indicates whether the messages are buffered or streamed with the connection-oriented transport.</span></span>|  
|<span data-ttu-id="9125d-165">connectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="9125d-165">connectionPoolSettings</span></span>|<span data-ttu-id="9125d-166">名前付きパイプ バインディングの追加の接続プール設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="9125d-166">Specifies additional connection pool settings for a Named Pipe binding.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9125d-167">子要素</span><span class="sxs-lookup"><span data-stu-id="9125d-167">Child Elements</span></span>  
 <span data-ttu-id="9125d-168">なし</span><span class="sxs-lookup"><span data-stu-id="9125d-168">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9125d-169">親要素</span><span class="sxs-lookup"><span data-stu-id="9125d-169">Parent Elements</span></span>  
  
|<span data-ttu-id="9125d-170">要素</span><span class="sxs-lookup"><span data-stu-id="9125d-170">Element</span></span>|<span data-ttu-id="9125d-171">説明</span><span class="sxs-lookup"><span data-stu-id="9125d-171">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9125d-172">\<binding></span><span class="sxs-lookup"><span data-stu-id="9125d-172">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="9125d-173">カスタム バインドのすべてのバインド機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="9125d-173">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9125d-174">Remarks</span><span class="sxs-lookup"><span data-stu-id="9125d-174">Remarks</span></span>  
 <span data-ttu-id="9125d-175">このトランスポートは、"net.tcp://hostname:port/path" の形式の URI を使用します。</span><span class="sxs-lookup"><span data-stu-id="9125d-175">This transport uses URIs of the form "net.tcp://hostname:port/path".</span></span> <span data-ttu-id="9125d-176">他の URI コンポーネントは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="9125d-176">Other URI components are optional.</span></span>  
  
 <span data-ttu-id="9125d-177">`tcpTransport` 要素は、TCP トランスポート プロトコルを実装するカスタム バインディングを作成する場合の開始点となります。</span><span class="sxs-lookup"><span data-stu-id="9125d-177">The `tcpTransport` element is the starting point for creating a custom binding that implements the TCP transport protocol.</span></span> <span data-ttu-id="9125d-178">このトランスポートは、WCF 間の通信用に最適化されています。</span><span class="sxs-lookup"><span data-stu-id="9125d-178">This transport is optimized for WCF-to-WCF communication.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9125d-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="9125d-179">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.TcpTransportElement>  
 <xref:System.ServiceModel.Channels.TcpTransportBindingElement>  
 <xref:System.ServiceModel.Channels.TransportBindingElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="9125d-180">トランスポート</span><span class="sxs-lookup"><span data-stu-id="9125d-180">Transports</span></span>](../../../../../docs/framework/wcf/feature-details/transports.md)  
 [<span data-ttu-id="9125d-181">トランスポートの選択</span><span class="sxs-lookup"><span data-stu-id="9125d-181">Choosing a Transport</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)  
 [<span data-ttu-id="9125d-182">バインディング</span><span class="sxs-lookup"><span data-stu-id="9125d-182">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="9125d-183">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="9125d-183">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="9125d-184">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="9125d-184">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="9125d-185">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="9125d-185">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
