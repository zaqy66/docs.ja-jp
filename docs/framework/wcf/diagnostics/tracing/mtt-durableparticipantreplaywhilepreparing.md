---
title: Microsoft.Transactions.TransactionBridge.DurableParticipantReplayWhilePreparing
ms.date: 03/30/2017
ms.assetid: 10ef3876-6f8e-4d4e-8444-f47847b64795
ms.openlocfilehash: 3b51a100677221866186b2e24f34396c012d11c1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54603132"
---
# <a name="microsofttransactionstransactionbridgedurableparticipantreplaywhilepreparing"></a><span data-ttu-id="25d9a-102">Microsoft.Transactions.TransactionBridge.DurableParticipantReplayWhilePreparing</span><span class="sxs-lookup"><span data-stu-id="25d9a-102">Microsoft.Transactions.TransactionBridge.DurableParticipantReplayWhilePreparing</span></span>
<span data-ttu-id="25d9a-103">WS-AT プロトコル サービスは、準備メッセージに応答していない永続的な参加要素から、リプレイ メッセージを受信しました。</span><span class="sxs-lookup"><span data-stu-id="25d9a-103">The WS-AT protocol service received a Replay message from a durable participant, which did not respond to Prepare.</span></span> <span data-ttu-id="25d9a-104">そのため、トランザクションが中止されました。</span><span class="sxs-lookup"><span data-stu-id="25d9a-104">Consequently, the transaction was aborted.</span></span>  
  
## <a name="description"></a><span data-ttu-id="25d9a-105">説明</span><span class="sxs-lookup"><span data-stu-id="25d9a-105">Description</span></span>  
 <span data-ttu-id="25d9a-106">永続的な参加要素がまだ準備している間にリプレイ メッセージが受信された場合は、トレースされます。</span><span class="sxs-lookup"><span data-stu-id="25d9a-106">Traced if a Replay message is received while a Durable participant is still Preparing.</span></span> <span data-ttu-id="25d9a-107">これは、この状態に対して無効なメッセージであり、トランザクションは中止されます。</span><span class="sxs-lookup"><span data-stu-id="25d9a-107">This is an illegal message for this state and the transaction is going to be aborted.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="25d9a-108">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="25d9a-108">Troubleshooting</span></span>  
 <span data-ttu-id="25d9a-109">このエラー メッセージは、永続的な参加要素 (下位トランザクション マネージャーを含む) がエラーから回復したが、トランザクション結果が不明であるため、状態を要求していることを示している場合があります。</span><span class="sxs-lookup"><span data-stu-id="25d9a-109">Receiving this error can indiate that a Durable participant (including Subordinate TransactionManagers) has recovered from failure, however it is unsure of the transaction outcome and request its status.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="25d9a-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="25d9a-110">See also</span></span>
- [<span data-ttu-id="25d9a-111">トレース</span><span class="sxs-lookup"><span data-stu-id="25d9a-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="25d9a-112">トレースを使用したアプリケーションのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="25d9a-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="25d9a-113">管理と診断</span><span class="sxs-lookup"><span data-stu-id="25d9a-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
