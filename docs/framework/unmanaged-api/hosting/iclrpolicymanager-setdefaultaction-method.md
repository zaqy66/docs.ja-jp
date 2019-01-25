---
title: ICLRPolicyManager::SetDefaultAction メソッド
ms.date: 03/30/2017
api_name:
- ICLRPolicyManager.SetDefaultAction
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRPolicyManager::SetDefaultAction
helpviewer_keywords:
- SetDefaultAction method [.NET Framework hosting]
- ICLRPolicyManager::SetDefaultAction method [.NET Framework hosting]
ms.assetid: f9411e7a-27df-451f-9f6c-d643d6a7a7ce
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 69a8d0cb09e057d4bcc3c9713c5b16c22fa45c5f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54602963"
---
# <a name="iclrpolicymanagersetdefaultaction-method"></a><span data-ttu-id="37b27-102">ICLRPolicyManager::SetDefaultAction メソッド</span><span class="sxs-lookup"><span data-stu-id="37b27-102">ICLRPolicyManager::SetDefaultAction Method</span></span>
<span data-ttu-id="37b27-103">共通言語ランタイム (CLR) が、指定された操作が発生したときに実行する必要がありますポリシーのアクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="37b27-103">Specifies the policy action the common language runtime (CLR) should take when the specified operation occurs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="37b27-104">構文</span><span class="sxs-lookup"><span data-stu-id="37b27-104">Syntax</span></span>  
  
