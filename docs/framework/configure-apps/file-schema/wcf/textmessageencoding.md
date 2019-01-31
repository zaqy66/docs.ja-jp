---
title: <textMessageEncoding>
ms.date: 03/30/2017
ms.assetid: e6d834d0-356e-45eb-b530-bbefbb9ec3f0
ms.openlocfilehash: c9f8347b4ee5f8fdbcf5c65c9a38b171ea6309de
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55289602"
---
# <a name="textmessageencoding"></a><span data-ttu-id="df9b5-101">\<textMessageEncoding></span><span class="sxs-lookup"><span data-stu-id="df9b5-101">\<textMessageEncoding></span></span>
<span data-ttu-id="df9b5-102">テキストベースの XML メッセージに使用される文字エンコーディングおよびメッセージ バージョン管理を指定します。</span><span class="sxs-lookup"><span data-stu-id="df9b5-102">Specifies the character encoding and message versioning used for text-based XML messages.</span></span>  
  
 <span data-ttu-id="df9b5-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="df9b5-103">\<system.serviceModel></span></span>  
<span data-ttu-id="df9b5-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="df9b5-104">\<bindings></span></span>  
<span data-ttu-id="df9b5-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="df9b5-105">\<customBinding></span></span>  
<span data-ttu-id="df9b5-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="df9b5-106">\<binding></span></span>  
<span data-ttu-id="df9b5-107">\<textMessageEncoding></span><span class="sxs-lookup"><span data-stu-id="df9b5-107">\<textMessageEncoding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="df9b5-108">構文</span><span class="sxs-lookup"><span data-stu-id="df9b5-108">Syntax</span></span>  
  
