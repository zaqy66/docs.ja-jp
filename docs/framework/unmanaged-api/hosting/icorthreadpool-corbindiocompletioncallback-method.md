---
title: ICorThreadpool::CorBindIoCompletionCallback メソッド
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorBindIoCompletionCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorBindIoCompletionCallback
helpviewer_keywords:
- CorBindIoCompletionCallback method [.NET Framework hosting]
- ICorThreadpool::CorBindIoCompletionCallback method [.NET Framework hosting]
ms.assetid: 2b159225-f09c-42f1-aa7c-44087e121249
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5efd9811b0d5bfd16b802f0d504d69a4e7522833
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54707857"
---
# <a name="icorthreadpoolcorbindiocompletioncallback-method"></a><span data-ttu-id="73c8c-102">ICorThreadpool::CorBindIoCompletionCallback メソッド</span><span class="sxs-lookup"><span data-stu-id="73c8c-102">ICorThreadpool::CorBindIoCompletionCallback Method</span></span>
<span data-ttu-id="73c8c-103">このメソッドは、.NET Framework インフラストラクチャをサポートします。独自に作成したコードから直接使用するためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="73c8c-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="73c8c-104">構文</span><span class="sxs-lookup"><span data-stu-id="73c8c-104">Syntax</span></span>  
  
```  
HRESULT CorBindIoCompletionCallback (  
    [in] HANDLE                          fileHandle,  
    [in] LPOVERLAPPED_COMPLETION_ROUTINE callback  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="73c8c-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="73c8c-105">Requirements</span></span>  
 <span data-ttu-id="73c8c-106">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="73c8c-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="73c8c-107">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="73c8c-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="73c8c-108">**ライブラリ:** MSCorEE.dll でリソースとして含まれます</span><span class="sxs-lookup"><span data-stu-id="73c8c-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="73c8c-109">**.NET Framework のバージョン:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="73c8c-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="73c8c-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="73c8c-110">See also</span></span>
- [<span data-ttu-id="73c8c-111">ICorThreadpool インターフェイス</span><span class="sxs-lookup"><span data-stu-id="73c8c-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
