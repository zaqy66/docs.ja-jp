---
title: 一般的なセキュリティ シナリオ
ms.date: 03/30/2017
helpviewer_keywords:
- security [WCF], scenarios
ms.assetid: 201923b5-5162-4a8a-8d4c-e7bd242748d5
ms.openlocfilehash: d4afeb8d406990256d0cffa74c440ffc75bfc462
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50183465"
---
# <a name="common-security-scenarios"></a><span data-ttu-id="f5617-102">一般的なセキュリティ シナリオ</span><span class="sxs-lookup"><span data-stu-id="f5617-102">Common Security Scenarios</span></span>
<span data-ttu-id="f5617-103">ここでは、考えられるさまざまなクライアントおよびサービスのセキュリティ構成の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="f5617-103">The topics in this section catalog a number of possible client and service security configurations.</span></span> <span data-ttu-id="f5617-104">構成はさまざまな要因により異なります。</span><span class="sxs-lookup"><span data-stu-id="f5617-104">Configurations vary according to a number of factors.</span></span> <span data-ttu-id="f5617-105">たとえば、サービスやクライアントがイントラネット上にあるかどうか、また、セキュリティが Windows とトランスポート (HTTPS など) のどちらで提供されるかなどが考えられます。</span><span class="sxs-lookup"><span data-stu-id="f5617-105">For example, whether a service or client is on an intranet, or whether the security is provided by Windows or transport (such as HTTPS).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f5617-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="f5617-106">In This Section</span></span>  
 [<span data-ttu-id="f5617-107">セキュリティで保護されていないインターネット環境のクライアントとサービス</span><span class="sxs-lookup"><span data-stu-id="f5617-107">Internet Unsecured Client and Service</span></span>](../../../../docs/framework/wcf/feature-details/internet-unsecured-client-and-service.md)  
 <span data-ttu-id="f5617-108">セキュリティで保護されていないパブリックなクライアントとサービスの例です。</span><span class="sxs-lookup"><span data-stu-id="f5617-108">An example of a public, unsecured client and service.</span></span>  
  
 [<span data-ttu-id="f5617-109">セキュリティで保護されていないイントラネットのクライアントとサービス</span><span class="sxs-lookup"><span data-stu-id="f5617-109">Intranet Unsecured Client and Service</span></span>](../../../../docs/framework/wcf/feature-details/intranet-unsecured-client-and-service.md)  
 <span data-ttu-id="f5617-110">WCF アプリケーションをセキュリティで保護されたプライベート ネットワーク上の情報を提供する基本的な Windows Communication Foundation (WCF) サービスを開発しました。</span><span class="sxs-lookup"><span data-stu-id="f5617-110">A basic Windows Communication Foundation (WCF) service developed to provide information on a secure private network to a WCF application.</span></span>  
  
 [<span data-ttu-id="f5617-111">基本認証を使用する場合のトランスポート セキュリティ</span><span class="sxs-lookup"><span data-stu-id="f5617-111">Transport Security with Basic Authentication</span></span>](../../../../docs/framework/wcf/feature-details/transport-security-with-basic-authentication.md)  
 <span data-ttu-id="f5617-112">アプリケーションは、カスタム認証を使用して、クライアントにログオンを許可します。</span><span class="sxs-lookup"><span data-stu-id="f5617-112">The application allows clients to log on using custom authentication.</span></span>  
  
 [<span data-ttu-id="f5617-113">Windows 認証を使用する場合のトランスポート セキュリティ</span><span class="sxs-lookup"><span data-stu-id="f5617-113">Transport Security with Windows Authentication</span></span>](../../../../docs/framework/wcf/feature-details/transport-security-with-windows-authentication.md)  
 <span data-ttu-id="f5617-114">Windows セキュリティによってセキュリティ保護されたクライアントとサービスを示します。</span><span class="sxs-lookup"><span data-stu-id="f5617-114">Shows a client and service secured by Windows security.</span></span>  
  
 [<span data-ttu-id="f5617-115">トランスポート セキュリティと匿名クライアント</span><span class="sxs-lookup"><span data-stu-id="f5617-115">Transport Security with an Anonymous Client</span></span>](../../../../docs/framework/wcf/feature-details/transport-security-with-an-anonymous-client.md)  
 <span data-ttu-id="f5617-116">このシナリオでは HTTPS などのようなトランスポート セキュリティを使用して、機密性と整合性を強化します。</span><span class="sxs-lookup"><span data-stu-id="f5617-116">This scenario uses transport security (such as HTTPS) to ensure confidentiality and integrity.</span></span>  
  
 [<span data-ttu-id="f5617-117">トランスポート セキュリティと証明書認証</span><span class="sxs-lookup"><span data-stu-id="f5617-117">Transport Security with Certificate Authentication</span></span>](../../../../docs/framework/wcf/feature-details/transport-security-with-certificate-authentication.md)  
 <span data-ttu-id="f5617-118">証明書によってセキュリティ保護されたクライアントとサービスを示します。</span><span class="sxs-lookup"><span data-stu-id="f5617-118">Shows a client and service secured by a certificate.</span></span>  
  
 [<span data-ttu-id="f5617-119">メッセージ セキュリティと匿名クライアント</span><span class="sxs-lookup"><span data-stu-id="f5617-119">Message Security with an Anonymous Client</span></span>](../../../../docs/framework/wcf/feature-details/message-security-with-an-anonymous-client.md)  
 <span data-ttu-id="f5617-120">クライアントと WCF メッセージ セキュリティで保護されたサービスを示します。</span><span class="sxs-lookup"><span data-stu-id="f5617-120">Shows a client and service secured by WCF message security.</span></span>  
  
 [<span data-ttu-id="f5617-121">ユーザー名クライアントを使用したメッセージ セキュリティ</span><span class="sxs-lookup"><span data-stu-id="f5617-121">Message Security with a User Name Client</span></span>](../../../../docs/framework/wcf/feature-details/message-security-with-a-user-name-client.md)  
 <span data-ttu-id="f5617-122">クライアントは、ドメイン ユーザー名とパスワードを使用してクライアントのログオンを許可する Windows フォーム アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="f5617-122">The client is a Windows Forms application that allows clients to log on using a domain user name and password.</span></span>  
  
 [<span data-ttu-id="f5617-123">メッセージ セキュリティと証明書クライアント</span><span class="sxs-lookup"><span data-stu-id="f5617-123">Message Security with a Certificate Client</span></span>](../../../../docs/framework/wcf/feature-details/message-security-with-a-certificate-client.md)  
 <span data-ttu-id="f5617-124">サーバー側の証明書は複数あり、クライアント側の証明書はそれぞれ 1 つです。</span><span class="sxs-lookup"><span data-stu-id="f5617-124">Servers have certificates, and each client has a certificate.</span></span> <span data-ttu-id="f5617-125">セキュリティのコンテキストは、トランスポート層セキュリティ (TLS: Transport Layer Security) ネゴシエーションを介して確立されます。</span><span class="sxs-lookup"><span data-stu-id="f5617-125">A security context is established through Transport Layer Security (TLS) negotiation.</span></span>  
  
 [<span data-ttu-id="f5617-126">Windows クライアントを使用する場合のメッセージ セキュリティ</span><span class="sxs-lookup"><span data-stu-id="f5617-126">Message Security with a Windows Client</span></span>](../../../../docs/framework/wcf/feature-details/message-security-with-a-windows-client.md)  
 <span data-ttu-id="f5617-127">証明書クライアントのバリエーションの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="f5617-127">A variation of the certificate client.</span></span> <span data-ttu-id="f5617-128">サーバー側の証明書は複数あり、クライアント側の証明書はそれぞれ 1 つです。</span><span class="sxs-lookup"><span data-stu-id="f5617-128">Servers have certificates, and each client has a certificate.</span></span> <span data-ttu-id="f5617-129">セキュリティのコンテキストは TLS ネゴシエーションを介して確立されます。</span><span class="sxs-lookup"><span data-stu-id="f5617-129">A security context is established through TLS negotiation.</span></span>  
  
 [<span data-ttu-id="f5617-130">資格情報ネゴシエーションを使用しない Windows クライアントを使用するメッセージ セキュリティ</span><span class="sxs-lookup"><span data-stu-id="f5617-130">Message Security with a Windows Client without Credential Negotiation</span></span>](../../../../docs/framework/wcf/feature-details/message-security-with-a-windows-client-without-credential-negotiation.md)  
 <span data-ttu-id="f5617-131">Kerberos ドメインによってセキュリティ保護されたクライアントとサービスを示します。</span><span class="sxs-lookup"><span data-stu-id="f5617-131">Shows a client and service secured by a Kerberos domain.</span></span>  
  
 [<span data-ttu-id="f5617-132">相互の証明書を使用する場合のメッセージ セキュリティ</span><span class="sxs-lookup"><span data-stu-id="f5617-132">Message Security with Mutual Certificates</span></span>](../../../../docs/framework/wcf/feature-details/message-security-with-mutual-certificates.md)  
 <span data-ttu-id="f5617-133">サーバー側の証明書は複数あり、クライアント側の証明書はそれぞれ 1 つです。</span><span class="sxs-lookup"><span data-stu-id="f5617-133">Servers have certificates, and each client has a certificate.</span></span> <span data-ttu-id="f5617-134">サーバーの証明書はアプリケーションと共に配布され、帯域外でも使用可能です。</span><span class="sxs-lookup"><span data-stu-id="f5617-134">The server certificate is distributed with the application and is available out of band.</span></span>  
  
 [<span data-ttu-id="f5617-135">発行済みトークンを使用したメッセージ セキュリティ</span><span class="sxs-lookup"><span data-stu-id="f5617-135">Message Security with Issued Tokens</span></span>](../../../../docs/framework/wcf/feature-details/message-security-with-issued-tokens.md)  
 <span data-ttu-id="f5617-136">フェデレーション セキュリティにより独立したドメイン間で信頼を確立できます。</span><span class="sxs-lookup"><span data-stu-id="f5617-136">Federated security that enables the establishment of trust between independent domains.</span></span>  
  
 [<span data-ttu-id="f5617-137">信頼できるサブシステム</span><span class="sxs-lookup"><span data-stu-id="f5617-137">Trusted Subsystem</span></span>](../../../../docs/framework/wcf/feature-details/trusted-subsystem.md)  
 <span data-ttu-id="f5617-138">クライアントは、ネットワーク全体に分散している 1 つ以上の Web サービスにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f5617-138">A client accesses one or more Web services that are distributed across a network.</span></span> <span data-ttu-id="f5617-139">Web サービスは、セキュリティで保護する必要がある追加のリソース (データベースや他の Web サービスなど) にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f5617-139">The Web services access additional resources (such as databases or other Web services) that must be secured.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="f5617-140">参照</span><span class="sxs-lookup"><span data-stu-id="f5617-140">Reference</span></span>  
 <xref:System.ServiceModel>  
  
