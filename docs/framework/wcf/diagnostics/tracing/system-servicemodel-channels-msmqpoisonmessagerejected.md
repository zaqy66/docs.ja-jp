---
title: System.ServiceModel.Channels.MsmqPoisonMessageRejected
ms.date: 03/30/2017
ms.assetid: 0e64b9bd-1f12-43df-a189-d7be3c2bace1
ms.openlocfilehash: c8e476ab90fda9214831fbd5beaba518f3e3bd20
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491429"
---
# <a name="systemservicemodelchannelsmsmqpoisonmessagerejected"></a><span data-ttu-id="a2217-102">System.ServiceModel.Channels.MsmqPoisonMessageRejected</span><span class="sxs-lookup"><span data-stu-id="a2217-102">System.ServiceModel.Channels.MsmqPoisonMessageRejected</span></span>
<span data-ttu-id="a2217-103">有害メッセージは拒否されました。</span><span class="sxs-lookup"><span data-stu-id="a2217-103">Poison message rejected.</span></span>  
  
## <a name="description"></a><span data-ttu-id="a2217-104">説明</span><span class="sxs-lookup"><span data-stu-id="a2217-104">Description</span></span>  
 <span data-ttu-id="a2217-105">このトレースは、有害メッセージが検出され、続いて拒否されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="a2217-105">The trace indicates that a poison message was encountered and subsequently rejected.</span></span> <span data-ttu-id="a2217-106">これは、NetMsmqBinding または MsmqIntegrationBinding の `ReceiveErrorHandling` プロパティが `Reject` に設定されると発生します。</span><span class="sxs-lookup"><span data-stu-id="a2217-106">This occurs when the `ReceiveErrorHandling` property on the NetMsmqBinding or MsmqIntegrationBinding is set to `Reject`.</span></span> <span data-ttu-id="a2217-107">拒否されたメッセージは、送信者に配信されます[配信不能キュー](https://go.microsoft.com/fwlink/?LinkId=99544)します。</span><span class="sxs-lookup"><span data-stu-id="a2217-107">A rejected message is delivered back to the sender’s [Dead-Letter Queue](https://go.microsoft.com/fwlink/?LinkId=99544).</span></span>  
  
 <span data-ttu-id="a2217-108">参照してください[有害メッセージの処理](https://go.microsoft.com/fwlink/?LinkId=99546)メッセージが有害になると、サービスを適切に処理を構成する方法の詳細についてはします。</span><span class="sxs-lookup"><span data-stu-id="a2217-108">See [Poison-Message Handling](https://go.microsoft.com/fwlink/?LinkId=99546) for more details on when messages become poison and how to configure your service to handle them appropriately.</span></span> <span data-ttu-id="a2217-109">参照してください[MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkId=99548)拒否されたメッセージは MSMQ では意味の詳細についてはします。</span><span class="sxs-lookup"><span data-stu-id="a2217-109">See [MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkId=99548) for more details on what a rejected message means in MSMQ.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2217-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="a2217-110">See also</span></span>
- [<span data-ttu-id="a2217-111">トレース</span><span class="sxs-lookup"><span data-stu-id="a2217-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="a2217-112">トレースを使用したアプリケーションのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="a2217-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="a2217-113">管理と診断</span><span class="sxs-lookup"><span data-stu-id="a2217-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
- [<span data-ttu-id="a2217-114">有害メッセージ処理</span><span class="sxs-lookup"><span data-stu-id="a2217-114">Poison-Message Handling</span></span>](https://go.microsoft.com/fwlink/?LinkId=99546)
- [<span data-ttu-id="a2217-115">MQMarkMessageRejected</span><span class="sxs-lookup"><span data-stu-id="a2217-115">MQMarkMessageRejected</span></span>](https://go.microsoft.com/fwlink/?LinkId=99548)