```xml  
<textMessageEncoding maxReadPoolSize="Integer"
                     maxWritePoolSize="Integer"
                     messageVersion="Soap11Addressing10/Soap12Addressing10"
                     writeEncoding="UnicodeFffeTextEncoding/Utf16TextEncoding/Utf8TextEncoding" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="df9b5-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="df9b5-109">Attributes and Elements</span></span>  
 <span data-ttu-id="df9b5-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="df9b5-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="df9b5-111">属性</span><span class="sxs-lookup"><span data-stu-id="df9b5-111">Attributes</span></span>  
  
|<span data-ttu-id="df9b5-112">属性</span><span class="sxs-lookup"><span data-stu-id="df9b5-112">Attribute</span></span>|<span data-ttu-id="df9b5-113">説明</span><span class="sxs-lookup"><span data-stu-id="df9b5-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="df9b5-114">maxReadPoolSize</span><span class="sxs-lookup"><span data-stu-id="df9b5-114">maxReadPoolSize</span></span>|<span data-ttu-id="df9b5-115">新しいリーダーを割り当てずに同時に読み取り可能なメッセージの数を指定する整数です。</span><span class="sxs-lookup"><span data-stu-id="df9b5-115">An integer that specifies how many messages can be read simultaneously without allocating new readers.</span></span> <span data-ttu-id="df9b5-116">プール サイズを大きくすると、システムでは、比較的大きい作業セットで、アクティビティの急増に対する許容度が高まります。</span><span class="sxs-lookup"><span data-stu-id="df9b5-116">Larger pool sizes make the system more tolerant to activity spikes at the cost of a larger working set.</span></span> <span data-ttu-id="df9b5-117">既定値は 64 です。</span><span class="sxs-lookup"><span data-stu-id="df9b5-117">The default is 64.</span></span>|  
|<span data-ttu-id="df9b5-118">maxWritePoolSize</span><span class="sxs-lookup"><span data-stu-id="df9b5-118">maxWritePoolSize</span></span>|<span data-ttu-id="df9b5-119">新しいライターを割り当てずに同時に送信可能なメッセージの数を指定する整数です。</span><span class="sxs-lookup"><span data-stu-id="df9b5-119">An integer that specifies how many messages can be sent simultaneously without allocating new writers.</span></span> <span data-ttu-id="df9b5-120">プール サイズを大きくすると、システムでは、比較的大きい作業セットで、アクティビティの急増に対する許容度が高まります。</span><span class="sxs-lookup"><span data-stu-id="df9b5-120">Larger pool sizes make the system more tolerant to activity spikes at the cost of a larger working set.</span></span> <span data-ttu-id="df9b5-121">既定値は 16 です。</span><span class="sxs-lookup"><span data-stu-id="df9b5-121">The default is 16.</span></span>|  
|<span data-ttu-id="df9b5-122">messageVersion</span><span class="sxs-lookup"><span data-stu-id="df9b5-122">messageVersion</span></span>|<span data-ttu-id="df9b5-123">バインディングを使用して送信されたメッセージの SOAP バージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="df9b5-123">Specifies the SOAP version of the messages sent using the binding.</span></span> <span data-ttu-id="df9b5-124">有効な値は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="df9b5-124">Valid values are</span></span><br /><br /> <span data-ttu-id="df9b5-125">-Soap11Addressing10</span><span class="sxs-lookup"><span data-stu-id="df9b5-125">-   Soap11Addressing10</span></span><br /><span data-ttu-id="df9b5-126">-Soap12addressing10 です。</span><span class="sxs-lookup"><span data-stu-id="df9b5-126">-   Soap12Addressing10</span></span><br /><br /> <span data-ttu-id="df9b5-127">既定値は Soap12Addressing10 です。</span><span class="sxs-lookup"><span data-stu-id="df9b5-127">The default is Soap12Addressing10.</span></span> <span data-ttu-id="df9b5-128">この属性は <xref:System.ServiceModel.Channels.MessageVersion> 型です。</span><span class="sxs-lookup"><span data-stu-id="df9b5-128">This attribute is of type <xref:System.ServiceModel.Channels.MessageVersion>.</span></span>|  
|<span data-ttu-id="df9b5-129">writeEncoding</span><span class="sxs-lookup"><span data-stu-id="df9b5-129">writeEncoding</span></span>|<span data-ttu-id="df9b5-130">バインドでメッセージの発行に使用される文字セット エンコーディングを指定します。</span><span class="sxs-lookup"><span data-stu-id="df9b5-130">Specifies the character set encoding to be used for emitting messages on the binding.</span></span> <span data-ttu-id="df9b5-131">有効な値は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="df9b5-131">Valid values are</span></span><br /><br /> <span data-ttu-id="df9b5-132">-   UnicodeFffeTextEncoding:Unicode BigEndian エンコーディング</span><span class="sxs-lookup"><span data-stu-id="df9b5-132">-   UnicodeFffeTextEncoding: Unicode BigEndian encoding</span></span><br /><span data-ttu-id="df9b5-133">-   Utf16TextEncoding:Unicode エンコーディング</span><span class="sxs-lookup"><span data-stu-id="df9b5-133">-   Utf16TextEncoding: Unicode encoding</span></span><br /><span data-ttu-id="df9b5-134">-   Utf8TextEncoding:8 ビット エンコード</span><span class="sxs-lookup"><span data-stu-id="df9b5-134">-   Utf8TextEncoding: 8-bit encoding</span></span><br /><br /> <span data-ttu-id="df9b5-135">既定値は Utf8TextEncoding です。</span><span class="sxs-lookup"><span data-stu-id="df9b5-135">The default is Utf8TextEncoding.</span></span> <span data-ttu-id="df9b5-136">この属性は <xref:System.Text.Encoding> 型です。</span><span class="sxs-lookup"><span data-stu-id="df9b5-136">This attribute is of type <xref:System.Text.Encoding>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="df9b5-137">子要素</span><span class="sxs-lookup"><span data-stu-id="df9b5-137">Child Elements</span></span>  
  
|<span data-ttu-id="df9b5-138">要素</span><span class="sxs-lookup"><span data-stu-id="df9b5-138">Element</span></span>|<span data-ttu-id="df9b5-139">説明</span><span class="sxs-lookup"><span data-stu-id="df9b5-139">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="df9b5-140">\<readerQuotas></span><span class="sxs-lookup"><span data-stu-id="df9b5-140">\<readerQuotas></span></span>](https://msdn.microsoft.com/library/3e5e42ff-cef8-478f-bf14-034449239bfd)|<span data-ttu-id="df9b5-141">このバインドを使用して設定されるエンドポイントにより処理可能な、SOAP メッセージの複雑さに対する制約を定義します。</span><span class="sxs-lookup"><span data-stu-id="df9b5-141">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="df9b5-142">この要素は <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="df9b5-142">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="df9b5-143">親要素</span><span class="sxs-lookup"><span data-stu-id="df9b5-143">Parent Elements</span></span>  
  
|<span data-ttu-id="df9b5-144">要素</span><span class="sxs-lookup"><span data-stu-id="df9b5-144">Element</span></span>|<span data-ttu-id="df9b5-145">説明</span><span class="sxs-lookup"><span data-stu-id="df9b5-145">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="df9b5-146">\<binding></span><span class="sxs-lookup"><span data-stu-id="df9b5-146">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="df9b5-147">カスタム バインドのすべてのバインド機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="df9b5-147">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="df9b5-148">Remarks</span><span class="sxs-lookup"><span data-stu-id="df9b5-148">Remarks</span></span>  
 <span data-ttu-id="df9b5-149">エンコーディングは、メッセージをバイト シーケンスに変換するプロセスです。</span><span class="sxs-lookup"><span data-stu-id="df9b5-149">Encoding is the process of transforming a message into a sequence of bytes.</span></span> <span data-ttu-id="df9b5-150">デコードは、その逆のプロセスです。</span><span class="sxs-lookup"><span data-stu-id="df9b5-150">Decoding is the reverse process.</span></span> <span data-ttu-id="df9b5-151">Windows Communication Foundation (WCF) には、SOAP メッセージのエンコードの 3 つの種類が含まれます。テキスト、バイナリ、および Message Transmission Optimization Mechanism (MTOM)。</span><span class="sxs-lookup"><span data-stu-id="df9b5-151">Windows Communication Foundation (WCF) includes three types of encoding for SOAP messages: Text, Binary and Message Transmission Optimization Mechanism (MTOM).</span></span>  
  
 <span data-ttu-id="df9b5-152">`textMessageEncoding` 要素で表されるテキスト エンコーディングでは相互運用性が最も高くなりますが、XML メッセージのエンコーダーとしての効率は最も低くなります。</span><span class="sxs-lookup"><span data-stu-id="df9b5-152">The text encoding represented by the `textMessageEncoding` element is the most interoperable, but the least efficient encoder for XML messages.</span></span>  <span data-ttu-id="df9b5-153">テキスト エンコーダーは、ネットワーク上でテキストベースのメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="df9b5-153">The text encoder creates text-based messages on the wire.</span></span> <span data-ttu-id="df9b5-154">このエンコーダーにより生成されるメッセージは、WS-\* ベースの相互運用に適しています。</span><span class="sxs-lookup"><span data-stu-id="df9b5-154">Messages produced by this encoder are suitable for WS-\* based interop.</span></span> <span data-ttu-id="df9b5-155">Web サービスまたは Web サービス クライアントは、一般に、テキスト形式の XML を認識できます。</span><span class="sxs-lookup"><span data-stu-id="df9b5-155">Web service or Web service client can generally understand textual XML.</span></span> <span data-ttu-id="df9b5-156">しかし、大きいブロックのバイナリ データをテキストとして転送するのは、XML メッセージをエンコードする上では、最も非効率的な方法です。</span><span class="sxs-lookup"><span data-stu-id="df9b5-156">However, transmitting large blocks of binary data as text is the least efficient method for encoding XML messages.</span></span>  
  
## <a name="example"></a><span data-ttu-id="df9b5-157">例</span><span class="sxs-lookup"><span data-stu-id="df9b5-157">Example</span></span>  
  
```xml  
<textMessageEncoding maxReadPoolSize="211"
                     maxWritePoolSize="2132"
                     messageVersion="Soap12Addressing10"
                     textEncoding="utf-8" />
```  
  
## <a name="see-also"></a><span data-ttu-id="df9b5-158">関連項目</span><span class="sxs-lookup"><span data-stu-id="df9b5-158">See also</span></span>
- <xref:System.ServiceModel.Configuration.TextMessageEncodingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Channels.MessageEncodingBindingElement>
- <xref:System.ServiceModel.Channels.TextMessageEncodingBindingElement>
- [<span data-ttu-id="df9b5-159">メッセージ エンコーダーを選択する</span><span class="sxs-lookup"><span data-stu-id="df9b5-159">Choosing a Message Encoder</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-message-encoder.md)
- [<span data-ttu-id="df9b5-160">メッセージ エンコーディング</span><span class="sxs-lookup"><span data-stu-id="df9b5-160">Message Encoding</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-encoding.md)
- [<span data-ttu-id="df9b5-161">バインディング</span><span class="sxs-lookup"><span data-stu-id="df9b5-161">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="df9b5-162">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="df9b5-162">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="df9b5-163">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="df9b5-163">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="df9b5-164">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="df9b5-164">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
