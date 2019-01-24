---
title: IHostSemaphore インターフェイス
ms.date: 03/30/2017
api_name:
- IHostSemaphore
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSemaphore
helpviewer_keywords:
- IHostSemaphore interface [.NET Framework hosting]
ms.assetid: c0765321-656c-441e-bab5-58176292be1e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 33c2a244622f562c074808a78f7c57134d5a9202
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54689066"
---
# <a name="ihostsemaphore-interface"></a><span data-ttu-id="fdbb4-102">IHostSemaphore インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fdbb4-102">IHostSemaphore Interface</span></span>
<span data-ttu-id="fdbb4-103">ホストのスレッド処理のセマフォの実装を表します。</span><span class="sxs-lookup"><span data-stu-id="fdbb4-103">Represents the host's implementation of a semaphore for threading.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="fdbb4-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="fdbb4-104">Methods</span></span>  
  
|<span data-ttu-id="fdbb4-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="fdbb4-105">Method</span></span>|<span data-ttu-id="fdbb4-106">説明</span><span class="sxs-lookup"><span data-stu-id="fdbb4-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="fdbb4-107">ReleaseSemaphore メソッド</span><span class="sxs-lookup"><span data-stu-id="fdbb4-107">ReleaseSemaphore Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-releasesemaphore-method.md)|<span data-ttu-id="fdbb4-108">現在のカウントを増やします`IHostSemaphore`インスタンスを指定の量。</span><span class="sxs-lookup"><span data-stu-id="fdbb4-108">Increases the count of the current `IHostSemaphore` instance by the specified amount.</span></span>|  
|[<span data-ttu-id="fdbb4-109">Wait メソッド</span><span class="sxs-lookup"><span data-stu-id="fdbb4-109">Wait Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-wait-method.md)|<span data-ttu-id="fdbb4-110">現在`IHostSemaphore`所有者になるまで待機するインスタンスまたは指定された時間が経過する量。</span><span class="sxs-lookup"><span data-stu-id="fdbb4-110">Causes the current `IHostSemaphore` instance to wait until it is owned or the specified amount of time elapses.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fdbb4-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="fdbb4-111">Requirements</span></span>  
 <span data-ttu-id="fdbb4-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fdbb4-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fdbb4-113">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="fdbb4-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fdbb4-114">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="fdbb4-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fdbb4-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fdbb4-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fdbb4-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="fdbb4-116">See also</span></span>
- [<span data-ttu-id="fdbb4-117">ICLRSyncManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fdbb4-117">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [<span data-ttu-id="fdbb4-118">IHostAutoEvent インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fdbb4-118">IHostAutoEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md)
- [<span data-ttu-id="fdbb4-119">IHostManualEvent インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fdbb4-119">IHostManualEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md)
- [<span data-ttu-id="fdbb4-120">IHostSyncManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fdbb4-120">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
- [<span data-ttu-id="fdbb4-121">ホスト インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fdbb4-121">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
