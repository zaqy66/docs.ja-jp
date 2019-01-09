---
title: '&lt;msmqTransportSecurity&gt;'
ms.date: 03/30/2017
ms.assetid: 092e911b-ab1b-4069-a26e-6134c3299e06
ms.openlocfilehash: 6ed7402ac7ec50a98b7d685813448edb173266d9
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151996"
---
# <a name="ltmsmqtransportsecuritygt"></a><span data-ttu-id="f2982-102">&lt;msmqTransportSecurity&gt;</span><span class="sxs-lookup"><span data-stu-id="f2982-102">&lt;msmqTransportSecurity&gt;</span></span>
<span data-ttu-id="f2982-103">カスタム バインドの MSMQ トランスポート セキュリティ設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="f2982-103">Specifies MSMQ transport security settings for a custom binding.</span></span>  
  
 <span data-ttu-id="f2982-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="f2982-104">\<system.serviceModel></span></span>  
<span data-ttu-id="f2982-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="f2982-105">\<bindings></span></span>  
<span data-ttu-id="f2982-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="f2982-106">\<customBinding></span></span>  
<span data-ttu-id="f2982-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="f2982-107">\<binding></span></span>  
<span data-ttu-id="f2982-108">\<msmqIntegration ></span><span class="sxs-lookup"><span data-stu-id="f2982-108">\<msmqIntegration></span></span>  
<span data-ttu-id="f2982-109">\<msmqTransportSecurity ></span><span class="sxs-lookup"><span data-stu-id="f2982-109">\<msmqTransportSecurity></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2982-110">構文</span><span class="sxs-lookup"><span data-stu-id="f2982-110">Syntax</span></span>  
  
