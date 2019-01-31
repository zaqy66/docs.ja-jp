---
title: <byteStreamMessageEncoding>
ms.date: 03/30/2017
ms.assetid: bbadd8dd-60a2-4007-b959-89373a8a7d60
ms.openlocfilehash: b1215f864822de7c2df181ff92858cb73700c0d7
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55286270"
---
# <a name="bytestreammessageencoding"></a><span data-ttu-id="982da-101">\<byteStreamMessageEncoding></span><span class="sxs-lookup"><span data-stu-id="982da-101">\<byteStreamMessageEncoding></span></span>
<span data-ttu-id="982da-102">文字エンコーディングを指定するオプションを使用し、メッセージ エンコーディングをバイト ストリームとして指定します。</span><span class="sxs-lookup"><span data-stu-id="982da-102">Specifies the message encoding as a stream of bytes, with the option to specify the character encoding.</span></span>  
  
 <span data-ttu-id="982da-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="982da-103">\<system.serviceModel></span></span>  
<span data-ttu-id="982da-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="982da-104">\<bindings></span></span>  
<span data-ttu-id="982da-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="982da-105">\<customBinding></span></span>  
<span data-ttu-id="982da-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="982da-106">\<binding></span></span>  
<span data-ttu-id="982da-107">\<binaryMessageEncoding></span><span class="sxs-lookup"><span data-stu-id="982da-107">\<binaryMessageEncoding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="982da-108">構文</span><span class="sxs-lookup"><span data-stu-id="982da-108">Syntax</span></span>  
  
```xml  
<byteStreamMessageEncoding />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="982da-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="982da-109">Attributes and Elements</span></span>  
 <span data-ttu-id="982da-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="982da-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="982da-111">属性</span><span class="sxs-lookup"><span data-stu-id="982da-111">Attributes</span></span>  
  
|<span data-ttu-id="982da-112">属性</span><span class="sxs-lookup"><span data-stu-id="982da-112">Attribute</span></span>|<span data-ttu-id="982da-113">説明</span><span class="sxs-lookup"><span data-stu-id="982da-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="982da-114">messageVersion</span><span class="sxs-lookup"><span data-stu-id="982da-114">messageVersion</span></span>|<span data-ttu-id="982da-115">バインディングを使用して送信されたメッセージの SOAP バージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="982da-115">Specifies the SOAP version of the messages sent using the binding.</span></span> <span data-ttu-id="982da-116">このプロパティは、<xref:System.ServiceModel.Channels.MessageVersion.None%2A> のメッセージ バージョン値にのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="982da-116">This property can only be set to the message version value of <xref:System.ServiceModel.Channels.MessageVersion.None%2A>.</span></span> <span data-ttu-id="982da-117">バイト ストリーム メッセージ エンコーダーは、他のメッセージ バージョンをサポートしません。</span><span class="sxs-lookup"><span data-stu-id="982da-117">The byte stream message encoder does not support any other message versions.</span></span><br /><br /> <span data-ttu-id="982da-118">この属性は <xref:System.ServiceModel.Channels.MessageVersion> 型です。</span><span class="sxs-lookup"><span data-stu-id="982da-118">This attribute is of type <xref:System.ServiceModel.Channels.MessageVersion>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="982da-119">子要素</span><span class="sxs-lookup"><span data-stu-id="982da-119">Child Elements</span></span>  
  
|<span data-ttu-id="982da-120">要素</span><span class="sxs-lookup"><span data-stu-id="982da-120">Element</span></span>|<span data-ttu-id="982da-121">説明</span><span class="sxs-lookup"><span data-stu-id="982da-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="982da-122">\<readerQuotas></span><span class="sxs-lookup"><span data-stu-id="982da-122">\<readerQuotas></span></span>](https://msdn.microsoft.com/library/3e5e42ff-cef8-478f-bf14-034449239bfd)|<span data-ttu-id="982da-123">このバインドを使用して設定されるエンドポイントにより処理可能な、SOAP メッセージの複雑さに対する制約を定義します。</span><span class="sxs-lookup"><span data-stu-id="982da-123">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="982da-124">この要素は <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="982da-124">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="982da-125">親要素</span><span class="sxs-lookup"><span data-stu-id="982da-125">Parent Elements</span></span>  
  
|<span data-ttu-id="982da-126">要素</span><span class="sxs-lookup"><span data-stu-id="982da-126">Element</span></span>|<span data-ttu-id="982da-127">説明</span><span class="sxs-lookup"><span data-stu-id="982da-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="982da-128">\<binding></span><span class="sxs-lookup"><span data-stu-id="982da-128">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="982da-129">カスタム バインドのすべてのバインド機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="982da-129">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="982da-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="982da-130">See also</span></span>
- <xref:System.ServiceModel.Configuration.ByteStreamMessageEncodingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Channels.MessageEncodingBindingElement>
- <xref:System.ServiceModel.Channels.ByteStreamMessageEncodingBindingElement>
- [<span data-ttu-id="982da-131">メッセージ エンコーディング</span><span class="sxs-lookup"><span data-stu-id="982da-131">Message Encoding</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-encoding.md)
- [<span data-ttu-id="982da-132">メッセージ エンコーダーを選択する</span><span class="sxs-lookup"><span data-stu-id="982da-132">Choosing a Message Encoder</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-message-encoder.md)
- [<span data-ttu-id="982da-133">バインディング</span><span class="sxs-lookup"><span data-stu-id="982da-133">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="982da-134">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="982da-134">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="982da-135">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="982da-135">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="982da-136">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="982da-136">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
