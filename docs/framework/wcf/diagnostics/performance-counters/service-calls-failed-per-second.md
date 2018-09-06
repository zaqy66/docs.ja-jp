---
title: 'サービス : 1 秒あたりの失敗した呼び出し'
ms.date: 03/30/2017
ms.assetid: 5a2c7939-107d-4f0c-b43c-e02e079e8a9d
ms.openlocfilehash: 9cd649788e1304c68caa1bbf4b5fd27e6fc9d508
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43861817"
---
# <a name="service-calls-failed-per-second"></a><span data-ttu-id="71fab-102">サービス : 1 秒あたりの失敗した呼び出し</span><span class="sxs-lookup"><span data-stu-id="71fab-102">Service: Calls Failed Per Second</span></span>
<span data-ttu-id="71fab-103">カウンター名 : 1 秒あたりの失敗した呼び出し。</span><span class="sxs-lookup"><span data-stu-id="71fab-103">Counter Name: Calls Failed Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="71fab-104">説明</span><span class="sxs-lookup"><span data-stu-id="71fab-104">Description</span></span>  
 <span data-ttu-id="71fab-105">このサービスが 1 秒間に受信した未処理の例外を含む呼び出しの回数。</span><span class="sxs-lookup"><span data-stu-id="71fab-105">Number of calls that have unhandled exceptions, and are received by this service in a second.</span></span>  
  
 <span data-ttu-id="71fab-106">このカウンターは、パフォーマンス カウンター型[PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649)、次の数式を使用して、その値が計算されます。</span><span class="sxs-lookup"><span data-stu-id="71fab-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="71fab-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="71fab-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="71fab-108">マネージド コードでは、エラー条件が発生すると例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="71fab-108">In managed code, exceptions are thrown when error conditions occur.</span></span>  
  
 <span data-ttu-id="71fab-109">マネージド コードでは、エラー条件が発生すると例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="71fab-109">In managed code, exceptions are thrown when error conditions occur.</span></span>  
  
 <span data-ttu-id="71fab-110">このカウンターは、このサービスで未処理の例外が発生するたびにインクリメントされます。</span><span class="sxs-lookup"><span data-stu-id="71fab-110">This counter is incremented every time there is an unhandled exception in this service.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71fab-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="71fab-111">See Also</span></span>  
 [<span data-ttu-id="71fab-112">コントラクトおよびサービスのエラーの指定と処理</span><span class="sxs-lookup"><span data-stu-id="71fab-112">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
