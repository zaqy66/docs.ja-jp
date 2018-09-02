---
title: 'エンドポイント : 1 秒あたりの承認されていないセキュリティ呼び出し'
ms.date: 03/30/2017
ms.assetid: c8a1547b-986b-45c1-b302-dea0cd4b516d
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 4cefdd7480c7d0e9475b1883e603d9db1f287d4a
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43386625"
---
# <a name="endpoint-security-calls-not-authorized-per-second"></a><span data-ttu-id="d4cef-102">エンドポイント : 1 秒あたりの承認されていないセキュリティ呼び出し</span><span class="sxs-lookup"><span data-stu-id="d4cef-102">Endpoint: Security Calls Not Authorized Per Second</span></span>
<span data-ttu-id="d4cef-103">カウンター名 : 1 秒あたりの承認されていないセキュリティ呼び出し。</span><span class="sxs-lookup"><span data-stu-id="d4cef-103">Counter Name: Security Calls Not Authorized Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="d4cef-104">説明</span><span class="sxs-lookup"><span data-stu-id="d4cef-104">Description</span></span>  
 <span data-ttu-id="d4cef-105">有効なユーザーから適切な保護を適用して送信されたが、特定のタスクの実行がユーザーに許可されていない、受信メッセージの 1 秒あたりの数です。</span><span class="sxs-lookup"><span data-stu-id="d4cef-105">Number of incoming messages in a second that are from a valid user and protected properly, but the user is not authorized to do specific tasks.</span></span>  
  
 <span data-ttu-id="d4cef-106">このカウンターは <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> メソッドで `false` が返された場合にインクリメントされます。</span><span class="sxs-lookup"><span data-stu-id="d4cef-106">This counter is incremented when the <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> method returns `false`.</span></span>  
  
 <span data-ttu-id="d4cef-107">このカウンターは、パフォーマンス カウンター型[PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649)、次の数式を使用して、その値が計算されます。</span><span class="sxs-lookup"><span data-stu-id="d4cef-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="d4cef-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="d4cef-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
