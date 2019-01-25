---
title: IGCThreadControl::SuspensionStarting メソッド
ms.date: 03/30/2017
api_name:
- IGCThreadControl.SuspensionStarting
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SuspensionStarting
helpviewer_keywords:
- IGCThreadControl::SuspensionStarting method [.NET Framework hosting]
- SuspensionStarting method, IGCThreadControl interface [.NET Framework hosting]
ms.assetid: 0af312af-98e9-415e-b182-42e80a1aee51
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ff0c95ea79978c0b58057ec06fea231f5632c941
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702653"
---
# <a name="igcthreadcontrolsuspensionstarting-method"></a><span data-ttu-id="a34c6-102">IGCThreadControl::SuspensionStarting メソッド</span><span class="sxs-lookup"><span data-stu-id="a34c6-102">IGCThreadControl::SuspensionStarting Method</span></span>
<span data-ttu-id="a34c6-103">ランタイムがガベージ コレクションのスレッドの中断またはその他の中断を開始していることをホストに通知します。</span><span class="sxs-lookup"><span data-stu-id="a34c6-103">Notifies the host that the runtime is beginning a thread suspension for a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a34c6-104">構文</span><span class="sxs-lookup"><span data-stu-id="a34c6-104">Syntax</span></span>  
  
```  
HRESULT SuspensionStarting ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="a34c6-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="a34c6-105">Remarks</span></span>  
 <span data-ttu-id="a34c6-106">中にすべてのスレッドを再スケジュールしないで、`SuspensionStarting`コールバック。</span><span class="sxs-lookup"><span data-stu-id="a34c6-106">Do not reschedule any threads during the `SuspensionStarting` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a34c6-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="a34c6-107">Requirements</span></span>  
 <span data-ttu-id="a34c6-108">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a34c6-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a34c6-109">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a34c6-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a34c6-110">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="a34c6-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a34c6-111">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a34c6-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a34c6-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="a34c6-112">See also</span></span>
- [<span data-ttu-id="a34c6-113">IGCThreadControl インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a34c6-113">IGCThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md)
