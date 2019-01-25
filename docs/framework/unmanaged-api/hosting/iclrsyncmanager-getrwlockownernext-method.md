---
title: ICLRSyncManager::GetRWLockOwnerNext メソッド
ms.date: 03/30/2017
api_name:
- ICLRSyncManager.GetRWLockOwnerNext
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRSyncManager::GetRWLockOwnerNext
helpviewer_keywords:
- ICLRSyncManager::GetRWLockOwnerNext method [.NET Framework hosting]
- GetRWLockOwnerNext method [.NET Framework hosting]
ms.assetid: 0e025b6a-280e-40a2-a2d0-b15f58777b81
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2d992a3eb05ae59f2dc380338531bdc38c37abfc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54572108"
---
# <a name="iclrsyncmanagergetrwlockownernext-method"></a><span data-ttu-id="574a2-102">ICLRSyncManager::GetRWLockOwnerNext メソッド</span><span class="sxs-lookup"><span data-stu-id="574a2-102">ICLRSyncManager::GetRWLockOwnerNext Method</span></span>
<span data-ttu-id="574a2-103">次の取得[IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)現在のリーダー/ライター ロックでブロックされているインスタンス。</span><span class="sxs-lookup"><span data-stu-id="574a2-103">Gets the next [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance that is blocked on the current reader-writer lock.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="574a2-104">構文</span><span class="sxs-lookup"><span data-stu-id="574a2-104">Syntax</span></span>  
  
```  
HRESULT GetRWLockOwnerNext (  
    [in] SIZE_T       Iterator,  
    [out] IHostTask  *ppOwnerHostTask  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="574a2-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="574a2-105">Parameters</span></span>  
 `Iterator`  
 <span data-ttu-id="574a2-106">[in]呼び出しを使用して作成された反復子[CreateRWLockOwnerIterator](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-createrwlockowneriterator-method.md)します。</span><span class="sxs-lookup"><span data-stu-id="574a2-106">[in] The iterator that was created by using a call to [CreateRWLockOwnerIterator](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-createrwlockowneriterator-method.md).</span></span>  
  
 `ppOwnerHostTask`  
 <span data-ttu-id="574a2-107">[out]次のポインター`IHostTask`待機しているタスクがない場合、ロック、または null を待機しています。</span><span class="sxs-lookup"><span data-stu-id="574a2-107">[out] A pointer to the next `IHostTask` that is waiting on the lock, or null if no task is waiting.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="574a2-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="574a2-108">Return Value</span></span>  
  
|<span data-ttu-id="574a2-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="574a2-109">HRESULT</span></span>|<span data-ttu-id="574a2-110">説明</span><span class="sxs-lookup"><span data-stu-id="574a2-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="574a2-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="574a2-111">S_OK</span></span>|<span data-ttu-id="574a2-112">`GetRWLockOwnerNext` 正常に返されます。</span><span class="sxs-lookup"><span data-stu-id="574a2-112">`GetRWLockOwnerNext` returned successfully.</span></span>|  
|<span data-ttu-id="574a2-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="574a2-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="574a2-114">共通言語ランタイム (CLR) は、プロセスに読み込まれていないか、CLR は状態をマネージ コードを実行または呼び出しを正常に処理ができません。</span><span class="sxs-lookup"><span data-stu-id="574a2-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="574a2-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="574a2-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="574a2-116">呼び出しがタイムアウトになりました。</span><span class="sxs-lookup"><span data-stu-id="574a2-116">The call timed out.</span></span>|  
|<span data-ttu-id="574a2-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="574a2-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="574a2-118">呼び出し元がロックを所有していません。</span><span class="sxs-lookup"><span data-stu-id="574a2-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="574a2-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="574a2-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="574a2-120">イベントがキャンセルされましたブロックされたスレッドまたはファイバーが待機しています。</span><span class="sxs-lookup"><span data-stu-id="574a2-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="574a2-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="574a2-121">E_FAIL</span></span>|<span data-ttu-id="574a2-122">不明な致命的なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="574a2-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="574a2-123">メソッドには、E_FAIL が返される、ときに、CLR は、プロセス内で使用可能ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="574a2-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="574a2-124">メソッドをホストする後続の呼び出しには、HOST_E_CLRNOTAVAILABLE が返されます。</span><span class="sxs-lookup"><span data-stu-id="574a2-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="574a2-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="574a2-125">Remarks</span></span>  
 <span data-ttu-id="574a2-126">場合`ppOwnerHostTask`に設定されている null の場合、イテレーションが終了していると、ホストが呼び出す必要があります、 [DeleteRWLockOwnerIterator](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-deleterwlockowneriterator-method.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="574a2-126">If `ppOwnerHostTask` is set to null, the iteration has terminated, and the host should call the [DeleteRWLockOwnerIterator](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-deleterwlockowneriterator-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="574a2-127">CLR 呼び出し`AddRef`上、`IHostTask`を`ppOwnerHostTask`ホストは、ポインターを保持している間に終了してからこのタスクを防ぐためにポイントします。</span><span class="sxs-lookup"><span data-stu-id="574a2-127">The CLR calls `AddRef` on the `IHostTask` to which `ppOwnerHostTask` points to prevent this task from exiting while the host holds the pointer.</span></span> <span data-ttu-id="574a2-128">ホストが呼び出す必要があります`Release`が完了したら、参照カウントをデクリメントします。</span><span class="sxs-lookup"><span data-stu-id="574a2-128">The host must call `Release` to decrement the reference count when it is finished.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="574a2-129">必要条件</span><span class="sxs-lookup"><span data-stu-id="574a2-129">Requirements</span></span>  
 <span data-ttu-id="574a2-130">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="574a2-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="574a2-131">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="574a2-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="574a2-132">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="574a2-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="574a2-133">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="574a2-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="574a2-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="574a2-134">See also</span></span>
- [<span data-ttu-id="574a2-135">ICLRSyncManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="574a2-135">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [<span data-ttu-id="574a2-136">IHostSyncManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="574a2-136">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
