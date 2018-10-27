---
title: 'サービス : 1 秒あたりの承認されていないセキュリティ呼び出し'
ms.date: 03/30/2017
ms.assetid: 1eeade5a-ea62-4757-b1f9-1b1b1746abd1
ms.openlocfilehash: 523e5182ca661e170e5cba01d5221b5c38251959
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/26/2018
ms.locfileid: "50135402"
---
# <a name="service-security-calls-not-authorized-per-second"></a><span data-ttu-id="469d0-102">サービス : 1 秒あたりの承認されていないセキュリティ呼び出し</span><span class="sxs-lookup"><span data-stu-id="469d0-102">Service: Security Calls Not Authorized Per Second</span></span>
<span data-ttu-id="469d0-103">カウンター名 : 1 秒あたりの承認されていないセキュリティ呼び出し</span><span class="sxs-lookup"><span data-stu-id="469d0-103">Counter name: Security Calls Not Authorized Per Second</span></span>  
  
## <a name="description"></a><span data-ttu-id="469d0-104">説明</span><span class="sxs-lookup"><span data-stu-id="469d0-104">Description</span></span>  
 <span data-ttu-id="469d0-105">有効なユーザーから適切な保護を適用して送信されたが、特定のタスクの実行がユーザーに許可されていない受信メッセージの 1 秒あたりの数です。</span><span class="sxs-lookup"><span data-stu-id="469d0-105">Number of incoming messages in one second, which are from a valid user and protected properly, but the user is not authorized to do specific tasks.</span></span>  
  
 <span data-ttu-id="469d0-106">このカウンターは <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> メソッドで `false` が返された場合にインクリメントされます。</span><span class="sxs-lookup"><span data-stu-id="469d0-106">This counter is incremented when the <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> method returns `false`.</span></span>  
  
 <span data-ttu-id="469d0-107">このカウンターは、パフォーマンス カウンター型[PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkId=94649)、次の数式を使用して、その値が計算されます。</span><span class="sxs-lookup"><span data-stu-id="469d0-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkId=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="469d0-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="469d0-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
