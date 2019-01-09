---
title: '&lt;netNamedPipeBinding&gt; の &lt;security&gt;'
ms.date: 03/30/2017
ms.assetid: bb3cb022-637e-49fd-92e8-6766038affa7
ms.openlocfilehash: 0079cb9e62abed42a36b67fed935f883473ebbb8
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147825"
---
# <a name="ltsecuritygt-of-ltnetnamedpipebindinggt"></a><span data-ttu-id="53b2f-102">&lt;netNamedPipeBinding&gt; の &lt;security&gt;</span><span class="sxs-lookup"><span data-stu-id="53b2f-102">&lt;security&gt; of &lt;netNamedPipeBinding&gt;</span></span>
<span data-ttu-id="53b2f-103">バインディングのセキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="53b2f-103">Defines the security settings for a binding.</span></span>  
  
 <span data-ttu-id="53b2f-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="53b2f-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="53b2f-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="53b2f-105">\<bindings></span></span>  
<span data-ttu-id="53b2f-106">\<netNamedPipeBinding></span><span class="sxs-lookup"><span data-stu-id="53b2f-106">\<netNamedPipeBinding></span></span>  
<span data-ttu-id="53b2f-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="53b2f-107">\<binding></span></span>  
<span data-ttu-id="53b2f-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="53b2f-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53b2f-109">構文</span><span class="sxs-lookup"><span data-stu-id="53b2f-109">Syntax</span></span>  
  
```xml  
<netNamedPipeBinding>
  <binding>
    <security mode="None/Transport">
      <transport protectionLevel="None/Sign/EncryptAndSign" />
    </security>
  </binding>
</netNamedPipeBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="53b2f-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="53b2f-110">Attributes and Elements</span></span>  
 <span data-ttu-id="53b2f-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="53b2f-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="53b2f-112">属性</span><span class="sxs-lookup"><span data-stu-id="53b2f-112">Attributes</span></span>  
  
|<span data-ttu-id="53b2f-113">属性</span><span class="sxs-lookup"><span data-stu-id="53b2f-113">Attribute</span></span>|<span data-ttu-id="53b2f-114">説明</span><span class="sxs-lookup"><span data-stu-id="53b2f-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="53b2f-115">モード</span><span class="sxs-lookup"><span data-stu-id="53b2f-115">mode</span></span>|<span data-ttu-id="53b2f-116">このバインディングに適用されるセキュリティの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="53b2f-116">Specifies the type of security that is applied to this binding.</span></span> <span data-ttu-id="53b2f-117">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="53b2f-117">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="53b2f-118">-None。これには、セキュリティが無効にします。</span><span class="sxs-lookup"><span data-stu-id="53b2f-118">-   None: This disables security.</span></span><br /><span data-ttu-id="53b2f-119">-トランスポート。基になるトランスポート ベースのセキュリティを使用してセキュリティが提供されます。</span><span class="sxs-lookup"><span data-stu-id="53b2f-119">-   Transport: Security is provided using underlying transport based security.</span></span> <span data-ttu-id="53b2f-120">このモードでの保護レベルを制御できます。</span><span class="sxs-lookup"><span data-stu-id="53b2f-120">It is possible to control the protection level with this mode.</span></span><br /><span data-ttu-id="53b2f-121">-既定値は、トランスポートです。</span><span class="sxs-lookup"><span data-stu-id="53b2f-121">-   The default value is Transport.</span></span> <span data-ttu-id="53b2f-122">この属性は <xref:System.ServiceModel.NetNamedPipeSecurityMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="53b2f-122">This attribute is of type <xref:System.ServiceModel.NetNamedPipeSecurityMode>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="53b2f-123">子要素</span><span class="sxs-lookup"><span data-stu-id="53b2f-123">Child Elements</span></span>  
  
|<span data-ttu-id="53b2f-124">要素</span><span class="sxs-lookup"><span data-stu-id="53b2f-124">Element</span></span>|<span data-ttu-id="53b2f-125">説明</span><span class="sxs-lookup"><span data-stu-id="53b2f-125">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="53b2f-126">transport</span><span class="sxs-lookup"><span data-stu-id="53b2f-126">transport</span></span>|<span data-ttu-id="53b2f-127">トランスポートのセキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="53b2f-127">Defines the security settings for the transport.</span></span> <span data-ttu-id="53b2f-128">この要素は <xref:System.ServiceModel.Configuration.NamedPipeTransportSecurityElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="53b2f-128">This element is of type <xref:System.ServiceModel.Configuration.NamedPipeTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="53b2f-129">親要素</span><span class="sxs-lookup"><span data-stu-id="53b2f-129">Parent Elements</span></span>  
  
|<span data-ttu-id="53b2f-130">要素</span><span class="sxs-lookup"><span data-stu-id="53b2f-130">Element</span></span>|<span data-ttu-id="53b2f-131">説明</span><span class="sxs-lookup"><span data-stu-id="53b2f-131">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="53b2f-132">バインド</span><span class="sxs-lookup"><span data-stu-id="53b2f-132">binding</span></span>|<span data-ttu-id="53b2f-133">バインド要素、 [ \<netNamedPipeBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netnamedpipebinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="53b2f-133">The binding element of the [\<netNamedPipeBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netnamedpipebinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="53b2f-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="53b2f-134">See Also</span></span>  
 <xref:System.ServiceModel.NetNamedPipeSecurity>  
 <xref:System.ServiceModel.NetNamedPipeBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.NetNamedPipeBindingElement.Security%2A>  
 <xref:System.ServiceModel.Configuration.NetNamedPipeSecurityElement>  
 [<span data-ttu-id="53b2f-135">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="53b2f-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="53b2f-136">資格情報の種類の選択</span><span class="sxs-lookup"><span data-stu-id="53b2f-136">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)  
 [<span data-ttu-id="53b2f-137">バインディング</span><span class="sxs-lookup"><span data-stu-id="53b2f-137">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="53b2f-138">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="53b2f-138">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="53b2f-139">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="53b2f-139">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="53b2f-140">\<binding></span><span class="sxs-lookup"><span data-stu-id="53b2f-140">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
