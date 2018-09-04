---
title: '&lt;netPeerTcpBinding&gt;'
ms.date: 03/30/2017
helpviewer_keywords:
- netPeerBinding element
ms.assetid: 2dd77ada-a176-47c7-a740-900b279f1aad
ms.openlocfilehash: 9032372f8e3344e9b1021be19a32230986b328a2
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43513281"
---
# <a name="ltnetpeertcpbindinggt"></a><span data-ttu-id="c0ff8-102">&lt;netPeerTcpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="c0ff8-102">&lt;netPeerTcpBinding&gt;</span></span>
<span data-ttu-id="c0ff8-103">ピア チャネル固有の TCP メッセージングのバインディングを定義します。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-103">Defines a binding for peer channel specific TCP messaging.</span></span>  
  
 <span data-ttu-id="c0ff8-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="c0ff8-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="c0ff8-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="c0ff8-105">\<bindings></span></span>  
<span data-ttu-id="c0ff8-106">\<netPeerTcpBinding></span><span class="sxs-lookup"><span data-stu-id="c0ff8-106">\<netPeerTcpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0ff8-107">構文</span><span class="sxs-lookup"><span data-stu-id="c0ff8-107">Syntax</span></span>  
  
```xml  
<netPeerBinding>  
    <binding name="string"  
         closeTimeout="TimeSpan"  
         openTimeout="TimeSpan"   
         receiveTimeout="TimeSpan"  
         sendTimeout="TimeSpan"  
         listenIPAddress="String"  
          maxBufferPoolSize="integer"  
         maxReceiveMessageSize="Integer"   
         port="Integer"  
         <security mode="None/Transport/Message/TransportWithMessageCredential">  
            <transport credentialType="Certificate/Password" />  
        </security>  
    </binding>  
</netPeerBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c0ff8-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="c0ff8-108">Attributes and Elements</span></span>  
 <span data-ttu-id="c0ff8-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-109">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c0ff8-110">属性</span><span class="sxs-lookup"><span data-stu-id="c0ff8-110">Attributes</span></span>  
  
|<span data-ttu-id="c0ff8-111">属性</span><span class="sxs-lookup"><span data-stu-id="c0ff8-111">Attribute</span></span>|<span data-ttu-id="c0ff8-112">説明</span><span class="sxs-lookup"><span data-stu-id="c0ff8-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c0ff8-113">closeTimeout</span><span class="sxs-lookup"><span data-stu-id="c0ff8-113">closeTimeout</span></span>|<span data-ttu-id="c0ff8-114">クローズ操作が完了するまでの期間を指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-114">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="c0ff8-115">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-115">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="c0ff8-116">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-116">The default is 00:01:00.</span></span>|  
|<span data-ttu-id="c0ff8-117">listenIPAddress</span><span class="sxs-lookup"><span data-stu-id="c0ff8-117">listenIPAddress</span></span>|<span data-ttu-id="c0ff8-118">ピア ノードが TCP メッセージをリッスンする IP アドレスを指定する文字列です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-118">A string that specifies an IP address on which the peer node will listen for TCP messages.</span></span> <span data-ttu-id="c0ff8-119">既定値は、`null` です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-119">The default is `null`.</span></span>|  
|<span data-ttu-id="c0ff8-120">maxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="c0ff8-120">maxBufferPoolSize</span></span>|<span data-ttu-id="c0ff8-121">このバインディングに使用するバッファー プール サイズの上限を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-121">An integer that specifies the maximum buffer pool size for this binding.</span></span> <span data-ttu-id="c0ff8-122">既定は 524,288 バイト (512 \* 1024) です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-122">The default is 524,288 bytes (512 \* 1024).</span></span> <span data-ttu-id="c0ff8-123">Windows Communication Foundation (WCF) では、多くの部分でバッファーを使用します。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-123">Many parts of Windows Communication Foundation (WCF) use buffers.</span></span> <span data-ttu-id="c0ff8-124">使用するたびに毎回バッファーを作成および破壊すると負荷が高くなります。バッファーのガベージ コレクションも同様です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-124">Creating and destroying buffers each time they are used is expensive, and garbage collection for buffers is also expensive.</span></span> <span data-ttu-id="c0ff8-125">バッファー プールを使用すると、バッファーをプールから取得して使用し、作業が終わったらプールに戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-125">With buffer pools, you can take a buffer from the pool, use it, and return it to the pool once you are done.</span></span> <span data-ttu-id="c0ff8-126">これで、バッファーの作成と破棄のオーバーヘッドを回避できます。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-126">Thus the overhead in creating and destroying buffers is avoided.</span></span>|  
|<span data-ttu-id="c0ff8-127">maxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="c0ff8-127">maxReceivedMessageSize</span></span>|<span data-ttu-id="c0ff8-128">このバインディングで構成されるチャネルで受信可能な最大メッセージ サイズ (ヘッダーを含む) をバイト単位で指定する正の整数。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-128">A positive integer that specifies the maximum message size, in bytes, including headers, that can be received on a channel configured with this binding.</span></span> <span data-ttu-id="c0ff8-129">この制限を超えるメッセージの送信者が、SOAP エラーを受信します。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-129">The sender of a message exceeding this limit will receive a SOAP fault.</span></span> <span data-ttu-id="c0ff8-130">メッセージは受信者によって破棄され、トレース ログにこのイベントのエントリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-130">The receiver drops the message and creates an entry of the event in the trace log.</span></span> <span data-ttu-id="c0ff8-131">既定値は 65536 です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-131">The default is 65536.</span></span>|  
|<span data-ttu-id="c0ff8-132">name</span><span class="sxs-lookup"><span data-stu-id="c0ff8-132">name</span></span>|<span data-ttu-id="c0ff8-133">バインディングの構成名を格納する文字列です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-133">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="c0ff8-134">この値は、バインディングの ID として使用されるため、一意にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-134">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="c0ff8-135">[!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)] 以降では、バインディングおよび動作に名前を付ける必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-135">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="c0ff8-136">既定の構成と無名のバインディングおよび動作の詳細については、「[簡略化された構成](../../../../../docs/framework/wcf/simplified-configuration.md)」と「[WCF サービスの構成を簡略化](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-136">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|<span data-ttu-id="c0ff8-137">openTimeout</span><span class="sxs-lookup"><span data-stu-id="c0ff8-137">openTimeout</span></span>|<span data-ttu-id="c0ff8-138">実行中の操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-138">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="c0ff8-139">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-139">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="c0ff8-140">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-140">The default is 00:01:00.</span></span>|  
|<span data-ttu-id="c0ff8-141">ポート</span><span class="sxs-lookup"><span data-stu-id="c0ff8-141">port</span></span>|<span data-ttu-id="c0ff8-142">このバインディングがピア チャネルの TCP メッセージを処理するネットワーク インターフェイス ポートを指定する整数です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-142">An integer that specifies the network interface port on which this binding will process peer channel TCP messages.</span></span> <span data-ttu-id="c0ff8-143">この値の有効値の範囲は <xref:System.Net.IPEndPoint.MinPort> ～ <xref:System.Net.IPEndPoint.MaxPort> です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-143">This value must be between <xref:System.Net.IPEndPoint.MinPort> and <xref:System.Net.IPEndPoint.MaxPort>.</span></span> <span data-ttu-id="c0ff8-144">既定値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-144">The default is 0.</span></span>|  
|<span data-ttu-id="c0ff8-145">receiveTimeout</span><span class="sxs-lookup"><span data-stu-id="c0ff8-145">receiveTimeout</span></span>|<span data-ttu-id="c0ff8-146">受信操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-146">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="c0ff8-147">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-147">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="c0ff8-148">既定値は 00:10:00 です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-148">The default is 00:10:00.</span></span>|  
|<span data-ttu-id="c0ff8-149">sendTimeout</span><span class="sxs-lookup"><span data-stu-id="c0ff8-149">sendTimeout</span></span>|<span data-ttu-id="c0ff8-150">送信操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-150">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="c0ff8-151">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-151">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="c0ff8-152">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-152">The default is 00:01:00.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c0ff8-153">子要素</span><span class="sxs-lookup"><span data-stu-id="c0ff8-153">Child Elements</span></span>  
  
|<span data-ttu-id="c0ff8-154">要素</span><span class="sxs-lookup"><span data-stu-id="c0ff8-154">Element</span></span>|<span data-ttu-id="c0ff8-155">説明</span><span class="sxs-lookup"><span data-stu-id="c0ff8-155">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c0ff8-156">\<readerQuotas></span><span class="sxs-lookup"><span data-stu-id="c0ff8-156">\<readerQuotas></span></span>](https://msdn.microsoft.com/library/3e5e42ff-cef8-478f-bf14-034449239bfd)|<span data-ttu-id="c0ff8-157">このバインドを使用して設定されるエンドポイントにより処理可能な、SOAP メッセージの複雑さに対する制約を定義します。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-157">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="c0ff8-158">この要素は <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-158">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
|[<span data-ttu-id="c0ff8-159">\<resolver></span><span class="sxs-lookup"><span data-stu-id="c0ff8-159">\<resolver></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/resolver.md)|<span data-ttu-id="c0ff8-160">ピア メッシュ ID を解決してピア メッシュ内のノードのエンドポイント ID アドレスを取得するために、このバインディングによって使用されるピア リゾルバーを指定します。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-160">Specifies a peer resolver used by this binding to resolve a peer mesh ID to the endpoint IP addresses of nodes within the peer mesh.</span></span>|  
|[<span data-ttu-id="c0ff8-161">\<security></span><span class="sxs-lookup"><span data-stu-id="c0ff8-161">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netpeerbinding.md)|<span data-ttu-id="c0ff8-162">メッセージのセキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-162">Defines the security settings for the message.</span></span> <span data-ttu-id="c0ff8-163">この要素は <xref:System.ServiceModel.Configuration.PeerSecurityElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-163">This element is of type <xref:System.ServiceModel.Configuration.PeerSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c0ff8-164">親要素</span><span class="sxs-lookup"><span data-stu-id="c0ff8-164">Parent Elements</span></span>  
  
|<span data-ttu-id="c0ff8-165">要素</span><span class="sxs-lookup"><span data-stu-id="c0ff8-165">Element</span></span>|<span data-ttu-id="c0ff8-166">説明</span><span class="sxs-lookup"><span data-stu-id="c0ff8-166">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c0ff8-167">\<bindings></span><span class="sxs-lookup"><span data-stu-id="c0ff8-167">\<bindings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|<span data-ttu-id="c0ff8-168">この要素には、標準バインディングおよびカスタム バインドのコレクションが保持されます。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-168">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c0ff8-169">Remarks</span><span class="sxs-lookup"><span data-stu-id="c0ff8-169">Remarks</span></span>  
 <span data-ttu-id="c0ff8-170">このバインディングは、TCP を介したピア トランスポートを使用するピア ツー ピア アプリケーションまたはマルチパーティ アプリケーションの作成をサポートします。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-170">This binding provides support for the creation of peer-to-peer or multiparty applications using peer transport over TCP.</span></span> <span data-ttu-id="c0ff8-171">各ピア ノードは、この種類のバイディングを使用して定義された複数のピア チャネルをホストできます。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-171">Each peer node can host multiple peer channels defined with this binding type.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c0ff8-172">例</span><span class="sxs-lookup"><span data-stu-id="c0ff8-172">Example</span></span>  
 <span data-ttu-id="c0ff8-173">次の例では、ピア チャネルを使用してマルチパーティ通信を実現する、NetPeerTcpBinding バインディングを使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-173">The following example demonstrates using the NetPeerTcpBinding binding, which provides multiparty communication using a peer channel.</span></span> <span data-ttu-id="c0ff8-174">このバインディングの使い方の詳細なシナリオでは、次を参照してください。[ネット ピア TCP](https://msdn.microsoft.com/library/31f4db66-edb2-40a6-b92a-14098e92acae)します。</span><span class="sxs-lookup"><span data-stu-id="c0ff8-174">For a detailed scenario of using this binding, see [Net Peer TCP](https://msdn.microsoft.com/library/31f4db66-edb2-40a6-b92a-14098e92acae).</span></span>  
  
```xml  
<configuration>  
<system.ServiceModel>  
<bindings>  
<netPeerBinding>  
    <binding   
         closeTimeout="00:00:10"  
         openTimeout="00:00:20"   
         receiveTimeout="00:00:30"  
         sendTimeout="00:00:40"  
         maxBufferSize="1001"  
         maxConnections="123"   
         maxReceiveMessageSize="1000">  
        <reliableSession ordered="false"  
            inactivityTimeout="00:02:00"  
            enabled="true" />  
        <security mode="TransportWithMessageCredential">  
            <message clientCredentialType="CardSpace" />  
        </security>  
    </binding>  
</netPeerBinding>  
</bindings>  
</system.ServiceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="c0ff8-175">関連項目</span><span class="sxs-lookup"><span data-stu-id="c0ff8-175">See Also</span></span>  
 <xref:System.ServiceModel.NetPeerTcpBinding>  
 <xref:System.ServiceModel.Configuration.NetPeerTcpBindingElement>  
 [<span data-ttu-id="c0ff8-176">バインディング</span><span class="sxs-lookup"><span data-stu-id="c0ff8-176">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="c0ff8-177">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="c0ff8-177">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="c0ff8-178">バインドを使用して、Windows Communication Foundation サービスとクライアントを構成するには</span><span class="sxs-lookup"><span data-stu-id="c0ff8-178">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="c0ff8-179">\<binding></span><span class="sxs-lookup"><span data-stu-id="c0ff8-179">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)  
 [<span data-ttu-id="c0ff8-180">ネット ピア TCP</span><span class="sxs-lookup"><span data-stu-id="c0ff8-180">Net Peer TCP</span></span>](https://msdn.microsoft.com/library/31f4db66-edb2-40a6-b92a-14098e92acae)  
 [<span data-ttu-id="c0ff8-181">ピアツーピア ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c0ff8-181">Peer-to-Peer Networking</span></span>](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)
