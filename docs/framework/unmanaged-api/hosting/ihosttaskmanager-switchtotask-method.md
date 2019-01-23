---
title: IHostTaskManager::SwitchToTask メソッド
ms.date: 03/30/2017
api_name:
- IHostTaskManager.SwitchToTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::SwitchToTask
helpviewer_keywords:
- IHostTaskManager::SwitchToTask method [.NET Framework hosting]
- SwitchToTask method [.NET Framework hosting]
ms.assetid: 35d0c27e-4b14-49ce-810d-7ab2120177e8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9c7bf550985b5177348541aaa148c88c7c205258
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54490718"
---
# <a name="ihosttaskmanagerswitchtotask-method"></a><span data-ttu-id="4c006-102">IHostTaskManager::SwitchToTask メソッド</span><span class="sxs-lookup"><span data-stu-id="4c006-102">IHostTaskManager::SwitchToTask Method</span></span>
<span data-ttu-id="4c006-103">現在のタスクを切り離すことをホストに通知します。</span><span class="sxs-lookup"><span data-stu-id="4c006-103">Notifies the host that it should switch out the current task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4c006-104">構文</span><span class="sxs-lookup"><span data-stu-id="4c006-104">Syntax</span></span>  
  
```  
HRESULT SwitchToTask (  
    [in] DWORD option  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4c006-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4c006-105">Parameters</span></span>  
 `option`  
 <span data-ttu-id="4c006-106">[in]1 つ、 [WAIT_OPTION](../../../../docs/framework/unmanaged-api/hosting/wait-option-enumeration.md)場合に、ホストが実行するアクションを示す、列挙値、要求された操作がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="4c006-106">[in] One of the [WAIT_OPTION](../../../../docs/framework/unmanaged-api/hosting/wait-option-enumeration.md) enumeration values, indicating the action the host should take if the requested operation blocks.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4c006-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="4c006-107">Return Value</span></span>  
  
|<span data-ttu-id="4c006-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="4c006-108">HRESULT</span></span>|<span data-ttu-id="4c006-109">説明</span><span class="sxs-lookup"><span data-stu-id="4c006-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="4c006-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c006-110">S_OK</span></span>|<span data-ttu-id="4c006-111">`SwitchToTask` 正常に返されます。</span><span class="sxs-lookup"><span data-stu-id="4c006-111">`SwitchToTask` returned successfully.</span></span>|  
|<span data-ttu-id="4c006-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="4c006-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="4c006-113">共通言語ランタイム (CLR) は、プロセスに読み込まれていないか、CLR は状態をマネージ コードを実行または呼び出しを正常に処理ができません。</span><span class="sxs-lookup"><span data-stu-id="4c006-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="4c006-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="4c006-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="4c006-115">呼び出しがタイムアウトになりました。</span><span class="sxs-lookup"><span data-stu-id="4c006-115">The call timed out.</span></span>|  
|<span data-ttu-id="4c006-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="4c006-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="4c006-117">呼び出し元がロックを所有していません。</span><span class="sxs-lookup"><span data-stu-id="4c006-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="4c006-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="4c006-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="4c006-119">イベントがキャンセルされましたブロックされたスレッドまたはファイバーが待機しています。</span><span class="sxs-lookup"><span data-stu-id="4c006-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="4c006-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="4c006-120">E_FAIL</span></span>|<span data-ttu-id="4c006-121">不明な致命的なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="4c006-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="4c006-122">メソッドには、E_FAIL が返される、ときに、CLR は、プロセス内で使用可能ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="4c006-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="4c006-123">メソッドをホストする後続の呼び出しには、HOST_E_CLRNOTAVAILABLE が返されます。</span><span class="sxs-lookup"><span data-stu-id="4c006-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4c006-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="4c006-124">Remarks</span></span>  
 <span data-ttu-id="4c006-125">ホストは、必要に応じて、別のタスクに切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="4c006-125">The host can switch in another task as desired or needed.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4c006-126">`SwitchToTask` ホストが切り替えるタスクで指定されていません。切り替える必要がありますが、タスクのみを指定します。</span><span class="sxs-lookup"><span data-stu-id="4c006-126">`SwitchToTask` does not specify which task the host should switch to; it specifies only the task that it should switch from.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4c006-127">必要条件</span><span class="sxs-lookup"><span data-stu-id="4c006-127">Requirements</span></span>  
 <span data-ttu-id="4c006-128">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c006-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4c006-129">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="4c006-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="4c006-130">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="4c006-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4c006-131">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4c006-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c006-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="4c006-132">See also</span></span>
- [<span data-ttu-id="4c006-133">ICLRTask インターフェイス</span><span class="sxs-lookup"><span data-stu-id="4c006-133">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="4c006-134">ICLRTaskManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="4c006-134">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="4c006-135">IHostTask インターフェイス</span><span class="sxs-lookup"><span data-stu-id="4c006-135">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="4c006-136">IHostTaskManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="4c006-136">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
