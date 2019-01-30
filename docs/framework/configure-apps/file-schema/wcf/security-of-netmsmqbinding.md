---
title: <security> の <netMsmqBinding>
ms.date: 03/30/2017
ms.assetid: 001d11a9-7439-498c-b09d-fca20eaf8cd3
ms.openlocfilehash: bb509bb0c4f7192aefbb51a98042f3f359969321
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55272618"
---
# <a name="security-of-netmsmqbinding"></a><span data-ttu-id="adfe8-102">\<セキュリティ > の\<netMsmqBinding ></span><span class="sxs-lookup"><span data-stu-id="adfe8-102">\<security> of \<netMsmqBinding></span></span>
<span data-ttu-id="adfe8-103">MSMQ バインディングのセキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="adfe8-103">Defines the security settings for a MSMQ binding.</span></span> <span data-ttu-id="adfe8-104">トランスポートまたは SOAP セキュリティが有効であるかどうか、および有効である場合は、どの認証モードと保護レベルを使用するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="adfe8-104">It specifies whether transport or SOAP security is enabled and, if so, what authentication mode and protection levels are in use.</span></span>  
  
 <span data-ttu-id="adfe8-105">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="adfe8-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="adfe8-106">\<bindings></span><span class="sxs-lookup"><span data-stu-id="adfe8-106">\<bindings></span></span>  
<span data-ttu-id="adfe8-107">\<netMsmqBinding></span><span class="sxs-lookup"><span data-stu-id="adfe8-107">\<netMsmqBinding></span></span>  
<span data-ttu-id="adfe8-108">\<binding></span><span class="sxs-lookup"><span data-stu-id="adfe8-108">\<binding></span></span>  
<span data-ttu-id="adfe8-109">\<セキュリティ ></span><span class="sxs-lookup"><span data-stu-id="adfe8-109">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="adfe8-110">構文</span><span class="sxs-lookup"><span data-stu-id="adfe8-110">Syntax</span></span>  
  
