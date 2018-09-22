---
title: '&lt;wsHttpBinding&gt;'
ms.date: 03/30/2017
helpviewer_keywords:
- wsHttpBinding Element
ms.assetid: 0eee8ced-ad68-427d-b95a-97260e98deed
ms.openlocfilehash: 480e10b9667712fbd2a3ffa95e1373d72ee1a9df
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/22/2018
ms.locfileid: "46585469"
---
# <a name="ltwshttpbindinggt"></a><span data-ttu-id="78e91-102">&lt;wsHttpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="78e91-102">&lt;wsHttpBinding&gt;</span></span>
<span data-ttu-id="78e91-103">双方向サービス コントラクト以外に適した、安全で信頼のおける相互操作可能なバインディングを定義します。</span><span class="sxs-lookup"><span data-stu-id="78e91-103">Defines a secure, reliable, interoperable binding suitable for non-duplex service contracts.</span></span> <span data-ttu-id="78e91-104">バインディングは、信頼のための WS-ReliableMessaging、およびメッセージのセキュリティと認証のための WS-Security を実装します。</span><span class="sxs-lookup"><span data-stu-id="78e91-104">The binding implements the following specifications: WS-Reliable Messaging for reliability, and WS-Security for message security and authentication.</span></span> <span data-ttu-id="78e91-105">トランスポートは HTTP、メッセージ エンコーディングは Text/XML エンコーディングです。</span><span class="sxs-lookup"><span data-stu-id="78e91-105">The transport is HTTP, and message encoding is Text/XML encoding.</span></span>  
  
 <span data-ttu-id="78e91-106">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="78e91-106">\<system.ServiceModel></span></span>  
<span data-ttu-id="78e91-107">\<bindings></span><span class="sxs-lookup"><span data-stu-id="78e91-107">\<bindings></span></span>  
<span data-ttu-id="78e91-108">\<wsHttpBinding></span><span class="sxs-lookup"><span data-stu-id="78e91-108">\<wsHttpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="78e91-109">構文</span><span class="sxs-lookup"><span data-stu-id="78e91-109">Syntax</span></span>  
  
