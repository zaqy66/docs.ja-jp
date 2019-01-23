---
title: CorMarkThreadInThreadPool 関数
ms.date: 03/30/2017
api_name:
- CorMarkThreadInThreadPool
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- CorMarkThreadInThreadPool
helpviewer_keywords:
- CorMarkThreadInThreadPool function [.NET Framework hosting]
ms.assetid: 3f958d41-e82e-4ec3-ae6f-16c7b3b31e3e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d1e0f79304c4ed0d052bb05e364f64d6cb524f21
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54495241"
---
# <a name="cormarkthreadinthreadpool-function"></a><span data-ttu-id="748fb-102">CorMarkThreadInThreadPool 関数</span><span class="sxs-lookup"><span data-stu-id="748fb-102">CorMarkThreadInThreadPool Function</span></span>
<span data-ttu-id="748fb-103">現在実行されているスレッド プールのスレッドに、マネージド コードの実行のマークを付けます。</span><span class="sxs-lookup"><span data-stu-id="748fb-103">Marks the currently executing thread-pool thread for the execution of managed code.</span></span> <span data-ttu-id="748fb-104">.NET Framework Version 2.0 以降では、この関数に効力はありません。</span><span class="sxs-lookup"><span data-stu-id="748fb-104">Starting with the .NET Framework version 2.0, this function has no effect.</span></span> <span data-ttu-id="748fb-105">必須ではありませんし、コードから削除することができます。この関数は非推奨、[!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)]します。</span><span class="sxs-lookup"><span data-stu-id="748fb-105">It is not required, and can be removed from your code.This function is deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="748fb-106">構文</span><span class="sxs-lookup"><span data-stu-id="748fb-106">Syntax</span></span>  
  
```  
void CorMarkThreadInThreadPool ();  
```  
  
## <a name="requirements"></a><span data-ttu-id="748fb-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="748fb-107">Requirements</span></span>  
 <span data-ttu-id="748fb-108">**プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="748fb-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="748fb-109">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="748fb-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="748fb-110">**ライブラリ:** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="748fb-110">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="748fb-111">**.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="748fb-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="748fb-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="748fb-112">See also</span></span>
- [<span data-ttu-id="748fb-113">非推奨の CLR ホスト関数</span><span class="sxs-lookup"><span data-stu-id="748fb-113">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
