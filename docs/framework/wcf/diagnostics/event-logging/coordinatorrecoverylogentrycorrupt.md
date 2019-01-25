---
title: CoordinatorRecoveryLogEntryCorrupt
ms.date: 03/30/2017
ms.assetid: 3cd0c3e3-84c8-4d43-a561-a8851c78e565
ms.openlocfilehash: 0dc74b784d8a9ed3ab27bb4b8d3de34143f6ce07
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54639485"
---
# <a name="coordinatorrecoverylogentrycorrupt"></a><span data-ttu-id="48a56-102">CoordinatorRecoveryLogEntryCorrupt</span><span class="sxs-lookup"><span data-stu-id="48a56-102">CoordinatorRecoveryLogEntryCorrupt</span></span>
<span data-ttu-id="48a56-103">Id:139</span><span class="sxs-lookup"><span data-stu-id="48a56-103">Id: 139</span></span>  
  
 <span data-ttu-id="48a56-104">重大度:Error</span><span class="sxs-lookup"><span data-stu-id="48a56-104">Severity: Error</span></span>  
  
 <span data-ttu-id="48a56-105">カテゴリ:TransactionBridge</span><span class="sxs-lookup"><span data-stu-id="48a56-105">Category: TransactionBridge</span></span>  
  
## <a name="description"></a><span data-ttu-id="48a56-106">説明</span><span class="sxs-lookup"><span data-stu-id="48a56-106">Description</span></span>  
 <span data-ttu-id="48a56-107">このイベントは、コーディネーターの回復ログ エントリが破損し、逆シリアル化できなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="48a56-107">This event indicates that a  coordinator recovery log entry was corrupt and could not be deserialized.</span></span> <span data-ttu-id="48a56-108">このエラーが原因で、データの損失が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="48a56-108">Data loss may result from this error.</span></span> <span data-ttu-id="48a56-109">イベントには、トランザクション ID、回復データ (Base64 エンコード)、例外、プロセス名、およびプロセス ID が表示されます。</span><span class="sxs-lookup"><span data-stu-id="48a56-109">The event lists the Transaction ID, Recovery data (Base64 encoded), exception, process name and process ID.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48a56-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="48a56-110">See also</span></span>
- [<span data-ttu-id="48a56-111">イベント ログ</span><span class="sxs-lookup"><span data-stu-id="48a56-111">Event Logging</span></span>](../../../../../docs/framework/wcf/diagnostics/event-logging/index.md)
- [<span data-ttu-id="48a56-112">イベント一覧</span><span class="sxs-lookup"><span data-stu-id="48a56-112">Events General Reference</span></span>](../../../../../docs/framework/wcf/diagnostics/event-logging/events-general-reference.md)
