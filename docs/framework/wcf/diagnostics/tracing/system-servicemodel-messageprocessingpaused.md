---
title: System.ServiceModel.MessageProcessingPaused
ms.date: 03/30/2017
ms.assetid: 36b5302a-93cc-478a-9bb2-8a1601fba1df
ms.openlocfilehash: ba067303d861bbd7d88c67f6fd868bd808e07dfd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54528681"
---
# <a name="systemservicemodelmessageprocessingpaused"></a><span data-ttu-id="85a21-102">System.ServiceModel.MessageProcessingPaused</span><span class="sxs-lookup"><span data-stu-id="85a21-102">System.ServiceModel.MessageProcessingPaused</span></span>
<span data-ttu-id="85a21-103">System.ServiceModel.MessageProcessingPaused</span><span class="sxs-lookup"><span data-stu-id="85a21-103">System.ServiceModel.MessageProcessingPaused</span></span>  
  
## <a name="description"></a><span data-ttu-id="85a21-104">説明</span><span class="sxs-lookup"><span data-stu-id="85a21-104">Description</span></span>  
 <span data-ttu-id="85a21-105">メッセージの処理中にスレッドが切り替わりました。</span><span class="sxs-lookup"><span data-stu-id="85a21-105">The threads were switched while processing a message.</span></span>  
  
 <span data-ttu-id="85a21-106">メッセージ処理は、次の理由によって一時停止することがあります。</span><span class="sxs-lookup"><span data-stu-id="85a21-106">Message processing can be paused by the following reasons:</span></span>  
  
-   <span data-ttu-id="85a21-107">ConcurrencyMode が単一または再入可能で、サービスが別のメッセージを処理している。</span><span class="sxs-lookup"><span data-stu-id="85a21-107">ConcurrencyMode is single or reentrant, and the service is processing another message.</span></span>  
  
-   <span data-ttu-id="85a21-108">トランザクションが有効で、サービスが別のトランザクションを処理している。</span><span class="sxs-lookup"><span data-stu-id="85a21-108">Transaction is enabled and the service is processing another transaction.</span></span>  
  
-   <span data-ttu-id="85a21-109">同期コンテキストが最新ではない。</span><span class="sxs-lookup"><span data-stu-id="85a21-109">Synchronization context is not current.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="85a21-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="85a21-110">See also</span></span>
- [<span data-ttu-id="85a21-111">トレース</span><span class="sxs-lookup"><span data-stu-id="85a21-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="85a21-112">トレースを使用したアプリケーションのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="85a21-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="85a21-113">管理と診断</span><span class="sxs-lookup"><span data-stu-id="85a21-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
