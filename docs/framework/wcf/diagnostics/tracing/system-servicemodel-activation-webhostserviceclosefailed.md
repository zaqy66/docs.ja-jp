---
title: System.ServiceModel.Activation.WebHostServiceCloseFailed
ms.date: 03/30/2017
ms.assetid: 3cab9856-a5cf-4f0e-a0cb-89425e368f8e
ms.openlocfilehash: 0ed3a9a1c16247f94c739a43d84d51e4750b3c2f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54597659"
---
# <a name="systemservicemodelactivationwebhostserviceclosefailed"></a><span data-ttu-id="eb63b-102">System.ServiceModel.Activation.WebHostServiceCloseFailed</span><span class="sxs-lookup"><span data-stu-id="eb63b-102">System.ServiceModel.Activation.WebHostServiceCloseFailed</span></span>
<span data-ttu-id="eb63b-103">サービスが正常に閉じられず、中止された場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="eb63b-103">Occurs when a service cannot be closed gracefully and is aborted.</span></span>  
  
## <a name="description"></a><span data-ttu-id="eb63b-104">説明</span><span class="sxs-lookup"><span data-stu-id="eb63b-104">Description</span></span>  
 <span data-ttu-id="eb63b-105">このエラー コードはログ ファイルにのみ記録されます。</span><span class="sxs-lookup"><span data-stu-id="eb63b-105">This error code only appears in the log file.</span></span> <span data-ttu-id="eb63b-106">通常は、Abort を既に呼び出した後でサービスを閉じようとした場合などの、プログラミング エラーを示します。</span><span class="sxs-lookup"><span data-stu-id="eb63b-106">It usually indicates a programming error, for example, when you try to close a service after Abort has already been called.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="eb63b-107">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="eb63b-107">Troubleshooting</span></span>  
 <span data-ttu-id="eb63b-108">アプリケーションのソース コードをチェックしてください。</span><span class="sxs-lookup"><span data-stu-id="eb63b-108">Check the application source code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb63b-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb63b-109">See also</span></span>
- [<span data-ttu-id="eb63b-110">トレース</span><span class="sxs-lookup"><span data-stu-id="eb63b-110">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="eb63b-111">トレースを使用したアプリケーションのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="eb63b-111">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="eb63b-112">管理と診断</span><span class="sxs-lookup"><span data-stu-id="eb63b-112">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
