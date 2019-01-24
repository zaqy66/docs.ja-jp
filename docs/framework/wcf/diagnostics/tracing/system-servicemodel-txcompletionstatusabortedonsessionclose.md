---
title: System.ServiceModel.TxCompletionStatusAbortedOnSessionClose
ms.date: 03/30/2017
ms.assetid: 7e142e9d-e81b-4309-974a-02e9cc064ea0
ms.openlocfilehash: f41fd08138591a90b6173b5e4806e5ac73ff07da
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54662765"
---
# <a name="systemservicemodeltxcompletionstatusabortedonsessionclose"></a><span data-ttu-id="36cb8-102">System.ServiceModel.TxCompletionStatusAbortedOnSessionClose</span><span class="sxs-lookup"><span data-stu-id="36cb8-102">System.ServiceModel.TxCompletionStatusAbortedOnSessionClose</span></span>
<span data-ttu-id="36cb8-103">指定されたトランザクションは、セッションが終了したときにまだ完了しておらず、TransactionAutoCompleteOnSessionClose OperationBehaviorAttribute が false に設定されているため、中止されました。</span><span class="sxs-lookup"><span data-stu-id="36cb8-103">The specified transaction was aborted because it was uncompleted when the session was closed and the TransactionAutoCompleteOnSessionClose OperationBehaviorAttribute was set to false.</span></span>  
  
## <a name="description"></a><span data-ttu-id="36cb8-104">説明</span><span class="sxs-lookup"><span data-stu-id="36cb8-104">Description</span></span>  
 <span data-ttu-id="36cb8-105">現在のアクティブなセッションが終了した時点でトランザクションが完了しておらず、TransactionAutoCompleteOnSessionClose が `false` に設定されている場合にトレースされます。</span><span class="sxs-lookup"><span data-stu-id="36cb8-105">Traced if the current active session was closed, and the transaction was not completed, and TransactionAutoCompleteOnSessionClose is set to `false`.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="36cb8-106">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="36cb8-106">Troubleshooting</span></span>  
 <span data-ttu-id="36cb8-107">このトレースは、アプリケーションに調査が必要なバグが含まれている可能性があることを示します。</span><span class="sxs-lookup"><span data-stu-id="36cb8-107">This trace indicates a potential application bug that should be investigated.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="36cb8-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="36cb8-108">See also</span></span>
- [<span data-ttu-id="36cb8-109">トレース</span><span class="sxs-lookup"><span data-stu-id="36cb8-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="36cb8-110">トレースを使用したアプリケーションのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="36cb8-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="36cb8-111">管理と診断</span><span class="sxs-lookup"><span data-stu-id="36cb8-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
