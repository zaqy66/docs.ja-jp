---
title: '&lt;peerAuthentication&gt;'
ms.date: 03/30/2017
ms.assetid: ad545e6f-f06e-4549-ac92-09d758d5c636
ms.openlocfilehash: bb83d2badad609394a66246fc14c19a6602399e0
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/13/2018
ms.locfileid: "44778201"
---
# <a name="ltpeerauthenticationgt"></a><span data-ttu-id="be110-102">&lt;peerAuthentication&gt;</span><span class="sxs-lookup"><span data-stu-id="be110-102">&lt;peerAuthentication&gt;</span></span>
<span data-ttu-id="be110-103">ピア ノードで使用されるピア証明書の認証設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="be110-103">Specifies authentication settings for a peer certificate used by a peer node.</span></span>  
  
 <span data-ttu-id="be110-104">\<system.ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="be110-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="be110-105">\<<behaviors></span><span class="sxs-lookup"><span data-stu-id="be110-105">\<behaviors></span></span>  
<span data-ttu-id="be110-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="be110-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="be110-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="be110-107">\<behavior></span></span>  
<span data-ttu-id="be110-108">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="be110-108">\<serviceCredentials></span></span>  
<span data-ttu-id="be110-109">\<ピア ></span><span class="sxs-lookup"><span data-stu-id="be110-109">\<peer></span></span>  
<span data-ttu-id="be110-110">\<peerAuthentication></span><span class="sxs-lookup"><span data-stu-id="be110-110">\<peerAuthentication></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="be110-111">構文</span><span class="sxs-lookup"><span data-stu-id="be110-111">Syntax</span></span>  
  
