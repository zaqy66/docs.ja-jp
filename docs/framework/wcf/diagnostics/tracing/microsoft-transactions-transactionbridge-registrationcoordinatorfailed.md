---
title: Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFailed
ms.date: 03/30/2017
ms.assetid: 96474056-0418-41e4-8c75-bbc0a853eaba
ms.openlocfilehash: 5c8592ac34375445964b3dbcbbd4800c47e53850
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54515051"
---
# <a name="microsofttransactionstransactionbridgeregistrationcoordinatorfailed"></a><span data-ttu-id="e1db6-102">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFailed</span><span class="sxs-lookup"><span data-stu-id="e1db6-102">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFailed</span></span>
<span data-ttu-id="e1db6-103">WS-AT プロトコル サービスは、Register メッセージをコーディネーターに送信できませんでした。</span><span class="sxs-lookup"><span data-stu-id="e1db6-103">The WS-AT protocol service failed to send a Register message to its coordinator</span></span>  
  
## <a name="description"></a><span data-ttu-id="e1db6-104">説明</span><span class="sxs-lookup"><span data-stu-id="e1db6-104">Description</span></span>  
 <span data-ttu-id="e1db6-105">メッセージを送信できないために、ローカルの TransactionManager がその上位の TransactionManager に登録できない場合にトレースされます。</span><span class="sxs-lookup"><span data-stu-id="e1db6-105">Traced if the local TransactionManager is not able to Register with its superior TransactionManager due to the inability to send a message.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="e1db6-106">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e1db6-106">Troubleshooting</span></span>  
 <span data-ttu-id="e1db6-107">トレース メッセージを調べて、メッセージの送信エラーの原因となった例外を確認してください。</span><span class="sxs-lookup"><span data-stu-id="e1db6-107">Inspect the trace message for the exception causing the message send failure</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e1db6-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="e1db6-108">See also</span></span>
- [<span data-ttu-id="e1db6-109">トレース</span><span class="sxs-lookup"><span data-stu-id="e1db6-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="e1db6-110">トレースを使用したアプリケーションのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e1db6-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="e1db6-111">管理と診断</span><span class="sxs-lookup"><span data-stu-id="e1db6-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
