---
title: 1 秒あたりの失敗した呼び出し
ms.date: 03/30/2017
ms.assetid: 81c88073-8e32-4520-a71a-2c56b71ee515
ms.openlocfilehash: 03ee2155504a021efadac00df6f7b9271baa5a65
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43505780"
---
# <a name="calls-faulted-per-second"></a><span data-ttu-id="d6f40-102">1 秒あたりの失敗した呼び出し</span><span class="sxs-lookup"><span data-stu-id="d6f40-102">Calls Faulted Per Second</span></span>
<span data-ttu-id="d6f40-103">カウンター名 : 1 秒あたりの失敗した呼び出し</span><span class="sxs-lookup"><span data-stu-id="d6f40-103">Counter Name: Calls Faulted Per Second</span></span>  
  
## <a name="description"></a><span data-ttu-id="d6f40-104">説明</span><span class="sxs-lookup"><span data-stu-id="d6f40-104">Description</span></span>  
 <span data-ttu-id="d6f40-105">この操作への呼び出しに失敗した回数です (1 秒あたり)。</span><span class="sxs-lookup"><span data-stu-id="d6f40-105">Number of calls that returned faults to this operation in a second.</span></span>  
  
 <span data-ttu-id="d6f40-106">このカウンターは、パフォーマンス カウンター型[PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649)、次の数式を使用して、その値が計算されます。</span><span class="sxs-lookup"><span data-stu-id="d6f40-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="d6f40-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="d6f40-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="d6f40-108">Windows Communication Foundation (WCF) アプリケーションでは、サービス メソッドは、SOAP エラー メッセージを使用して、処理のエラー情報を通知します。</span><span class="sxs-lookup"><span data-stu-id="d6f40-108">In Windows Communication Foundation (WCF) applications, service methods communicate processing error information using SOAP fault messages.</span></span> <span data-ttu-id="d6f40-109">SOAP エラーは、サービス操作のメタデータに含まれるメッセージ型であり、堅牢かつインタラクティブに実行できるようにクライアントが使用するエラー コントラクトを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d6f40-109">SOAP faults are message types that are included in the metadata for a service operation and therefore create a fault contract that clients can use to make their execution more robust or interactive.</span></span> <span data-ttu-id="d6f40-110">SOAP エラーは XML 形式でクライアントに渡されるので、相互運用性の面でも優れています。</span><span class="sxs-lookup"><span data-stu-id="d6f40-110">Since SOAP faults are expressed to clients in XML form, they are highly interoperable.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d6f40-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="d6f40-111">See Also</span></span>  
 [<span data-ttu-id="d6f40-112">コントラクトおよびサービスのエラーの指定と処理</span><span class="sxs-lookup"><span data-stu-id="d6f40-112">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
