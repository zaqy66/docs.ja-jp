---
title: セキュリティの拡張
ms.date: 03/30/2017
helpviewer_keywords:
- security [WCF], extending
ms.assetid: a015a040-9fdf-4147-9ea9-f83b570be1d4
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: a16416e580dabd6a9057e11a8183437529ca83e8
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/14/2018
ms.locfileid: "45597044"
---
# <a name="extending-security"></a><span data-ttu-id="68dce-102">セキュリティの拡張</span><span class="sxs-lookup"><span data-stu-id="68dce-102">Extending Security</span></span>
<span data-ttu-id="68dce-103">新しいクレームの種類とカスタム トークンに対応するためには、Windows Communication Foundation (WCF) のセキュリティ インフラストラクチャを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="68dce-103">To accommodate new claim types and custom tokens, you can extend the security infrastructure of Windows Communication Foundation (WCF).</span></span> <span data-ttu-id="68dce-104">このセクションの各トピックでは、この方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="68dce-104">The topics in this section show you how this is done.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="68dce-105">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="68dce-105">In This Section</span></span>  
 [<span data-ttu-id="68dce-106">セキュリティ アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="68dce-106">Security Architecture</span></span>](https://msdn.microsoft.com/library/16593476-d36a-408d-808c-ae6fd483e28f)  
 <span data-ttu-id="68dce-107">WCF セキュリティ システムのアーキテクチャについて説明します。</span><span class="sxs-lookup"><span data-stu-id="68dce-107">Walks through the architecture of the WCF security system.</span></span>  
  
 [<span data-ttu-id="68dce-108">カスタム資格情報と資格情報の検証</span><span class="sxs-lookup"><span data-stu-id="68dce-108">Custom Credential and Credential Validation</span></span>](../../../../docs/framework/wcf/extending/custom-credential-and-credential-validation.md)  
 <span data-ttu-id="68dce-109">カスタム資格情報の検証中に ID モデルを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="68dce-109">Explains how the Identity Model is used when validating custom credentials.</span></span>  
  
 [<span data-ttu-id="68dce-110">カスタム トークン</span><span class="sxs-lookup"><span data-stu-id="68dce-110">Custom Tokens</span></span>](../../../../docs/framework/wcf/extending/custom-tokens.md)  
 <span data-ttu-id="68dce-111">通常、セキュリティ トークン サービス (STS) から発行されるトークンは SAML トークンです。</span><span class="sxs-lookup"><span data-stu-id="68dce-111">Issued tokens from a Security Token Service (STS) are typically SAML tokens.</span></span> <span data-ttu-id="68dce-112">ここでは、カスタムのトークンの種類を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="68dce-112">This topic explains how to create a custom token type.</span></span>  
  
 [<span data-ttu-id="68dce-113">カスタム承認</span><span class="sxs-lookup"><span data-stu-id="68dce-113">Custom Authorization</span></span>](../../../../docs/framework/wcf/extending/custom-authorization.md)  
 <span data-ttu-id="68dce-114">カスタム承認を実装する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="68dce-114">Explains how to implement custom authorization.</span></span>  
  
 [<span data-ttu-id="68dce-115">認証のためのサービスの ID のオーバーライド</span><span class="sxs-lookup"><span data-stu-id="68dce-115">Overriding the Identity of a Service for Authentication</span></span>](../../../../docs/framework/wcf/extending/overriding-the-identity-of-a-service-for-authentication.md)  
 <span data-ttu-id="68dce-116">認証のためにサービスの ID をオーバーライドする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="68dce-116">Describes how to override the identity of a service for authentication.</span></span>  
  
 [<span data-ttu-id="68dce-117">方法 : カスタム クライアント ID 検証機能を作成する</span><span class="sxs-lookup"><span data-stu-id="68dce-117">How to: Create a Custom Client Identity Verifier</span></span>](../../../../docs/framework/wcf/extending/how-to-create-a-custom-client-identity-verifier.md)  
 <span data-ttu-id="68dce-118">カスタム エンドポイント ID を検証する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="68dce-118">Demonstrates how to validate a custom endpoint identity.</span></span>  
  
 [<span data-ttu-id="68dce-119">方法 : 署名および暗号化に個別の X.509 証明書を使用する</span><span class="sxs-lookup"><span data-stu-id="68dce-119">How to: Use Separate X.509 Certificates for Signing and Encryption</span></span>](../../../../docs/framework/wcf/extending/how-to-use-separate-x-509-certificates-for-signing-and-encryption.md)  
 <span data-ttu-id="68dce-120">通常、メッセージの署名および暗号化は 1 つの証明書を使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="68dce-120">Messages are typically signed and encrypted with a single certificate.</span></span> <span data-ttu-id="68dce-121">ここでは、必要に応じて 2 つの証明書を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="68dce-121">This topic explains how two certificates can be used, when required.</span></span>  
  
 [<span data-ttu-id="68dce-122">方法 : X.509 証明書の秘密キーの暗号化プロバイダーを変更する</span><span class="sxs-lookup"><span data-stu-id="68dce-122">How to: Change the Cryptographic Provider for an X.509 Certificate's Private Key</span></span>](../../../../docs/framework/wcf/extending/change-cryptographic-provider-x509-certificate-private-key.md)  
 <span data-ttu-id="68dce-123">X.509 証明書の秘密キーを提供するために使用する暗号化サービス プロバイダーを変更する方法と、Windows Communication Foundation (WCF) フレームワークにプロバイダーを統合する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="68dce-123">Explains how to change the cryptographic provider used to provide an X.509 certificate's private key and how to integrate the provider into the Windows Communication Foundation (WCF) framework.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="68dce-124">参照</span><span class="sxs-lookup"><span data-stu-id="68dce-124">Reference</span></span>  
 <xref:System.ServiceModel.ServiceAuthorizationManager>  
  
 <xref:System.ServiceModel.Security>  
  
 <xref:System.IdentityModel.Claims>  
  
 <xref:System.IdentityModel.Policy>  
  
 <xref:System.IdentityModel.Tokens>  
  
 <xref:System.IdentityModel.Selectors>  
  
## <a name="related-sections"></a><span data-ttu-id="68dce-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="68dce-125">Related Sections</span></span>  
 [<span data-ttu-id="68dce-126">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="68dce-126">Security</span></span>](../../../../docs/framework/wcf/feature-details/security.md)  
  
 [<span data-ttu-id="68dce-127">基本的な WCF プログラミング</span><span class="sxs-lookup"><span data-stu-id="68dce-127">Basic WCF Programming</span></span>](../../../../docs/framework/wcf/basic-wcf-programming.md)  
  
## <a name="see-also"></a><span data-ttu-id="68dce-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="68dce-128">See Also</span></span>  
 [<span data-ttu-id="68dce-129">セキュリティの概要</span><span class="sxs-lookup"><span data-stu-id="68dce-129">Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/security-overview.md)
