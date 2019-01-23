---
title: Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFaulted
ms.date: 03/30/2017
ms.assetid: 8193027e-9db2-4af9-a072-27300cd24330
ms.openlocfilehash: 6b25c9f9aed30e06d503deb52880ef928857541a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54591047"
---
# <a name="microsofttransactionstransactionbridgeregistrationcoordinatorfaulted"></a><span data-ttu-id="23f5c-102">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFaulted</span><span class="sxs-lookup"><span data-stu-id="23f5c-102">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFaulted</span></span>
<span data-ttu-id="23f5c-103">WS-AT プロトコル サービスは、Register メッセージへの応答として、コーディネーターからエラーを受信しました。</span><span class="sxs-lookup"><span data-stu-id="23f5c-103">The WS-AT protocol service received a fault from its coordinator in response to a Register message.</span></span>  
  
## <a name="description"></a><span data-ttu-id="23f5c-104">説明</span><span class="sxs-lookup"><span data-stu-id="23f5c-104">Description</span></span>  
 <span data-ttu-id="23f5c-105">エラーが返されたためにローカルの TransactionManager がその上位の TransactionManager に登録できない場合に、トレースされます。</span><span class="sxs-lookup"><span data-stu-id="23f5c-105">Traced if the local TransactionManager is not able to Register with its superior TransactionManager due to a fault being returned.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="23f5c-106">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="23f5c-106">Troubleshooting</span></span>  
 <span data-ttu-id="23f5c-107">トレース メッセージを調べて、返されたエラーを確認してください。</span><span class="sxs-lookup"><span data-stu-id="23f5c-107">Inspect the trace message for the fault returned.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="23f5c-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="23f5c-108">See also</span></span>
- [<span data-ttu-id="23f5c-109">トレース</span><span class="sxs-lookup"><span data-stu-id="23f5c-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="23f5c-110">トレースを使用したアプリケーションのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="23f5c-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="23f5c-111">管理と診断</span><span class="sxs-lookup"><span data-stu-id="23f5c-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
