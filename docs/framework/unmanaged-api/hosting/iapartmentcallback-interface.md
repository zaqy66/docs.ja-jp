---
title: IApartmentCallback インターフェイス
ms.date: 03/30/2017
api_name:
- IApartmentCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IApartmentCallback
helpviewer_keywords:
- IApartmentCallback interface [.NET Framework hosting]
ms.assetid: 57c33c58-bf0b-4533-b569-e6a682d02cba
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bc3f9e8c581bc95bea8cfeb549177966eae22a43
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54584494"
---
# <a name="iapartmentcallback-interface"></a><span data-ttu-id="937b5-102">IApartmentCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="937b5-102">IApartmentCallback Interface</span></span>
<span data-ttu-id="937b5-103">アパートメント内でのコールバックを行うためのメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="937b5-103">Provides methods for making callbacks within an apartment.</span></span> <span data-ttu-id="937b5-104">*アパートメント*は同じスレッドへのアクセス要件を共有するオブジェクトのプロセス内の論理コンテナーです。</span><span class="sxs-lookup"><span data-stu-id="937b5-104">An *apartment* is a logical container within a process for objects that share the same thread access requirements.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="937b5-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="937b5-105">Methods</span></span>  
  
|<span data-ttu-id="937b5-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="937b5-106">Method</span></span>|<span data-ttu-id="937b5-107">説明</span><span class="sxs-lookup"><span data-stu-id="937b5-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="937b5-108">DoCallback メソッド</span><span class="sxs-lookup"><span data-stu-id="937b5-108">DoCallback Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iapartmentcallback-docallback-method.md)|<span data-ttu-id="937b5-109">アパートメント内で指定された関数を実行します。</span><span class="sxs-lookup"><span data-stu-id="937b5-109">Executes the specified function within an apartment.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="937b5-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="937b5-110">Requirements</span></span>  
 <span data-ttu-id="937b5-111">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="937b5-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="937b5-112">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="937b5-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="937b5-113">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="937b5-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="937b5-114">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="937b5-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="937b5-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="937b5-115">See also</span></span>
- [<span data-ttu-id="937b5-116">ホスト インターフェイス</span><span class="sxs-lookup"><span data-stu-id="937b5-116">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
