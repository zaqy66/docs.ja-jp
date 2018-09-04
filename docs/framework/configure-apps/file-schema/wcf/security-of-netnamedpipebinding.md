---
title: '&lt;netNamedPipeBinding&gt; の &lt;security&gt;'
ms.date: 03/30/2017
ms.assetid: bb3cb022-637e-49fd-92e8-6766038affa7
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 0e5a22d6e517bc7a05f74089b7c8ece8c8a4bd39
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43558673"
---
# <a name="ltsecuritygt-of-ltnetnamedpipebindinggt"></a><span data-ttu-id="b8066-102">&lt;netNamedPipeBinding&gt; の &lt;security&gt;</span><span class="sxs-lookup"><span data-stu-id="b8066-102">&lt;security&gt; of &lt;netNamedPipeBinding&gt;</span></span>
<span data-ttu-id="b8066-103">バインディングのセキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="b8066-103">Defines the security settings for a binding.</span></span>  
  
 <span data-ttu-id="b8066-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="b8066-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="b8066-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="b8066-105">\<bindings></span></span>  
<span data-ttu-id="b8066-106">\<netNamedPipeBinding></span><span class="sxs-lookup"><span data-stu-id="b8066-106">\<netNamedPipeBinding></span></span>  
<span data-ttu-id="b8066-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="b8066-107">\<binding></span></span>  
<span data-ttu-id="b8066-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="b8066-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b8066-109">構文</span><span class="sxs-lookup"><span data-stu-id="b8066-109">Syntax</span></span>  
  
```xml  
<netNamedPipeBinding>  
      <binding>  
            <security mode="None/Transport">  
                        <transport protectionLevel="None/Sign/EncryptAndSign" />  
            </security>  
      </binding>  
</netNamedPipeBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b8066-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="b8066-110">Attributes and Elements</span></span>  
 <span data-ttu-id="b8066-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="b8066-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b8066-112">属性</span><span class="sxs-lookup"><span data-stu-id="b8066-112">Attributes</span></span>  
  
|<span data-ttu-id="b8066-113">属性</span><span class="sxs-lookup"><span data-stu-id="b8066-113">Attribute</span></span>|<span data-ttu-id="b8066-114">説明</span><span class="sxs-lookup"><span data-stu-id="b8066-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b8066-115">モード</span><span class="sxs-lookup"><span data-stu-id="b8066-115">mode</span></span>|<span data-ttu-id="b8066-116">このバインディングに適用されるセキュリティの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="b8066-116">Specifies the type of security that is applied to this binding.</span></span> <span data-ttu-id="b8066-117">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="b8066-117">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="b8066-118">-None。 こうとセキュリティ。</span><span class="sxs-lookup"><span data-stu-id="b8066-118">-   None: This disables security.</span></span><br /><span data-ttu-id="b8066-119">-トランスポート: 基になるトランスポート ベースのセキュリティを使用してセキュリティが提供されます。</span><span class="sxs-lookup"><span data-stu-id="b8066-119">-   Transport: Security is provided using underlying transport based security.</span></span> <span data-ttu-id="b8066-120">このモードでの保護レベルを制御できます。</span><span class="sxs-lookup"><span data-stu-id="b8066-120">It is possible to control the protection level with this mode.</span></span><br /><span data-ttu-id="b8066-121">-既定値は、トランスポートです。</span><span class="sxs-lookup"><span data-stu-id="b8066-121">-   The default value is Transport.</span></span> <span data-ttu-id="b8066-122">この属性は <xref:System.ServiceModel.NetNamedPipeSecurityMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="b8066-122">This attribute is of type <xref:System.ServiceModel.NetNamedPipeSecurityMode>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b8066-123">子要素</span><span class="sxs-lookup"><span data-stu-id="b8066-123">Child Elements</span></span>  
  
|<span data-ttu-id="b8066-124">要素</span><span class="sxs-lookup"><span data-stu-id="b8066-124">Element</span></span>|<span data-ttu-id="b8066-125">説明</span><span class="sxs-lookup"><span data-stu-id="b8066-125">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b8066-126">transport</span><span class="sxs-lookup"><span data-stu-id="b8066-126">transport</span></span>|<span data-ttu-id="b8066-127">トランスポートのセキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="b8066-127">Defines the security settings for the transport.</span></span> <span data-ttu-id="b8066-128">この要素は <xref:System.ServiceModel.Configuration.NamedPipeTransportSecurityElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="b8066-128">This element is of type <xref:System.ServiceModel.Configuration.NamedPipeTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b8066-129">親要素</span><span class="sxs-lookup"><span data-stu-id="b8066-129">Parent Elements</span></span>  
  
|<span data-ttu-id="b8066-130">要素</span><span class="sxs-lookup"><span data-stu-id="b8066-130">Element</span></span>|<span data-ttu-id="b8066-131">説明</span><span class="sxs-lookup"><span data-stu-id="b8066-131">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b8066-132">バインド</span><span class="sxs-lookup"><span data-stu-id="b8066-132">binding</span></span>|<span data-ttu-id="b8066-133">バインド要素、 [ \<netNamedPipeBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netnamedpipebinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="b8066-133">The binding element of the [\<netNamedPipeBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netnamedpipebinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b8066-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="b8066-134">See Also</span></span>  
 <xref:System.ServiceModel.NetNamedPipeSecurity>  
 <xref:System.ServiceModel.NetNamedPipeBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.NetNamedPipeBindingElement.Security%2A>  
 <xref:System.ServiceModel.Configuration.NetNamedPipeSecurityElement>  
 [<span data-ttu-id="b8066-135">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="b8066-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="b8066-136">資格情報の種類の選択</span><span class="sxs-lookup"><span data-stu-id="b8066-136">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)  
 [<span data-ttu-id="b8066-137">バインディング</span><span class="sxs-lookup"><span data-stu-id="b8066-137">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="b8066-138">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="b8066-138">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="b8066-139">バインドを使用して、Windows Communication Foundation サービスとクライアントを構成するには</span><span class="sxs-lookup"><span data-stu-id="b8066-139">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="b8066-140">\<binding></span><span class="sxs-lookup"><span data-stu-id="b8066-140">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
