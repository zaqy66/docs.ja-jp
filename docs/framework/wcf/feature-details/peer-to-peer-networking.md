---
title: ピアツーピア ネットワーク
ms.date: 03/30/2017
ms.assetid: ad6cb67b-fd1c-4ca1-a767-b410da2e16ca
ms.openlocfilehash: 16416ec467caa10216930ae3c961869cbfcd59d8
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43456986"
---
# <a name="peer-to-peer-networking"></a><span data-ttu-id="07e75-102">ピアツーピア ネットワーク</span><span class="sxs-lookup"><span data-stu-id="07e75-102">Peer-to-Peer Networking</span></span>
<span data-ttu-id="07e75-103">ピア チャネルとは、マルチパーティ、ピア ツー ピア (P2P) 通信技術では、Windows Communication Foundation (WCF) です。</span><span class="sxs-lookup"><span data-stu-id="07e75-103">Peer Channel is a multiparty, peer-to-peer (P2P) communication technology in Windows Communication Foundation (WCF).</span></span> <span data-ttu-id="07e75-104">この技術によって、アプリケーション開発者は安全で拡張可能なメッセージ ベースの P2P 通信チャネルを利用できます。</span><span class="sxs-lookup"><span data-stu-id="07e75-104">It provides a secure and scalable message-based P2P communication channel for application developers.</span></span> <span data-ttu-id="07e75-105">ピア チャネルのメリットを活用するマルチパーティ アプリケーションの一般的な例は、チャットなどの共同作業アプリケーションです。チャットでは、ユーザーのグループがサーバーなしのピアツーピア方式で互いに会話します。</span><span class="sxs-lookup"><span data-stu-id="07e75-105">One common example of a multiparty application that can benefit from Peer Channel is a collaborative application, such as chat, where a group of people chat with one another in a peer-to-peer manner without servers.</span></span> <span data-ttu-id="07e75-106">ピア チャネルを使用することで、顧客シナリオや企業シナリオでの P2P コラボレーション、コンテンツ配布、負荷分散、および分散処理が実現します。</span><span class="sxs-lookup"><span data-stu-id="07e75-106">Peer Channel enables P2P collaboration, content distribution, load balancing, and distributed processing for both consumer and enterprise scenarios.</span></span>  
  
 <span data-ttu-id="07e75-107">ピア チャネルは既定で有効に[!INCLUDE[wv](../../../../includes/wv-md.md)]すべての WCF には、します。</span><span class="sxs-lookup"><span data-stu-id="07e75-107">Peer Channel is enabled by default on [!INCLUDE[wv](../../../../includes/wv-md.md)], as is all of WCF.</span></span> <span data-ttu-id="07e75-108">ピア チャネルのクラスにアクセスするには、プロジェクトに System.ServiceModel.dll への参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="07e75-108">To access Peer Channel classes, add references to System.ServiceModel.dll to your project.</span></span>  
  
 <span data-ttu-id="07e75-109">次の各セクションには、ピアツーピア ネットワークに関する情報と、ピア チャネルのクラスを使用してピア対応のネットワーク アプリケーションを作成する方法が記載されています。</span><span class="sxs-lookup"><span data-stu-id="07e75-109">The following sections contain information about peer-to-peer networking and the use of Peer Channel classes to create peer-enabled network applications.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="07e75-110">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="07e75-110">In This Section</span></span>  
 <span data-ttu-id="07e75-111">[ピア チャネルのシナリオ](../../../../docs/framework/wcf/feature-details/peer-channel-scenarios.md): パブリケーション/サブスクリプション メッセージング、コラボレーション、分散処理、ゲームなど、ピア チャネル Api でサポートされる開発シナ リオをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="07e75-111">[Peer Channel Scenarios](../../../../docs/framework/wcf/feature-details/peer-channel-scenarios.md):  Describes development scenarios supported by the Peer Channel APIs, such as publication/subscription messaging, collaboration, distributed processing, and gaming.</span></span>  
  
 <span data-ttu-id="07e75-112">[ピア チャネルの概念](../../../../docs/framework/wcf/feature-details/peer-channel-concepts.md): について説明しますがピア メッシュ、ピア ノード、ピア チャネルのセキュリティ、およびピア リゾルバー。</span><span class="sxs-lookup"><span data-stu-id="07e75-112">[Peer Channel Concepts](../../../../docs/framework/wcf/feature-details/peer-channel-concepts.md):  Describes Peer Meshes, Peer Nodes, Peer Channel security, and Peer Resolvers.</span></span>  
  
 <span data-ttu-id="07e75-113">[ピア チャネル アプリケーションの構築](../../../../docs/framework/wcf/feature-details/building-a-peer-channel-application.md): ピア チャネル アプリケーションの開発に関するガイダンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="07e75-113">[Building a Peer Channel Application](../../../../docs/framework/wcf/feature-details/building-a-peer-channel-application.md):  Provides guidance on developing Peer Channel applications.</span></span>  
  
## <a name="peer-channel-code-examples"></a><span data-ttu-id="07e75-114">ピア チャネルのコード例</span><span class="sxs-lookup"><span data-stu-id="07e75-114">Peer Channel Code Examples</span></span>  
 [<span data-ttu-id="07e75-115">ピア チャネル カスタム ピア リゾルバー</span><span class="sxs-lookup"><span data-stu-id="07e75-115">Peer Channel Custom Peer Resolver</span></span>](https://msdn.microsoft.com/library/5b75a2bb-7ff1-4a14-abe7-3debf0537d23)  
  
## <a name="peer-channel-team-blog"></a><span data-ttu-id="07e75-116">ピア チャネル チームのブログ</span><span class="sxs-lookup"><span data-stu-id="07e75-116">Peer Channel Team blog</span></span>  
 [<span data-ttu-id="07e75-117">ピア チャネル チームのブログ</span><span class="sxs-lookup"><span data-stu-id="07e75-117">Peer Channel Team Blog</span></span>](https://go.microsoft.com/fwlink/?LinkID=114530)
