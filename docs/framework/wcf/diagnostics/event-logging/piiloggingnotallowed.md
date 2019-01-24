---
title: PiiLoggingNotAllowed
ms.date: 03/30/2017
ms.assetid: fc34a0b6-fee7-4da4-b146-b0c1c8b7519a
ms.openlocfilehash: 4df8a9cae517baff99f7fb47047a3dd275c63524
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54592654"
---
# <a name="piiloggingnotallowed"></a><span data-ttu-id="29044-102">PiiLoggingNotAllowed</span><span class="sxs-lookup"><span data-stu-id="29044-102">PiiLoggingNotAllowed</span></span>
<span data-ttu-id="29044-103">Id:108</span><span class="sxs-lookup"><span data-stu-id="29044-103">Id: 108</span></span>  
  
 <span data-ttu-id="29044-104">重大度:Error</span><span class="sxs-lookup"><span data-stu-id="29044-104">Severity: Error</span></span>  
  
 <span data-ttu-id="29044-105">カテゴリ:トレース</span><span class="sxs-lookup"><span data-stu-id="29044-105">Category: Tracing</span></span>  
  
## <a name="description"></a><span data-ttu-id="29044-106">説明</span><span class="sxs-lookup"><span data-stu-id="29044-106">Description</span></span>  
 <span data-ttu-id="29044-107">このイベントは、既知の PII がログ記録されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="29044-107">This event indicates that no known PII is being logged.</span></span> <span data-ttu-id="29044-108">既知の PII はログ記録できません。</span><span class="sxs-lookup"><span data-stu-id="29044-108">Logging of known PII is not allowed.</span></span> <span data-ttu-id="29044-109">既知の PII をログ記録できるようにするには、Machine.config の "enableLoggingKnownPii" を `true` に設定します。イベントには、プロセス名とプロセス ID が表示されます。</span><span class="sxs-lookup"><span data-stu-id="29044-109">To allow logging of known PII, set "enableLoggingKnownPii" to `true` in Machine.config. The event lists the process name and process ID.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="29044-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="29044-110">See also</span></span>
- [<span data-ttu-id="29044-111">イベント ログ</span><span class="sxs-lookup"><span data-stu-id="29044-111">Event Logging</span></span>](../../../../../docs/framework/wcf/diagnostics/event-logging/index.md)
- [<span data-ttu-id="29044-112">イベント一覧</span><span class="sxs-lookup"><span data-stu-id="29044-112">Events General Reference</span></span>](../../../../../docs/framework/wcf/diagnostics/event-logging/events-general-reference.md)
