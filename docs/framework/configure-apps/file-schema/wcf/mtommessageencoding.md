---
title: '&lt;mtomMessageEncoding&gt;'
ms.date: 03/30/2017
ms.assetid: 7865d171-cd1e-430a-8421-39cc13541d1b
ms.openlocfilehash: b9fe4a9eb0176c97920c0dde5cb003c8ca1ae989
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54697440"
---
# <a name="ltmtommessageencodinggt"></a><span data-ttu-id="adb06-102">&lt;mtomMessageEncoding&gt;</span><span class="sxs-lookup"><span data-stu-id="adb06-102">&lt;mtomMessageEncoding&gt;</span></span>
<span data-ttu-id="adb06-103">SOAP Message Transmission Optimization Mechanism (MTOM) ベースのメッセージに使用されるエンコーディングおよびメッセージ バージョン管理を指定します。</span><span class="sxs-lookup"><span data-stu-id="adb06-103">Specifies the encoding and message versioning used for SOAP Message Transmission Optimization Mechanism (MTOM) based messages.</span></span>  
  
 <span data-ttu-id="adb06-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="adb06-104">\<system.serviceModel></span></span>  
<span data-ttu-id="adb06-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="adb06-105">\<bindings></span></span>  
<span data-ttu-id="adb06-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="adb06-106">\<customBinding></span></span>  
<span data-ttu-id="adb06-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="adb06-107">\<binding></span></span>  
<span data-ttu-id="adb06-108">\<mtomMessageEncoding></span><span class="sxs-lookup"><span data-stu-id="adb06-108">\<mtomMessageEncoding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="adb06-109">構文</span><span class="sxs-lookup"><span data-stu-id="adb06-109">Syntax</span></span>  
  
