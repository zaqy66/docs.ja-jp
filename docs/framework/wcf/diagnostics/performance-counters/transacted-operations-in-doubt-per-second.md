---
title: 1 秒あたりの不明なトランザクション操作
ms.date: 03/30/2017
ms.assetid: 7e6b0716-c107-42e5-a21d-31d988e7a691
ms.openlocfilehash: f7365c4e5f03711129916c8c6964f7e25e9b553e
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2018
ms.locfileid: "47027558"
---
# <a name="transacted-operations-in-doubt-per-second"></a><span data-ttu-id="aac24-102">1 秒あたりの不明なトランザクション操作</span><span class="sxs-lookup"><span data-stu-id="aac24-102">Transacted Operations In Doubt Per Second</span></span>
<span data-ttu-id="aac24-103">カウンター名 : 1 秒あたりの不明なトランザクション操作。</span><span class="sxs-lookup"><span data-stu-id="aac24-103">Counter Name: Transacted Operations In Doubt Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="aac24-104">説明</span><span class="sxs-lookup"><span data-stu-id="aac24-104">Description</span></span>  
 <span data-ttu-id="aac24-105">このサービスでの 1 秒あたりの結果が不明なトランザクション操作の数です。</span><span class="sxs-lookup"><span data-stu-id="aac24-105">Number of transactional operations with an in-doubt outcome in this service in a second.</span></span>  
  
 <span data-ttu-id="aac24-106">このカウンターは、パフォーマンス カウンター型[PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649)、次の数式を使用して、その値が計算されます。</span><span class="sxs-lookup"><span data-stu-id="aac24-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="aac24-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="aac24-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
