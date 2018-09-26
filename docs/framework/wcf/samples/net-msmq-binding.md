---
title: ネット MSMQ バインディング
ms.date: 03/30/2017
ms.assetid: fe4bb696-f57c-4cb3-9b7e-9d95fe6b8323
ms.openlocfilehash: ee32ea09eed28c1c7cd5df2df2d13fd5f41f4b22
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47200972"
---
# <a name="net-msmq-binding"></a><span data-ttu-id="a4758-102">ネット MSMQ バインディング</span><span class="sxs-lookup"><span data-stu-id="a4758-102">Net MSMQ Binding</span></span>
<span data-ttu-id="a4758-103">このセクションには、エンドポイント要素の MSMQ バインディング属性の使用方法を示すサンプルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a4758-103">This section contains samples that demonstrate using MSMQ binding attributes of an endpoint element.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="a4758-104">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="a4758-104">In This Section</span></span>  
 [<span data-ttu-id="a4758-105">トランザクション MSMQ バインディング</span><span class="sxs-lookup"><span data-stu-id="a4758-105">Transacted MSMQ Binding</span></span>](../../../../docs/framework/wcf/samples/transacted-msmq-binding.md)  
 <span data-ttu-id="a4758-106">メッセージ キュー (MSMQ) を使用して、トランザクション キューによる通信を実行する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a4758-106">Demonstrates how to perform transacted queued communication by using Message Queuing (MSMQ).</span></span>  
  
 [<span data-ttu-id="a4758-107">揮発性キューによる通信</span><span class="sxs-lookup"><span data-stu-id="a4758-107">Volatile Queued Communication</span></span>](../../../../docs/framework/wcf/samples/volatile-queued-communication.md)  
 <span data-ttu-id="a4758-108">メッセージ キュー (MSMQ) トランスポートで揮発性キューによる通信を実行する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a4758-108">Demonstrates how to perform volatile queued communication over the Message Queuing (MSMQ) transport.</span></span>  
  
 [<span data-ttu-id="a4758-109">配信不能キュー</span><span class="sxs-lookup"><span data-stu-id="a4758-109">Dead Letter Queues</span></span>](../../../../docs/framework/wcf/samples/dead-letter-queues.md)  
 <span data-ttu-id="a4758-110">配信できなかったメッセージの処理方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a4758-110">Demonstrates how to handle and process messages that have failed delivery.</span></span>  
  
 [<span data-ttu-id="a4758-111">MSMQ 4.0 での有害メッセージ処理</span><span class="sxs-lookup"><span data-stu-id="a4758-111">Poison Message Handling in MSMQ 4.0</span></span>](../../../../docs/framework/wcf/samples/poison-message-handling-in-msmq-4-0.md)  
 <span data-ttu-id="a4758-112">MSMQ 4.0 を使用して、サービスで有害メッセージの処理を実行する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a4758-112">Demonstrates how to perform poison message handling in a service using MSMQ 4.0.</span></span>  
  
 [<span data-ttu-id="a4758-113">セッションとキュー</span><span class="sxs-lookup"><span data-stu-id="a4758-113">Sessions and Queues</span></span>](../../../../docs/framework/wcf/samples/sessions-and-queues.md)  
 <span data-ttu-id="a4758-114">メッセージ キュー (MSMQ) トランスポートを介して、キュー通信で一連の関連メッセージを送受信する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a4758-114">Demonstrates how to send and receive a set of related messages in queued communication over the Message Queuing (MSMQ) transport.</span></span>  
  
 [<span data-ttu-id="a4758-115">双方向通信</span><span class="sxs-lookup"><span data-stu-id="a4758-115">Two-Way Communication</span></span>](../../../../docs/framework/wcf/samples/two-way-communication.md)  
 <span data-ttu-id="a4758-116">MSMQ を介して、トランザクション キューによる双方向通信を実行する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a4758-116">Demonstrates how to perform transacted two-way queued communication over MSMQ.</span></span>
  
 [<span data-ttu-id="a4758-117">SRMP</span><span class="sxs-lookup"><span data-stu-id="a4758-117">SRMP</span></span>](../../../../docs/framework/wcf/samples/srmp.md)  
 <span data-ttu-id="a4758-118">HTTP 経由でメッセージ キュー (MSMQ) を使用して、トランザクション キューによる通信を実行する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a4758-118">Demonstrates how to perform transacted queued communication by using Message Queuing (MSMQ) over HTTP.</span></span>  
  
 [<span data-ttu-id="a4758-119">メッセージ キューを介したメッセージ セキュリティ</span><span class="sxs-lookup"><span data-stu-id="a4758-119">Message Security over Message Queuing</span></span>](../../../../docs/framework/wcf/samples/message-security-over-message-queuing.md)  
 <span data-ttu-id="a4758-120">クライアントの認証で X.509v3 証明書による WS-Security を使用するアプリケーションを実装する方法を示します。このアプリケーションでは、MSMQ 経由でサーバーの X.509v3 証明書を使用するサーバー認証が必要です。</span><span class="sxs-lookup"><span data-stu-id="a4758-120">Demonstrates how to implement an application that uses WS-Security with X.509v3 certificate authentication for the client and requires server authentication using the server's X.509v3 certificate over MSMQ.</span></span>
