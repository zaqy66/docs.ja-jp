---
title: '&lt;windowsStreamSecurity&gt;'
ms.date: 03/30/2017
ms.assetid: 926bea29-90c7-4a26-9cf0-fb4aa44f6f70
author: BrucePerlerMS
ms.openlocfilehash: 6c1253e6f402da6b818a4438142e122f8b31809c
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48032453"
---
# <a name="ltwindowsstreamsecuritygt"></a><span data-ttu-id="6c482-102">&lt;windowsStreamSecurity&gt;</span><span class="sxs-lookup"><span data-stu-id="6c482-102">&lt;windowsStreamSecurity&gt;</span></span>
<span data-ttu-id="6c482-103">カスタム バインドの Windows ストリーム セキュリティ設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="6c482-103">Specify Windows stream security settings of the custom binding.</span></span>  
  
 <span data-ttu-id="6c482-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="6c482-104">\<system.serviceModel></span></span>  
<span data-ttu-id="6c482-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="6c482-105">\<bindings></span></span>  
<span data-ttu-id="6c482-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="6c482-106">\<customBinding></span></span>  
<span data-ttu-id="6c482-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="6c482-107">\<binding></span></span>  
<span data-ttu-id="6c482-108">\<windowsStreamSecurity ></span><span class="sxs-lookup"><span data-stu-id="6c482-108">\<windowsStreamSecurity></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c482-109">構文</span><span class="sxs-lookup"><span data-stu-id="6c482-109">Syntax</span></span>  
  
```xml  
<windowsStreamSecurity protectionLevel="None/Sign/EncryptAndSign"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6c482-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="6c482-110">Attributes and Elements</span></span>  
 <span data-ttu-id="6c482-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="6c482-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6c482-112">属性</span><span class="sxs-lookup"><span data-stu-id="6c482-112">Attributes</span></span>  
  
|<span data-ttu-id="6c482-113">属性</span><span class="sxs-lookup"><span data-stu-id="6c482-113">Attribute</span></span>|<span data-ttu-id="6c482-114">説明</span><span class="sxs-lookup"><span data-stu-id="6c482-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6c482-115">protectionLevel</span><span class="sxs-lookup"><span data-stu-id="6c482-115">protectionLevel</span></span>|<span data-ttu-id="6c482-116">メッセージ レベルのセキュリティを定義します。</span><span class="sxs-lookup"><span data-stu-id="6c482-116">Defines message-level security.</span></span> <span data-ttu-id="6c482-117">メッセージに署名すると、転送中のメッセージが第三者によって改ざんされるリスクを軽減します。</span><span class="sxs-lookup"><span data-stu-id="6c482-117">Signing messages mitigates the risk of a third party tampering with the message while it is being transferred.</span></span> <span data-ttu-id="6c482-118">暗号化により、転送中にデータレベルのプライバシーが提供されます。</span><span class="sxs-lookup"><span data-stu-id="6c482-118">Encryption provides data-level privacy during transport.</span></span> <span data-ttu-id="6c482-119">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="6c482-119">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="6c482-120">-None: 保護されません。</span><span class="sxs-lookup"><span data-stu-id="6c482-120">-   None: No protection.</span></span><br /><span data-ttu-id="6c482-121">署名: メッセージが署名されます。</span><span class="sxs-lookup"><span data-stu-id="6c482-121">-   Sign: Messages are signed.</span></span><br /><span data-ttu-id="6c482-122">-EncryptAndSign: メッセージに署名および暗号化します。</span><span class="sxs-lookup"><span data-stu-id="6c482-122">-   EncryptAndSign: Messages are signed and encrypted.</span></span><br /><br /> <span data-ttu-id="6c482-123">既定値は EncryptAndSign です。</span><span class="sxs-lookup"><span data-stu-id="6c482-123">The default is EncryptAndSign.</span></span><br /><br /> <span data-ttu-id="6c482-124">この属性は <xref:System.Net.Security.ProtectionLevel> 型です。</span><span class="sxs-lookup"><span data-stu-id="6c482-124">This attribute is of type <xref:System.Net.Security.ProtectionLevel>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6c482-125">子要素</span><span class="sxs-lookup"><span data-stu-id="6c482-125">Child Elements</span></span>  
 <span data-ttu-id="6c482-126">なし</span><span class="sxs-lookup"><span data-stu-id="6c482-126">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6c482-127">親要素</span><span class="sxs-lookup"><span data-stu-id="6c482-127">Parent Elements</span></span>  
  
|<span data-ttu-id="6c482-128">要素</span><span class="sxs-lookup"><span data-stu-id="6c482-128">Element</span></span>|<span data-ttu-id="6c482-129">説明</span><span class="sxs-lookup"><span data-stu-id="6c482-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6c482-130">\<binding></span><span class="sxs-lookup"><span data-stu-id="6c482-130">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="6c482-131">カスタム バインドのすべてのバインド機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="6c482-131">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6c482-132">Remarks</span><span class="sxs-lookup"><span data-stu-id="6c482-132">Remarks</span></span>  
 <span data-ttu-id="6c482-133">TCP などのストリーム指向プロトコルおよび名前付きパイプを使用するトランスポートは、ストリーム ベースのトランスポート アップグレードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6c482-133">Transports that use a stream-oriented protocol such as TCP and named pipes support stream-based transport upgrades.</span></span> <span data-ttu-id="6c482-134">特に、WCF にはセキュリティ アップグレードが用意されています。</span><span class="sxs-lookup"><span data-stu-id="6c482-134">Specifically, WCF provides security upgrades.</span></span> <span data-ttu-id="6c482-135">およびこのトランスポート セキュリティの構成がこの構成要素によってカプセル化[ \<sslStreamSecurity >](../../../../../docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md)、構成し、カスタム バインドに追加するには、この</span><span class="sxs-lookup"><span data-stu-id="6c482-135">The configuration of this transport security is encapsulated by this configuration element  as well as by [\<sslStreamSecurity>](../../../../../docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md), which can be configured and added to a custom binding</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c482-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="6c482-136">See Also</span></span>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 <xref:System.ServiceModel.Configuration.WindowsStreamSecurityElement>  
 <xref:System.ServiceModel.Channels.WindowsStreamSecurityBindingElement>  
 [<span data-ttu-id="6c482-137">バインディング</span><span class="sxs-lookup"><span data-stu-id="6c482-137">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="6c482-138">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="6c482-138">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="6c482-139">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="6c482-139">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="6c482-140">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="6c482-140">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
