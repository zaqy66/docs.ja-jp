---
title: System.ServiceModel.Channels.MsmqMessageRejected
ms.date: 03/30/2017
ms.assetid: 9b7c10a7-2af6-44a2-8b1a-90bba0c7cf26
ms.openlocfilehash: 0addf987eac62c750a3c418e1b1c431d3f9bc1b0
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47195623"
---
# <a name="systemservicemodelchannelsmsmqmessagerejected"></a><span data-ttu-id="ac3c4-102">System.ServiceModel.Channels.MsmqMessageRejected</span><span class="sxs-lookup"><span data-stu-id="ac3c4-102">System.ServiceModel.Channels.MsmqMessageRejected</span></span>
<span data-ttu-id="ac3c4-103">MSMQ はメッセージを拒否しました。</span><span class="sxs-lookup"><span data-stu-id="ac3c4-103">MSMQ rejected the message.</span></span>  
  
## <a name="description"></a><span data-ttu-id="ac3c4-104">説明</span><span class="sxs-lookup"><span data-stu-id="ac3c4-104">Description</span></span>  
 <span data-ttu-id="ac3c4-105">このトレースは、MSMQ メッセージが拒否されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="ac3c4-105">This trace indicates that an MSMQ message was rejected.</span></span>  
  
 <span data-ttu-id="ac3c4-106">Windows Communication Foundation (WCF) が (NetMsmqBinding または MsmqIntegrationBinding のいずれかで使用) が、それらを処理できない場合、MSMQ メッセージを拒否できます。</span><span class="sxs-lookup"><span data-stu-id="ac3c4-106">MSMQ messages can be rejected when Windows Communication Foundation (WCF) (used with either the NetMsmqBinding or MsmqIntegrationBinding) is unable to process them.</span></span> <span data-ttu-id="ac3c4-107">このようなメッセージは、有害メッセージと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="ac3c4-107">Such messages are referred to as poison messages.</span></span> <span data-ttu-id="ac3c4-108">有害メッセージは、NetMsmqBinding または MsmqIntegrationBinding の `ReceiveErrorHandling` プロパティが `Reject` に設定されると拒否されます。</span><span class="sxs-lookup"><span data-stu-id="ac3c4-108">A poison message is rejected when the `ReceiveErrorHandling` property on the NetMsmqBinding or MsmqIntegrationBinding is set to `Reject`.</span></span> <span data-ttu-id="ac3c4-109">拒否されたメッセージは、送信者に配信されます[配信不能キュー](https://go.microsoft.com/fwlink/?LinkID=99544)します。</span><span class="sxs-lookup"><span data-stu-id="ac3c4-109">A rejected message is delivered back to the sender’s [Dead-Letter Queue](https://go.microsoft.com/fwlink/?LinkID=99544).</span></span>  
  
 <span data-ttu-id="ac3c4-110">参照してください[有害メッセージの処理](https://go.microsoft.com/fwlink/?LinkID=99546)メッセージが有害になると、サービスを適切に処理を構成する方法の詳細についてはします。</span><span class="sxs-lookup"><span data-stu-id="ac3c4-110">See [Poison-Message Handling](https://go.microsoft.com/fwlink/?LinkID=99546) for more details on when messages become poison and how to configure your service to handle them appropriately.</span></span>  
  
 <span data-ttu-id="ac3c4-111">参照してください[MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkID=99548)拒否されたメッセージは MSMQ では意味の詳細についてはします。</span><span class="sxs-lookup"><span data-stu-id="ac3c4-111">See [MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkID=99548) for more details on what a rejected message means in MSMQ.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac3c4-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="ac3c4-112">See Also</span></span>  
 [<span data-ttu-id="ac3c4-113">トレース</span><span class="sxs-lookup"><span data-stu-id="ac3c4-113">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [<span data-ttu-id="ac3c4-114">トレースを使用したアプリケーションのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="ac3c4-114">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [<span data-ttu-id="ac3c4-115">管理と診断</span><span class="sxs-lookup"><span data-stu-id="ac3c4-115">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)  
 [<span data-ttu-id="ac3c4-116">有害メッセージ処理</span><span class="sxs-lookup"><span data-stu-id="ac3c4-116">Poison-Message Handling</span></span>](https://go.microsoft.com/fwlink/?LinkID=99546)  
 [<span data-ttu-id="ac3c4-117">MQMarkMessageRejected</span><span class="sxs-lookup"><span data-stu-id="ac3c4-117">MQMarkMessageRejected</span></span>](https://go.microsoft.com/fwlink/?LinkID=99548)
