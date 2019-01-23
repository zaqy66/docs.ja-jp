---
title: '&lt;sslStreamSecurity&gt;'
ms.date: 03/30/2017
ms.assetid: 430a378b-a742-4858-8a12-9f9b235fd627
ms.openlocfilehash: fe633aa1ed2b165a83f415748b70b6a66bbb0130
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54540920"
---
# <a name="ltsslstreamsecuritygt"></a><span data-ttu-id="b0f90-102">&lt;sslStreamSecurity&gt;</span><span class="sxs-lookup"><span data-stu-id="b0f90-102">&lt;sslStreamSecurity&gt;</span></span>
<span data-ttu-id="b0f90-103">SSL ストリームを使用してチャネル セキュリティをサポートするカスタム バインド要素を表します。</span><span class="sxs-lookup"><span data-stu-id="b0f90-103">Represents a custom binding element that supports channel security using an SSL stream.</span></span>  
  
 <span data-ttu-id="b0f90-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="b0f90-104">\<system.serviceModel></span></span>  
<span data-ttu-id="b0f90-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="b0f90-105">\<bindings></span></span>  
<span data-ttu-id="b0f90-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="b0f90-106">\<customBinding></span></span>  
<span data-ttu-id="b0f90-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="b0f90-107">\<binding></span></span>  
<span data-ttu-id="b0f90-108">\<sslStreamSecurity></span><span class="sxs-lookup"><span data-stu-id="b0f90-108">\<sslStreamSecurity></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b0f90-109">構文</span><span class="sxs-lookup"><span data-stu-id="b0f90-109">Syntax</span></span>  
  
```xml  
<sslStreamSecurity requireClientCertificate="Boolean"
                   sslProtocols="Ssl3|Tls|Tls11|Tls12" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b0f90-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="b0f90-110">Attributes and Elements</span></span>  
 <span data-ttu-id="b0f90-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="b0f90-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b0f90-112">属性</span><span class="sxs-lookup"><span data-stu-id="b0f90-112">Attributes</span></span>  
  
|<span data-ttu-id="b0f90-113">属性</span><span class="sxs-lookup"><span data-stu-id="b0f90-113">Attribute</span></span>|<span data-ttu-id="b0f90-114">説明</span><span class="sxs-lookup"><span data-stu-id="b0f90-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b0f90-115">requireClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b0f90-115">requireClientCertificate</span></span>|<span data-ttu-id="b0f90-116">クライアント証明書がこのバインディングに必要かどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="b0f90-116">A Boolean value that specifies if a client certificate is required for this binding.</span></span> <span data-ttu-id="b0f90-117">既定値は `false` です。</span><span class="sxs-lookup"><span data-stu-id="b0f90-117">The default is `false`.</span></span>|  
|<span data-ttu-id="b0f90-118">sslProtocols</span><span class="sxs-lookup"><span data-stu-id="b0f90-118">sslProtocols</span></span>|<span data-ttu-id="b0f90-119">どの SslProtocols がサポートされているのかを指定する SslProtocols 列挙型フラグの値。</span><span class="sxs-lookup"><span data-stu-id="b0f90-119">A SslProtocols enum flag value that specifies which SslProtocols are supported.</span></span> <span data-ttu-id="b0f90-120">既定値は Ssl3&#124;Tls&#124;Tls11&#124;tls12 です。</span><span class="sxs-lookup"><span data-stu-id="b0f90-120">The default is Ssl3&#124;Tls&#124;Tls11&#124;Tls12.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b0f90-121">子要素</span><span class="sxs-lookup"><span data-stu-id="b0f90-121">Child Elements</span></span>  
 <span data-ttu-id="b0f90-122">なし。</span><span class="sxs-lookup"><span data-stu-id="b0f90-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b0f90-123">親要素</span><span class="sxs-lookup"><span data-stu-id="b0f90-123">Parent Elements</span></span>  
  
|<span data-ttu-id="b0f90-124">要素</span><span class="sxs-lookup"><span data-stu-id="b0f90-124">Element</span></span>|<span data-ttu-id="b0f90-125">説明</span><span class="sxs-lookup"><span data-stu-id="b0f90-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b0f90-126">\<binding></span><span class="sxs-lookup"><span data-stu-id="b0f90-126">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="b0f90-127">カスタム バインドのすべてのバインド機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="b0f90-127">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b0f90-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="b0f90-128">See also</span></span>
- <xref:System.ServiceModel.Configuration.SslStreamSecurityElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement>
- [<span data-ttu-id="b0f90-129">バインディング</span><span class="sxs-lookup"><span data-stu-id="b0f90-129">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="b0f90-130">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="b0f90-130">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="b0f90-131">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="b0f90-131">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="b0f90-132">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="b0f90-132">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