```  
HRESULT SetDefaultAction (  
    [in] EClrOperation operation,  
    [in] EPolicyAction action  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="37b27-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37b27-105">Parameters</span></span>  
 `operation`  
 <span data-ttu-id="37b27-106">[in]1 つ、 [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) CLR の動作をカスタマイズする必要がありますの操作を示す値。</span><span class="sxs-lookup"><span data-stu-id="37b27-106">[in] One of the [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) values, indicating the action for which CLR behavior should be customized.</span></span>  
  
 `action`  
 <span data-ttu-id="37b27-107">[in]1 つ、 [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md)ポリシー アクション、CLR には、ときに実行する必要がありますを示す値`operation`に発生します。</span><span class="sxs-lookup"><span data-stu-id="37b27-107">[in] One of the [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) values, indicating the policy action the CLR should take when `operation` occurs.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="37b27-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="37b27-108">Return Value</span></span>  
  
|<span data-ttu-id="37b27-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="37b27-109">HRESULT</span></span>|<span data-ttu-id="37b27-110">説明</span><span class="sxs-lookup"><span data-stu-id="37b27-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="37b27-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="37b27-111">S_OK</span></span>|<span data-ttu-id="37b27-112">`SetDefaultAction` 正常に返されます。</span><span class="sxs-lookup"><span data-stu-id="37b27-112">`SetDefaultAction` returned successfully.</span></span>|  
|<span data-ttu-id="37b27-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="37b27-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="37b27-114">プロセスに CLR が読み込まれていないか、CLR は状態をマネージ コードを実行または呼び出しを正常に処理ができません。</span><span class="sxs-lookup"><span data-stu-id="37b27-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="37b27-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="37b27-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="37b27-116">呼び出しがタイムアウトになりました。</span><span class="sxs-lookup"><span data-stu-id="37b27-116">The call timed out.</span></span>|  
|<span data-ttu-id="37b27-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="37b27-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="37b27-118">呼び出し元がロックを所有していません。</span><span class="sxs-lookup"><span data-stu-id="37b27-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="37b27-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="37b27-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="37b27-120">イベントがキャンセルされましたブロックされたスレッドまたはファイバーが待機しています。</span><span class="sxs-lookup"><span data-stu-id="37b27-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="37b27-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="37b27-121">E_FAIL</span></span>|<span data-ttu-id="37b27-122">不明な致命的なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="37b27-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="37b27-123">メソッドには、E_FAIL が返された、後に、CLR は、プロセス内で使用可能ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="37b27-123">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="37b27-124">メソッドをホストする後続の呼び出しには、HOST_E_CLRNOTAVAILABLE が返されます。</span><span class="sxs-lookup"><span data-stu-id="37b27-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="37b27-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="37b27-125">E_INVALIDARG</span></span>|<span data-ttu-id="37b27-126">無効な`action`が指定されました、`operation`の無効な値が指定されているまたは`operation`します。</span><span class="sxs-lookup"><span data-stu-id="37b27-126">An invalid `action` was specified for the `operation`, or an invalid value was supplied for `operation`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="37b27-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="37b27-127">Remarks</span></span>  
 <span data-ttu-id="37b27-128">すべてのポリシーのアクション値は、CLR 操作では既定の動作として指定できます。</span><span class="sxs-lookup"><span data-stu-id="37b27-128">Not all policy action values can be specified as the default behavior for CLR operations.</span></span> <span data-ttu-id="37b27-129">`SetDefaultAction` エスカレーションの動作だけに通常使用できます。</span><span class="sxs-lookup"><span data-stu-id="37b27-129">`SetDefaultAction` can typically be used only to escalate behavior.</span></span> <span data-ttu-id="37b27-130">たとえば、ホストにルード スレッドの中止するになっていることを指定することができますが、スレッドの中止、その逆を指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="37b27-130">For example, a host can specify that thread aborts be turned into rude thread aborts, but cannot specify the opposite.</span></span> <span data-ttu-id="37b27-131">次の表は、有効な説明`action`可能性のある各値`operation`値。</span><span class="sxs-lookup"><span data-stu-id="37b27-131">The table below describes the valid `action` values for each possible `operation` value.</span></span>  
  
|<span data-ttu-id="37b27-132">値 `operation`</span><span class="sxs-lookup"><span data-stu-id="37b27-132">Value for `operation`</span></span>|<span data-ttu-id="37b27-133">有効な値 `action`</span><span class="sxs-lookup"><span data-stu-id="37b27-133">Valid values for `action`</span></span>|  
|---------------------------|-------------------------------|  
|<span data-ttu-id="37b27-134">OPR_ThreadAbort</span><span class="sxs-lookup"><span data-stu-id="37b27-134">OPR_ThreadAbort</span></span>|<span data-ttu-id="37b27-135">-   eAbortThread</span><span class="sxs-lookup"><span data-stu-id="37b27-135">-   eAbortThread</span></span><br /><span data-ttu-id="37b27-136">-   eRudeAbortThread</span><span class="sxs-lookup"><span data-stu-id="37b27-136">-   eRudeAbortThread</span></span><br /><span data-ttu-id="37b27-137">-eUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="37b27-137">-   eUnloadAppDomain</span></span><br /><span data-ttu-id="37b27-138">-   eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="37b27-138">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="37b27-139">-eExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-139">-   eExitProcess</span></span><br /><span data-ttu-id="37b27-140">-eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-140">-   eFastExitProcess</span></span><br /><span data-ttu-id="37b27-141">-   eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-141">-   eRudeExitProcess</span></span><br /><span data-ttu-id="37b27-142">-   eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="37b27-142">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="37b27-143">OPR_ThreadRudeAbortInNonCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="37b27-143">OPR_ThreadRudeAbortInNonCriticalRegion</span></span><br /><br /> <span data-ttu-id="37b27-144">OPR_ThreadRudeAbortInCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="37b27-144">OPR_ThreadRudeAbortInCriticalRegion</span></span>|<span data-ttu-id="37b27-145">-   eRudeAbortThread</span><span class="sxs-lookup"><span data-stu-id="37b27-145">-   eRudeAbortThread</span></span><br /><span data-ttu-id="37b27-146">-eUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="37b27-146">-   eUnloadAppDomain</span></span><br /><span data-ttu-id="37b27-147">-   eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="37b27-147">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="37b27-148">-eExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-148">-   eExitProcess</span></span><br /><span data-ttu-id="37b27-149">-eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-149">-   eFastExitProcess</span></span><br /><span data-ttu-id="37b27-150">-   eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-150">-   eRudeExitProcess</span></span><br /><span data-ttu-id="37b27-151">-   eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="37b27-151">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="37b27-152">OPR_AppDomainUnload</span><span class="sxs-lookup"><span data-stu-id="37b27-152">OPR_AppDomainUnload</span></span>|<span data-ttu-id="37b27-153">-eUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="37b27-153">-   eUnloadAppDomain</span></span><br /><span data-ttu-id="37b27-154">-   eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="37b27-154">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="37b27-155">-eExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-155">-   eExitProcess</span></span><br /><span data-ttu-id="37b27-156">-eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-156">-   eFastExitProcess</span></span><br /><span data-ttu-id="37b27-157">-   eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-157">-   eRudeExitProcess</span></span><br /><span data-ttu-id="37b27-158">-   eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="37b27-158">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="37b27-159">OPR_AppDomainRudeUnload</span><span class="sxs-lookup"><span data-stu-id="37b27-159">OPR_AppDomainRudeUnload</span></span>|<span data-ttu-id="37b27-160">-   eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="37b27-160">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="37b27-161">-eExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-161">-   eExitProcess</span></span><br /><span data-ttu-id="37b27-162">-eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-162">-   eFastExitProcess</span></span><br /><span data-ttu-id="37b27-163">-   eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-163">-   eRudeExitProcess</span></span><br /><span data-ttu-id="37b27-164">-   eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="37b27-164">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="37b27-165">OPR_ProcessExit</span><span class="sxs-lookup"><span data-stu-id="37b27-165">OPR_ProcessExit</span></span>|<span data-ttu-id="37b27-166">-eExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-166">-   eExitProcess</span></span><br /><span data-ttu-id="37b27-167">-eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-167">-   eFastExitProcess</span></span><br /><span data-ttu-id="37b27-168">-   eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-168">-   eRudeExitProcess</span></span><br /><span data-ttu-id="37b27-169">-   eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="37b27-169">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="37b27-170">OPR_FinalizerRun</span><span class="sxs-lookup"><span data-stu-id="37b27-170">OPR_FinalizerRun</span></span>|<span data-ttu-id="37b27-171">-eNoAction</span><span class="sxs-lookup"><span data-stu-id="37b27-171">-   eNoAction</span></span><br /><span data-ttu-id="37b27-172">-   eAbortThread</span><span class="sxs-lookup"><span data-stu-id="37b27-172">-   eAbortThread</span></span><br /><span data-ttu-id="37b27-173">-   eRudeAbortThread</span><span class="sxs-lookup"><span data-stu-id="37b27-173">-   eRudeAbortThread</span></span><br /><span data-ttu-id="37b27-174">-eUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="37b27-174">-   eUnloadAppDomain</span></span><br /><span data-ttu-id="37b27-175">-   eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="37b27-175">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="37b27-176">-eExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-176">-   eExitProcess</span></span><br /><span data-ttu-id="37b27-177">-eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-177">-   eFastExitProcess</span></span><br /><span data-ttu-id="37b27-178">-   eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="37b27-178">-   eRudeExitProcess</span></span><br /><span data-ttu-id="37b27-179">-   eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="37b27-179">-   eDisableRuntime</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="37b27-180">必要条件</span><span class="sxs-lookup"><span data-stu-id="37b27-180">Requirements</span></span>  
 <span data-ttu-id="37b27-181">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="37b27-181">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="37b27-182">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="37b27-182">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="37b27-183">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="37b27-183">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="37b27-184">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="37b27-184">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37b27-185">関連項目</span><span class="sxs-lookup"><span data-stu-id="37b27-185">See also</span></span>
- [<span data-ttu-id="37b27-186">EClrOperation 列挙型</span><span class="sxs-lookup"><span data-stu-id="37b27-186">EClrOperation Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md)
- [<span data-ttu-id="37b27-187">EPolicyAction 列挙型</span><span class="sxs-lookup"><span data-stu-id="37b27-187">EPolicyAction Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md)
- [<span data-ttu-id="37b27-188">ICLRPolicyManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="37b27-188">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)
