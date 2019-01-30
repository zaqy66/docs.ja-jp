---
title: <security> の <wsDualHttpBinding>
ms.date: 03/30/2017
ms.assetid: 869c05e7-4ebe-467d-95ab-c8f8de4e6b9e
ms.openlocfilehash: 8bc35b3bc8f0cbe1a51ceab63d876d5859d6b325
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55270855"
---
# <a name="security-of-wsdualhttpbinding"></a><span data-ttu-id="f6afd-102">\<セキュリティ > の\<wsDualHttpBinding ></span><span class="sxs-lookup"><span data-stu-id="f6afd-102">\<security> of \<wsDualHttpBinding></span></span>
<span data-ttu-id="f6afd-103">セキュリティ機能を定義、 [ \<wsDualHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="f6afd-103">Defines the security capabilities of the [\<wsDualHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md).</span></span>  
  
 <span data-ttu-id="f6afd-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="f6afd-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="f6afd-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="f6afd-105">\<bindings></span></span>  
<span data-ttu-id="f6afd-106">\<wsDualHttpBinding ></span><span class="sxs-lookup"><span data-stu-id="f6afd-106">\<wsDualHttpBinding></span></span>  
<span data-ttu-id="f6afd-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="f6afd-107">\<binding></span></span>  
<span data-ttu-id="f6afd-108">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="f6afd-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6afd-109">構文</span><span class="sxs-lookup"><span data-stu-id="f6afd-109">Syntax</span></span>  
  
```xml  
<security mode="Message/None">
  <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
           clientCredentialType="Certificate/IssuedToken/None/UserName/Windows"
           negotiateServiceCredential="Boolean"/>
</security>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f6afd-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="f6afd-110">Attributes and Elements</span></span>  
 <span data-ttu-id="f6afd-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="f6afd-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f6afd-112">属性</span><span class="sxs-lookup"><span data-stu-id="f6afd-112">Attributes</span></span>  
  
|<span data-ttu-id="f6afd-113">属性</span><span class="sxs-lookup"><span data-stu-id="f6afd-113">Attribute</span></span>|<span data-ttu-id="f6afd-114">説明</span><span class="sxs-lookup"><span data-stu-id="f6afd-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f6afd-115">モード</span><span class="sxs-lookup"><span data-stu-id="f6afd-115">mode</span></span>|<span data-ttu-id="f6afd-116">-省略可能。</span><span class="sxs-lookup"><span data-stu-id="f6afd-116">-   Optional.</span></span> <span data-ttu-id="f6afd-117">適用するセキュリティの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="f6afd-117">Specifies the type of security that is applied.</span></span> <span data-ttu-id="f6afd-118">既定値は `Message` です。</span><span class="sxs-lookup"><span data-stu-id="f6afd-118">The default value is `Message`.</span></span> <span data-ttu-id="f6afd-119">この属性は <xref:System.ServiceModel.WSDualHttpSecurityMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="f6afd-119">This attribute is of type <xref:System.ServiceModel.WSDualHttpSecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="f6afd-120">Mode 属性</span><span class="sxs-lookup"><span data-stu-id="f6afd-120">Mode Attribute</span></span>  
  
|<span data-ttu-id="f6afd-121">値</span><span class="sxs-lookup"><span data-stu-id="f6afd-121">Value</span></span>|<span data-ttu-id="f6afd-122">説明</span><span class="sxs-lookup"><span data-stu-id="f6afd-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="f6afd-123">なし</span><span class="sxs-lookup"><span data-stu-id="f6afd-123">None</span></span>|<span data-ttu-id="f6afd-124">セキュリティを無効にします。</span><span class="sxs-lookup"><span data-stu-id="f6afd-124">Security is disabled.</span></span>|  
|<span data-ttu-id="f6afd-125">メッセージ</span><span class="sxs-lookup"><span data-stu-id="f6afd-125">Message</span></span>|<span data-ttu-id="f6afd-126">セキュリティは、SOAP メッセージ セキュリティを使用して確保されます。</span><span class="sxs-lookup"><span data-stu-id="f6afd-126">Security is provided using SOAP message security.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f6afd-127">子要素</span><span class="sxs-lookup"><span data-stu-id="f6afd-127">Child Elements</span></span>  
  
|<span data-ttu-id="f6afd-128">要素</span><span class="sxs-lookup"><span data-stu-id="f6afd-128">Element</span></span>|<span data-ttu-id="f6afd-129">説明</span><span class="sxs-lookup"><span data-stu-id="f6afd-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f6afd-130">\<message></span><span class="sxs-lookup"><span data-stu-id="f6afd-130">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-of-wsdualhttpbinding.md)|<span data-ttu-id="f6afd-131">メッセージ レベル セキュリティの設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="f6afd-131">Defines the settings for the message-level security.</span></span> <span data-ttu-id="f6afd-132">この要素は <xref:System.ServiceModel.MessageSecurityOverHttp> 型です。</span><span class="sxs-lookup"><span data-stu-id="f6afd-132">This element is of type <xref:System.ServiceModel.MessageSecurityOverHttp>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f6afd-133">親要素</span><span class="sxs-lookup"><span data-stu-id="f6afd-133">Parent Elements</span></span>  
  
|<span data-ttu-id="f6afd-134">要素</span><span class="sxs-lookup"><span data-stu-id="f6afd-134">Element</span></span>|<span data-ttu-id="f6afd-135">説明</span><span class="sxs-lookup"><span data-stu-id="f6afd-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f6afd-136">\<binding></span><span class="sxs-lookup"><span data-stu-id="f6afd-136">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="f6afd-137">すべてのバインド機能を定義、 [ \<wsDualHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md)します。</span><span class="sxs-lookup"><span data-stu-id="f6afd-137">Defines all binding capabilities of the [\<wsDualHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f6afd-138">Remarks</span><span class="sxs-lookup"><span data-stu-id="f6afd-138">Remarks</span></span>  
 <span data-ttu-id="f6afd-139">二重バインディングでは、クライアントの IP アドレスをサービスに公開します。</span><span class="sxs-lookup"><span data-stu-id="f6afd-139">A dual binding exposes the IP address of the client to the service.</span></span> <span data-ttu-id="f6afd-140">クライアントは、セキュリティを使用して信頼するサービスに対して接続のみを可能にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6afd-140">The client should use security to ensure that it only connects to services it trusts.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6afd-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6afd-141">See also</span></span>
- <xref:System.ServiceModel.WSDualHttpSecurity>
- <xref:System.ServiceModel.BasicHttpSecurity>
- [<span data-ttu-id="f6afd-142">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="f6afd-142">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="f6afd-143">バインディング</span><span class="sxs-lookup"><span data-stu-id="f6afd-143">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="f6afd-144">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="f6afd-144">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="f6afd-145">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="f6afd-145">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="f6afd-146">\<binding></span><span class="sxs-lookup"><span data-stu-id="f6afd-146">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
