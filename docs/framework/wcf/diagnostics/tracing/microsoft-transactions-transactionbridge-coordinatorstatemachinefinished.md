---
title: Microsoft.Transactions.TransactionBridge.CoordinatorStateMachineFinished
ms.date: 03/30/2017
ms.assetid: 16cb428d-d886-4789-a961-6fded4b0dbba
ms.openlocfilehash: 8cc32e7b38bfd1bdafd2377ad759f98b248d722e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54710457"
---
# <a name="microsofttransactionstransactionbridgecoordinatorstatemachinefinished"></a><span data-ttu-id="b708e-102">Microsoft.Transactions.TransactionBridge.CoordinatorStateMachineFinished</span><span class="sxs-lookup"><span data-stu-id="b708e-102">Microsoft.Transactions.TransactionBridge.CoordinatorStateMachineFinished</span></span>
<span data-ttu-id="b708e-103">コーディネーターの登録リストのステート マシンが完了状態になりました。</span><span class="sxs-lookup"><span data-stu-id="b708e-103">The state machine for a coordinator enlistment has entered the finished state.</span></span>  
  
## <a name="description"></a><span data-ttu-id="b708e-104">説明</span><span class="sxs-lookup"><span data-stu-id="b708e-104">Description</span></span>  
 <span data-ttu-id="b708e-105">上位のコーディネーターの登録リストが 2PC 処理を完了したとローカル トランザクション マネージャーが判断したときに、トレースされます。</span><span class="sxs-lookup"><span data-stu-id="b708e-105">Traced when the local Transaction Manager believes a superior coordinator enlistment has completed 2pc processing.</span></span> <span data-ttu-id="b708e-106">登録リストの結果は、Committed、Aborted、または Forgotten のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="b708e-106">The outcome for the enlistment can be Committed or Aborted or Forgotten.</span></span> <span data-ttu-id="b708e-107">ローカル トランザクション マネージャーが準備中に読み取り専用にする場合にもトレースされます。</span><span class="sxs-lookup"><span data-stu-id="b708e-107">It is also traced if the local Transaction Manager votes ReadOnly during Prepare.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b708e-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="b708e-108">See also</span></span>
- [<span data-ttu-id="b708e-109">トレース</span><span class="sxs-lookup"><span data-stu-id="b708e-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="b708e-110">トレースを使用したアプリケーションのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="b708e-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="b708e-111">管理と診断</span><span class="sxs-lookup"><span data-stu-id="b708e-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
