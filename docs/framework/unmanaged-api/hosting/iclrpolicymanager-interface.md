---
title: ICLRPolicyManager インターフェイス
ms.date: 03/30/2017
api_name:
- ICLRPolicyManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRPolicyManager
helpviewer_keywords:
- ICLRPolicyManager interface [.NET Framework hosting]
ms.assetid: 5c834aa1-f2db-408a-b230-c7bec093d364
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cfce4276c651e5cb6ed20bd2616b68294e49da8e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629146"
---
# <a name="iclrpolicymanager-interface"></a><span data-ttu-id="6b4cd-102">ICLRPolicyManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6b4cd-102">ICLRPolicyManager Interface</span></span>
<span data-ttu-id="6b4cd-103">ホスト ポリシー エラーやタイムアウトが発生した場合に実行されるアクションを指定できるようにするメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="6b4cd-103">Provides methods that allow the host to specify policy actions to be taken in the event of failures and timeouts.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="6b4cd-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="6b4cd-104">Methods</span></span>  
  
|<span data-ttu-id="6b4cd-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="6b4cd-105">Method</span></span>|<span data-ttu-id="6b4cd-106">説明</span><span class="sxs-lookup"><span data-stu-id="6b4cd-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6b4cd-107">SetActionOnFailure メソッド</span><span class="sxs-lookup"><span data-stu-id="6b4cd-107">SetActionOnFailure Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactiononfailure-method.md)|<span data-ttu-id="6b4cd-108">共通言語ランタイム (CLR) が指定したエラーが発生したときに実行する必要がありますポリシーのアクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="6b4cd-108">Specifies the policy action the common language runtime (CLR) should take when the specified failure occurs.</span></span>|  
|[<span data-ttu-id="6b4cd-109">SetActionOnTimeout メソッド</span><span class="sxs-lookup"><span data-stu-id="6b4cd-109">SetActionOnTimeout Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactionontimeout-method.md)|<span data-ttu-id="6b4cd-110">指定された操作がタイムアウトしたときに、CLR が実行ポリシーのアクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="6b4cd-110">Specifies the policy action the CLR should take when the specified operation times out.</span></span>|  
|[<span data-ttu-id="6b4cd-111">SetDefaultAction メソッド</span><span class="sxs-lookup"><span data-stu-id="6b4cd-111">SetDefaultAction Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setdefaultaction-method.md)|<span data-ttu-id="6b4cd-112">指定された操作が発生したときに、CLR が実行ポリシーのアクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="6b4cd-112">Specifies the policy action the CLR should take when the specified operation occurs.</span></span>|  
|[<span data-ttu-id="6b4cd-113">SetTimeout メソッド</span><span class="sxs-lookup"><span data-stu-id="6b4cd-113">SetTimeout Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-settimeout-method.md)|<span data-ttu-id="6b4cd-114">指定された操作のタイムアウト値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6b4cd-114">Sets a timeout value for the specified operation.</span></span>|  
|[<span data-ttu-id="6b4cd-115">SetTimeoutAndAction メソッド</span><span class="sxs-lookup"><span data-stu-id="6b4cd-115">SetTimeoutAndAction Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-settimeoutandaction-method.md)|<span data-ttu-id="6b4cd-116">指定された操作のタイムアウト値を設定し、操作が発生したときに、CLR が実行ポリシーのアクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="6b4cd-116">Sets a timeout value for the specified operation, and specifies the policy action the CLR should take when the operation occurs.</span></span>|  
|[<span data-ttu-id="6b4cd-117">SetUnhandledExceptionPolicy メソッド</span><span class="sxs-lookup"><span data-stu-id="6b4cd-117">SetUnhandledExceptionPolicy Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setunhandledexceptionpolicy-method.md)|<span data-ttu-id="6b4cd-118">ハンドルされない例外が発生したときに、CLR の動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b4cd-118">Specifies the behavior of the CLR when an unhandled exception occurs.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6b4cd-119">必要条件</span><span class="sxs-lookup"><span data-stu-id="6b4cd-119">Requirements</span></span>  
 <span data-ttu-id="6b4cd-120">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b4cd-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6b4cd-121">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="6b4cd-121">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6b4cd-122">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="6b4cd-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6b4cd-123">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6b4cd-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6b4cd-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b4cd-124">See also</span></span>
- [<span data-ttu-id="6b4cd-125">EClrFailure 列挙型</span><span class="sxs-lookup"><span data-stu-id="6b4cd-125">EClrFailure Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md)
- [<span data-ttu-id="6b4cd-126">EClrOperation 列挙型</span><span class="sxs-lookup"><span data-stu-id="6b4cd-126">EClrOperation Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md)
- [<span data-ttu-id="6b4cd-127">EPolicyAction 列挙型</span><span class="sxs-lookup"><span data-stu-id="6b4cd-127">EPolicyAction Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md)
- [<span data-ttu-id="6b4cd-128">ICLRControl インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6b4cd-128">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
