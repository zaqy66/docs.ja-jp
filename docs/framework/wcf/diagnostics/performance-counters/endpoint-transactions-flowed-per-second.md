---
title: 'エンドポイント : 1 秒あたりのトランザクション フロー'
ms.date: 03/30/2017
ms.assetid: 0f370ff1-a913-450b-bccb-c279ad165b3d
ms.openlocfilehash: 79f50b6706facd040ec2d325c676f210d5327bf8
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2018
ms.locfileid: "44514330"
---
# <a name="endpoint-transactions-flowed-per-second"></a><span data-ttu-id="0e1a8-102">エンドポイント : 1 秒あたりのトランザクション フロー</span><span class="sxs-lookup"><span data-stu-id="0e1a8-102">Endpoint: Transactions Flowed Per Second</span></span>
<span data-ttu-id="0e1a8-103">カウンター名 : 1 秒あたりのトランザクション フロー。</span><span class="sxs-lookup"><span data-stu-id="0e1a8-103">Counter Name: Transactions Flowed Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="0e1a8-104">説明</span><span class="sxs-lookup"><span data-stu-id="0e1a8-104">Description</span></span>  
 <span data-ttu-id="0e1a8-105">このエンドポイントでの操作に対して実行された 1 秒あたりのトランザクションの数です。</span><span class="sxs-lookup"><span data-stu-id="0e1a8-105">Number of transactions flowed to operations at this endpoint in a second.</span></span> <span data-ttu-id="0e1a8-106">このカウンターは、エンドポイントに送信されたメッセージにトランザクション ID が付与されている場合は常にインクリメントされます。</span><span class="sxs-lookup"><span data-stu-id="0e1a8-106">This counter is incremented any time a transaction ID is present in a message sent to the endpoint.</span></span>  
  
 <span data-ttu-id="0e1a8-107">このカウンターは、パフォーマンス カウンター型[PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649)、次の数式を使用して、その値が計算されます。</span><span class="sxs-lookup"><span data-stu-id="0e1a8-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="0e1a8-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="0e1a8-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