```xml  
<security mode="None/Transport/Message/Both">
  <transport msmqAuthenticationMode="None/WindowsDomain/Certificate"
             msmqEncryptionAlgorithm="RC4Stream/AES"
             msmqProtectionLevel="None/Sign/EncryptAndSign"
             msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />
    <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
             clientCredentialType="None/Windows/UserName/Certificate/CardSpace" />
</security>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="adfe8-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="adfe8-111">Attributes and Elements</span></span>  
 <span data-ttu-id="adfe8-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="adfe8-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="adfe8-113">属性</span><span class="sxs-lookup"><span data-stu-id="adfe8-113">Attributes</span></span>  
  
|<span data-ttu-id="adfe8-114">属性</span><span class="sxs-lookup"><span data-stu-id="adfe8-114">Attribute</span></span>|<span data-ttu-id="adfe8-115">説明</span><span class="sxs-lookup"><span data-stu-id="adfe8-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="adfe8-116">モード</span><span class="sxs-lookup"><span data-stu-id="adfe8-116">mode</span></span>|<span data-ttu-id="adfe8-117">整合性、機密性、および認証を制御するセキュリティの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="adfe8-117">Specifies the type of security that controls integrity, confidentiality and authentication.</span></span> <span data-ttu-id="adfe8-118">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="adfe8-118">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="adfe8-119">-None。これには、セキュリティが無効にします。</span><span class="sxs-lookup"><span data-stu-id="adfe8-119">-   None: This disables security.</span></span><br /><span data-ttu-id="adfe8-120">-トランスポート。保護と認証はトランスポートによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="adfe8-120">-   Transport: Protection and authentication are offered by the transport.</span></span> <span data-ttu-id="adfe8-121">これは、2 つのキュー マネージャー間のメッセージ セキュリティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="adfe8-121">This applies to the message security between the two queue managers.</span></span> <span data-ttu-id="adfe8-122">アプリケーションとキュー マネージャーとの間にセキュリティは提供されません。</span><span class="sxs-lookup"><span data-stu-id="adfe8-122">There is no security offered between the application and queue manager.</span></span> <span data-ttu-id="adfe8-123">既存の Msmq アプリケーションは、この種類のセキュリティ モードと機能的に等価です。</span><span class="sxs-lookup"><span data-stu-id="adfe8-123">Existing Msmq applications are functionally equivalent with this type of security mode.</span></span><br /><span data-ttu-id="adfe8-124">-メッセージ:エンド ツー エンド アプリケーションのセキュリティを指定します。</span><span class="sxs-lookup"><span data-stu-id="adfe8-124">-   Message: Specifies end-end application security.</span></span> <span data-ttu-id="adfe8-125">トランスポート層で提供されるセキュリティありません。</span><span class="sxs-lookup"><span data-stu-id="adfe8-125">There is no security offered at the transport layer.</span></span> <span data-ttu-id="adfe8-126">これは、他の標準バインディングによって提供されたセキュリティと同様です。</span><span class="sxs-lookup"><span data-stu-id="adfe8-126">This is similar to the security offered by other standard bindings.</span></span><br /><span data-ttu-id="adfe8-127">-両方。トランスポートと SOAP メッセージング層の両方でセキュリティを提供します。</span><span class="sxs-lookup"><span data-stu-id="adfe8-127">-   Both: Offers security at both the transport and SOAP messaging layer.</span></span> <span data-ttu-id="adfe8-128">同じ資格情報が、両方のレベルで要求されます。</span><span class="sxs-lookup"><span data-stu-id="adfe8-128">The same credential is required at both the levels.</span></span><br /><br /> <span data-ttu-id="adfe8-129">既定値は、Transport です。</span><span class="sxs-lookup"><span data-stu-id="adfe8-129">The default value is Transport.</span></span> <span data-ttu-id="adfe8-130">この属性は <xref:System.ServiceModel.NetMsmqSecurityMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="adfe8-130">This attribute is of type <xref:System.ServiceModel.NetMsmqSecurityMode>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="adfe8-131">子要素</span><span class="sxs-lookup"><span data-stu-id="adfe8-131">Child Elements</span></span>  
  
|<span data-ttu-id="adfe8-132">要素</span><span class="sxs-lookup"><span data-stu-id="adfe8-132">Element</span></span>|<span data-ttu-id="adfe8-133">説明</span><span class="sxs-lookup"><span data-stu-id="adfe8-133">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="adfe8-134">\<message></span><span class="sxs-lookup"><span data-stu-id="adfe8-134">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-of-netmsmqbinding.md)|<span data-ttu-id="adfe8-135">SOAP メッセージのセキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="adfe8-135">Defines the SOAP message security settings.</span></span> <span data-ttu-id="adfe8-136">この要素は <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="adfe8-136">This element is of type <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement>.</span></span>|  
|[<span data-ttu-id="adfe8-137">\<transport></span><span class="sxs-lookup"><span data-stu-id="adfe8-137">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-netmsmqbinding.md)|<span data-ttu-id="adfe8-138">MSMQ トランスポートのセキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="adfe8-138">Defines the security settings for the MSMQ transport.</span></span> <span data-ttu-id="adfe8-139">この要素は <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement> 型です。</span><span class="sxs-lookup"><span data-stu-id="adfe8-139">This element is of type <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="adfe8-140">親要素</span><span class="sxs-lookup"><span data-stu-id="adfe8-140">Parent Elements</span></span>  
  
|<span data-ttu-id="adfe8-141">要素</span><span class="sxs-lookup"><span data-stu-id="adfe8-141">Element</span></span>|<span data-ttu-id="adfe8-142">説明</span><span class="sxs-lookup"><span data-stu-id="adfe8-142">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="adfe8-143">バインド</span><span class="sxs-lookup"><span data-stu-id="adfe8-143">binding</span></span>|<span data-ttu-id="adfe8-144">バインド要素、 [ \<netMsmqBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netmsmqbinding.md)</span><span class="sxs-lookup"><span data-stu-id="adfe8-144">The binding element of the [\<netMsmqBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netmsmqbinding.md)</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="adfe8-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="adfe8-145">See also</span></span>
- <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement>
- <xref:System.ServiceModel.NetMsmqBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.NetMsmqBindingElement.Security%2A>
- <xref:System.ServiceModel.NetMsmqSecurity>
- [<span data-ttu-id="adfe8-146">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="adfe8-146">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="adfe8-147">バインディング</span><span class="sxs-lookup"><span data-stu-id="adfe8-147">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="adfe8-148">システムが提供するバインディングの構成</span><span class="sxs-lookup"><span data-stu-id="adfe8-148">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="adfe8-149">サービスとクライアントを構成するためのバインディングの使用</span><span class="sxs-lookup"><span data-stu-id="adfe8-149">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="adfe8-150">\<binding></span><span class="sxs-lookup"><span data-stu-id="adfe8-150">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
- [<span data-ttu-id="adfe8-151">WCF のキュー</span><span class="sxs-lookup"><span data-stu-id="adfe8-151">Queues in WCF</span></span>](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)