```xml  
<mtomMessageEncoding maxBufferSize="Integer"
                     maxReadPoolSize="Integer"
                     maxWritePoolSize="Integer"
                     messageVersion="Soap11Addressing1/Soap12Addressing10"
                     writeEncoding="UnicodeFffeTextEncoding/Utf16TextEncoding/Utf8TextEncoding" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="adb06-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="adb06-110">Attributes and Elements</span></span>  
 <span data-ttu-id="adb06-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="adb06-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="adb06-112">属性</span><span class="sxs-lookup"><span data-stu-id="adb06-112">Attributes</span></span>  
  
|<span data-ttu-id="adb06-113">属性</span><span class="sxs-lookup"><span data-stu-id="adb06-113">Attribute</span></span>|<span data-ttu-id="adb06-114">説明</span><span class="sxs-lookup"><span data-stu-id="adb06-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="adb06-115">maxBufferSize</span><span class="sxs-lookup"><span data-stu-id="adb06-115">maxBufferSize</span></span>|<span data-ttu-id="adb06-116">使用できるバッファーの最大サイズを指定する整数。</span><span class="sxs-lookup"><span data-stu-id="adb06-116">An integer that specifies the maximum size of the buffer that can be used.</span></span>|  
|<span data-ttu-id="adb06-117">maxReadPoolSize</span><span class="sxs-lookup"><span data-stu-id="adb06-117">maxReadPoolSize</span></span>|<span data-ttu-id="adb06-118">新しいリーダーを割り当てずに同時に読み取り可能なメッセージの数を指定する整数です。</span><span class="sxs-lookup"><span data-stu-id="adb06-118">An integer that specifies how many messages can be read simultaneously without allocating new readers.</span></span> <span data-ttu-id="adb06-119">プール サイズを大きくすると、システムでは、比較的大きい作業セットで、アクティビティの急増に対する許容度が高まります。</span><span class="sxs-lookup"><span data-stu-id="adb06-119">Larger pool sizes make the system more tolerant to activity spikes at the cost of a larger working set.</span></span> <span data-ttu-id="adb06-120">既定値は 64 です。</span><span class="sxs-lookup"><span data-stu-id="adb06-120">The default is 64.</span></span>|  
|<span data-ttu-id="adb06-121">maxWritePoolSize</span><span class="sxs-lookup"><span data-stu-id="adb06-121">maxWritePoolSize</span></span>|<span data-ttu-id="adb06-122">新しいライターを割り当てずに同時に送信可能なメッセージの数を指定する整数です。</span><span class="sxs-lookup"><span data-stu-id="adb06-122">An integer that specifies how many messages can be sent simultaneously without allocating new writers.</span></span> <span data-ttu-id="adb06-123">プール サイズを大きくすると、システムでは、比較的大きい作業セットで、アクティビティの急増に対する許容度が高まります。</span><span class="sxs-lookup"><span data-stu-id="adb06-123">Larger pool sizes make the system more tolerant to activity spikes at the cost of a larger working set.</span></span> <span data-ttu-id="adb06-124">既定値は 16 です。</span><span class="sxs-lookup"><span data-stu-id="adb06-124">The default is 16.</span></span>|  
|<span data-ttu-id="adb06-125">messageVersion</span><span class="sxs-lookup"><span data-stu-id="adb06-125">messageVersion</span></span>|<span data-ttu-id="adb06-126">バインディングを使用して送信されたメッセージの SOAP バージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="adb06-126">Specifies the SOAP version of the messages sent using the binding.</span></span> <span data-ttu-id="adb06-127">有効な値は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="adb06-127">Valid values are</span></span><br /><br /> <span data-ttu-id="adb06-128">-Soap11addressing1 です。</span><span class="sxs-lookup"><span data-stu-id="adb06-128">-   Soap11Addressing1</span></span><br /><span data-ttu-id="adb06-129">-Soap12addressing10 です。</span><span class="sxs-lookup"><span data-stu-id="adb06-129">-   Soap12Addressing10</span></span><br /><br /> <span data-ttu-id="adb06-130">既定値は Soap12Addressing10 です。</span><span class="sxs-lookup"><span data-stu-id="adb06-130">The default is Soap12Addressing10.</span></span> <span data-ttu-id="adb06-131">この属性は <xref:System.ServiceModel.Channels.MessageVersion> 型です。</span><span class="sxs-lookup"><span data-stu-id="adb06-131">This attribute is of type <xref:System.ServiceModel.Channels.MessageVersion>.</span></span>|  
|<span data-ttu-id="adb06-132">writeEncoding</span><span class="sxs-lookup"><span data-stu-id="adb06-132">writeEncoding</span></span>|<span data-ttu-id="adb06-133">バインドでメッセージの発行に使用される文字セット エンコーディングを指定します。</span><span class="sxs-lookup"><span data-stu-id="adb06-133">Specifies the character set encoding to be used for emitting messages on the binding.</span></span> <span data-ttu-id="adb06-134">有効な値は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="adb06-134">Valid values are</span></span><br /><br /> <span data-ttu-id="adb06-135">-   UnicodeFffeTextEncoding:Unicode BigEndian エンコーディング</span><span class="sxs-lookup"><span data-stu-id="adb06-135">-   UnicodeFffeTextEncoding: Unicode BigEndian encoding</span></span><br /><span data-ttu-id="adb06-136">-   Utf16TextEncoding:Unicode エンコーディング</span><span class="sxs-lookup"><span data-stu-id="adb06-136">-   Utf16TextEncoding: Unicode encoding</span></span><br /><span data-ttu-id="adb06-137">-   Utf8TextEncoding:8 ビット エンコード</span><span class="sxs-lookup"><span data-stu-id="adb06-137">-   Utf8TextEncoding: 8-bit encoding</span></span><br /><br /> <span data-ttu-id="adb06-138">既定値は Utf8TextEncoding です。</span><span class="sxs-lookup"><span data-stu-id="adb06-138">The default is Utf8TextEncoding.</span></span> <span data-ttu-id="adb06-139">この属性は <xref:System.Text.Encoding> 型です。</span><span class="sxs-lookup"><span data-stu-id="adb06-139">This attribute is of type <xref:System.Text.Encoding>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="adb06-140">子要素</span><span class="sxs-lookup"><span data-stu-id="adb06-140">Child Elements</span></span>  
  
|<span data-ttu-id="adb06-141">要素</span><span class="sxs-lookup"><span data-stu-id="adb06-141">Element</span></span>|<span data-ttu-id="adb06-142">説明</span><span class="sxs-lookup"><span data-stu-id="adb06-142">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="adb06-143">\<readerQuotas></span><span class="sxs-lookup"><span data-stu-id="adb06-143">\<readerQuotas></span></span>](https://msdn.microsoft.com/library/3e5e42ff-cef8-478f-bf14-034449239bfd)|<span data-ttu-id="adb06-144">このバインドを使用して設定されるエンドポイントにより処理可能な、SOAP メッセージの複雑さに対する制約を定義します。</span><span class="sxs-lookup"><span data-stu-id="adb06-144">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="adb06-145">この要素は <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="adb06-145">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="adb06-146">親要素</span><span class="sxs-lookup"><span data-stu-id="adb06-146">Parent Elements</span></span>  
  
|<span data-ttu-id="adb06-147">要素</span><span class="sxs-lookup"><span data-stu-id="adb06-147">Element</span></span>|<span data-ttu-id="adb06-148">説明</span><span class="sxs-lookup"><span data-stu-id="adb06-148">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="adb06-149">\<binding></span><span class="sxs-lookup"><span data-stu-id="adb06-149">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="adb06-150">カスタム バインドのすべてのバインド機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="adb06-150">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="adb06-151">Remarks</span><span class="sxs-lookup"><span data-stu-id="adb06-151">Remarks</span></span>  
 <span data-ttu-id="adb06-152">エンコーディングは、メッセージをバイト シーケンスに変換するプロセスです。</span><span class="sxs-lookup"><span data-stu-id="adb06-152">Encoding is the process of transforming a message into a sequence of bytes.</span></span> <span data-ttu-id="adb06-153">デコードは、その逆のプロセスです。</span><span class="sxs-lookup"><span data-stu-id="adb06-153">Decoding is the reverse process.</span></span> <span data-ttu-id="adb06-154">Windows Communication Foundation (WCF) には、SOAP メッセージのエンコードの 3 つの種類が含まれます。テキスト、バイナリ、および Message Transmission Optimization Mechanism (MTOM)。</span><span class="sxs-lookup"><span data-stu-id="adb06-154">Windows Communication Foundation (WCF) includes three types of encoding for SOAP messages: Text, Binary and Message Transmission Optimization Mechanism (MTOM).</span></span>  
  
 <span data-ttu-id="adb06-155">`MtomMessageEncoding` 要素は、MTOM (Message Transmission Optimization Mechanism) エンコーディングを使用するメッセージの文字エンコーディング、メッセージのバージョン管理、およびその他の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="adb06-155">The `MtomMessageEncoding` element specifies the character encoding and message versioning and other settings used for messages using a Message Transmission Optimization Mechanism (MTOM) encoding.</span></span> <span data-ttu-id="adb06-156">MTOM は、WCF メッセージでバイナリ データを転送するための効率的なテクノロジです。</span><span class="sxs-lookup"><span data-stu-id="adb06-156">MTOM is an efficient technology for transmitting binary data in WCF messages.</span></span> <span data-ttu-id="adb06-157">MTOM エンコーダーは、効率と相互運用性のバランスをとろうとします。</span><span class="sxs-lookup"><span data-stu-id="adb06-157">The MTOM encoder attempts to create a balance between efficiency and interoperability.</span></span> <span data-ttu-id="adb06-158">MTOM エンコーディングは、ほとんどの XML をテキスト形式で転送しますが、大きいサイズのバイナリ データ ブロックは、base64 でエンコードされた形式に変換せずに、そのまま転送することによって最適化します。</span><span class="sxs-lookup"><span data-stu-id="adb06-158">The MTOM encoding transmits most XML in textual form, but optimizes large blocks of binary data by transmitting them as-is, without conversion to their base64 encoded format.</span></span>  
  
## <a name="example"></a><span data-ttu-id="adb06-159">例</span><span class="sxs-lookup"><span data-stu-id="adb06-159">Example</span></span>  
  
```xml  
<mtomMessageEncoding maxReadPoolSize="211"
                     maxWritePoolSize="2132"
                     messageVersion="Soap11Addressing10"
                     textEncoding="utf-8" />
```  
  
## <a name="see-also"></a><span data-ttu-id="adb06-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="adb06-160">See also</span></span>
- <xref:System.ServiceModel.Configuration.MtomMessageEncodingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Channels.MessageEncodingBindingElement>
- <xref:System.ServiceModel.Channels.MtomMessageEncodingBindingElement>
- [<span data-ttu-id="adb06-161">メッセージ エンコーディング</span><span class="sxs-lookup"><span data-stu-id="adb06-161">Message Encoding</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-encoding.md)
- [<span data-ttu-id="adb06-162">メッセージ エンコーダーを選択する</span><span class="sxs-lookup"><span data-stu-id="adb06-162">Choosing a Message Encoder</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-message-encoder.md)
- [<span data-ttu-id="adb06-163">バインディング</span><span class="sxs-lookup"><span data-stu-id="adb06-163">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="adb06-164">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="adb06-164">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="adb06-165">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="adb06-165">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="adb06-166">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="adb06-166">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
