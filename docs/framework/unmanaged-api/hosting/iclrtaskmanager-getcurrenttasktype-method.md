---
title: ICLRTaskManager::GetCurrentTaskType メソッド
ms.date: 03/30/2017
api_name:
- ICLRTaskManager.GetCurrentTaskType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTaskManager::GetCurrentTaskType
helpviewer_keywords:
- GetCurrentTaskType method [.NET Framework hosting]
- ICLRTaskManager::GetCurrentTaskType method [.NET Framework hosting]
ms.assetid: 6b0d9259-dbe2-45bb-b34d-990f60c73424
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7d2a8818ef180b3522a53e29fa84453ea9033a2a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54522402"
---
# <a name="iclrtaskmanagergetcurrenttasktype-method"></a><span data-ttu-id="8bc7c-102">ICLRTaskManager::GetCurrentTaskType メソッド</span><span class="sxs-lookup"><span data-stu-id="8bc7c-102">ICLRTaskManager::GetCurrentTaskType Method</span></span>
<span data-ttu-id="8bc7c-103">現在実行しているタスクの種類を取得します。</span><span class="sxs-lookup"><span data-stu-id="8bc7c-103">Gets the type of the task that is currently executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8bc7c-104">構文</span><span class="sxs-lookup"><span data-stu-id="8bc7c-104">Syntax</span></span>  
  
```  
HRESULT GetCurrentTaskType(  
    [out] ETaskType *pTaskType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8bc7c-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8bc7c-105">Parameters</span></span>  
 `pTaskType`  
 <span data-ttu-id="8bc7c-106">[out]値へのポインター、 [ETaskType](../../../../docs/framework/unmanaged-api/hosting/etasktype-enumeration.md)現在実行しているタスクの種類を示す列挙体。</span><span class="sxs-lookup"><span data-stu-id="8bc7c-106">[out] A pointer to a value of the [ETaskType](../../../../docs/framework/unmanaged-api/hosting/etasktype-enumeration.md) enumeration that indicates the type of task that is currently executing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8bc7c-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="8bc7c-107">Requirements</span></span>  
 <span data-ttu-id="8bc7c-108">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bc7c-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8bc7c-109">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="8bc7c-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8bc7c-110">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="8bc7c-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8bc7c-111">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8bc7c-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8bc7c-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="8bc7c-112">See also</span></span>
- [<span data-ttu-id="8bc7c-113">ICLRTaskManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8bc7c-113">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
