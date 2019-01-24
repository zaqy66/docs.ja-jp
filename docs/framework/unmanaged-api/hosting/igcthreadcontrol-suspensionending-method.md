---
title: IGCThreadControl::SuspensionEnding メソッド
ms.date: 03/30/2017
api_name:
- IGCThreadControl.SuspensionEnding
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SuspensionEnding
helpviewer_keywords:
- IGCThreadControl::SuspensionEnding method [.NET Framework hosting]
- SuspensionEnding method, IGCThreadControl interface [.NET Framework hosting]
ms.assetid: 70814265-c734-4ddc-9502-fe8b28d2b414
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d77380e35d8f5eee1e50b1030493e0b17cbadfba
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54713289"
---
# <a name="igcthreadcontrolsuspensionending-method"></a><span data-ttu-id="ed6b3-102">IGCThreadControl::SuspensionEnding メソッド</span><span class="sxs-lookup"><span data-stu-id="ed6b3-102">IGCThreadControl::SuspensionEnding Method</span></span>
<span data-ttu-id="ed6b3-103">ランタイムがガベージ コレクションまたはその他の中断の後のスレッドを再開することをホストに通知します。</span><span class="sxs-lookup"><span data-stu-id="ed6b3-103">Notifies the host that the runtime is resuming threads after a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed6b3-104">構文</span><span class="sxs-lookup"><span data-stu-id="ed6b3-104">Syntax</span></span>  
  
```  
HRESULT SuspensionEnding (  
    [in] DWORD Generation  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ed6b3-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ed6b3-105">Parameters</span></span>  
 `Generation`  
 <span data-ttu-id="ed6b3-106">[in]ガベージ コレクションが実行されて生成されます。</span><span class="sxs-lookup"><span data-stu-id="ed6b3-106">[in] The generation on which a garbage collection has been performed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ed6b3-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="ed6b3-107">Remarks</span></span>  
 <span data-ttu-id="ed6b3-108">中にすべてのスレッドを再スケジュールしないで、`SuspensionEnding`コールバック。</span><span class="sxs-lookup"><span data-stu-id="ed6b3-108">Do not reschedule any threads during the `SuspensionEnding` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ed6b3-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="ed6b3-109">Requirements</span></span>  
 <span data-ttu-id="ed6b3-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed6b3-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ed6b3-111">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="ed6b3-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ed6b3-112">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="ed6b3-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ed6b3-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ed6b3-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed6b3-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed6b3-114">See also</span></span>
- [<span data-ttu-id="ed6b3-115">IGCThreadControl インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ed6b3-115">IGCThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md)
