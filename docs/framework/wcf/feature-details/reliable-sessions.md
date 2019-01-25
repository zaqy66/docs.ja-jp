---
title: 信頼できるセッション
ms.date: 03/30/2017
f1_keywords:
- Windows Communication Foundation, sessions and instances
- WCF, sessions and instances
- sessions and instances [WCF]
helpviewer_keywords:
- instances [WCF]
- sessions [WCF]
ms.assetid: 143951b3-3aa0-4540-b4b7-d33e77e874a1
ms.openlocfilehash: 1d87f6f4d94763dc8f6ac7e929c22b17940097ca
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54735426"
---
# <a name="reliable-sessions"></a><span data-ttu-id="5e9b3-102">信頼できるセッション</span><span class="sxs-lookup"><span data-stu-id="5e9b3-102">Reliable Sessions</span></span>

<span data-ttu-id="5e9b3-103">このセクションでは、どのような Windows Communication Foundation (WCF) 信頼できるセッションが、用途も、方法およびと 1 つを使用するバインド構成をサポートしのポインターのベスト プラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5e9b3-103">This section describes what a Windows Communication Foundation (WCF) reliable session is, what it's used for, how and when to use one, what binding configurations support it, and pointers on best practices.</span></span> <span data-ttu-id="5e9b3-104">このセクションの重要なポイントと関連するトピックの詳細について、次の表にまとめます。</span><span class="sxs-lookup"><span data-stu-id="5e9b3-104">The following table summarizes details about the essential points and related topics in this section.</span></span>

<span data-ttu-id="5e9b3-105">信頼できるセッションが WCF には、エンドポイント間で送信されるメッセージが SOAP またはトランスポート中継ぎ局を介して転送して、1 回のみと、必要に応じて、送信された順序で配信されることを確認する機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="5e9b3-105">The reliable session WCF provides featrues ensuring that messages sent between endpoints are transferred across SOAP or transport intermediaries and are delivered only once and, optionally, in the same order in which they were sent.</span></span>

<span data-ttu-id="5e9b3-106">で WCF アプリケーションを信頼できるセッションを使用するには、既定またはオプションとして、信頼できるセッションをサポートして WCF でのシステム提供バインディングのいずれかを使用するか、セッションをサポートする独自のカスタム バインドを作成します。</span><span class="sxs-lookup"><span data-stu-id="5e9b3-106">To use a reliable session with a WCF application, either use one of the system-provided bindings in WCF that support a reliable session by default or as an option, or create your own custom binding that supports the session.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5e9b3-107">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="5e9b3-107">In This Section</span></span>

<span data-ttu-id="5e9b3-108">[信頼できるセッションの概要](../../../../docs/framework/wcf/feature-details/reliable-sessions-overview.md) </span><span class="sxs-lookup"><span data-stu-id="5e9b3-108">[Reliable Sessions Overview](../../../../docs/framework/wcf/feature-details/reliable-sessions-overview.md) </span></span>  
<span data-ttu-id="5e9b3-109">信頼できるセッションの概要、信頼できるセッションを使用する状況、信頼できるセッションをサポートする各種のバインディング、および動作のしくみについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5e9b3-109">Describes reliable sessions, when to use them, the different bindings that support reliable sessions, and how they work.</span></span>

<span data-ttu-id="5e9b3-110">[方法: 信頼できるセッション内でメッセージを交換](../../../../docs/framework/wcf/feature-details/how-to-exchange-messages-within-a-reliable-session.md) </span><span class="sxs-lookup"><span data-stu-id="5e9b3-110">[How to: Exchange Messages Within a Reliable Session](../../../../docs/framework/wcf/feature-details/how-to-exchange-messages-within-a-reliable-session.md) </span></span>  
<span data-ttu-id="5e9b3-111">構成で指定したカスタム バインドを使用して、HTTP 上で信頼できるセッションを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5e9b3-111">Describes how to create a reliable session over HTTP using a custom binding specified in the configuration.</span></span>

<span data-ttu-id="5e9b3-112">[方法: 信頼できるセッション内でメッセージをセキュリティ保護します。](../../../../docs/framework/wcf/feature-details/how-to-secure-messages-within-reliable-sessions.md) </span><span class="sxs-lookup"><span data-stu-id="5e9b3-112">[How to: Secure Messages within Reliable Sessions](../../../../docs/framework/wcf/feature-details/how-to-secure-messages-within-reliable-sessions.md) </span></span>  
<span data-ttu-id="5e9b3-113">信頼できるセッションを保護する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5e9b3-113">Describes how to secure a reliable session.</span></span>

<span data-ttu-id="5e9b3-114">[方法: HTTPS で信頼できるセッションをカスタム バインディングを作成します。](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md) </span><span class="sxs-lookup"><span data-stu-id="5e9b3-114">[How to: Create a Custom Reliable Session Binding with HTTPS](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md) </span></span>  
<span data-ttu-id="5e9b3-115">HTTPS 上で信頼できるセッションを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5e9b3-115">Describes how to create a reliable session over HTTPS.</span></span>

<span data-ttu-id="5e9b3-116">[信頼できるセッションのベスト プラクティス](../../../../docs/framework/wcf/feature-details/best-practices-for-reliable-sessions.md) </span><span class="sxs-lookup"><span data-stu-id="5e9b3-116">[Best Practices for Reliable Sessions](../../../../docs/framework/wcf/feature-details/best-practices-for-reliable-sessions.md) </span></span>  
<span data-ttu-id="5e9b3-117">信頼できるセッションの使用に関するベスト プラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5e9b3-117">Describes some of the best practices associated with using a reliable session.</span></span>

## <a name="reference"></a><span data-ttu-id="5e9b3-118">参照</span><span class="sxs-lookup"><span data-stu-id="5e9b3-118">Reference</span></span>

<xref:System.ServiceModel.ReliableSession>

## <a name="see-also"></a><span data-ttu-id="5e9b3-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e9b3-119">See also</span></span>

- [<span data-ttu-id="5e9b3-120">キューと信頼できるセッション</span><span class="sxs-lookup"><span data-stu-id="5e9b3-120">Queues and Reliable Sessions</span></span>](../../../../docs/framework/wcf/feature-details/queues-and-reliable-sessions.md)
- [<span data-ttu-id="5e9b3-121">セッション、インスタンス化、およびコンカレンシー</span><span class="sxs-lookup"><span data-stu-id="5e9b3-121">Sessions, Instancing, and Concurrency</span></span>](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)
