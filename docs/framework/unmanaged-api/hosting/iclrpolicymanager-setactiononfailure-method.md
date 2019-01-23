---
title: ICLRPolicyManager::SetActionOnFailure メソッド
ms.date: 03/30/2017
api_name:
- ICLRPolicyManager.SetActionOnFailure
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRPolicyManager::SetActionOnFailure
helpviewer_keywords:
- SetActionOnFailure method [.NET Framework hosting]
- ICLRPolicyManager::SetActionOnFailure method [.NET Framework hosting]
ms.assetid: 4664033f-db97-4388-b988-2ec470796e58
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 535a0cbfd3224c13b42a69d01876867297b218d3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54544222"
---
# <a name="iclrpolicymanagersetactiononfailure-method"></a><span data-ttu-id="501c2-102">ICLRPolicyManager::SetActionOnFailure メソッド</span><span class="sxs-lookup"><span data-stu-id="501c2-102">ICLRPolicyManager::SetActionOnFailure Method</span></span>
<span data-ttu-id="501c2-103">共通言語ランタイム (CLR) が指定したエラーが発生したときに実行する必要がありますポリシーのアクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="501c2-103">Specifies the policy action the common language runtime (CLR) should take when the specified failure occurs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="501c2-104">構文</span><span class="sxs-lookup"><span data-stu-id="501c2-104">Syntax</span></span>  
  
