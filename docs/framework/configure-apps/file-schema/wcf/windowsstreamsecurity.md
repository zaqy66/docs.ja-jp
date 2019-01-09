---
title: '&lt;windowsStreamSecurity&gt;'
ms.date: 03/30/2017
ms.assetid: 926bea29-90c7-4a26-9cf0-fb4aa44f6f70
ms.openlocfilehash: 6cce178910767d7fd197aff0d007b7cc3f4e60f3
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151125"
---
# <a name="ltwindowsstreamsecuritygt"></a><span data-ttu-id="0b573-102">&lt;windowsStreamSecurity&gt;</span><span class="sxs-lookup"><span data-stu-id="0b573-102">&lt;windowsStreamSecurity&gt;</span></span>
<span data-ttu-id="0b573-103">カスタム バインドの Windows ストリーム セキュリティ設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b573-103">Specify Windows stream security settings of the custom binding.</span></span>  
  
 <span data-ttu-id="0b573-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="0b573-104">\<system.serviceModel></span></span>  
<span data-ttu-id="0b573-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="0b573-105">\<bindings></span></span>  
<span data-ttu-id="0b573-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="0b573-106">\<customBinding></span></span>  
<span data-ttu-id="0b573-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="0b573-107">\<binding></span></span>  
<span data-ttu-id="0b573-108">\<windowsStreamSecurity ></span><span class="sxs-lookup"><span data-stu-id="0b573-108">\<windowsStreamSecurity></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0b573-109">構文</span><span class="sxs-lookup"><span data-stu-id="0b573-109">Syntax</span></span>  
  
```xml  
<windowsStreamSecurity protectionLevel="None/Sign/EncryptAndSign" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0b573-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="0b573-110">Attributes and Elements</span></span>  
 <span data-ttu-id="0b573-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="0b573-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0b573-112">属性</span><span class="sxs-lookup"><span data-stu-id="0b573-112">Attributes</span></span>  
  
|<span data-ttu-id="0b573-113">属性</span><span class="sxs-lookup"><span data-stu-id="0b573-113">Attribute</span></span>|<span data-ttu-id="0b573-114">説明</span><span class="sxs-lookup"><span data-stu-id="0b573-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0b573-115">protectionLevel</span><span class="sxs-lookup"><span data-stu-id="0b573-115">protectionLevel</span></span>|<span data-ttu-id="0b573-116">メッセージ レベルのセキュリティを定義します。</span><span class="sxs-lookup"><span data-stu-id="0b573-116">Defines message-level security.</span></span> <span data-ttu-id="0b573-117">メッセージに署名すると、転送中のメッセージが第三者によって改ざんされるリスクを軽減します。</span><span class="sxs-lookup"><span data-stu-id="0b573-117">Signing messages mitigates the risk of a third party tampering with the message while it is being transferred.</span></span> <span data-ttu-id="0b573-118">暗号化により、転送中にデータレベルのプライバシーが提供されます。</span><span class="sxs-lookup"><span data-stu-id="0b573-118">Encryption provides data-level privacy during transport.</span></span> <span data-ttu-id="0b573-119">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="0b573-119">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="0b573-120">-None。保護されません。</span><span class="sxs-lookup"><span data-stu-id="0b573-120">-   None: No protection.</span></span><br /><span data-ttu-id="0b573-121">署名:メッセージは署名されます。</span><span class="sxs-lookup"><span data-stu-id="0b573-121">-   Sign: Messages are signed.</span></span><br /><span data-ttu-id="0b573-122">-EncryptAndSign:メッセージに署名および暗号化します。</span><span class="sxs-lookup"><span data-stu-id="0b573-122">-   EncryptAndSign: Messages are signed and encrypted.</span></span><br /><br /> <span data-ttu-id="0b573-123">既定値は EncryptAndSign です。</span><span class="sxs-lookup"><span data-stu-id="0b573-123">The default is EncryptAndSign.</span></span><br /><br /> <span data-ttu-id="0b573-124">この属性は <xref:System.Net.Security.ProtectionLevel> 型です。</span><span class="sxs-lookup"><span data-stu-id="0b573-124">This attribute is of type <xref:System.Net.Security.ProtectionLevel>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0b573-125">子要素</span><span class="sxs-lookup"><span data-stu-id="0b573-125">Child Elements</span></span>  
 <span data-ttu-id="0b573-126">なし</span><span class="sxs-lookup"><span data-stu-id="0b573-126">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0b573-127">親要素</span><span class="sxs-lookup"><span data-stu-id="0b573-127">Parent Elements</span></span>  
  
|<span data-ttu-id="0b573-128">要素</span><span class="sxs-lookup"><span data-stu-id="0b573-128">Element</span></span>|<span data-ttu-id="0b573-129">説明</span><span class="sxs-lookup"><span data-stu-id="0b573-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0b573-130">\<binding></span><span class="sxs-lookup"><span data-stu-id="0b573-130">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="0b573-131">カスタム バインドのすべてのバインド機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="0b573-131">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0b573-132">Remarks</span><span class="sxs-lookup"><span data-stu-id="0b573-132">Remarks</span></span>  
 <span data-ttu-id="0b573-133">TCP などのストリーム指向プロトコルおよび名前付きパイプを使用するトランスポートは、ストリーム ベースのトランスポート アップグレードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="0b573-133">Transports that use a stream-oriented protocol such as TCP and named pipes support stream-based transport upgrades.</span></span> <span data-ttu-id="0b573-134">特に、WCF にはセキュリティ アップグレードが用意されています。</span><span class="sxs-lookup"><span data-stu-id="0b573-134">Specifically, WCF provides security upgrades.</span></span> <span data-ttu-id="0b573-135">およびこのトランスポート セキュリティの構成がこの構成要素によってカプセル化[ \<sslStreamSecurity >](../../../../../docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md)、構成し、カスタム バインドに追加するには、この</span><span class="sxs-lookup"><span data-stu-id="0b573-135">The configuration of this transport security is encapsulated by this configuration element  as well as by [\<sslStreamSecurity>](../../../../../docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md), which can be configured and added to a custom binding</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b573-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="0b573-136">See Also</span></span>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 <xref:System.ServiceModel.Configuration.WindowsStreamSecurityElement>  
 <xref:System.ServiceModel.Channels.WindowsStreamSecurityBindingElement>  
 [<span data-ttu-id="0b573-137">バインディング</span><span class="sxs-lookup"><span data-stu-id="0b573-137">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="0b573-138">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="0b573-138">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="0b573-139">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="0b573-139">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="0b573-140">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="0b573-140">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
