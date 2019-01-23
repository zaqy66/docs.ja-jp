---
title: IHostTask::SetCLRTask メソッド
ms.date: 03/30/2017
api_name:
- IHostTask.SetCLRTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTask::SetCLRTask
helpviewer_keywords:
- SetCLRTask method [.NET Framework hosting]
- IHostTask::SetCLRTask method [.NET Framework hosting]
ms.assetid: e9d39c80-41a1-49e7-bb5e-ea3433bfb5d7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bce823bd6a9ad26a705649a666aeb97dcfa0cdbc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54636548"
---
# <a name="ihosttasksetclrtask-method"></a><span data-ttu-id="56ecb-102">IHostTask::SetCLRTask メソッド</span><span class="sxs-lookup"><span data-stu-id="56ecb-102">IHostTask::SetCLRTask Method</span></span>
<span data-ttu-id="56ecb-103">関連付けます、`ICLRTask`を現在[IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)インスタンス。</span><span class="sxs-lookup"><span data-stu-id="56ecb-103">Associates an `ICLRTask` instance with the current [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="56ecb-104">構文</span><span class="sxs-lookup"><span data-stu-id="56ecb-104">Syntax</span></span>  
  
```  
HRESULT SetCLRTask (  
    [in] ICLRTask *pCLRTask  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="56ecb-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="56ecb-105">Parameters</span></span>  
 `pCLRTask`  
 <span data-ttu-id="56ecb-106">[in]インターフェイス ポインター、`ICLRTask`インスタンスに現在関連付けられる`IHostTask`インスタンス。</span><span class="sxs-lookup"><span data-stu-id="56ecb-106">[in] An interface pointer to the `ICLRTask` instance to be associated with the current `IHostTask` instance.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="56ecb-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="56ecb-107">Return Value</span></span>  
  
|<span data-ttu-id="56ecb-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="56ecb-108">HRESULT</span></span>|<span data-ttu-id="56ecb-109">説明</span><span class="sxs-lookup"><span data-stu-id="56ecb-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="56ecb-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="56ecb-110">S_OK</span></span>|<span data-ttu-id="56ecb-111">`SetCLRTask` 正常に返されます。</span><span class="sxs-lookup"><span data-stu-id="56ecb-111">`SetCLRTask` returned successfully.</span></span>|  
|<span data-ttu-id="56ecb-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="56ecb-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="56ecb-113">共通言語ランタイム (CLR) は、プロセスに読み込まれていないか、CLR は状態をマネージ コードを実行または呼び出しを正常に処理ができません。</span><span class="sxs-lookup"><span data-stu-id="56ecb-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="56ecb-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="56ecb-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="56ecb-115">呼び出しがタイムアウトになりました。</span><span class="sxs-lookup"><span data-stu-id="56ecb-115">The call timed out.</span></span>|  
|<span data-ttu-id="56ecb-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="56ecb-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="56ecb-117">呼び出し元がロックを所有していません。</span><span class="sxs-lookup"><span data-stu-id="56ecb-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="56ecb-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="56ecb-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="56ecb-119">イベントがキャンセルされましたブロックされたスレッドまたはファイバーが待機しています。</span><span class="sxs-lookup"><span data-stu-id="56ecb-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="56ecb-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="56ecb-120">E_FAIL</span></span>|<span data-ttu-id="56ecb-121">不明な致命的なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="56ecb-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="56ecb-122">メソッドには、E_FAIL が返される、ときに、CLR は、プロセス内で使用可能ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="56ecb-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="56ecb-123">メソッドをホストする後続の呼び出しには、HOST_E_CLRNOTAVAILABLE が返されます。</span><span class="sxs-lookup"><span data-stu-id="56ecb-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="56ecb-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="56ecb-124">Remarks</span></span>  
 <span data-ttu-id="56ecb-125">CLR 呼び出し`SetCLRTask`に関連付ける、`ICLRTask`を現在`IHostTask`インスタンスへの呼び出しによって作成された[ihosttaskmanager::createtask](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-createtask-method.md)します。</span><span class="sxs-lookup"><span data-stu-id="56ecb-125">The CLR calls `SetCLRTask` to associate an `ICLRTask` instance with the current `IHostTask` instance, which was created by a call to [IHostTaskManager::CreateTask](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-createtask-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="56ecb-126">必要条件</span><span class="sxs-lookup"><span data-stu-id="56ecb-126">Requirements</span></span>  
 <span data-ttu-id="56ecb-127">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="56ecb-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="56ecb-128">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="56ecb-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="56ecb-129">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="56ecb-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="56ecb-130">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="56ecb-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="56ecb-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="56ecb-131">See also</span></span>
- [<span data-ttu-id="56ecb-132">ICLRTask インターフェイス</span><span class="sxs-lookup"><span data-stu-id="56ecb-132">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="56ecb-133">ICLRTaskManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="56ecb-133">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="56ecb-134">IHostTask インターフェイス</span><span class="sxs-lookup"><span data-stu-id="56ecb-134">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="56ecb-135">IHostTaskManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="56ecb-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