## <a name="related-sections"></a><span data-ttu-id="f5617-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="f5617-141">Related Sections</span></span>  
 [<span data-ttu-id="f5617-142">承認</span><span class="sxs-lookup"><span data-stu-id="f5617-142">Authorization</span></span>](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md)  
  
 [<span data-ttu-id="f5617-143">セキュリティの概要</span><span class="sxs-lookup"><span data-stu-id="f5617-143">Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/security-overview.md)  
  
 [<span data-ttu-id="f5617-144">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="f5617-144">Security</span></span>](../../../../docs/framework/wcf/feature-details/security.md)  
  
 [<span data-ttu-id="f5617-145">バインディングとセキュリティ</span><span class="sxs-lookup"><span data-stu-id="f5617-145">Bindings and Security</span></span>](../../../../docs/framework/wcf/feature-details/bindings-and-security.md)  
  
 [<span data-ttu-id="f5617-146">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="f5617-146">Securing Services and Clients</span></span>](../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
  
 [<span data-ttu-id="f5617-147">認証</span><span class="sxs-lookup"><span data-stu-id="f5617-147">Authentication</span></span>](../../../../docs/framework/wcf/feature-details/authentication-in-wcf.md)  
  
 [<span data-ttu-id="f5617-148">承認</span><span class="sxs-lookup"><span data-stu-id="f5617-148">Authorization</span></span>](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md)  
  
 [<span data-ttu-id="f5617-149">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="f5617-149">Federation and Issued Tokens</span></span>](../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
  
 [<span data-ttu-id="f5617-150">監査</span><span class="sxs-lookup"><span data-stu-id="f5617-150">Auditing</span></span>](../../../../docs/framework/wcf/feature-details/auditing-security-events.md)  
  
## <a name="see-also"></a><span data-ttu-id="f5617-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="f5617-151">See Also</span></span>  
 [<span data-ttu-id="f5617-152">セキュリティ ガイドラインとベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="f5617-152">Security Guidance and Best Practices</span></span>](../../../../docs/framework/wcf/feature-details/security-guidance-and-best-practices.md)  
 [<span data-ttu-id="f5617-153">Windows Server App Fabric のセキュリティ モデル</span><span class="sxs-lookup"><span data-stu-id="f5617-153">Security Model for Windows Server App Fabric</span></span>](https://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
