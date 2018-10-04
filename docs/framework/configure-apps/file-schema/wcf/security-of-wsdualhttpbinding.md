---
title: '&lt;wsDualHttpBinding&gt; の &lt;security&gt;'
ms.date: 03/30/2017
ms.assetid: 869c05e7-4ebe-467d-95ab-c8f8de4e6b9e
author: BrucePerlerMS
ms.openlocfilehash: 761eb9d111630d64d0fe4450c7a8950a8181366d
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "48776540"
---
# <a name="ltsecuritygt-of-ltwsdualhttpbindinggt"></a><span data-ttu-id="795d5-102">&lt;wsDualHttpBinding&gt; の &lt;security&gt;</span><span class="sxs-lookup"><span data-stu-id="795d5-102">&lt;security&gt; of &lt;wsDualHttpBinding&gt;</span></span>
<span data-ttu-id="795d5-103">セキュリティ機能を定義、 [ \<wsDualHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="795d5-103">Defines the security capabilities of the [\<wsDualHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md).</span></span>  
  
 <span data-ttu-id="795d5-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="795d5-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="795d5-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="795d5-105">\<bindings></span></span>  
<span data-ttu-id="795d5-106">\<wsDualHttpBinding ></span><span class="sxs-lookup"><span data-stu-id="795d5-106">\<wsDualHttpBinding></span></span>  
<span data-ttu-id="795d5-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="795d5-107">\<binding></span></span>  
<span data-ttu-id="795d5-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="795d5-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="795d5-109">構文</span><span class="sxs-lookup"><span data-stu-id="795d5-109">Syntax</span></span>  
  
```xml  
<security mode="Message/None">  
   <message  
      algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
      clientCredentialType="Certificate/IssuedToken/None/UserName/Windows"  
      negotiateServiceCredential="Boolean"/>  
</security>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="795d5-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="795d5-110">Attributes and Elements</span></span>  
 <span data-ttu-id="795d5-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="795d5-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="795d5-112">属性</span><span class="sxs-lookup"><span data-stu-id="795d5-112">Attributes</span></span>  
  
|<span data-ttu-id="795d5-113">属性</span><span class="sxs-lookup"><span data-stu-id="795d5-113">Attribute</span></span>|<span data-ttu-id="795d5-114">説明</span><span class="sxs-lookup"><span data-stu-id="795d5-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="795d5-115">モード</span><span class="sxs-lookup"><span data-stu-id="795d5-115">mode</span></span>|<span data-ttu-id="795d5-116">-省略可能。</span><span class="sxs-lookup"><span data-stu-id="795d5-116">-   Optional.</span></span> <span data-ttu-id="795d5-117">適用するセキュリティの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="795d5-117">Specifies the type of security that is applied.</span></span> <span data-ttu-id="795d5-118">既定値は `Message` です。</span><span class="sxs-lookup"><span data-stu-id="795d5-118">The default value is `Message`.</span></span> <span data-ttu-id="795d5-119">この属性は <xref:System.ServiceModel.WSDualHttpSecurityMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="795d5-119">This attribute is of type <xref:System.ServiceModel.WSDualHttpSecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="795d5-120">Mode 属性</span><span class="sxs-lookup"><span data-stu-id="795d5-120">Mode Attribute</span></span>  
  
|<span data-ttu-id="795d5-121">値</span><span class="sxs-lookup"><span data-stu-id="795d5-121">Value</span></span>|<span data-ttu-id="795d5-122">説明</span><span class="sxs-lookup"><span data-stu-id="795d5-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="795d5-123">なし</span><span class="sxs-lookup"><span data-stu-id="795d5-123">None</span></span>|<span data-ttu-id="795d5-124">セキュリティを無効にします。</span><span class="sxs-lookup"><span data-stu-id="795d5-124">Security is disabled.</span></span>|  
|<span data-ttu-id="795d5-125">メッセージ</span><span class="sxs-lookup"><span data-stu-id="795d5-125">Message</span></span>|<span data-ttu-id="795d5-126">セキュリティは、SOAP メッセージ セキュリティを使用して確保されます。</span><span class="sxs-lookup"><span data-stu-id="795d5-126">Security is provided using SOAP message security.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="795d5-127">子要素</span><span class="sxs-lookup"><span data-stu-id="795d5-127">Child Elements</span></span>  
  
|<span data-ttu-id="795d5-128">要素</span><span class="sxs-lookup"><span data-stu-id="795d5-128">Element</span></span>|<span data-ttu-id="795d5-129">説明</span><span class="sxs-lookup"><span data-stu-id="795d5-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="795d5-130">\<message></span><span class="sxs-lookup"><span data-stu-id="795d5-130">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-of-wsdualhttpbinding.md)|<span data-ttu-id="795d5-131">メッセージ レベル セキュリティの設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="795d5-131">Defines the settings for the message-level security.</span></span> <span data-ttu-id="795d5-132">この要素は <xref:System.ServiceModel.MessageSecurityOverHttp> 型です。</span><span class="sxs-lookup"><span data-stu-id="795d5-132">This element is of type <xref:System.ServiceModel.MessageSecurityOverHttp>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="795d5-133">親要素</span><span class="sxs-lookup"><span data-stu-id="795d5-133">Parent Elements</span></span>  
  
|<span data-ttu-id="795d5-134">要素</span><span class="sxs-lookup"><span data-stu-id="795d5-134">Element</span></span>|<span data-ttu-id="795d5-135">説明</span><span class="sxs-lookup"><span data-stu-id="795d5-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="795d5-136">\<binding></span><span class="sxs-lookup"><span data-stu-id="795d5-136">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="795d5-137">すべてのバインド機能を定義、 [ \<wsDualHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="795d5-137">Defines all binding capabilities of the [\<wsDualHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="795d5-138">Remarks</span><span class="sxs-lookup"><span data-stu-id="795d5-138">Remarks</span></span>  
 <span data-ttu-id="795d5-139">二重バインディングでは、クライアントの IP アドレスをサービスに公開します。</span><span class="sxs-lookup"><span data-stu-id="795d5-139">A dual binding exposes the IP address of the client to the service.</span></span> <span data-ttu-id="795d5-140">クライアントは、セキュリティを使用して信頼するサービスに対して接続のみを可能にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="795d5-140">The client should use security to ensure that it only connects to services it trusts.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="795d5-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="795d5-141">See Also</span></span>  
 <xref:System.ServiceModel.WSDualHttpSecurity>  
 <xref:System.ServiceModel.BasicHttpSecurity>  
 [<span data-ttu-id="795d5-142">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="795d5-142">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="795d5-143">バインディング</span><span class="sxs-lookup"><span data-stu-id="795d5-143">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="795d5-144">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="795d5-144">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="795d5-145">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="795d5-145">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="795d5-146">\<binding></span><span class="sxs-lookup"><span data-stu-id="795d5-146">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
