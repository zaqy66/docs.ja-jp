---
title: System.ServiceModel.TxCompletionStatusCompletedForAsyncAbort
ms.date: 03/30/2017
ms.assetid: 155c3203-2e17-4709-b896-2254e22da45e
ms.openlocfilehash: 3d43524b7141a134b9560e92da66ef2349b8119a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631286"
---
# <a name="systemservicemodeltxcompletionstatuscompletedforasyncabort"></a><span data-ttu-id="09c32-102">System.ServiceModel.TxCompletionStatusCompletedForAsyncAbort</span><span class="sxs-lookup"><span data-stu-id="09c32-102">System.ServiceModel.TxCompletionStatusCompletedForAsyncAbort</span></span>
<span data-ttu-id="09c32-103">非同期中止が実行されたため、指定された操作の指定のトランザクションは完了されました。</span><span class="sxs-lookup"><span data-stu-id="09c32-103">The specified transaction for the specified operation was completed due to asynchronous abort.</span></span>  
  
## <a name="description"></a><span data-ttu-id="09c32-104">説明</span><span class="sxs-lookup"><span data-stu-id="09c32-104">Description</span></span>  
 <span data-ttu-id="09c32-105">別の参加要素による中止、タイムアウト、またはトランザクションの参加要素内での別のエラーが発生したため、現在のトランザクションが中止されました。</span><span class="sxs-lookup"><span data-stu-id="09c32-105">The current transaction was aborted due to another participant voting for Abort, time-outs occurring, or another error inside the participant of a transaction.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="09c32-106">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="09c32-106">Troubleshooting</span></span>  
 <span data-ttu-id="09c32-107">予期された中止ではない場合は、すべてのシステム ログを調べて中止の原因を確認してください。</span><span class="sxs-lookup"><span data-stu-id="09c32-107">If this abort is unexpected, check all system logs to determine the real reason for the abort.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09c32-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="09c32-108">See also</span></span>
- [<span data-ttu-id="09c32-109">トレース</span><span class="sxs-lookup"><span data-stu-id="09c32-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="09c32-110">トレースを使用したアプリケーションのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="09c32-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="09c32-111">管理と診断</span><span class="sxs-lookup"><span data-stu-id="09c32-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
