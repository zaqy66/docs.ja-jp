---
title: Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished
ms.date: 03/30/2017
ms.assetid: 54b677f7-03ad-40f2-9c5d-297a8ad9bf90
ms.openlocfilehash: 56eb40d4e8b2580ba094e67552872cf558c8a617
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54642296"
---
# <a name="microsofttransactionstransactionbridgeparticipantstatemachinefinished"></a><span data-ttu-id="a1603-102">Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished</span><span class="sxs-lookup"><span data-stu-id="a1603-102">Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished</span></span>
<span data-ttu-id="a1603-103">参加要素の登録リストのステート マシンは完了状態になりました。</span><span class="sxs-lookup"><span data-stu-id="a1603-103">The state machine for a participant enlistment entered the finished state.</span></span>  
  
## <a name="description"></a><span data-ttu-id="a1603-104">説明</span><span class="sxs-lookup"><span data-stu-id="a1603-104">Description</span></span>  
 <span data-ttu-id="a1603-105">下位参加要素登録リストの 2PC 処理が完了したときにトレースされます。</span><span class="sxs-lookup"><span data-stu-id="a1603-105">Traced when a subordinate participant enlistment has completed 2pc processing.</span></span> <span data-ttu-id="a1603-106">登録リストの結果は、Committed または Aborted のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="a1603-106">The outcome for the enlistment can be Committed or Aborted.</span></span> <span data-ttu-id="a1603-107">準備中、すべての参加要素を読み取り専用にする場合にもトレースされます。</span><span class="sxs-lookup"><span data-stu-id="a1603-107">It is also traced if any participant votes ReadOnly during Prepare.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1603-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="a1603-108">See also</span></span>
- [<span data-ttu-id="a1603-109">トレース</span><span class="sxs-lookup"><span data-stu-id="a1603-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="a1603-110">トレースを使用したアプリケーションのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="a1603-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="a1603-111">管理と診断</span><span class="sxs-lookup"><span data-stu-id="a1603-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