```xml  
<wsHttpBinding>  
    <binding   
        allowCookies="Boolean"  
        bypassProxyOnLocal="Boolean"  
        closeTimeout="TimeSpan"  
        hostNameComparisonMode="StrongWildCard/Exact/WeakWildcard"  
        maxBufferPoolSize="integer"  
        maxReceivedMessageSize="Integer"  
        messageEncoding="Text/Mtom"   
                name="string"  
        openTimeout="TimeSpan"   
        proxyAddress="URI"  
        receiveTimeout="TimeSpan"  
        sendTimeout="TimeSpan"  
                textEncoding="UnicodeFffeTextEncoding/Utf16TextEncoding/Utf8TextEncoding"  
        transactionFlow="Boolean"  
        useDefaultWebProxy="Boolean">  
        <reliableSession ordered="Boolean"  
           inactivityTimeout="TimeSpan"  
           enabled="Boolean" />  
        <security mode="Message/None/Transport/TransportWithCredential">  
           <transport clientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"  
                proxyCredentialType="Basic/Digest/None/Ntlm/Windows"  
                realm="string" />  
          <message   
             algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
                          clientCredentialType="Certificate/IssuedToken/None/UserName/Windows"  
             establishSecurityContext="Boolean"  
             negotiateServiceCredential="Boolean" />  
        </security>  
       <readerQuotas             maxArrayLength="Integer"            maxBytesPerRead="Integer"            maxDepth="Integer"             maxNameTableCharCount="Integer"                     maxStringContentLength="Integer" />  
    </binding>  
</wsHttpBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="78e91-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="78e91-110">Attributes and Elements</span></span>  
 <span data-ttu-id="78e91-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="78e91-111">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="78e91-112">属性</span><span class="sxs-lookup"><span data-stu-id="78e91-112">Attributes</span></span>  
  
|<span data-ttu-id="78e91-113">属性</span><span class="sxs-lookup"><span data-stu-id="78e91-113">Attribute</span></span>|<span data-ttu-id="78e91-114">説明</span><span class="sxs-lookup"><span data-stu-id="78e91-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="78e91-115">allowCookies</span><span class="sxs-lookup"><span data-stu-id="78e91-115">allowCookies</span></span>|<span data-ttu-id="78e91-116">クライアントがクッキーを受け入れて、それらを今後の要求に反映させるかどうかを指定するブール値です。</span><span class="sxs-lookup"><span data-stu-id="78e91-116">A Boolean value that indicates whether the client accepts cookies and propagates them on future requests.</span></span> <span data-ttu-id="78e91-117">既定値は false です。</span><span class="sxs-lookup"><span data-stu-id="78e91-117">The default is false.</span></span><br /><br /> <span data-ttu-id="78e91-118">クッキーを使用する ASMX Web サービスと対話する場合にこのプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="78e91-118">You can use this property when you interact with ASMX Web services that use cookies.</span></span> <span data-ttu-id="78e91-119">この方法で、サーバーから返されるクッキーを、それ以降のサービスに対するすべてのクライアント要求に自動的にコピーできます。</span><span class="sxs-lookup"><span data-stu-id="78e91-119">In this way, you can be sure that the cookies returned from the server are automatically copied to all future client requests for that service.</span></span>|  
|<span data-ttu-id="78e91-120">bypassProxyOnLocal</span><span class="sxs-lookup"><span data-stu-id="78e91-120">bypassProxyOnLocal</span></span>|<span data-ttu-id="78e91-121">ローカル アドレスでプロキシ サーバーをバイパスするかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="78e91-121">A Boolean value that indicates whether to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="78e91-122">既定値は、`false` です。</span><span class="sxs-lookup"><span data-stu-id="78e91-122">The default is `false`.</span></span>|  
|<span data-ttu-id="78e91-123">closeTimeout</span><span class="sxs-lookup"><span data-stu-id="78e91-123">closeTimeout</span></span>|<span data-ttu-id="78e91-124">クローズ操作が完了するまでの期間を指定する <xref:System.TimeSpan> 値。</span><span class="sxs-lookup"><span data-stu-id="78e91-124">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="78e91-125">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="78e91-125">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="78e91-126">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="78e91-126">The default is 00:01:00.</span></span>|  
|<span data-ttu-id="78e91-127">hostnameComparisonMode</span><span class="sxs-lookup"><span data-stu-id="78e91-127">hostnameComparisonMode</span></span>|<span data-ttu-id="78e91-128">URI の解析に使用する HTTP ホスト名比較モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="78e91-128">Specifies the HTTP hostname comparison mode used to parse URIs.</span></span> <span data-ttu-id="78e91-129">この属性は <xref:System.ServiceModel.HostNameComparisonMode> 型で、URI が一致したときにサービスへのアクセスにホスト名を使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="78e91-129">This attribute is of type <xref:System.ServiceModel.HostNameComparisonMode>, which indicates whether the hostname is used to reach the service when matching on the URI.</span></span> <span data-ttu-id="78e91-130">既定値は <xref:System.ServiceModel.HostNameComparisonMode.StrongWildcard> で、一致しているホスト名を無視します。</span><span class="sxs-lookup"><span data-stu-id="78e91-130">The default value is <xref:System.ServiceModel.HostNameComparisonMode.StrongWildcard>, which ignores the hostname in the match.</span></span>|  
|<span data-ttu-id="78e91-131">maxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="78e91-131">maxBufferPoolSize</span></span>|<span data-ttu-id="78e91-132">このバインディングに使用するバッファー プール サイズの上限を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="78e91-132">An integer that specifies the maximum buffer pool size for this binding.</span></span> <span data-ttu-id="78e91-133">既定は 524,288 バイト (512 \* 1024) です。</span><span class="sxs-lookup"><span data-stu-id="78e91-133">The default is 524,288 bytes (512 \* 1024).</span></span> <span data-ttu-id="78e91-134">Windows Communication Foundation (WCF) では、多くの部分でバッファーを使用します。</span><span class="sxs-lookup"><span data-stu-id="78e91-134">Many parts of Windows Communication Foundation (WCF) use buffers.</span></span> <span data-ttu-id="78e91-135">使用するたびに毎回バッファーを作成および破壊すると負荷が高くなります。バッファーのガベージ コレクションも同様です。</span><span class="sxs-lookup"><span data-stu-id="78e91-135">Creating and destroying buffers each time they are used is expensive, and garbage collection for buffers is also expensive.</span></span> <span data-ttu-id="78e91-136">バッファー プールを使用すると、バッファーをプールから取得して使用し、作業が終わったらプールに戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="78e91-136">With buffer pools, you can take a buffer from the pool, use it, and return it to the pool once you are done.</span></span> <span data-ttu-id="78e91-137">これで、バッファーの作成と破棄のオーバーヘッドを回避できます。</span><span class="sxs-lookup"><span data-stu-id="78e91-137">Thus the overhead in creating and destroying buffers is avoided.</span></span>|  
|<span data-ttu-id="78e91-138">maxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="78e91-138">maxReceivedMessageSize</span></span>|<span data-ttu-id="78e91-139">このバインディングで構成されるチャネルで受信可能な最大メッセージ サイズ (ヘッダーを含む) をバイト単位で指定する正の整数。</span><span class="sxs-lookup"><span data-stu-id="78e91-139">A positive integer that specifies the maximum message size, in bytes, including headers, that can be received on a channel configured with this binding.</span></span> <span data-ttu-id="78e91-140">この制限を超えるメッセージの送信者が、SOAP エラーを受信します。</span><span class="sxs-lookup"><span data-stu-id="78e91-140">The sender of a message exceeding this limit will receive a SOAP fault.</span></span> <span data-ttu-id="78e91-141">メッセージは受信者によって破棄され、トレース ログにこのイベントのエントリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="78e91-141">The receiver drops the message and creates an entry of the event in the trace log.</span></span> <span data-ttu-id="78e91-142">既定値は 65536 です。</span><span class="sxs-lookup"><span data-stu-id="78e91-142">The default is 65536.</span></span>|  
|<span data-ttu-id="78e91-143">messageEncoding</span><span class="sxs-lookup"><span data-stu-id="78e91-143">messageEncoding</span></span>|<span data-ttu-id="78e91-144">メッセージのエンコードに使用されるエンコーダーを定義します。</span><span class="sxs-lookup"><span data-stu-id="78e91-144">Defines the encoder used to encode the message.</span></span> <span data-ttu-id="78e91-145">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="78e91-145">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="78e91-146">テキスト: は、テキスト メッセージ エンコーダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="78e91-146">-   Text: Use a text message encoder.</span></span><br /><span data-ttu-id="78e91-147">Mtom: Message Transmission 組織 Mechanism 1.0 (MTOM) エンコーダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="78e91-147">-   Mtom: Use a Message Transmission Organization Mechanism 1.0 (MTOM) encoder.</span></span><br /><span data-ttu-id="78e91-148">-既定値はテキストです。</span><span class="sxs-lookup"><span data-stu-id="78e91-148">-   The default is Text.</span></span><br /><br /> <span data-ttu-id="78e91-149">この属性は <xref:System.ServiceModel.WSMessageEncoding> 型です。</span><span class="sxs-lookup"><span data-stu-id="78e91-149">This attribute is of type <xref:System.ServiceModel.WSMessageEncoding>.</span></span>|  
|<span data-ttu-id="78e91-150">name</span><span class="sxs-lookup"><span data-stu-id="78e91-150">name</span></span>|<span data-ttu-id="78e91-151">バインディングの構成名を格納する文字列です。</span><span class="sxs-lookup"><span data-stu-id="78e91-151">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="78e91-152">この値は、バインディングの ID として使用されるため、一意にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="78e91-152">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="78e91-153">[!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)] 以降では、バインディングおよび動作に名前を付ける必要はありません。</span><span class="sxs-lookup"><span data-stu-id="78e91-153">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="78e91-154">既定の構成と無名のバインディングおよび動作の詳細については、「[簡略化された構成](../../../../../docs/framework/wcf/simplified-configuration.md)」と「[WCF サービスの構成を簡略化](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="78e91-154">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|<span data-ttu-id="78e91-155">openTimeout</span><span class="sxs-lookup"><span data-stu-id="78e91-155">openTimeout</span></span>|<span data-ttu-id="78e91-156">実行中の操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。</span><span class="sxs-lookup"><span data-stu-id="78e91-156">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="78e91-157">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="78e91-157">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="78e91-158">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="78e91-158">The default is 00:01:00.</span></span>|  
|<span data-ttu-id="78e91-159">proxyAddress</span><span class="sxs-lookup"><span data-stu-id="78e91-159">proxyAddress</span></span>|<span data-ttu-id="78e91-160">HTTP プロキシのアドレスを指定する URI。</span><span class="sxs-lookup"><span data-stu-id="78e91-160">A URI that specifies the address of the HTTP proxy.</span></span> <span data-ttu-id="78e91-161">`useSystemWebProxy` が `true` の場合、この設定を `null` にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="78e91-161">If `useSystemWebProxy` is `true`, this setting must be `null`.</span></span> <span data-ttu-id="78e91-162">既定値は、`null` です。</span><span class="sxs-lookup"><span data-stu-id="78e91-162">The default is `null`.</span></span>|  
|<span data-ttu-id="78e91-163">receiveTimeout</span><span class="sxs-lookup"><span data-stu-id="78e91-163">receiveTimeout</span></span>|<span data-ttu-id="78e91-164">受信操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。</span><span class="sxs-lookup"><span data-stu-id="78e91-164">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="78e91-165">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="78e91-165">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="78e91-166">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="78e91-166">The default is 00:01:00.</span></span>|  
|<span data-ttu-id="78e91-167">sendTimeout</span><span class="sxs-lookup"><span data-stu-id="78e91-167">sendTimeout</span></span>|<span data-ttu-id="78e91-168">送信操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。</span><span class="sxs-lookup"><span data-stu-id="78e91-168">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="78e91-169">この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="78e91-169">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="78e91-170">既定値は 00:01:00 です。</span><span class="sxs-lookup"><span data-stu-id="78e91-170">The default is 00:01:00.</span></span>|  
|<span data-ttu-id="78e91-171">textEncoding</span><span class="sxs-lookup"><span data-stu-id="78e91-171">textEncoding</span></span>|<span data-ttu-id="78e91-172">バインドでメッセージの発行に使用される文字セット エンコーディングを指定します。</span><span class="sxs-lookup"><span data-stu-id="78e91-172">Specifies the character set encoding to be used for emitting messages on the binding.</span></span> <span data-ttu-id="78e91-173">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="78e91-173">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="78e91-174">-UnicodeFffeTextEncoding: Unicode BigEndian エンコーディングします。</span><span class="sxs-lookup"><span data-stu-id="78e91-174">-   UnicodeFffeTextEncoding: Unicode BigEndian encoding.</span></span><br /><span data-ttu-id="78e91-175">-Utf16TextEncoding: 16 ビット エンコーディング。</span><span class="sxs-lookup"><span data-stu-id="78e91-175">-   Utf16TextEncoding: 16-bit encoding.</span></span><br /><span data-ttu-id="78e91-176">-Utf8TextEncoding: 8 ビット エンコーディング。</span><span class="sxs-lookup"><span data-stu-id="78e91-176">-   Utf8TextEncoding: 8-bit encoding.</span></span><br /><br /> <span data-ttu-id="78e91-177">既定値は Utf8TextEncoding です。</span><span class="sxs-lookup"><span data-stu-id="78e91-177">The default is Utf8TextEncoding.</span></span><br /><br /> <span data-ttu-id="78e91-178">この属性は <xref:System.Text.Encoding> 型です。</span><span class="sxs-lookup"><span data-stu-id="78e91-178">This attribute is of type <xref:System.Text.Encoding>.</span></span>|  
|<span data-ttu-id="78e91-179">transactionFlow</span><span class="sxs-lookup"><span data-stu-id="78e91-179">transactionFlow</span></span>|<span data-ttu-id="78e91-180">バインディングが WS-Transactions のフローをサポートするかどうかを指定するブール値です。</span><span class="sxs-lookup"><span data-stu-id="78e91-180">A Boolean value that specifies whether the binding supports flowing WS-Transactions.</span></span> <span data-ttu-id="78e91-181">既定値は、`false` です。</span><span class="sxs-lookup"><span data-stu-id="78e91-181">The default is `false`.</span></span>|  
|<span data-ttu-id="78e91-182">useDefaultWebProxy</span><span class="sxs-lookup"><span data-stu-id="78e91-182">useDefaultWebProxy</span></span>|<span data-ttu-id="78e91-183">システムの自動設定 HTTP プロキシを使用するかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="78e91-183">A Boolean value that specifies whether the system’s auto-configured HTTP proxy is used.</span></span> <span data-ttu-id="78e91-184">既定値は `true` です。</span><span class="sxs-lookup"><span data-stu-id="78e91-184">The default is `true`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="78e91-185">子要素</span><span class="sxs-lookup"><span data-stu-id="78e91-185">Child Elements</span></span>  
  
|<span data-ttu-id="78e91-186">要素</span><span class="sxs-lookup"><span data-stu-id="78e91-186">Element</span></span>|<span data-ttu-id="78e91-187">説明</span><span class="sxs-lookup"><span data-stu-id="78e91-187">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="78e91-188">\<security></span><span class="sxs-lookup"><span data-stu-id="78e91-188">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-wshttpbinding.md)|<span data-ttu-id="78e91-189">バインディングのセキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="78e91-189">Defines the security settings for the binding.</span></span> <span data-ttu-id="78e91-190">この要素は <xref:System.ServiceModel.Configuration.WSHttpSecurityElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="78e91-190">This element is of type <xref:System.ServiceModel.Configuration.WSHttpSecurityElement>.</span></span>|  
|[<span data-ttu-id="78e91-191">\<readerQuotas></span><span class="sxs-lookup"><span data-stu-id="78e91-191">\<readerQuotas></span></span>](https://msdn.microsoft.com/library/3e5e42ff-cef8-478f-bf14-034449239bfd)|<span data-ttu-id="78e91-192">このバインドを使用して設定されるエンドポイントにより処理可能な、SOAP メッセージの複雑さに対する制約を定義します。</span><span class="sxs-lookup"><span data-stu-id="78e91-192">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="78e91-193">この要素は <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="78e91-193">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
|[<span data-ttu-id="78e91-194">reliableSession</span><span class="sxs-lookup"><span data-stu-id="78e91-194">reliableSession</span></span>](https://msdn.microsoft.com/library/9c93818a-7dfa-43d5-b3a1-1aafccf3a00b)|<span data-ttu-id="78e91-195">チャネルのエンドポイント間に信頼できるセッションを確立するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="78e91-195">Specifies if reliable sessions are established between channel endpoints.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="78e91-196">親要素</span><span class="sxs-lookup"><span data-stu-id="78e91-196">Parent Elements</span></span>  
  
|<span data-ttu-id="78e91-197">要素</span><span class="sxs-lookup"><span data-stu-id="78e91-197">Element</span></span>|<span data-ttu-id="78e91-198">説明</span><span class="sxs-lookup"><span data-stu-id="78e91-198">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="78e91-199">\<bindings></span><span class="sxs-lookup"><span data-stu-id="78e91-199">\<bindings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|<span data-ttu-id="78e91-200">この要素には、標準バインディングおよびカスタム バインドのコレクションが保持されます。</span><span class="sxs-lookup"><span data-stu-id="78e91-200">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="78e91-201">Remarks</span><span class="sxs-lookup"><span data-stu-id="78e91-201">Remarks</span></span>  
 <span data-ttu-id="78e91-202">`WSHttpBinding` は `BasicHttpBinding` に似ていますが、より多くの Web サービス機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="78e91-202">The `WSHttpBinding` is similar to the `BasicHttpBinding` but provides more Web service features.</span></span> <span data-ttu-id="78e91-203">BasicHttpBinding と同じように HTTP トランスポートを使用し、メッセージ セキュリティを提供します。さらに、トランザクション、信頼できるメッセージング、および WS-Addressing も提供します。これらは、既定で有効化になっているか、または単一の制御設定で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="78e91-203">It uses the HTTP transport and provides message security, as does BasicHttpBinding, but it also provides transactions, reliable messaging, and WS-Addressing, either enabled by default or available through a single control setting.</span></span>  
  
## <a name="example"></a><span data-ttu-id="78e91-204">例</span><span class="sxs-lookup"><span data-stu-id="78e91-204">Example</span></span>  
  
```xml  
<configuration>  
    <system.ServiceModel>  
        <bindings>  
            <wsHttpBinding>  
                <binding   
                    closeTimeout="00:00:10"  
                    openTimeout="00:00:20"   
                    receiveTimeout="00:00:30"  
                    sendTimeout="00:00:40"  
                    bypassProxyOnLocal="false"  
                    transactionFlow="false"   
                    hostNameComparisonMode="WeakWildcard"  
                    maxReceivedMessageSize="1000"  
                    messageEncoding="Mtom"   
                    proxyAddress="http://foo/bar"  
                    textEncoding="utf-16"  
                    useDefaultWebProxy="false">  
                    <reliableSession ordered="false"  
                         inactivityTimeout="00:02:00"  
                         enabled="true" />  
                    <security mode="Transport">  
                         <transport clientCredentialType="Digest"  
                            proxyCredentialType="None"  
                            realm="someRealm" />  
                         <message clientCredentialType="Windows"  
                            negotiateServiceCredential="false"  
                            algorithmSuite="Aes128"   
                            defaultProtectionLevel="None" />  
                    </security>  
                </binding>  
           </wsHttpBinding>  
        </bindings>  
    </system.ServiceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="78e91-205">関連項目</span><span class="sxs-lookup"><span data-stu-id="78e91-205">See Also</span></span>  
 <xref:System.ServiceModel.WSHttpBinding>  
 <xref:System.ServiceModel.Configuration.WSHttpBindingElement>  
 [<span data-ttu-id="78e91-206">バインディング</span><span class="sxs-lookup"><span data-stu-id="78e91-206">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="78e91-207">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="78e91-207">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="78e91-208">バインドを使用して、Windows Communication Foundation サービスとクライアントを構成するには</span><span class="sxs-lookup"><span data-stu-id="78e91-208">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="78e91-209">\<binding></span><span class="sxs-lookup"><span data-stu-id="78e91-209">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
