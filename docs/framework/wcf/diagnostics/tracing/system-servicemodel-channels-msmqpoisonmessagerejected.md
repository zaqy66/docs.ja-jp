---
title: System.ServiceModel.Channels.MsmqPoisonMessageRejected
ms.date: 03/30/2017
ms.assetid: 0e64b9bd-1f12-43df-a189-d7be3c2bace1
ms.openlocfilehash: 27402017e5e79194578719fd0c921dfc1e047b80
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43512961"
---
# <a name="systemservicemodelchannelsmsmqpoisonmessagerejected"></a><span data-ttu-id="16a36-102">System.ServiceModel.Channels.MsmqPoisonMessageRejected</span><span class="sxs-lookup"><span data-stu-id="16a36-102">System.ServiceModel.Channels.MsmqPoisonMessageRejected</span></span>
<span data-ttu-id="16a36-103">有害メッセージは拒否されました。</span><span class="sxs-lookup"><span data-stu-id="16a36-103">Poison message rejected.</span></span>  
  
## <a name="description"></a><span data-ttu-id="16a36-104">説明</span><span class="sxs-lookup"><span data-stu-id="16a36-104">Description</span></span>  
 <span data-ttu-id="16a36-105">このトレースは、有害メッセージが検出され、続いて拒否されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="16a36-105">The trace indicates that a poison message was encountered and subsequently rejected.</span></span> <span data-ttu-id="16a36-106">これは、NetMsmqBinding または MsmqIntegrationBinding の `ReceiveErrorHandling` プロパティが `Reject` に設定されると発生します。</span><span class="sxs-lookup"><span data-stu-id="16a36-106">This occurs when the `ReceiveErrorHandling` property on the NetMsmqBinding or MsmqIntegrationBinding is set to `Reject`.</span></span> <span data-ttu-id="16a36-107">拒否されたメッセージは、送信者に配信されます[配信不能キュー](https://go.microsoft.com/fwlink/?LinkId=99544)します。</span><span class="sxs-lookup"><span data-stu-id="16a36-107">A rejected message is delivered back to the sender’s [Dead-Letter Queue](https://go.microsoft.com/fwlink/?LinkId=99544).</span></span>  
  
 <span data-ttu-id="16a36-108">参照してください[有害メッセージの処理](https://go.microsoft.com/fwlink/?LinkId=99546)メッセージが有害になると、サービスを適切に処理を構成する方法の詳細についてはします。</span><span class="sxs-lookup"><span data-stu-id="16a36-108">See [Poison-Message Handling](https://go.microsoft.com/fwlink/?LinkId=99546) for more details on when messages become poison and how to configure your service to handle them appropriately.</span></span> <span data-ttu-id="16a36-109">参照してください[MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkId=99548)拒否されたメッセージは MSMQ では意味の詳細についてはします。</span><span class="sxs-lookup"><span data-stu-id="16a36-109">See [MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkId=99548) for more details on what a rejected message means in MSMQ.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="16a36-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="16a36-110">See Also</span></span>  
 [<span data-ttu-id="16a36-111">トレース</span><span class="sxs-lookup"><span data-stu-id="16a36-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [<span data-ttu-id="16a36-112">トレースを使用したアプリケーションのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="16a36-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [<span data-ttu-id="16a36-113">管理と診断</span><span class="sxs-lookup"><span data-stu-id="16a36-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)  
 [<span data-ttu-id="16a36-114">有害メッセージ処理</span><span class="sxs-lookup"><span data-stu-id="16a36-114">Poison-Message Handling</span></span>](https://go.microsoft.com/fwlink/?LinkId=99546)  
 [<span data-ttu-id="16a36-115">MQMarkMessageRejected</span><span class="sxs-lookup"><span data-stu-id="16a36-115">MQMarkMessageRejected</span></span>](https://go.microsoft.com/fwlink/?LinkId=99548)
