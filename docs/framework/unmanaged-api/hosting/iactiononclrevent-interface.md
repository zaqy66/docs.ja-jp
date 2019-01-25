---
title: IActionOnCLREvent インターフェイス
ms.date: 03/30/2017
api_name:
- IActionOnCLREvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IActionOnCLREvent
helpviewer_keywords:
- IActionOnCLREvent interface [.NET Framework hosting]
ms.assetid: b5f9b41e-7301-429c-911f-21d5422292b3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0f547d1bafa37c2cbb285a5d55cef8e1a6e29d0a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54688247"
---
# <a name="iactiononclrevent-interface"></a><span data-ttu-id="b0583-102">IActionOnCLREvent インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b0583-102">IActionOnCLREvent Interface</span></span>
<span data-ttu-id="b0583-103">提供、 [iactiononclrevent::onevent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md)への呼び出しを使用して登録されているイベントのコールバックを実行するメソッドに、 [iclroneventmanager::registeractiononevent](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-registeractiononevent-method.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="b0583-103">Provides the [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) method, which performs callbacks on events that have been registered by using a call to the [ICLROnEventManager::RegisterActionOnEvent](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-registeractiononevent-method.md) method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b0583-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="b0583-104">Methods</span></span>  
  
|<span data-ttu-id="b0583-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="b0583-105">Method</span></span>|<span data-ttu-id="b0583-106">説明</span><span class="sxs-lookup"><span data-stu-id="b0583-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b0583-107">OnEvent メソッド</span><span class="sxs-lookup"><span data-stu-id="b0583-107">OnEvent Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md)|<span data-ttu-id="b0583-108">登録済みのイベントのコールバックを実行します。</span><span class="sxs-lookup"><span data-stu-id="b0583-108">Performs a callback for a registered event.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b0583-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="b0583-109">Requirements</span></span>  
 <span data-ttu-id="b0583-110">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0583-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b0583-111">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="b0583-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b0583-112">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="b0583-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b0583-113">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b0583-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0583-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="b0583-114">See also</span></span>
- [<span data-ttu-id="b0583-115">EClrEvent 列挙型</span><span class="sxs-lookup"><span data-stu-id="b0583-115">EClrEvent Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md)
- [<span data-ttu-id="b0583-116">ICLRControl インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b0583-116">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
- [<span data-ttu-id="b0583-117">ICLROnEventManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b0583-117">ICLROnEventManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-interface.md)
- [<span data-ttu-id="b0583-118">ホスト インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b0583-118">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
