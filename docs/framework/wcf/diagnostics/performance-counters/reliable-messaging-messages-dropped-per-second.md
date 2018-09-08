---
title: 信頼できるメッセージの 1 秒あたりの破棄されたメッセージ
ms.date: 03/30/2017
ms.assetid: a11b0b80-b242-48e1-b0bb-7f756db5486b
ms.openlocfilehash: 7722b32f99b302c5c272e095033879c9e04c7ee1
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44188921"
---
# <a name="reliable-messaging-messages-dropped-per-second"></a><span data-ttu-id="04e45-102">信頼できるメッセージの 1 秒あたりの破棄されたメッセージ</span><span class="sxs-lookup"><span data-stu-id="04e45-102">Reliable Messaging Messages Dropped Per Second</span></span>
<span data-ttu-id="04e45-103">カウンター名 : 1 秒あたりに破棄された信頼できるメッセージ セッション</span><span class="sxs-lookup"><span data-stu-id="04e45-103">Counter Name: Reliable Messaging Sessions Dropped Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="04e45-104">説明</span><span class="sxs-lookup"><span data-stu-id="04e45-104">Description</span></span>  
 <span data-ttu-id="04e45-105">このサービスで 1 秒間に破棄された信頼できるメッセージング メッセージの合計数です。</span><span class="sxs-lookup"><span data-stu-id="04e45-105">Total number of reliable messaging messages that have been dropped in this service in a second.</span></span>  
  
 <span data-ttu-id="04e45-106">このカウンターは、パフォーマンス カウンター型[PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649)、次の数式を使用して、その値が計算されます。</span><span class="sxs-lookup"><span data-stu-id="04e45-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="04e45-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="04e45-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