```xml  
<msmqTransportSecurity msmqAuthenticationMode="None/Windows/Certificate"
                       msmqEncryptionAlgorithm="RC4Stream/AES"
                       msmqProtectionLevel="None/Sign/EncryptAndSign"
                       msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />
</msmqTransportSecurity>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f2982-111">属性および要素</span><span class="sxs-lookup"><span data-stu-id="f2982-111">Attributes and Elements</span></span>  
 <span data-ttu-id="f2982-112">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="f2982-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f2982-113">属性</span><span class="sxs-lookup"><span data-stu-id="f2982-113">Attributes</span></span>  
  
|<span data-ttu-id="f2982-114">属性</span><span class="sxs-lookup"><span data-stu-id="f2982-114">Attribute</span></span>|<span data-ttu-id="f2982-115">説明</span><span class="sxs-lookup"><span data-stu-id="f2982-115">Description</span></span>|  
|---------------|-----------------|  
|`msmqAuthenticationMode`|<span data-ttu-id="f2982-116">MSMQ トランスポートによるメッセージの認証方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="f2982-116">Specifies how the message must be authenticated by the MSMQ transport.</span></span> <span data-ttu-id="f2982-117">これが `None` に設定されている場合、`msmqProtectionLevel` 属性の値も `None` に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2982-117">If this is set to `None`, the value of the `msmqProtectionLevel` attribute must also be set to `None`.</span></span><br /><br /> <span data-ttu-id="f2982-118">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="f2982-118">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="f2982-119">-None。認証はありません。</span><span class="sxs-lookup"><span data-stu-id="f2982-119">-   None: No authentication.</span></span><br /><span data-ttu-id="f2982-120">-Windows:認証メカニズムでは、Active Directory を使用して、メッセージに関連付けられている SID の X.509 証明書を取得します。</span><span class="sxs-lookup"><span data-stu-id="f2982-120">-   Windows: The authentication mechanism uses Active Directory to get the X.509 certificate for the SID associated with the message.</span></span> <span data-ttu-id="f2982-121">次に、これを使用してキューの ACL がチェックされ、ユーザーがキューに書き込む権限を持っていることが確認されます。</span><span class="sxs-lookup"><span data-stu-id="f2982-121">This is then used to check the ACL of the queue to ensure the user has permission to write to the queue.</span></span><br /><span data-ttu-id="f2982-122">-証明書:チャネルは、証明書ストアから証明書を取得します。</span><span class="sxs-lookup"><span data-stu-id="f2982-122">-   Certificate: The channel gets the certificate from the certificate store.</span></span><br /><br /> <span data-ttu-id="f2982-123">既定値は Windows です。</span><span class="sxs-lookup"><span data-stu-id="f2982-123">The default value is Windows.</span></span> <span data-ttu-id="f2982-124">この属性は <xref:System.ServiceModel.MsmqAuthenticationMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="f2982-124">This attribute is of type <xref:System.ServiceModel.MsmqAuthenticationMode>.</span></span>|  
|`msmqEncryptionAlgorithm`|<span data-ttu-id="f2982-125">メッセージ キュー マネージャー間でメッセージを転送するときに、ネットワーク上でメッセージの暗号化に使用されるアルゴリズムを指定します。</span><span class="sxs-lookup"><span data-stu-id="f2982-125">Specifies the algorithm to be used for message encryption on the wire when transferring messages between message queue managers.</span></span> <span data-ttu-id="f2982-126">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="f2982-126">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="f2982-127">-[Rc4stream]</span><span class="sxs-lookup"><span data-stu-id="f2982-127">-   RC4Stream</span></span><br /><span data-ttu-id="f2982-128">-AES</span><span class="sxs-lookup"><span data-stu-id="f2982-128">-   AES</span></span><br /><br /> <span data-ttu-id="f2982-129">既定値は RC4Stream です。</span><span class="sxs-lookup"><span data-stu-id="f2982-129">The default value is RC4Stream.</span></span> <span data-ttu-id="f2982-130">この属性は <xref:System.ServiceModel.MsmqEncryptionAlgorithm> 型です。</span><span class="sxs-lookup"><span data-stu-id="f2982-130">This attribute is of type <xref:System.ServiceModel.MsmqEncryptionAlgorithm>.</span></span>|  
|`msmqProtectionLevel`|<span data-ttu-id="f2982-131">MSMQ トランスポートのレベルでメッセージをセキュリティで保護する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="f2982-131">Specifies how the message is secured at the level of the MSMQ transport.</span></span> <span data-ttu-id="f2982-132">暗号化を行うとメッセージの整合性が確保されますが、EncryptAndSign を使用するとメッセージの整合性と否認防止の両方が確保されます。つまり、メッセージは本当にその送信者から送信されていることになり、記載されている送信者が実際の送信者になります。</span><span class="sxs-lookup"><span data-stu-id="f2982-132">Encryption ensures message integrity while EncryptAndSign ensures both message integrity and non-repudiation; that is, the message indeed comes from the sender and the sender is who he says he is.</span></span> <span data-ttu-id="f2982-133">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="f2982-133">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="f2982-134">-None。保護されません。</span><span class="sxs-lookup"><span data-stu-id="f2982-134">-   None: No protection.</span></span><br /><span data-ttu-id="f2982-135">署名:メッセージは署名されます。</span><span class="sxs-lookup"><span data-stu-id="f2982-135">-   Sign: Messages are signed.</span></span><br /><span data-ttu-id="f2982-136">-EncryptAndSign:メッセージは暗号化および署名されます。</span><span class="sxs-lookup"><span data-stu-id="f2982-136">-   EncryptAndSign: Messages are encrypted and signed.</span></span><br /><br /> <span data-ttu-id="f2982-137">既定値は Sign です。</span><span class="sxs-lookup"><span data-stu-id="f2982-137">The default value is Sign.</span></span> <span data-ttu-id="f2982-138">この属性は <xref:System.Net.Security.ProtectionLevel> 型です。</span><span class="sxs-lookup"><span data-stu-id="f2982-138">This attribute is of type <xref:System.Net.Security.ProtectionLevel>.</span></span>|  
|`msmqSecureHashAlgorithm`|<span data-ttu-id="f2982-139">署名の一部としてダイジェストの計算に使用されるアルゴリズムを指定します。</span><span class="sxs-lookup"><span data-stu-id="f2982-139">Specifies the algorithm to be used in computing the digest as part of signatures.</span></span> <span data-ttu-id="f2982-140">以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="f2982-140">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="f2982-141">-   MD5</span><span class="sxs-lookup"><span data-stu-id="f2982-141">-   MD5</span></span><br /><span data-ttu-id="f2982-142">-SHA1</span><span class="sxs-lookup"><span data-stu-id="f2982-142">-   SHA1</span></span><br /><span data-ttu-id="f2982-143">-   SHA256</span><span class="sxs-lookup"><span data-stu-id="f2982-143">-   SHA256</span></span><br /><span data-ttu-id="f2982-144">-SHA512</span><span class="sxs-lookup"><span data-stu-id="f2982-144">-   SHA512</span></span><br /><br /> <span data-ttu-id="f2982-145">既定値は SHA1 です。</span><span class="sxs-lookup"><span data-stu-id="f2982-145">The default value is SHA1.</span></span> <span data-ttu-id="f2982-146">この属性は <xref:System.ServiceModel.MsmqSecureHashAlgorithm> 型です。</span><span class="sxs-lookup"><span data-stu-id="f2982-146">This attribute is of type <xref:System.ServiceModel.MsmqSecureHashAlgorithm>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f2982-147">子要素</span><span class="sxs-lookup"><span data-stu-id="f2982-147">Child Elements</span></span>  
 <span data-ttu-id="f2982-148">なし。</span><span class="sxs-lookup"><span data-stu-id="f2982-148">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f2982-149">親要素</span><span class="sxs-lookup"><span data-stu-id="f2982-149">Parent Elements</span></span>  
  
|<span data-ttu-id="f2982-150">要素</span><span class="sxs-lookup"><span data-stu-id="f2982-150">Element</span></span>|<span data-ttu-id="f2982-151">説明</span><span class="sxs-lookup"><span data-stu-id="f2982-151">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f2982-152">\<msmqIntegration ></span><span class="sxs-lookup"><span data-stu-id="f2982-152">\<msmqIntegration></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/msmqintegration.md)|<span data-ttu-id="f2982-153">Message Queuing (MSMQ) の送信側または受信側とのやり取りに必要な設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="f2982-153">Specifies settings required for interaction with a Message Queuing (MSMQ) sender or receiver.</span></span>|  
|[<span data-ttu-id="f2982-154">\<msmqTransport ></span><span class="sxs-lookup"><span data-stu-id="f2982-154">\<msmqTransport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/msmqtransport.md)|<span data-ttu-id="f2982-155">ネイティブ MSMQ プロトコルを使用する Windows Communication Foundation (WCF) サービスのキュー通信プロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="f2982-155">Specifies the queuing communication properties for a Windows Communication Foundation (WCF) service that uses the native MSMQ protocol.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f2982-156">Remarks</span><span class="sxs-lookup"><span data-stu-id="f2982-156">Remarks</span></span>  
 <span data-ttu-id="f2982-157">トランスポート セキュリティの詳細については、次を参照してください。[トランスポート セキュリティ](../../../../../docs/framework/wcf/feature-details/transport-security.md)します。</span><span class="sxs-lookup"><span data-stu-id="f2982-157">For more information on transport security, see [Transport Security](../../../../../docs/framework/wcf/feature-details/transport-security.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2982-158">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2982-158">See Also</span></span>  
 <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurity>  
 <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="f2982-159">WCF のキュー</span><span class="sxs-lookup"><span data-stu-id="f2982-159">Queues in WCF</span></span>](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)  
 [<span data-ttu-id="f2982-160">トランスポート</span><span class="sxs-lookup"><span data-stu-id="f2982-160">Transports</span></span>](../../../../../docs/framework/wcf/feature-details/transports.md)  
 [<span data-ttu-id="f2982-161">トランスポートの選択</span><span class="sxs-lookup"><span data-stu-id="f2982-161">Choosing a Transport</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)  
 [<span data-ttu-id="f2982-162">バインディング</span><span class="sxs-lookup"><span data-stu-id="f2982-162">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="f2982-163">バインディングの拡張</span><span class="sxs-lookup"><span data-stu-id="f2982-163">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="f2982-164">カスタム バインディング</span><span class="sxs-lookup"><span data-stu-id="f2982-164">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="f2982-165">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="f2982-165">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)  
 [<span data-ttu-id="f2982-166">トランスポート セキュリティ</span><span class="sxs-lookup"><span data-stu-id="f2982-166">Transport Security</span></span>](../../../../../docs/framework/wcf/feature-details/transport-security.md)
