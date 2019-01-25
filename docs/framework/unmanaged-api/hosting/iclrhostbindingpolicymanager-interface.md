---
title: ICLRHostBindingPolicyManager インターフェイス
ms.date: 03/30/2017
api_name:
- ICLRHostBindingPolicyManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRHostBindingPolicyManager
helpviewer_keywords:
- ICLRHostBindingPolicyManager interface [.NET Framework hosting]
ms.assetid: f9da168b-366b-4b2b-bdb9-330b6bad5a6b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 98a2978b440e0e72b3b4c1ac3065fbaf5d70e508
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54666099"
---
# <a name="iclrhostbindingpolicymanager-interface"></a><span data-ttu-id="a68c0-102">ICLRHostBindingPolicyManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a68c0-102">ICLRHostBindingPolicyManager Interface</span></span>
<span data-ttu-id="a68c0-103">現在のバインディング ポリシーを評価し、指定したアセンブリのポリシーの変更を通信するホストのメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="a68c0-103">Provides methods for the host to evaluate current binding policy and communicate policy changes for a specified assembly.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a68c0-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="a68c0-104">Methods</span></span>  
  
|<span data-ttu-id="a68c0-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="a68c0-105">Method</span></span>|<span data-ttu-id="a68c0-106">説明</span><span class="sxs-lookup"><span data-stu-id="a68c0-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a68c0-107">EvaluatePolicy メソッド</span><span class="sxs-lookup"><span data-stu-id="a68c0-107">EvaluatePolicy Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-evaluatepolicy-method.md)|<span data-ttu-id="a68c0-108">ホストに代わってバインディング ポリシーを評価します。</span><span class="sxs-lookup"><span data-stu-id="a68c0-108">Evaluates binding policy on behalf of the host.</span></span>|  
|[<span data-ttu-id="a68c0-109">ModifyApplicationPolicy メソッド</span><span class="sxs-lookup"><span data-stu-id="a68c0-109">ModifyApplicationPolicy Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-modifyapplicationpolicy-method.md)|<span data-ttu-id="a68c0-110">指定されたアセンブリのバインディング ポリシーを変更し、新しいバージョンのポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="a68c0-110">Modifies the binding policy for the specified assembly, and creates a new version of the policy.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a68c0-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="a68c0-111">Requirements</span></span>  
 <span data-ttu-id="a68c0-112">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a68c0-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a68c0-113">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a68c0-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a68c0-114">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="a68c0-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a68c0-115">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a68c0-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a68c0-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="a68c0-116">See also</span></span>
- [<span data-ttu-id="a68c0-117">ICLRAssemblyIdentityManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a68c0-117">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="a68c0-118">IHostAssemblyStore インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a68c0-118">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
- [<span data-ttu-id="a68c0-119">ホスト インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a68c0-119">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
