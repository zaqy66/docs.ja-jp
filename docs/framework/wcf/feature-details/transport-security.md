---
title: トランスポート セキュリティ
ms.date: 03/30/2017
ms.assetid: 86c94153-e48d-4539-b6cf-cd8060582e7f
ms.openlocfilehash: 7fab84b830917c22d684a06dfbfb2dd540703845
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50192500"
---
# <a name="transport-security"></a><span data-ttu-id="e7a23-102">トランスポート セキュリティ</span><span class="sxs-lookup"><span data-stu-id="e7a23-102">Transport Security</span></span>
<span data-ttu-id="e7a23-103">Windows Communication Foundation (WCF) でのトランスポート セキュリティは、選択したバインドに依存します。</span><span class="sxs-lookup"><span data-stu-id="e7a23-103">Transport security in Windows Communication Foundation (WCF) depends on the binding selected.</span></span> <span data-ttu-id="e7a23-104">バインディングが実装するトランスポートによって実際のセキュリティ機構が決まります。</span><span class="sxs-lookup"><span data-stu-id="e7a23-104">The transport that the binding implements determines the actual security mechanism.</span></span> <span data-ttu-id="e7a23-105">このセクションの各トピックでは、実装される機構とそのオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e7a23-105">The topics in this section explain the mechanisms that are implemented and their options.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="e7a23-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="e7a23-106">In This Section</span></span>  
 [<span data-ttu-id="e7a23-107">トランスポート セキュリティの概要</span><span class="sxs-lookup"><span data-stu-id="e7a23-107">Transport Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/transport-security-overview.md)  
 <span data-ttu-id="e7a23-108">WCF でのトランスポート セキュリティの基本について説明します。</span><span class="sxs-lookup"><span data-stu-id="e7a23-108">Explains the basics of transport security in WCF.</span></span>  
  
 [<span data-ttu-id="e7a23-109">HTTP トランスポート セキュリティ</span><span class="sxs-lookup"><span data-stu-id="e7a23-109">HTTP Transport Security</span></span>](../../../../docs/framework/wcf/feature-details/http-transport-security.md)  
 <span data-ttu-id="e7a23-110">WCF が (、SSL または HTTPS) の Secure Sockets Layer を実装する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e7a23-110">Explains how WCF implements Secure Sockets Layer (SSL, or HTTPS).</span></span>  
  
 [<span data-ttu-id="e7a23-111">HTTP 認証の理解</span><span class="sxs-lookup"><span data-stu-id="e7a23-111">Understanding HTTP Authentication</span></span>](../../../../docs/framework/wcf/feature-details/understanding-http-authentication.md)  
 <span data-ttu-id="e7a23-112">HTTP 認証方式 (基本、ダイジェスト、NTLM (NT LAN Manager) など) について説明します。</span><span class="sxs-lookup"><span data-stu-id="e7a23-112">Describes HTTP authentication schemes, such as Basic, Digest, NT LAN Manager (NTLM), and others.</span></span>  
  
 [<span data-ttu-id="e7a23-113">トランスポート セキュリティでの偽装の使用</span><span class="sxs-lookup"><span data-stu-id="e7a23-113">Using Impersonation with Transport Security</span></span>](../../../../docs/framework/wcf/feature-details/using-impersonation-with-transport-security.md)  
 <span data-ttu-id="e7a23-114">トランスポート セキュリティ モードで使用できる 5 つの偽装レベルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e7a23-114">Explains the five levels of impersonation that are possible with transport security mode.</span></span>  
  
 [<span data-ttu-id="e7a23-115">方法 : SSL 証明書を使用してポートを構成する</span><span class="sxs-lookup"><span data-stu-id="e7a23-115">How to: Configure a Port with an SSL Certificate</span></span>](../../../../docs/framework/wcf/feature-details/how-to-configure-a-port-with-an-ssl-certificate.md)  
 <span data-ttu-id="e7a23-116">SSL (トランスポート) セキュリティを実現するために、X.509 証明書を使用してコンピューターのポートを構成する際の基本事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="e7a23-116">Walks through the basics of configuring a port on a machine with an X.509 certificate for SSL (transport) security.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="e7a23-117">参照</span><span class="sxs-lookup"><span data-stu-id="e7a23-117">Reference</span></span>  
 <xref:System.ServiceModel>  
  
 <xref:System.ServiceModel.Channels>  
  
 <xref:System.ServiceModel.Security>  
  
## <a name="related-sections"></a><span data-ttu-id="e7a23-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7a23-118">Related Sections</span></span>  
 [<span data-ttu-id="e7a23-119">サービスおよびクライアントのセキュリティ保護</span><span class="sxs-lookup"><span data-stu-id="e7a23-119">Securing Services and Clients</span></span>](../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
  
## <a name="see-also"></a><span data-ttu-id="e7a23-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7a23-120">See Also</span></span>  
 [<span data-ttu-id="e7a23-121">WCF セキュリティのプログラミング</span><span class="sxs-lookup"><span data-stu-id="e7a23-121">Programming WCF Security</span></span>](../../../../docs/framework/wcf/feature-details/programming-wcf-security.md)