```  
HRESULT SetActionOnFailure (  
    [in] EClrFailure   failure,  
    [in] EPolicyAction action  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="501c2-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="501c2-105">Parameters</span></span>  
 `failure`  
 <span data-ttu-id="501c2-106">[in]1 つ、 [EClrFailure](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md)アクションを実行する対象のエラーの種類を示す値。</span><span class="sxs-lookup"><span data-stu-id="501c2-106">[in] One of the [EClrFailure](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md) values, indicating the type of failure for which to take action.</span></span>  
  
 `action`  
 <span data-ttu-id="501c2-107">[in]1 つ、 [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md)障害が発生したときに実行されるアクションを示す値。</span><span class="sxs-lookup"><span data-stu-id="501c2-107">[in] One of the [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) values, indicating the action to be taken when a failure occurs.</span></span> <span data-ttu-id="501c2-108">サポートされている値の一覧は、「解説」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="501c2-108">For a list of supported values, see the Remarks section.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="501c2-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="501c2-109">Return Value</span></span>  
  
|<span data-ttu-id="501c2-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="501c2-110">HRESULT</span></span>|<span data-ttu-id="501c2-111">説明</span><span class="sxs-lookup"><span data-stu-id="501c2-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="501c2-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="501c2-112">S_OK</span></span>|<span data-ttu-id="501c2-113">`SetActionOnFailure` 正常に返されます。</span><span class="sxs-lookup"><span data-stu-id="501c2-113">`SetActionOnFailure` returned successfully.</span></span>|  
|<span data-ttu-id="501c2-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="501c2-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="501c2-115">プロセスに CLR が読み込まれていないか、CLR は状態をマネージ コードを実行または呼び出しを正常に処理ができません。</span><span class="sxs-lookup"><span data-stu-id="501c2-115">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="501c2-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="501c2-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="501c2-117">呼び出しがタイムアウトになりました。</span><span class="sxs-lookup"><span data-stu-id="501c2-117">The call timed out.</span></span>|  
|<span data-ttu-id="501c2-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="501c2-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="501c2-119">呼び出し元がロックを所有していません。</span><span class="sxs-lookup"><span data-stu-id="501c2-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="501c2-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="501c2-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="501c2-121">イベントがキャンセルされましたブロックされたスレッドまたはファイバーが待機しています。</span><span class="sxs-lookup"><span data-stu-id="501c2-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="501c2-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="501c2-122">E_FAIL</span></span>|<span data-ttu-id="501c2-123">不明な致命的なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="501c2-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="501c2-124">メソッドには、E_FAIL が返された、後に、CLR は、プロセス内で使用可能ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="501c2-124">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="501c2-125">メソッドをホストする後続の呼び出しには、HOST_E_CLRNOTAVAILABLE が返されます。</span><span class="sxs-lookup"><span data-stu-id="501c2-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="501c2-126">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="501c2-126">E_INVALIDARG</span></span>|<span data-ttu-id="501c2-127">指定された操作のポリシーのアクションを設定することはできませんまたは操作に無効なポリシー アクションが指定されました。</span><span class="sxs-lookup"><span data-stu-id="501c2-127">A policy action cannot be set for the specified operation, or an invalid policy action was specified for the operation.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="501c2-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="501c2-128">Remarks</span></span>  
 <span data-ttu-id="501c2-129">既定では、CLR は、メモリなどのリソースの割り当てに失敗した場合に例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="501c2-129">By default, the CLR throws an exception when it fails to allocate a resource such as memory.</span></span> <span data-ttu-id="501c2-130">`SetActionOnFailure` により、ホストは、障害発生時に実行するポリシーのアクションを指定することでこの動作をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="501c2-130">`SetActionOnFailure` allows the host to override this behavior by specifying the policy action to take upon failure.</span></span> <span data-ttu-id="501c2-131">次の表は、組み合わせの[EClrFailure](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md)と[EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md)サポートされている値。</span><span class="sxs-lookup"><span data-stu-id="501c2-131">The following table shows the combinations of [EClrFailure](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md) and [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) values that are supported.</span></span> <span data-ttu-id="501c2-132">(から FAIL_ プレフィックスを省略すると[EClrFailure](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md)値)。</span><span class="sxs-lookup"><span data-stu-id="501c2-132">(The FAIL_ prefix is omitted from [EClrFailure](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md) values.)</span></span>  
  
||<span data-ttu-id="501c2-133">NonCriticalResource</span><span class="sxs-lookup"><span data-stu-id="501c2-133">NonCriticalResource</span></span>|<span data-ttu-id="501c2-134">CriticalResource</span><span class="sxs-lookup"><span data-stu-id="501c2-134">CriticalResource</span></span>|<span data-ttu-id="501c2-135">FatalRuntime</span><span class="sxs-lookup"><span data-stu-id="501c2-135">FatalRuntime</span></span>|<span data-ttu-id="501c2-136">OrphanedLock</span><span class="sxs-lookup"><span data-stu-id="501c2-136">OrphanedLock</span></span>|<span data-ttu-id="501c2-137">StackOverflow</span><span class="sxs-lookup"><span data-stu-id="501c2-137">StackOverflow</span></span>|<span data-ttu-id="501c2-138">AccessViolation</span><span class="sxs-lookup"><span data-stu-id="501c2-138">AccessViolation</span></span>|<span data-ttu-id="501c2-139">CodeContract</span><span class="sxs-lookup"><span data-stu-id="501c2-139">CodeContract</span></span>|  
|-|-------------------------|----------------------|------------------|------------------|-------------------|---------------------|------------------|  
|`eNoAction`|<span data-ttu-id="501c2-140">x</span><span class="sxs-lookup"><span data-stu-id="501c2-140">X</span></span>|<span data-ttu-id="501c2-141">x</span><span class="sxs-lookup"><span data-stu-id="501c2-141">X</span></span>||||<span data-ttu-id="501c2-142">N/A</span><span class="sxs-lookup"><span data-stu-id="501c2-142">N/A</span></span>||  
|<span data-ttu-id="501c2-143">eThrowException</span><span class="sxs-lookup"><span data-stu-id="501c2-143">eThrowException</span></span>|<span data-ttu-id="501c2-144">x</span><span class="sxs-lookup"><span data-stu-id="501c2-144">X</span></span>|<span data-ttu-id="501c2-145">x</span><span class="sxs-lookup"><span data-stu-id="501c2-145">X</span></span>||||<span data-ttu-id="501c2-146">N/A</span><span class="sxs-lookup"><span data-stu-id="501c2-146">N/A</span></span>||  
|`eAbortThread`|<span data-ttu-id="501c2-147">x</span><span class="sxs-lookup"><span data-stu-id="501c2-147">X</span></span>|<span data-ttu-id="501c2-148">x</span><span class="sxs-lookup"><span data-stu-id="501c2-148">X</span></span>||||<span data-ttu-id="501c2-149">N/A</span><span class="sxs-lookup"><span data-stu-id="501c2-149">N/A</span></span>|<span data-ttu-id="501c2-150">x</span><span class="sxs-lookup"><span data-stu-id="501c2-150">X</span></span>|  
|`eRudeAbortThread`|<span data-ttu-id="501c2-151">x</span><span class="sxs-lookup"><span data-stu-id="501c2-151">X</span></span>|<span data-ttu-id="501c2-152">x</span><span class="sxs-lookup"><span data-stu-id="501c2-152">X</span></span>||||<span data-ttu-id="501c2-153">N/A</span><span class="sxs-lookup"><span data-stu-id="501c2-153">N/A</span></span>|<span data-ttu-id="501c2-154">x</span><span class="sxs-lookup"><span data-stu-id="501c2-154">X</span></span>|  
|`eUnloadAppDomain`|<span data-ttu-id="501c2-155">x</span><span class="sxs-lookup"><span data-stu-id="501c2-155">X</span></span>|<span data-ttu-id="501c2-156">x</span><span class="sxs-lookup"><span data-stu-id="501c2-156">X</span></span>||<span data-ttu-id="501c2-157">x</span><span class="sxs-lookup"><span data-stu-id="501c2-157">X</span></span>||<span data-ttu-id="501c2-158">N/A</span><span class="sxs-lookup"><span data-stu-id="501c2-158">N/A</span></span>|<span data-ttu-id="501c2-159">x</span><span class="sxs-lookup"><span data-stu-id="501c2-159">X</span></span>|  
|`eRudeUnloadAppDomain`|<span data-ttu-id="501c2-160">x</span><span class="sxs-lookup"><span data-stu-id="501c2-160">X</span></span>|<span data-ttu-id="501c2-161">x</span><span class="sxs-lookup"><span data-stu-id="501c2-161">X</span></span>||<span data-ttu-id="501c2-162">x</span><span class="sxs-lookup"><span data-stu-id="501c2-162">X</span></span>|<span data-ttu-id="501c2-163">x</span><span class="sxs-lookup"><span data-stu-id="501c2-163">X</span></span>|<span data-ttu-id="501c2-164">N/A</span><span class="sxs-lookup"><span data-stu-id="501c2-164">N/A</span></span>|<span data-ttu-id="501c2-165">x</span><span class="sxs-lookup"><span data-stu-id="501c2-165">X</span></span>|  
|`eExitProcess`|<span data-ttu-id="501c2-166">x</span><span class="sxs-lookup"><span data-stu-id="501c2-166">X</span></span>|<span data-ttu-id="501c2-167">x</span><span class="sxs-lookup"><span data-stu-id="501c2-167">X</span></span>||<span data-ttu-id="501c2-168">x</span><span class="sxs-lookup"><span data-stu-id="501c2-168">X</span></span>|<span data-ttu-id="501c2-169">x</span><span class="sxs-lookup"><span data-stu-id="501c2-169">X</span></span>|<span data-ttu-id="501c2-170">N/A</span><span class="sxs-lookup"><span data-stu-id="501c2-170">N/A</span></span>|<span data-ttu-id="501c2-171">x</span><span class="sxs-lookup"><span data-stu-id="501c2-171">X</span></span>|  
|<span data-ttu-id="501c2-172">eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="501c2-172">eFastExitProcess</span></span>|<span data-ttu-id="501c2-173">x</span><span class="sxs-lookup"><span data-stu-id="501c2-173">X</span></span>|<span data-ttu-id="501c2-174">x</span><span class="sxs-lookup"><span data-stu-id="501c2-174">X</span></span>||<span data-ttu-id="501c2-175">x</span><span class="sxs-lookup"><span data-stu-id="501c2-175">X</span></span>|<span data-ttu-id="501c2-176">x</span><span class="sxs-lookup"><span data-stu-id="501c2-176">X</span></span>|<span data-ttu-id="501c2-177">N/A</span><span class="sxs-lookup"><span data-stu-id="501c2-177">N/A</span></span>||  
|`eRudeExitProcess`|<span data-ttu-id="501c2-178">x</span><span class="sxs-lookup"><span data-stu-id="501c2-178">X</span></span>|<span data-ttu-id="501c2-179">x</span><span class="sxs-lookup"><span data-stu-id="501c2-179">X</span></span>|<span data-ttu-id="501c2-180">x</span><span class="sxs-lookup"><span data-stu-id="501c2-180">X</span></span>|<span data-ttu-id="501c2-181">x</span><span class="sxs-lookup"><span data-stu-id="501c2-181">X</span></span>|<span data-ttu-id="501c2-182">x</span><span class="sxs-lookup"><span data-stu-id="501c2-182">X</span></span>|<span data-ttu-id="501c2-183">N/A</span><span class="sxs-lookup"><span data-stu-id="501c2-183">N/A</span></span>||  
|`eDisableRuntime`|<span data-ttu-id="501c2-184">x</span><span class="sxs-lookup"><span data-stu-id="501c2-184">X</span></span>|<span data-ttu-id="501c2-185">x</span><span class="sxs-lookup"><span data-stu-id="501c2-185">X</span></span>|<span data-ttu-id="501c2-186">x</span><span class="sxs-lookup"><span data-stu-id="501c2-186">X</span></span>|<span data-ttu-id="501c2-187">x</span><span class="sxs-lookup"><span data-stu-id="501c2-187">X</span></span>|<span data-ttu-id="501c2-188">x</span><span class="sxs-lookup"><span data-stu-id="501c2-188">X</span></span>|<span data-ttu-id="501c2-189">N/A</span><span class="sxs-lookup"><span data-stu-id="501c2-189">N/A</span></span>||  
  
## <a name="requirements"></a><span data-ttu-id="501c2-190">必要条件</span><span class="sxs-lookup"><span data-stu-id="501c2-190">Requirements</span></span>  
 <span data-ttu-id="501c2-191">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="501c2-191">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="501c2-192">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="501c2-192">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="501c2-193">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="501c2-193">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="501c2-194">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="501c2-194">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="501c2-195">関連項目</span><span class="sxs-lookup"><span data-stu-id="501c2-195">See also</span></span>
- [<span data-ttu-id="501c2-196">EClrFailure 列挙型</span><span class="sxs-lookup"><span data-stu-id="501c2-196">EClrFailure Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md)
- [<span data-ttu-id="501c2-197">EPolicyAction 列挙型</span><span class="sxs-lookup"><span data-stu-id="501c2-197">EPolicyAction Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md)
- [<span data-ttu-id="501c2-198">ICLRControl インターフェイス</span><span class="sxs-lookup"><span data-stu-id="501c2-198">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
- [<span data-ttu-id="501c2-199">ICLRPolicyManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="501c2-199">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)
