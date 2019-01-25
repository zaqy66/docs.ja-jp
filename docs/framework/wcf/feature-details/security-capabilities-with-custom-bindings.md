---
title: カスタム バインドを使用したセキュリティ機能
ms.date: 03/30/2017
ms.assetid: a2425679-484a-4e6c-9c98-7da7304f1516
ms.openlocfilehash: 51359dd555db44891b4c8fe7bca9b62cab5f8d29
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54708520"
---
# <a name="security-capabilities-with-custom-bindings"></a><span data-ttu-id="4f48d-102">カスタム バインドを使用したセキュリティ機能</span><span class="sxs-lookup"><span data-stu-id="4f48d-102">Security Capabilities with Custom Bindings</span></span>
<span data-ttu-id="4f48d-103">一般的なセキュリティ タスクのほとんどは、システム指定のバインディングのいずれかを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="4f48d-103">You can perform most common security tasks by using one of the system-provided bindings.</span></span> <span data-ttu-id="4f48d-104">ただし、より高度な制御が必要な場合は、以下のトピックで説明するように、<xref:System.ServiceModel.Channels.SecurityBindingElement> を使用してカスタム バインドを作成できます。</span><span class="sxs-lookup"><span data-stu-id="4f48d-104">If you need more control, however, you can create a custom binding with a <xref:System.ServiceModel.Channels.SecurityBindingElement>, as explained in these topics.</span></span> <span data-ttu-id="4f48d-105">カスタム バインドの詳細については、次を参照してください。[カスタム バインド](../../../../docs/framework/wcf/extending/custom-bindings.md)します。</span><span class="sxs-lookup"><span data-stu-id="4f48d-105">For more information about custom bindings, see [Custom Bindings](../../../../docs/framework/wcf/extending/custom-bindings.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="4f48d-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="4f48d-106">In This Section</span></span>  
 [<span data-ttu-id="4f48d-107">SecurityBindingElement 認証モード</span><span class="sxs-lookup"><span data-stu-id="4f48d-107">SecurityBindingElement Authentication Modes</span></span>](../../../../docs/framework/wcf/feature-details/securitybindingelement-authentication-modes.md)  
 <span data-ttu-id="4f48d-108">カスタム バインドで使用できる認証モードについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4f48d-108">Describes the authentication modes that are possible with a custom binding.</span></span>  
  
 [<span data-ttu-id="4f48d-109">方法: SecurityBindingElement を使用してカスタム バインディングを作成します。</span><span class="sxs-lookup"><span data-stu-id="4f48d-109">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)  
 <span data-ttu-id="4f48d-110">セキュリティ要素を使用してカスタム バインドを作成するための基本手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f48d-110">Describes the basic steps for creating a custom binding with a security element.</span></span>  
  
 [<span data-ttu-id="4f48d-111">方法: 指定した認証モード用の SecurityBindingElement を作成します。</span><span class="sxs-lookup"><span data-stu-id="4f48d-111">How to: Create a SecurityBindingElement for a Specified Authentication Mode</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-securitybindingelement-for-a-specified-authentication-mode.md)  
 <span data-ttu-id="4f48d-112">指定した認証モード用のセキュリティ要素を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f48d-112">Describes how to create a security element for a specified authentication mode.</span></span>  
  
 [<span data-ttu-id="4f48d-113">方法: WSFederationHttpBinding のセキュリティで保護されたセッションを無効にします。</span><span class="sxs-lookup"><span data-stu-id="4f48d-113">How to: Disable Secure Sessions on a WSFederationHttpBinding</span></span>](../../../../docs/framework/wcf/feature-details/how-to-disable-secure-sessions-on-a-wsfederationhttpbinding.md)  
 <span data-ttu-id="4f48d-114">フェデレーション サービスを作成する際に、セキュリティで保護されたセッションを無効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f48d-114">Describes how to disable secure sessions when creating a federation service.</span></span>  
  
 [<span data-ttu-id="4f48d-115">方法: メッセージ リプレイ検出を有効にします。</span><span class="sxs-lookup"><span data-stu-id="4f48d-115">How to: Enable Message Replay Detection</span></span>](../../../../docs/framework/wcf/feature-details/how-to-enable-message-replay-detection.md)  
 <span data-ttu-id="4f48d-116">リプレイ攻撃の発生を確認する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f48d-116">Describes how to determine when a replay attack occurs.</span></span>  
  
 [<span data-ttu-id="4f48d-117">方法: サポート資格情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="4f48d-117">How to: Create a Supporting Credential</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-supporting-credential.md)  
 <span data-ttu-id="4f48d-118">必要な場合に、サービスにサポート資格情報を提供する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f48d-118">Describes how to supply a supporting credential to a service, if the service requires it.</span></span>  
  
 [<span data-ttu-id="4f48d-119">方法: 署名確認を設定します。</span><span class="sxs-lookup"><span data-stu-id="4f48d-119">How to: Set Up a Signature Confirmation</span></span>](../../../../docs/framework/wcf/feature-details/how-to-set-up-a-signature-confirmation.md)  
 <span data-ttu-id="4f48d-120">メッセージにデジタル署名する際に署名を確認する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f48d-120">Describes the steps to confirm signatures when digitally signing messages.</span></span>  
  
 [<span data-ttu-id="4f48d-121">方法: 最大クロックのずれを設定</span><span class="sxs-lookup"><span data-stu-id="4f48d-121">How to: Set a Max Clock Skew</span></span>](../../../../docs/framework/wcf/feature-details/how-to-set-a-max-clock-skew.md)  
 <span data-ttu-id="4f48d-122">サービスとクライアント間で許容される最大の時刻のずれを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f48d-122">Describes how to set the maximum allowed time difference between a service and a client.</span></span>  
  
 [<span data-ttu-id="4f48d-123">方法: デジタル署名の暗号化を無効にします。</span><span class="sxs-lookup"><span data-stu-id="4f48d-123">How to: Disable Encryption of Digital Signatures</span></span>](../../../../docs/framework/wcf/feature-details/how-to-disable-encryption-of-digital-signatures.md)  
 <span data-ttu-id="4f48d-124">デジタル署名の暗号化を無効にするとどのようなパフォーマンス上の利点があるかを説明します。</span><span class="sxs-lookup"><span data-stu-id="4f48d-124">Describes how disabling encryption of digital signatures can have a performance benefit.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="4f48d-125">参照</span><span class="sxs-lookup"><span data-stu-id="4f48d-125">Reference</span></span>  
 <xref:System.ServiceModel.Channels.SecurityBindingElement>  
  
 [<span data-ttu-id="4f48d-126">\<security></span><span class="sxs-lookup"><span data-stu-id="4f48d-126">\<security></span></span>](../../../../docs/framework/configure-apps/file-schema/wcf/security-of-custombinding.md)  
  
## <a name="related-sections"></a><span data-ttu-id="4f48d-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f48d-127">Related Sections</span></span>  
 [<span data-ttu-id="4f48d-128">保護レベルの理解</span><span class="sxs-lookup"><span data-stu-id="4f48d-128">Understanding Protection Level</span></span>](../../../../docs/framework/wcf/understanding-protection-level.md)  
  
 [<span data-ttu-id="4f48d-129">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="4f48d-129">Securing Services and Clients</span></span>](../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
  
## <a name="see-also"></a><span data-ttu-id="4f48d-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f48d-130">See also</span></span>
- [<span data-ttu-id="4f48d-131">バインディングとセキュリティ</span><span class="sxs-lookup"><span data-stu-id="4f48d-131">Bindings and Security</span></span>](../../../../docs/framework/wcf/feature-details/bindings-and-security.md)
- [<span data-ttu-id="4f48d-132">セキュリティの概要</span><span class="sxs-lookup"><span data-stu-id="4f48d-132">Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/security-overview.md)
- [<span data-ttu-id="4f48d-133">システム標準のバインディング</span><span class="sxs-lookup"><span data-stu-id="4f48d-133">System-Provided Bindings</span></span>](../../../../docs/framework/wcf/system-provided-bindings.md)
