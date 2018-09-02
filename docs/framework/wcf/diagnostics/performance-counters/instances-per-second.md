---
title: 1 秒あたりのインスタンス
ms.date: 03/30/2017
ms.assetid: 74579397-1058-4278-80cf-2d00854a480f
ms.openlocfilehash: f0797c38a5eb7399817eaf6aad9fb5b6ecbfab89
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43387908"
---
# <a name="instances-per-second"></a><span data-ttu-id="4e0d9-102">1 秒あたりのインスタンス</span><span class="sxs-lookup"><span data-stu-id="4e0d9-102">Instances Per Second</span></span>
<span data-ttu-id="4e0d9-103">カウンター名 : 1 秒あたりに作成されたインスタンス。</span><span class="sxs-lookup"><span data-stu-id="4e0d9-103">Counter Name: Instances Created Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="4e0d9-104">説明</span><span class="sxs-lookup"><span data-stu-id="4e0d9-104">Description</span></span>  
 <span data-ttu-id="4e0d9-105">1 秒あたりに作成されたサービス インスタンスの合計数です。</span><span class="sxs-lookup"><span data-stu-id="4e0d9-105">Total number of service instances created in a second.</span></span>  
  
 <span data-ttu-id="4e0d9-106">このカウンターは、パフォーマンス カウンター型[PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649)、次の数式を使用して、その値が計算されます。</span><span class="sxs-lookup"><span data-stu-id="4e0d9-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="4e0d9-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="4e0d9-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
