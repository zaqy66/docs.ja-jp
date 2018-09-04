---
title: Windows Communication Foundation セキュリティ
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Communication Foundation, programming
- security [WCF]
- Windows Communication Foundation, security
ms.assetid: 7ea87fcb-dcfb-4a4a-8b03-6b954575d45b
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: a070800ea15c5a7f16b52ca69c7e454c92618e1a
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43503333"
---
# <a name="windows-communication-foundation-security"></a><span data-ttu-id="06212-102">Windows Communication Foundation セキュリティ</span><span class="sxs-lookup"><span data-stu-id="06212-102">Windows Communication Foundation Security</span></span>
<span data-ttu-id="06212-103">このセクションのトピックでは、Windows Communication Foundation (WCF) のセキュリティ機能とそれらを使用してメッセージをセキュリティで保護する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="06212-103">The topics in this section describe Windows Communication Foundation (WCF) security features and how to use them to help secure messages.</span></span>  
  
 <span data-ttu-id="06212-104">Windows Server AppFabric およびセキュリティの詳細については、次を参照してください[Windows Server AppFabric のセキュリティ モデル。](https://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)</span><span class="sxs-lookup"><span data-stu-id="06212-104">For more information about Windows Server AppFabric and security, see [Security Model for Windows Server AppFabric](https://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="06212-105">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="06212-105">In This Section</span></span>  
 [<span data-ttu-id="06212-106">セキュリティの概要</span><span class="sxs-lookup"><span data-stu-id="06212-106">Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/security-overview.md)  
 <span data-ttu-id="06212-107">WCF のセキュリティ機能をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="06212-107">Describes the security features in WCF.</span></span>  
  
 [<span data-ttu-id="06212-108">セキュリティの概念</span><span class="sxs-lookup"><span data-stu-id="06212-108">Security Concepts</span></span>](../../../../docs/framework/wcf/feature-details/security-concepts.md)  
 <span data-ttu-id="06212-109">基本的な用語と WCF のセキュリティに使用される概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="06212-109">Describes the basic terminology and concepts used in WCF security.</span></span>  
  
 [<span data-ttu-id="06212-110">一般的なセキュリティ シナリオ</span><span class="sxs-lookup"><span data-stu-id="06212-110">Common Security Scenarios</span></span>](../../../../docs/framework/wcf/feature-details/common-security-scenarios.md)  
 <span data-ttu-id="06212-111">シナリオと WCF を構成することができますトポロジについて説明します。</span><span class="sxs-lookup"><span data-stu-id="06212-111">Describes scenarios and topologies you can configure with WCF.</span></span>  
  
 [<span data-ttu-id="06212-112">セキュリティ動作</span><span class="sxs-lookup"><span data-stu-id="06212-112">Security Behaviors</span></span>](../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)  
 <span data-ttu-id="06212-113">資格情報の設定など、セキュリティに影響する WCF の動作に関する概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="06212-113">Provides an overview of WCF behaviors that affect security, such as setting credentials.</span></span>  
  
 [<span data-ttu-id="06212-114">バインディングとセキュリティ</span><span class="sxs-lookup"><span data-stu-id="06212-114">Bindings and Security</span></span>](../../../../docs/framework/wcf/feature-details/bindings-and-security.md)  
 <span data-ttu-id="06212-115">カスタム セキュリティ バインディングの作成方法を示すトピックなど、バインディングをセキュリティの観点から説明します。</span><span class="sxs-lookup"><span data-stu-id="06212-115">A security-oriented view of the bindings, including topics that demonstrate how to create custom security bindings.</span></span>  
  
 [<span data-ttu-id="06212-116">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="06212-116">Securing Services and Clients</span></span>](../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 <span data-ttu-id="06212-117">WCF セキュリティ機能を使用してメッセージをセキュリティで保護する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="06212-117">Describes how to secure messages using WCF security features.</span></span>  
  
 [<span data-ttu-id="06212-118">認証</span><span class="sxs-lookup"><span data-stu-id="06212-118">Authentication</span></span>](../../../../docs/framework/wcf/feature-details/authentication-in-wcf.md)  
 <span data-ttu-id="06212-119">一般的な認証タスクを示します。</span><span class="sxs-lookup"><span data-stu-id="06212-119">Demonstrates common authentication tasks.</span></span>  
  
 [<span data-ttu-id="06212-120">承認</span><span class="sxs-lookup"><span data-stu-id="06212-120">Authorization</span></span>](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md)  
 <span data-ttu-id="06212-121">セキュリティ実装を使用した一般的な承認シナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="06212-121">Describes common authorization scenarios with security implementations.</span></span>  
  
 [<span data-ttu-id="06212-122">フェデレーションと発行済みトークン</span><span class="sxs-lookup"><span data-stu-id="06212-122">Federation and Issued Tokens</span></span>](../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 <span data-ttu-id="06212-123">フェデレーションの基本事項と、フェデレーション サーバーと通信するクライアントを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="06212-123">Describes the basics of federation and how to create clients that communicate with federated servers.</span></span>  
  
 [<span data-ttu-id="06212-124">部分信頼</span><span class="sxs-lookup"><span data-stu-id="06212-124">Partial Trust</span></span>](../../../../docs/framework/wcf/feature-details/partial-trust.md)  
 <span data-ttu-id="06212-125">部分的に信頼されたを実行している場合は、部分的に信頼のシナリオと WCF の制限事項を実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="06212-125">Describes how to run partially-trusted scenarios and WCF limitations when running partially trusted.</span></span>  
  
 [<span data-ttu-id="06212-126">監査</span><span class="sxs-lookup"><span data-stu-id="06212-126">Auditing</span></span>](../../../../docs/framework/wcf/feature-details/auditing-security-events.md)  
 <span data-ttu-id="06212-127">セキュリティ イベントを監査する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="06212-127">Describes how to audit security events.</span></span>  
  
 [<span data-ttu-id="06212-128">セキュリティ ガイドラインとベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="06212-128">Security Guidance and Best Practices</span></span>](../../../../docs/framework/wcf/feature-details/security-guidance-and-best-practices.md)  
 <span data-ttu-id="06212-129">セキュリティで保護された WCF アプリケーションの作成に関するガイドラインです。</span><span class="sxs-lookup"><span data-stu-id="06212-129">Guidelines for creating secure WCF applications.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="06212-130">参照</span><span class="sxs-lookup"><span data-stu-id="06212-130">Reference</span></span>  
 <xref:System.ServiceModel>  
  
 <xref:System.ServiceModel.Security>  
  
## <a name="related-sections"></a><span data-ttu-id="06212-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="06212-131">Related Sections</span></span>  
 [<span data-ttu-id="06212-132">WCF 機能の詳細</span><span class="sxs-lookup"><span data-stu-id="06212-132">WCF Feature Details</span></span>](../../../../docs/framework/wcf/feature-details/index.md)  
  
 [<span data-ttu-id="06212-133">基本的な WCF プログラミング</span><span class="sxs-lookup"><span data-stu-id="06212-133">Basic WCF Programming</span></span>](../../../../docs/framework/wcf/basic-wcf-programming.md)  
  
 [<span data-ttu-id="06212-134">チュートリアル入門</span><span class="sxs-lookup"><span data-stu-id="06212-134">Getting Started Tutorial</span></span>](../../../../docs/framework/wcf/getting-started-tutorial.md)  
  
 [<span data-ttu-id="06212-135">概念</span><span class="sxs-lookup"><span data-stu-id="06212-135">Conceptual Overview</span></span>](../../../../docs/framework/wcf/conceptual-overview.md)  
  
## <a name="see-also"></a><span data-ttu-id="06212-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="06212-136">See Also</span></span>  
 [<span data-ttu-id="06212-137">アプリケーションの構成</span><span class="sxs-lookup"><span data-stu-id="06212-137">Configuring Your Application</span></span>](../../../../docs/framework/wcf/diagnostics/configuring-your-application.md)
