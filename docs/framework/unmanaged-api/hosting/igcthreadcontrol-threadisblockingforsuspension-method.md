---
title: IGCThreadControl::ThreadIsBlockingForSuspension メソッド
ms.date: 03/30/2017
api_name:
- IGCThreadControl.ThreadIsBlockingForSuspension
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ThreadIsBlockingForSuspension
helpviewer_keywords:
- IGCThreadControl::ThreadIsBlockingForSuspension method [.NET Framework hosting]
- ThreadIsBlockingForSuspension method [.NET Framework hosting]
ms.assetid: ed5b5b58-7db7-46b5-9e2c-278db7159cee
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: aa2872fec7765f38fba9589a6fab659e73131937
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54620462"
---
# <a name="igcthreadcontrolthreadisblockingforsuspension-method"></a><span data-ttu-id="f8f23-102">IGCThreadControl::ThreadIsBlockingForSuspension メソッド</span><span class="sxs-lookup"><span data-stu-id="f8f23-102">IGCThreadControl::ThreadIsBlockingForSuspension Method</span></span>
<span data-ttu-id="f8f23-103">ガベージ コレクションまたはその他の中断のためにブロックするには、約呼び出しを行っているスレッドであることをホストに通知します。</span><span class="sxs-lookup"><span data-stu-id="f8f23-103">Notifies the host that the thread that is making the call is about to block, perhaps for a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8f23-104">構文</span><span class="sxs-lookup"><span data-stu-id="f8f23-104">Syntax</span></span>  
  
```  
HRESULT ThreadIsBlockingForSuspension ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="f8f23-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="f8f23-105">Remarks</span></span>  
 <span data-ttu-id="f8f23-106">内でホストを選択できます、`ThreadIsBlockingForSuspension`コールバック スレッドのスケジュールを変更するかどうか。</span><span class="sxs-lookup"><span data-stu-id="f8f23-106">The host may choose within the `ThreadIsBlockingForSuspension` callback whether to reschedule a thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f8f23-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="f8f23-107">Requirements</span></span>  
 <span data-ttu-id="f8f23-108">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8f23-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f8f23-109">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f8f23-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f8f23-110">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="f8f23-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f8f23-111">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f8f23-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8f23-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8f23-112">See also</span></span>
- [<span data-ttu-id="f8f23-113">IGCThreadControl インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f8f23-113">IGCThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md)
