---
title: エンドポイント:1 秒あたりの失敗した呼び出し
ms.date: 03/30/2017
ms.assetid: bcbe9da4-c8dd-4e27-b630-11611adc7580
ms.openlocfilehash: 03fbdd83246fa811424f445823f705a3bef5697a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54608038"
---
# <a name="endpoint-calls-failed-per-second"></a><span data-ttu-id="03b66-102">エンドポイント:1 秒あたりの失敗した呼び出し</span><span class="sxs-lookup"><span data-stu-id="03b66-102">Endpoint: Calls Failed Per Second</span></span>
<span data-ttu-id="03b66-103">カウンター名:1 秒あたりの呼び出しに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="03b66-103">Counter Name: Calls Failed Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="03b66-104">説明</span><span class="sxs-lookup"><span data-stu-id="03b66-104">Description</span></span>  
 <span data-ttu-id="03b66-105">未処理の例外を伴ってこのエンドポイントに到達した、1 秒あたりの呼び出しの回数。</span><span class="sxs-lookup"><span data-stu-id="03b66-105">Number of calls that have unhandled exceptions and are received by this endpoint in a second.</span></span>  
  
 <span data-ttu-id="03b66-106">このカウンターは、パフォーマンス カウンター型[PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649)、次の数式を使用して、その値が計算されます。</span><span class="sxs-lookup"><span data-stu-id="03b66-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="03b66-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="03b66-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="03b66-108">このカウンターは、このエンドポイントで未処理の例外が発生すると常にインクリメントされます。</span><span class="sxs-lookup"><span data-stu-id="03b66-108">This counter is incremented every time there is an unhandled exception at this endpoint.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="03b66-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="03b66-109">See also</span></span>
- [<span data-ttu-id="03b66-110">コントラクトおよびサービスのエラーの指定と処理</span><span class="sxs-lookup"><span data-stu-id="03b66-110">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