```xml  
<peerAuthentication  
      customCertificateValidatorType="namespace.typeName, [,AssemblyName] [,Version=version number] [,Culture=culture] [,PublicKeyToken=token]"  
      certificateValidationMode="ChainTrust/None/PeerTrust/PeerOrChainTrust/Custom"  
      revocationMode="NoCheck/Online/Offline"  
      trustedStoreLocation="CurrentUser/LocalMachine"   
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="be110-112">属性および要素</span><span class="sxs-lookup"><span data-stu-id="be110-112">Attributes and Elements</span></span>  
 <span data-ttu-id="be110-113">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="be110-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="be110-114">属性</span><span class="sxs-lookup"><span data-stu-id="be110-114">Attributes</span></span>  
  
|<span data-ttu-id="be110-115">属性</span><span class="sxs-lookup"><span data-stu-id="be110-115">Attribute</span></span>|<span data-ttu-id="be110-116">説明</span><span class="sxs-lookup"><span data-stu-id="be110-116">Description</span></span>|  
|---------------|-----------------|  
|`certificateValidationMode`|<span data-ttu-id="be110-117">省略可能な列挙体です。</span><span class="sxs-lookup"><span data-stu-id="be110-117">Optional enumeration.</span></span> <span data-ttu-id="be110-118">資格情報の検証に使用される 3 つのモードのいずれかを指定します。</span><span class="sxs-lookup"><span data-stu-id="be110-118">Specifies one of three modes used to validate credentials.</span></span> <span data-ttu-id="be110-119">この属性は <xref:System.ServiceModel.Security.X509CertificateValidationMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="be110-119">This attribute is of type <xref:System.ServiceModel.Security.X509CertificateValidationMode>.</span></span> <span data-ttu-id="be110-120">`Custom` に設定されている場合、`customCertificateValidator` も指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be110-120">If set to `Custom`, then a `customCertificateValidator` must also be supplied.</span></span>|  
|`customCertificateValidatorType`|<span data-ttu-id="be110-121">省略可能な文字列。</span><span class="sxs-lookup"><span data-stu-id="be110-121">Optional string.</span></span> <span data-ttu-id="be110-122">ユーザー設定タイプの検証に使用されるタイプおよびアセンブリを指定します。</span><span class="sxs-lookup"><span data-stu-id="be110-122">Specifies a type and assembly used to validate a custom type.</span></span> <span data-ttu-id="be110-123">`certificateValidationMode` が `Custom` に設定されている場合は、この属性を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be110-123">This attribute must be set when `certificateValidationMode` is set to `Custom`.</span></span> <span data-ttu-id="be110-124">この属性は <xref:System.IdentityModel.Selectors.X509CertificateValidator> 型です。</span><span class="sxs-lookup"><span data-stu-id="be110-124">This attribute is of type <xref:System.IdentityModel.Selectors.X509CertificateValidator>.</span></span> <span data-ttu-id="be110-125">Windows Communication Foundation (WCF) は、既定のピア信頼されたユーザー ストアに対してピア証明書を検証する証明書検証を提供します。</span><span class="sxs-lookup"><span data-stu-id="be110-125">Windows Communication Foundation (WCF) provides a default peer certificate validator that verifies the peer certificate against the trusted people store.</span></span> <span data-ttu-id="be110-126">証明書が有効なルートまでつながっていることを検証します。</span><span class="sxs-lookup"><span data-stu-id="be110-126">It also verifies that the certificate chains up to a valid root.</span></span> <span data-ttu-id="be110-127">カスタム検証を実装して別の動作を指定したり、この属性を使用してカスタム検証を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="be110-127">You can implement a custom validator to specify a different behavior and use this attribute to point to the custom validator.</span></span>|  
|`revocationMode`|<span data-ttu-id="be110-128">省略可能な列挙体です。</span><span class="sxs-lookup"><span data-stu-id="be110-128">Optional enumeration.</span></span> <span data-ttu-id="be110-129">証明書失効モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="be110-129">Specifies the certificate revocation mode.</span></span> <span data-ttu-id="be110-130">この属性は <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> 型です。</span><span class="sxs-lookup"><span data-stu-id="be110-130">This attribute is of type <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode>.</span></span> <span data-ttu-id="be110-131">システムは、ピア証明書を失効証明書リストで検索して、それが失効していないことを検証します。</span><span class="sxs-lookup"><span data-stu-id="be110-131">The system verifies that the peer certificate has not been revoked by looking it up in the revoked certificate list.</span></span> <span data-ttu-id="be110-132">このチェックは、オンラインで、またはキャッシュされた失効リストをチェックする方法で実行されます。</span><span class="sxs-lookup"><span data-stu-id="be110-132">This check can be performed either by checking online or against a cached revocation list.</span></span> <span data-ttu-id="be110-133">失効チェックは、この属性を NoCheck に設定することにより無効にできます。</span><span class="sxs-lookup"><span data-stu-id="be110-133">Revocation checking can be turned off by setting this attribute to NoCheck.</span></span>|  
|`trustedStoreLocation`|<span data-ttu-id="be110-134">省略可能な列挙体です。</span><span class="sxs-lookup"><span data-stu-id="be110-134">Optional enumeration.</span></span> <span data-ttu-id="be110-135">WCF セキュリティ システムによってピア証明書を検証する信頼されたストアの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="be110-135">Specifies the trusted store location where the peer certificate is validated by the WCF security system.</span></span> <span data-ttu-id="be110-136">この属性は <xref:System.Security.Cryptography.X509Certificates.StoreLocation> 型です。</span><span class="sxs-lookup"><span data-stu-id="be110-136">This attribute is of type <xref:System.Security.Cryptography.X509Certificates.StoreLocation>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="be110-137">子要素</span><span class="sxs-lookup"><span data-stu-id="be110-137">Child Elements</span></span>  
 <span data-ttu-id="be110-138">なし。</span><span class="sxs-lookup"><span data-stu-id="be110-138">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="be110-139">親要素</span><span class="sxs-lookup"><span data-stu-id="be110-139">Parent Elements</span></span>  
  
|<span data-ttu-id="be110-140">要素</span><span class="sxs-lookup"><span data-stu-id="be110-140">Element</span></span>|<span data-ttu-id="be110-141">説明</span><span class="sxs-lookup"><span data-stu-id="be110-141">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="be110-142">\<peer></span><span class="sxs-lookup"><span data-stu-id="be110-142">\<peer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-servicecredentials.md)|<span data-ttu-id="be110-143">ピア ノードの現在の資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="be110-143">Specifies the current credentials for a peer node.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="be110-144">Remarks</span><span class="sxs-lookup"><span data-stu-id="be110-144">Remarks</span></span>  
 <span data-ttu-id="be110-145">`<authentication>` 要素は、<xref:System.ServiceModel.Security.X509PeerCertificateAuthentication> クラスに対応します。</span><span class="sxs-lookup"><span data-stu-id="be110-145">The `<authentication>` element corresponds to the <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication> class.</span></span> <span data-ttu-id="be110-146">この要素は、メッシュ内の近隣ノード間の認証時に呼び出される検証コントロールを指定します。</span><span class="sxs-lookup"><span data-stu-id="be110-146">This element specifies a validator, which is invoked during neighbor-to-neighbor authentication in the mesh.</span></span> <span data-ttu-id="be110-147">新しいピアが近隣ノードとの接続を確立しようとするとき、自身の資格情報を応答側のピアに渡します。</span><span class="sxs-lookup"><span data-stu-id="be110-147">When a new peer tries to establish a neighbor connection, it passes its own credential to the responding peer.</span></span> <span data-ttu-id="be110-148">リモート パーティの資格情報を検証するために、応答側の検証が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="be110-148">The validator of the responder is invoked to verify the credential of the remote party.</span></span> <span data-ttu-id="be110-149">メッシュ内でピア接続が確立されるたびに、両方のピアが相互に認証されます。つまり、双方の検証が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="be110-149">Whenever a peer connection is established in the mesh, both peers are mutually authenticated, meaning validators on both ends are invoked.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be110-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="be110-150">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PeerCredentialElement>  
 <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication>  
 <xref:System.ServiceModel.Security.PeerCredential.PeerAuthentication%2A>  
 <xref:System.ServiceModel.Configuration.PeerCredentialElement.PeerAuthentication%2A>  
 <xref:System.ServiceModel.Configuration.X509PeerCertificateAuthenticationElement>  
 [<span data-ttu-id="be110-151">証明書の使用</span><span class="sxs-lookup"><span data-stu-id="be110-151">Working with Certificates</span></span>](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 [<span data-ttu-id="be110-152">ピアツーピア ネットワーク</span><span class="sxs-lookup"><span data-stu-id="be110-152">Peer-to-Peer Networking</span></span>](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)  
 [<span data-ttu-id="be110-153">ピア チャネル メッセージの認証</span><span class="sxs-lookup"><span data-stu-id="be110-153">Peer Channel Message Authentication</span></span>](https://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95)  
 [<span data-ttu-id="be110-154">ピア チャネル カスタム認証</span><span class="sxs-lookup"><span data-stu-id="be110-154">Peer Channel Custom Authentication</span></span>](https://msdn.microsoft.com/library/4aa8a82e-41a8-48e2-8621-7e1cbabdca7c)  
 [<span data-ttu-id="be110-155">セキュリティによるピア チャネル アプリケーションの保護</span><span class="sxs-lookup"><span data-stu-id="be110-155">Securing Peer Channel Applications</span></span>](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
