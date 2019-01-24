---
title: System.ServiceModel.MessageClosedAgain
ms.date: 03/30/2017
ms.assetid: 24c274d4-65cd-4c91-9869-bc6eb34ef979
ms.openlocfilehash: bcac4683655476c6aa868232b0483336b815b6cc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54705983"
---
# <a name="systemservicemodelmessageclosedagain"></a><span data-ttu-id="70f2b-102">System.ServiceModel.MessageClosedAgain</span><span class="sxs-lookup"><span data-stu-id="70f2b-102">System.ServiceModel.MessageClosedAgain</span></span>
<span data-ttu-id="70f2b-103">System.ServiceModel.MessageClosedAgain</span><span class="sxs-lookup"><span data-stu-id="70f2b-103">System.ServiceModel.MessageClosedAgain</span></span>  
  
## <a name="description"></a><span data-ttu-id="70f2b-104">説明</span><span class="sxs-lookup"><span data-stu-id="70f2b-104">Description</span></span>  
 <span data-ttu-id="70f2b-105">メッセージがもう一度閉じられました。</span><span class="sxs-lookup"><span data-stu-id="70f2b-105">A message was closed again.</span></span>  
  
 <span data-ttu-id="70f2b-106">メッセージを閉じることができるのは一度だけです。</span><span class="sxs-lookup"><span data-stu-id="70f2b-106">A message should be closed only once.</span></span> <span data-ttu-id="70f2b-107">このトレースがユーザー拡張コード内で出力されている場合は、ユーザー拡張コードは既に閉じられているメッセージをさらに閉じようとしていることが示されています。</span><span class="sxs-lookup"><span data-stu-id="70f2b-107">If this trace is being emitted in user extension code, it indicates that the user extension code is closing a message that has already been closed.</span></span> <span data-ttu-id="70f2b-108">このトレースが製品のコード内で出力されている場合は、ユーザー拡張コードがメッセージを閉じるのが早すぎる可能性があることが示されています。</span><span class="sxs-lookup"><span data-stu-id="70f2b-108">If this trace is being emitted through product code, it indicates that the user extension code could potentially be closing a message too early.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="70f2b-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="70f2b-109">See also</span></span>
- [<span data-ttu-id="70f2b-110">トレース</span><span class="sxs-lookup"><span data-stu-id="70f2b-110">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="70f2b-111">トレースを使用したアプリケーションのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="70f2b-111">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="70f2b-112">管理と診断</span><span class="sxs-lookup"><span data-stu-id="70f2b-112">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
